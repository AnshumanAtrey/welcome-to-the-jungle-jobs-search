# Welcome to the Jungle Jobs Scraper & API - Otta, WTTJ, Salary

Welcome to the Jungle jobs scraper and API: search every open job on welcometothejungle.com (WTTJ), in France, Europe, the UK and the US, with the UK site that was Otta, live by job title, place, contract, remote policy, pay and posting date, and get each job's title, company, offices, contract type, remote policy, salary, years of experience, education, company size, industry, summary, key missions, perks, posting date and link, newest first, internships and alternance (work-study) included. Turn on full details for the description, the experience wanted, the recruitment process, skills, tools and the employer's own apply link.

Use it as a Welcome to the Jungle API with no login and no API key, a WTTJ job scraper, an Otta jobs alternative or a daily feed of new jobs in France and Europe from the Apify Console, the Apify API, Python, JavaScript, n8n, Make or an AI agent, and export JSON, CSV or Excel. Every row's title holds the words you typed, French and English place names both work (Bretagne and Brittany), and a pasted Welcome to the Jungle search link keeps its filters. Available as an [Apify Actor](https://apify.com/anshumanatrey/welcome-to-the-jungle-jobs-search). $0.00002 per job, $0.00006 with full details, $0.002 per run start at the default memory.

## What does it do?

- **Searches all of Welcome to the Jungle, live.** 84,849 open jobs at 4,515 companies on 2026-11-10, read from the site's own search index at the moment of your run, newest first: offices in France (54,471), the US (18,024), the UK (5,573), Canada, Germany, Spain, Ireland, the Netherlands, Italy, Belgium and 239 more countries.
- **Otta's jobs too.** otta.com/jobs now leads to uk.welcometothejungle.com, "Welcome To The Jungle UK (formerly Otta)", and the UK and US startups that hired on Otta post their jobs here (Monzo, Airbnb, Carwow, Funding Circle, Dropbox).
- **Titles that match.** A job is kept when its title holds every word you typed, in any order: data analyst finds "Business Analyst Data H/F" and leaves out "Data Engineer". Wider match (`searchDescriptions`) also reads the summary and the profile wanted.
- **Contract, remote and pay on every row.** Contract type on every job (permanent, fixed-term, internship, work-study, freelance, part-time, VIE), the employer's remote policy on 53% (full remote, a few days at home, occasional, none), pay on 34% with its currency (EUR, USD, GBP) and period (year, month, day), and the years of experience the job asks for on 63%.
- **Company facts on every row.** Headcount (99% of jobs), year founded, industry (97%), logo, perks and the site's own summary and three key missions of the job.
- **Filters the way people ask.** Remote or office, contract type, years of experience (3, 2-5, 5+, fresher), minimum yearly pay (monthly pay counts 12 months), company size, industry, the language of the ad (English ads for people who do not speak French), company names.
- **Checks job links.** Paste Welcome to the Jungle job links, and each comes back open with the job, closed (archived by the employer) or not found.

## How is it different from other Welcome to the Jungle scrapers?

- **Newest first, always.** clearpath and blackfalcondata, the first and third most used Welcome to the Jungle actors, sort by relevance unless you pick date (their `sortBy` input), as do maximedupre and memo23; this actor always returns the newest jobs first, by the moment each job went live, which is the job page's own posting date.
- **The title matches what you typed.** Every row's title holds every word of a line, and several titles and several places go in one run (développeur and developer, Paris and Lyon). The six most used Welcome to the Jungle actors take one query a run (memo23 takes several).
- **Otta's offices get their region.** Most offices of the UK and US jobs that came from Otta name only the town (2,758 of 2,795 in San Francisco, 3,170 of 3,878 in London), so a search for California or England misses them elsewhere. Here each such office gets the one region the site gives its town, and California finds San Francisco, Mountain View and Palo Alto jobs.
- **Work-study is a contract of its own.** Alternance (apprenticeship) is a job type next to internship, fixed-term and permanent, as on the site.
- **Pay you can compare.** Minimum pay (`minSalary`) reads a yearly amount and compares every job's pay on a year, from monthly and daily pay too.
- **Exactly the number you asked for.** Number of jobs (`maxJobs`) is the number of rows you get, newest first, and you pay per row delivered.

## When should I use it?

- **Job seekers and job boards:** new jobs in France, Europe, the UK or the US by title, town, contract and pay, every morning, with salary and remote policy.
- **Recruiters and staffing firms:** who is hiring for a role right now, with what contract, pay and experience, and which companies post most.
- **Sales and market research:** companies hiring in a town or an industry as a buying signal, with their size and founding year.
- **Students:** internships and alternance (work-study) by town and field, with duration and monthly pay.
- **Data teams and AI agents:** one clean feed of European startup and tech jobs through the API or MCP.

## How much does it cost to scrape Welcome to the Jungle jobs?

Pay per event: $0.02 per 1,000 jobs, or $0.06 per 1,000 with full details, plus $0.002 per run at the default 512 MB. Apify's free $5 monthly credit covers about 125,000 jobs in runs of 100. Platform usage is included, and there is no monthly fee.

| Event | Price | When it is charged |
|---|---|---|
| Job | $0.00002 | One saved job, and one checked link that is closed or not found |
| Job with details | $0.00006 | One saved job with full details on |
| Run start | $0.002 per GB of memory | Charged by Apify when a run starts: once up to 1 GB and once more for each extra GB, so $0.002 at the default 512 MB |

Welcome to the Jungle Jobs Scraper's Apify Store header shows the lowest discount-tier price, the GOLD price: $0.018 per 1,000 jobs. FREE and BRONZE users (Apify's Free and Starter plans) pay $0.00002 a job; with full details FREE pays $0.00006 and BRONZE $0.000058. SILVER (Scale) pays $0.000019 and $0.000056, and GOLD (Business) and the enterprise tiers $0.000018 and $0.000054. The run start is a flat fee on every plan, $0.002 per GB of memory, and the header never shows it.

| Run (Free and Starter price, default memory) | Cost |
|---|---|
| 100 newest jobs | $0.004 |
| 100 jobs with full details | $0.008 |
| 1,000 jobs | $0.022 |
| 20,000 jobs | $0.40 |

## How does the price compare with other Welcome to the Jungle scrapers?

Every actor on the Apify Store whose title names Welcome to the Jungle, WTTJ or Otta and had 8 or more users in the last 30 days, from the Store's own search on 2026-11-10 (94 actors read), ordered by users. Free-plan list prices from each actor's current pricing.

| Actor | Users, 30 days | Per job | Start fee | Input |
|---|---|---|---|---|
| clearpath/welcome-to-the-jungle-jobs-api | 236 | $0.00299 with full details, +$0.00001 a row | $0.00005 | One query and one location, radius, country, sort by relevance, contract, remote, experience, pay, size, language, sector |
| bebity/welcome-to-the-jungle-jobs-scraper | 136 | $0.0003, $0.0005 with details | $0.00005 | Jobs, articles or companies; one query, city with radius, contract, remote, pay, experience, education, size |
| blackfalcondata/wttj-scraper | 79 | $0.00045 | $0.005 | One query, country, place, contract, remote, sector, experience, pay, size, change tracking and alerts |
| shahidirfan/Jungle-Job-Scraper | 62 | $0.00099 | $0.0005 | One keyword and one location, 20 jobs by default |
| logiover/welcome-to-the-jungle-jobs-scraper | 13 | $0.0025 | $0.00005 | One query, contract, remote, categories, experience, pay |
| maximedupre/welcometothejungle-jobs-extractor | 12 | $0.00085 | none | One query, places, countries, remote, contract, categories, search links |
| scrapeworks/otta-jobs-scraper | 9 | free, you pay the platform usage | none | Company names or job links, residential proxy by default |
| memo23/welcometothejungle-jobs-scraper | 8 | $0.00099, +$0.001 extra data | $0.005 | Several searches, market and country, filters, company pages |
| This actor | new | $0.00002, $0.00006 with details | $0.002 per GB | Titles, places and the site's filters, live, newest first |

Where others are cheaper: this actor's run start, $0.002, is above clearpath's, bebity's and logiover's ($0.00005), so a run of a few jobs costs less there. Where others do more: bebity also returns the site's articles and company profiles; blackfalcondata adds change tracking and Slack, Telegram and webhook alerts; clearpath and bebity search around a point with a radius; memo23 adds contact emails.

## Which inputs does it take?

Nothing is required. Type a job title and press Start, or press Start with the form empty for the newest jobs of every kind.

| Field | What it does |
|---|---|
| Job titles to find (`searchTerms`) | One per line. A job matches when its title has every word: frontend also finds Front-End, accents do not matter. A pasted Welcome to the Jungle search link works too, with its country, contract and remote filters |
| Where the job is (`location`) | Towns, departments, regions or countries: Paris, Lyon, Ile-de-France, London, New York, Germany, Europe. French and English names both work. Remote alone asks for fully remote jobs |
| Remote or office (`workType`) | remote (fully remote), hybrid (a few days or occasional days at home) or onsite (no remote) |
| Contract type (`employmentType`) | full-time (permanent, CDI), part-time, contract (freelance), intern, temporary (fixed-term, CDD) or apprenticeship (work-study, alternance) |
| Posted in the last (`postedWithin`) | 24 hours, 3, 7, 15 or 30 days (the default), any time, or your own period such as 48 hours |
| Minimum pay a year (`minSalary`) | A yearly amount in the job's own currency: 50000 keeps the jobs whose pay can reach 50,000 a year |
| Experience (`experienceYears`) | Your years: 3, a range such as 2-5, 5+ or fresher. Keeps the jobs whose band overlaps it |
| Company size (`companySize`) | under-15, 15-50, 50-250, 250-2000 or over-2000 employees |
| Business sectors (`industries`) | Industries as the site names them: Software, FinTech, Banking, Health, Cyber Security |
| Language of the ad (`jobLanguage`) | en, fr, de, es, it, nl or pt |
| Number of jobs (`maxJobs`) | How many, newest first: 100 by default, 0 for every match |
| Full details (`includeDetails`) | Adds the description, experience wanted and recruitment process as text and HTML, skills, tools, start date, the company's website and apply link |
| Leave out words (`excludeTerms`) | Drops jobs whose title has these words, such as senior or stage |
| Wider match (`searchDescriptions`) | Every job whose title, summary or profile wanted holds your words |
| Only these companies (`companies`) | Company names as the site writes them (Doctolib, Back Market), a company page link, or a `companySlug` |
| Job links to check (`jobUrls`) | Welcome to the Jungle job links, to check whether they are still open, instead of searching |

Example input:

```json
{
  "searchTerms": ["data analyst", "business analyst"],
  "location": ["Paris", "Lyon"],
  "employmentType": ["full-time"],
  "workType": ["hybrid", "remote"],
  "minSalary": 45000,
  "postedWithin": "7 days",
  "maxJobs": 100
}
```

## What does the output look like?

One row per job, newest first. These rows are from a local run on 2026-11-10 at 10:35 UTC: data analyst, 100 jobs saved in 2 s. A job with several offices shows the first in `location` and the others in `otherLocations`.

| Job title (`title`) | Company name (`company`) | Main location (`location`) | Remote or office (`workType`) | Contract type (`employmentType`) | Pay summary (`salary`) | Posted on (`postedAt`) |
|---|---|---|---|---|---|---|
| Stage- Investment Risk Data Analyst H/F | Crédit Agricole | Paris, Ile-de-France, France | hybrid | intern |  | 2026-11-10 |
| Data Analyst Supply Chain H/F | skiils | Lille, Hauts-de-France, France | hybrid | full-time | EUR 45,000 - 65,000 per year | 2026-11-10 |
| Data Analyst E-commerce & Marketing H/F | skiils | Lille, Hauts-de-France, France | hybrid | full-time | EUR 40,000 - 70,000 per year | 2026-11-10 |
| Data analyst - Lutte contre la fraude (F/H) - stage | AXA | Nanterre, Ile-de-France, France | hybrid | intern |  | 2026-11-10 |
| CDD - Data Analyst F/H | La Banque Postale | Paris, Ile-de-France, France |  | temporary |  | 2026-11-09 |

One row as JSON:

```json
{
  "title": "Data Analyst Supply Chain H/F",
  "company": "skiils",
  "location": "Lille, Hauts-de-France, France",
  "otherLocations": ["Casablanca, Casablanca - Settat, Morocco", "Suresnes, Ile-de-France, France"],
  "workType": "hybrid",
  "employmentType": "full-time",
  "department": "Data / Business Intelligence",
  "salary": "EUR 45,000 - 65,000 per year",
  "postedAt": "2026-11-10T08:55:42Z",
  "jobUrl": "https://www.welcometothejungle.com/en/companies/skiils/jobs/data-analyst-supply-chain-h-f",
  "applyUrl": "https://www.welcometothejungle.com/en/companies/skiils/jobs/data-analyst-supply-chain-h-f",
  "status": "open",
  "platform": "welcometothejungle",
  "companySlug": "skiils",
  "companyWebsite": null,
  "jobId": "skiils/data-analyst-supply-chain-h-f",
  "checkedAt": "2026-11-10T10:35:06+00:00",
  "experienceMin": 5.0,
  "experienceMax": 7.0,
  "salaryMin": 45000.0,
  "salaryMax": 65000.0,
  "salaryCurrency": "EUR",
  "salaryPeriod": "year",
  "contractType": "full_time",
  "contractDurationMin": null,
  "contractDurationMax": null,
  "remotePolicy": "partial",
  "education": "Bac+5 (master's)",
  "jobLanguage": "fr",
  "role": "Data Analyst",
  "roleCategory": "Tech & Engineering",
  "industry": "Artificial Intelligence / Machine Learning, Change Management, Big Data",
  "companySize": 200,
  "companyFounded": 2020,
  "companyLogo": "https://cdn-images.welcometothejungle.com/5_es0apSaeqfD5vtQ7A-pDWdJvMk_U-lCfDVsZlHDxs/rs:auto:400/q:85/czM6Ly93dHRqLXByb2R1Y3Rpb24vdXBsb2Fkcy9vcmdhbml6YXRpb24vbG9nby80NzU1LzE2ODAxNi9iMDlmMGFhYy1iYTQ3LTRhMzYtYjIwNy0xY2M4MzJjYjczZmQucG5n",
  "summary": "Rejoins notre équipe en tant que Data Analyst Supply Chain. Tu seras responsable de cadrer les besoins fonctionnels, d'extraire et d'exploiter les données, de construire des outils de pilotage...",
  "keyMissions": ["Cadrer les besoins fonctionnels en échangeant avec les équipes métier, IT et direction pour définir des analyses pertinentes.", "Extraire et exploiter la donnée en requêtant un datalake à grande échelle pour mener des analyses poussées de prévision et d'optimisation."],
  "benefits": ["Between 3-4 days at home", "Between 2-3 days at home", "Between 1-2 days at home", "Food service or stocked kitchen"],
  "skills": null,
  "tools": null,
  "startDate": null
}
```

Full details fill `skills`, `tools`, `startDate` and `companyWebsite`, and add `description`, `descriptionHtml`, `reference`, `city`, `region` and `country`; for a job the employer posts from its own careers site (29 of 30 in a London product manager sample), `applyUrl` becomes that page. A checked link that is closed comes back with its `status`, company and link, and the other fields empty. A run also writes an `OUTPUT` record: how many jobs were read, how many matched and were saved, any notes on how your input was read, and the calls made.

## How fast is it?

Seconds. In local runs on 2026-11-10: the form as it opens (100 newest jobs) took 2 s and 2 calls, data analyst 2 s, developer in Paris with a permanent contract 1 s, product manager in the UK with full details for 30 jobs 2 s (32 calls), 20,000 jobs 18 s (22 calls, about 1,100 jobs a second) and all 81,443 jobs of the board 87 s. The site's search answers 1,000 jobs a call, newest first, and reads only titles, so a rare title is as fast as a common one. A place the site does not list makes the run check every job by name (85 calls, 32 s for the whole board). Apify run times come with the first release.

## Common questions

### Is Welcome to the Jungle the same as Otta?

Otta, the UK job search for startups, became part of Welcome to the Jungle: otta.com/jobs now leads to uk.welcometothejungle.com, titled "Welcome To The Jungle UK (formerly Otta)", and the Otta app tells its users it is moving to welcometothejungle.com. The UK and US companies that hired on Otta post their jobs on Welcome to the Jungle now (Monzo 51 open jobs, Airbnb 78, Carwow 34 on 2026-11-10), so Welcome to the Jungle Jobs Scraper covers them: type London, United Kingdom or New York.

### Does it cover the UK and the US, or only France?

Every country site: one search reads all of Welcome to the Jungle. On 2026-11-10 its jobs had offices in France (54,471), the US (18,024), the UK (5,573), Canada (1,818), Germany (1,078), Spain (857) and 243 more countries. 62% of the ads are written in French and 37% in English; pick en in Language of the ad (`jobLanguage`) for the jobs open to English speakers.

### Which posting date does it use?

Welcome to the Jungle Jobs Scraper uses the moment each job went live on the site, `postedAt`, which equals the date the job page gives Google (its JobPosting datePosted: 9 of 9 pages checked on 2026-11-10). It orders the rows by it and applies Posted in the last (`postedWithin`) to it. About 3,000 jobs go live a day: 12,500 in the 7 days to 2026-11-10 and 44,000 in 30.

### Why do I get fewer jobs than Welcome to the Jungle shows?

The site's own search ranks jobs by how close they are to your words and also returns related roles: its first 10 pages for data analyst held 99 jobs, of which 58 had both words in the title and were posted in the last 30 days. Welcome to the Jungle Jobs Scraper keeps the jobs whose title holds every word: on 2026-11-10 it saved 156 data analyst jobs of the last 30 days, holding all 58. A company's same title at the same office is kept once, the newest (3.1% of the board are such copies, mostly reposts). Tick Wider match (`searchDescriptions`) to also find the jobs whose summary or profile holds your words. A run that saves no job says why, such as "11 jobs had your words but not your other filters: the pay alone left out 11", and how to loosen it.

### How do places work?

Welcome to the Jungle Jobs Scraper reads places the way the site writes them: towns (Paris, Lyon, Courbevoie), departments (Hauts-de-Seine), regions (Ile-de-France, Brittany or Bretagne, California, England), countries (France, Germany, United States) and groups of countries (Europe, DACH, EMEA). A job matches when one of its offices does. Most UK and US offices name only their town; each gets the one region the site gives that town elsewhere, so England finds London jobs and California finds San Francisco jobs. A place the site does not list is checked against every job by name, which takes longer, and the run says so. The site gives every job an office country and marks none as open worldwide, so Worldwide keeps every country; pick remote in Remote or office (`workType`) for fully remote jobs.

### How do I get only jobs above a salary?

Type the lowest yearly pay in Minimum pay a year (`minSalary`): 50000 keeps the jobs whose pay can reach 50,000 a year in the job's own currency. Monthly pay counts 12 months and a day rate 218 working days, so an internship at 1,200 a month counts as 14,400. Jobs that show no pay are left out; a third of jobs show it, most US jobs among them.

### How do I find internships or alternance?

Pick intern (internship, stage) or apprenticeship (work-study, alternance) in Contract type (`employmentType`), and add a field such as marketing in Job titles to find (`searchTerms`). Rows carry the duration in months (`contractDurationMin`, `contractDurationMax`) and the education asked (`education`). Typing alternance or stage as a title word works too, but finds only the jobs that say it in their title (81% of work-study jobs and 90% of internships).

### Does it need a login or an API key?

Welcome to the Jungle Jobs Scraper needs no Welcome to the Jungle login and no API key: it reads the same public search index and job API the site's own pages call in every visitor's browser, with the search key the site hands every visitor. You need only an Apify account.

### Does it work on Apify's free plan?

Welcome to the Jungle Jobs Scraper works on Apify's free plan, which pays $0.00002 a job plus the $0.002 run start at the default 512 MB. The free $5 monthly credit pays for about 125,000 jobs in runs of 100, at $0.004 a run.

### How often should I run it?

Running Welcome to the Jungle Jobs Scraper once a day keeps a job feed fresh: set Posted in the last (`postedWithin`) to 24 hours and Number of jobs (`maxJobs`) to 0 to get every job of the day for your titles and places. Set it up under Schedules in Apify Console, and match rows on `jobId` to skip jobs you already have.

### How do I get every job of one company?

Type the company's name, as the site writes it, in Only these companies (`companies`), such as Doctolib or Back Market, or paste its company page link, and set Number of jobs (`maxJobs`) to 0. Welcome to the Jungle Jobs Scraper finds the company's page and reads only its jobs; a company with two pages (Qonto has two) gets both.

### How do I check a list of job links?

Paste Welcome to the Jungle job links into Job links to check (`jobUrls`), one per line, instead of searching. Welcome to the Jungle Jobs Scraper reads each job from the site's job API: an open job comes back with all its fields, an archived one as closed, and a link to no job as not found.

### How do I call it from the API, Python, JavaScript, n8n or an AI agent?

Welcome to the Jungle Jobs Scraper runs from the Apify API, Python, JavaScript, n8n, Make or an AI agent over MCP. Each way uses your Apify token (Apify Console, Settings, API & Integrations) and takes the input as JSON keyed by the field names, such as `searchTerms` and `maxJobs`.

**API.** One call runs the actor and returns its rows (Apify waits up to 300 seconds; for runs of thousands of jobs, use a client below):

```bash
curl -X POST "https://api.apify.com/v2/acts/anshumanatrey~welcome-to-the-jungle-jobs-search/run-sync-get-dataset-items" \
  -H "Authorization: Bearer <YOUR_APIFY_TOKEN>" \
  -H "Content-Type: application/json" \
  -d '{"searchTerms": ["data analyst"], "location": ["Paris"]}'
```

**Python** (`pip install apify-client`):

```python
from apify_client import ApifyClient

client = ApifyClient("<YOUR_APIFY_TOKEN>")
run = client.actor("anshumanatrey/welcome-to-the-jungle-jobs-search").call(run_input={"searchTerms": ["data analyst"]})
for row in client.dataset(run.default_dataset_id).iterate_items():  # apify-client 3+; on 2.x use run["defaultDatasetId"]
    print(row["title"], row["company"], row["location"], row["employmentType"], row["salary"], row["jobUrl"])
```

**JavaScript** (`npm install apify-client`):

```js
import { ApifyClient } from 'apify-client';

const client = new ApifyClient({ token: '<YOUR_APIFY_TOKEN>' });
const run = await client.actor('anshumanatrey/welcome-to-the-jungle-jobs-search').call({ searchTerms: ['data analyst'] });
const { items } = await client.dataset(run.defaultDatasetId).listItems();
for (const row of items) console.log(row.title, row.company, row.location, row.employmentType, row.salary, row.jobUrl);
```

**n8n and Make.** In n8n, add the Apify node, pick Run an Actor and get dataset, choose this actor and paste the input JSON: the rows come out as n8n items. In Make, the Apify app's Run an Actor and Get Dataset Items modules do the same.

**AI agents (MCP).** Add `https://mcp.apify.com?tools=anshumanatrey/welcome-to-the-jungle-jobs-search` to your MCP client and sign in with Apify, or send `Authorization: Bearer <YOUR_APIFY_TOKEN>`. The agent gets this actor as a tool and sees every input field by its JSON key.

### Am I charged for closed jobs?

Welcome to the Jungle Jobs Scraper charges for a closed job only when you paste its link to check. A search returns open jobs only, and a pasted link that turns out closed is one Job row, because it was checked and answered.

### Is it legal to use?

Welcome to the Jungle Jobs Scraper reads public job postings, the data any visitor sees without logging in. It is not affiliated with Welcome to the Jungle or Otta. You are responsible for how you use the data, including Welcome to the Jungle's terms and the privacy laws that apply to you.

## Limitations

- Titles are matched by their words in the ad's own language: developer does not find Développeur, so type both (French ads are 62% of the board).
- A job that states no remote policy (47%), no experience (37%) or no pay (66%) is left out once you set that filter.
- Pay is as the employer entered it, period included; a few entries are off at the source (one work-study ad shows EUR 1,400 - 1,800 per day).
- Places are matched by their words: Paris also finds Le Touquet-Paris-Plage. A few US towns that the site never gives a region (San Jose, Sunnyvale) are not found by their state; type the town.
- A company's same title at the same office is delivered once, the newest, unless the job's own address names another town (Keolis lists one ambulance job per town at its head office).
- The site's summary and key missions come in French on some English ads, as the site writes them.
- Full details make one call per job.
- The run reads the site's search key from welcometothejungle.com each time; if the site stops handing it out, a run stops with a message that says so.

## Who maintains it?

Built and maintained by **Anshuman Atrey** ([@AnshumanAtrey](https://github.com/AnshumanAtrey)), who publishes a portfolio of data and OSINT actors on Apify Store. For a feature request or a bug, message [LinkedIn](https://linkedin.com/in/anshumanatrey) (fastest), open an issue on the GitHub repo, or write through [atrey.dev](https://atrey.dev).

## Sibling actors

| Actor | What it searches |
|---|---|
| [Greenhouse Jobs Scraper](https://apify.com/anshumanatrey/greenhouse-jobs-search) | Jobs from every company on Greenhouse, searched live |
| [Lever Jobs Scraper](https://apify.com/anshumanatrey/lever-jobs-search) | Jobs from 2,300+ companies on Lever (jobs.lever.co), searched live |
| [Workday Jobs Scraper](https://apify.com/anshumanatrey/workday-job-search) | Jobs from every company on Workday (myworkdayjobs.com), searched live |
| [Ashby Jobs Scraper](https://apify.com/anshumanatrey/ashby-jobs-search) | Jobs from every company on Ashby (jobs.ashbyhq.com), searched live |
| [SmartRecruiters Jobs Scraper](https://apify.com/anshumanatrey/smartrecruiters-jobs-search) | Jobs from 2,900+ companies on SmartRecruiters, searched live |
| [Workable Jobs Scraper](https://apify.com/anshumanatrey/workable-job-search) | Jobs from every company on Workable, in one search |
| [Cornerstone Jobs Scraper](https://apify.com/anshumanatrey/cornerstone-jobs-search) | Jobs from every company on Cornerstone (csod.com), searched live |
| [Deel Jobs Scraper](https://apify.com/anshumanatrey/deel-jobs-search) | Jobs from every company on Deel ATS (jobs.deel.com), with pay |

For the people behind a company: [LinkedIn Profile Finder](https://apify.com/anshumanatrey/linkedin-harvester) turns an email into a public LinkedIn profile.

## Documentation

- Apify Store: https://apify.com/anshumanatrey/welcome-to-the-jungle-jobs-search
- GitHub repo: https://github.com/AnshumanAtrey/welcome-to-the-jungle-jobs-search (MIT license, see [LICENSE](LICENSE))
- The engine behind it: https://github.com/AnshumanAtrey/ats-jobs-engine

## Last updated

2026-11-10 (version 1.0)
