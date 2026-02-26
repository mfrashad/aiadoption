# aiadoption

Open data and interactive visualization of AI adoption rates across 16 countries.

**Live site:** [aiadoption.dev](https://aiadoption.dev) _(coming soon)_

## What is this?

An interactive dot-grid visualization showing how AI adoption varies dramatically across countries — from the UAE at 64% to Nigeria at 7%. Each dot represents 0.25% of a country's population, color-coded by adoption category.

Inspired by [global-ai-adoption.netlify.app](https://global-ai-adoption.netlify.app/) which tracks global AI adoption over time. This project adapts that concept to compare adoption **by country**.

## Countries covered

| Country | Adoption | AI Users | Region |
|---------|----------|----------|--------|
| UAE | 64.0% | 7.3M | Middle East |
| Singapore | 60.9% | 3.7M | Southeast Asia |
| France | 44.0% | 29.9M | Europe |
| China | 42.8% | 603M | East Asia |
| United Kingdom | 40.5% | 27.5M | Europe |
| Australia | 38.9% | 10.5M | Oceania |
| Canada | 35.0% | 14.3M | North America |
| Malaysia | 32.0% | 10.9M | Southeast Asia |
| Germany | 31.4% | 26.4M | Europe |
| South Korea | 30.7% | 16.0M | East Asia |
| United States | 28.3% | 98.2M | North America |
| Indonesia | 25.0% | 70.0M | Southeast Asia |
| Japan | 19.1% | 23.7M | East Asia |
| India | 18.0% | 263M | South Asia |
| Brazil | 16.0% | 34.6M | South America |
| Nigeria | 7.0% | 16.1M | Africa |

## API

The dataset is available as a JSON file you can fetch directly:

```
https://raw.githubusercontent.com/mfrashad/aiadoption/main/api/v1/countries.json
```

### Usage

```javascript
const res = await fetch('https://raw.githubusercontent.com/mfrashad/aiadoption/main/api/v1/countries.json');
const data = await res.json();

// Get all countries sorted by adoption rate
const ranked = data.countries.sort((a, b) => b.adoption - a.adoption);

// Get a specific country
const usa = data.countries.find(c => c.iso === 'US');
console.log(`${usa.name}: ${usa.adoption}% adoption, ${usa.population}M people`);
```

```python
import requests

data = requests.get('https://raw.githubusercontent.com/mfrashad/aiadoption/main/api/v1/countries.json').json()

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
- [CNNIC](https://www.chinadaily.com.cn/a/202602/05/WS6984014ca310d6866eb37a16.html) — China domestic gen AI users
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
