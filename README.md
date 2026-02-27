# aiadoption

Open data and interactive visualization of AI adoption rates across 16 countries.

**Live site:** [aiadoption-gray.vercel.app](https://aiadoption-gray.vercel.app)

Part of the [aiforgood.my](https://aiforgood.my) project — a hub for open-source AI projects for good.

## What is this?

An interactive dot-grid visualization showing how AI adoption varies dramatically across countries — from the UAE at 64% to Nigeria at 9.3%. Each dot represents 0.25% of a country's population, color-coded by adoption category.

Inspired by [global-ai-adoption.netlify.app](https://global-ai-adoption.netlify.app/) which tracks global AI adoption over time. This project focuses on comparing adoption **by country**.

## Countries covered

| Country | Adoption | AI Users | Region |
|---------|----------|----------|--------|
| UAE | 64.0% | 7.3M | Middle East |
| Singapore | 60.9% | 3.7M | Southeast Asia |
| France | 44.0% | 29.9M | Europe |
| China | 42.8% | 603M | East Asia |
| United Kingdom | 38.9% | 26.5M | Europe |
| Australia | 36.9% | 10.0M | Oceania |
| Canada | 35.0% | 14.3M | North America |
| South Korea | 30.7% | 16.0M | East Asia |
| Germany | 28.6% | 24.0M | Europe |
| United States | 28.3% | 98.2M | North America |
| Malaysia | 19.7% | 6.7M | Southeast Asia |
| Japan | 19.1% | 23.7M | East Asia |
| Brazil | 17.1% | 36.9M | South America |
| India | 15.7% | 229M | South Asia |
| Indonesia | 12.7% | 35.6M | Southeast Asia |
| Nigeria | 9.3% | 21.4M | Africa |

## API

The dataset is available as a JSON file you can fetch directly:

```
https://aiadoption-gray.vercel.app/api/v1/countries.json
```

### Usage

```javascript
const res = await fetch('https://aiadoption-gray.vercel.app/api/v1/countries.json');
const data = await res.json();

// Get all countries sorted by adoption rate
const ranked = data.countries.sort((a, b) => b.adoption - a.adoption);

// Get a specific country
const usa = data.countries.find(c => c.iso === 'US');
console.log(`${usa.name}: ${usa.adoption}% adoption, ${usa.population}M people`);
```

```python
import requests

data = requests.get('https://aiadoption-gray.vercel.app/api/v1/countries.json').json()

for country in sorted(data['countries'], key=lambda c: -c['adoption']):
    users = country['population'] * country['adoption'] / 100
    print(f"{country['name']:20s} {country['adoption']:5.1f}%  ~{users:.0f}M users")
```

### Data schema

Each country object contains:

| Field | Type | Description |
|-------|------|-------------|
| `id` | string | Short identifier (e.g. `"us"`, `"cn"`) |
| `name` | string | Full country name |
| `iso` | string | ISO 3166-1 alpha-2 code |
| `region` | string | Geographic region |
| `population` | number | Population in millions (2025 est.) |
| `adoption` | number | Gen AI adoption rate, % of working-age population |
| `paid` | number | Estimated % of population with paid AI subscriptions |
| `aiWorkforce` | number | % of population working professionally in AI/ML |
| `researchers` | number | % of population in AI research/academia |
| `aiInvestment` | string | Private AI investment in 2024 |
| `microsoftRank` | number\|null | Rank in Microsoft AI Diffusion Report (if available) |
| `highlight` | string | Key insight about this country |
| `detail` | string | Additional context |

## Data sources

- [Microsoft AI Diffusion Report H2 2025](https://www.microsoft.com/en-us/corporate-responsibility/topics/ai-economy-institute/reports/global-ai-adoption-2025/) — primary source for adoption rates
- [Stanford HAI AI Index Report 2025](https://hai.stanford.edu/ai-index/2025-ai-index-report) — AI investment, publications, models
- [DemandSage ChatGPT Statistics](https://www.demandsage.com/chatgpt-statistics/) — ChatGPT traffic by country
- [CNBC/LinkedIn AI Talent Data](https://www.cnbc.com/2025/04/11/linkedin-these-countries-have-a-high-concentration-of-ai-talent.html) — AI workforce
- [CNNIC 57th Statistical Report](https://english.www.gov.cn/archive/statistics/202602/05/content_WS698442cac6d00ca5f9a08edc.html) — China domestic gen AI users
- [UN World Population Prospects](https://population.un.org/wpp/) — population data

See the full list of 14 sources in [`api/v1/countries.json`](api/v1/countries.json).

## Run locally

No build step needed — just serve the HTML file:

```bash
# Python
python3 -m http.server 8090

# Node
npx serve .

# Or just open index.html directly in your browser
```

## Tech stack

Single `index.html` file: React 18 + Babel standalone, all data inline. No dependencies, no build step.

## Contributing

PRs welcome! Especially for:
- Adding more countries
- Updating data as new reports come out
- Improving the visualization
- Building a proper REST API

## License

MIT
