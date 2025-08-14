# Technical Runbook

## Execution Plan


### Step 1: Foundation setup

**Inputs:** Development Environment: Docker, Node.js 18+, TypeScript, Git setup  API Credentials: Bright Data API key, OpenAI API key ($100+ budget), n8n instance, database hosting  Configuration Files: Environment templates, Docker compose, migration scripts

**Outputs:** Infrastructure: Functional dev environment with n8n at localhost:5678, Bright Data node installed  Architecture: Database models, API routes, authentication system, CI/CD pipeline  Frontend: Next.js with TypeScript, essential UI components

**Tools:** Core: Docker, n8n (self-hosted), PostgreSQL, Redis, MongoDB  Authentication: NextAuth.js, JWT implementation  Monitoring: Winston logging, basic error handling


### Step 2: Core scraping engine

**Inputs:** Target Sources: Reddit (r/entrepreneur, r/business, r/consulting, r/startups), LinkedIn professional content  Configuration: Rate limits (1 req/2sec Reddit, 1 req/5sec LinkedIn), engagement filters (50+ upvotes, 10+ reactions)  Compliance: robots.txt adherence, GDPR compliance

**Outputs:** Data Volume: 500+ Reddit posts/week, 200+ LinkedIn posts/week with 95%+ unique content  n8n Workflows: Content scraper, quality filter, duplicate detection, error handling  Processing: Real-time validation, categorization, engagement scoring

**Tools:** Primary: Bright Data Web Unlocker API ($0.001/request), Reddit JSON endpoints  Processing: Python/Node.js content cleaning, MongoDB storage  Compliance: Rate limiting middleware, attribution tracking


### Step 3: Content generation

**Inputs:** Source Material: 100+ viral posts with psychological trigger analysis, UNITE brand guidelines  AI Configuration: GPT-4o for quality content, custom prompts for psychological analysis  Brand Integration: Company voice, service descriptions, target personas

**Outputs:** Content Volume: 50+ blog posts/month (2,000-3,000 words), 200+ social posts, 20+ landing pages  Quality Metrics: 90%+ approval rate, 60-80 readability scores, 80+ SEO scores  AI Analysis: Psychological trigger identification, performance predictions, competitor gap analysis

**Tools:** AI Services: GPT-4o ($2.50/1M input, $10.00/1M output), GPT-4o-mini ($0.15/1M input)  Analysis: Custom trigger detection, sentiment analysis, SEO tools integration  Publishing: WordPress/Ghost APIs, social media APIs, email automation


### Step 4: UI and testing

**Inputs:** None specified

**Outputs:** None specified

**Tools:** None specified


## Validation

### Tests
- Foundation Tests ✅ All services start in Docker without errors  ✅ Database connections <2 second response time  ✅ Authentication generates/validates JWT tokens correctly  ✅ API security prevents unauthorized access (401 status)  ✅ Rate limiting prevents abuse (100 req/min/IP)  Scraping Engine Tests ✅ Reddit: 50+ posts/subreddit/day extraction  ✅ LinkedIn: 200+ posts/week with ToS compliance  ✅ Content deduplication >95% unique rate  ✅ Rate limiting prevents IP blocks  ✅ Error handling with exponential backoff  Content Generation Tests ✅ Brand voice consistency >95%  ✅ Blog posts meet 2,000 word minimum  ✅ SEO keyword density 1-2% for primary keywords  ✅ Readability scores 60-80 range  ✅ Plagiarism check <5% similarity

### Quality Gates
- 95%+ test coverage for core services  Sub-3-second performance requirements  90%+ content quality approval rates  Full compliance and security verification

### Manual Checks
- Foundation Manual Checks  Single command repository setup for developers   Documentation includes clear setup instructions   Dashboard loads <3 seconds, mobile responsive   WCAG AA accessibility compliance   Intuitive navigation for non-technical users  Scraping Engine Manual Checks  Content relevant to business consulting/software development   No personal information captured   Platform rate limits prevent blocks/warnings   GDPR compliance for EU data handling   Content attribution preserved  Content Generation Manual Checks  Generated content reflects UNITE expertise   Technical terminology used correctly   Value propositions align with services   Psychological triggers incorporated naturally   Authority positioning backed by credentials

## Environment

### Environment Variables
No environment variables specified

### Secrets Policy
API key rotation every 90 days

Encrypted secret storage

Separate dev/production environments

Comprehensive access logging

---

*Generated on 2025-08-14*
