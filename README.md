# aiadoption

Open data and interactive visualization of AI adoption rates across 147 countries.

**Live site:** [aiadoption-gray.vercel.app](https://aiadoption-gray.vercel.app)

Part of the [aiforgood.my](https://aiforgood.my) project — a hub for open-source AI projects for good.

## What is this?

An interactive dot-grid visualization showing how AI adoption varies dramatically across countries — from the UAE at 64% to Cambodia at 5.1%. Each dot represents 0.25% of a country's population, color-coded by adoption category.

Inspired by [global-ai-adoption.netlify.app](https://global-ai-adoption.netlify.app/) which tracks global AI adoption over time. This project focuses on comparing adoption **by country**.

## Countries covered

147 countries, sorted by adoption rate. Adoption is the H2 2025 figure from the Microsoft AI Diffusion Report (China uses CNNIC data instead, since ChatGPT is banned there). AI Users ≈ population × adoption.

<details>
<summary><strong>Show all 147 countries</strong></summary>

| Country | Adoption | AI Users | Region |
|---------|----------|----------|--------|
| UAE | 64.0% | 7.3M | Middle East |
| Singapore | 60.9% | 3.7M | Southeast Asia |
| Norway | 46.4% | 2.6M | Europe |
| Ireland | 44.6% | 2.4M | Europe |
| France | 44.0% | 29.9M | Europe |
| China | 42.8% | 603M | East Asia |
| Spain | 41.8% | 20.0M | Europe |
| New Zealand | 40.5% | 2.1M | Oceania |
| Netherlands | 38.9% | 7.0M | Europe |
| United Kingdom | 38.9% | 26.5M | Europe |
| Qatar | 38.3% | 1.1M | Middle East |
| Australia | 36.9% | 10.0M | Oceania |
| Israel | 36.1% | 3.5M | Middle East |
| Belgium | 36.0% | 4.2M | Europe |
| Canada | 35.0% | 14.3M | North America |
| Switzerland | 34.8% | 3.1M | Europe |
| Sweden | 33.3% | 3.5M | Europe |
| Austria | 31.4% | 2.9M | Europe |
| South Korea | 30.7% | 16.0M | East Asia |
| Hungary | 29.8% | 2.9M | Europe |
| Denmark | 28.7% | 1.7M | Europe |
| Germany | 28.6% | 24.0M | Europe |
| Poland | 28.5% | 10.5M | Europe |
| Taiwan | 28.4% | 6.6M | East Asia |
| United States | 28.3% | 98.2M | North America |
| Czechia | 27.8% | 3.0M | Europe |
| Italy | 27.8% | 16.3M | Europe |
| Bulgaria | 27.3% | 1.7M | Europe |
| Finland | 27.3% | 1.5M | Europe |
| Jordan | 27.0% | 3.1M | Middle East |
| Costa Rica | 26.5% | 1.4M | Central America |
| Slovenia | 26.5% | 557K | Europe |
| Saudi Arabia | 26.2% | 8.7M | Middle East |
| Lebanon | 25.7% | 1.4M | Middle East |
| Oman | 24.2% | 1.1M | Middle East |
| Portugal | 24.2% | 2.5M | Europe |
| Slovakia | 23.8% | 1.3M | Europe |
| Croatia | 23.7% | 924K | Europe |
| Vietnam | 23.5% | 23.4M | Southeast Asia |
| Dominican Republic | 22.7% | 2.6M | Caribbean |
| Uruguay | 22.5% | 765K | South America |
| Lithuania | 22.4% | 627K | Europe |
| Jamaica | 22.1% | 619K | Caribbean |
| Colombia | 22.0% | 11.6M | South America |
| Panama | 21.5% | 968K | Central America |
| Serbia | 21.5% | 1.4M | Europe |
| South Africa | 21.1% | 13.3M | Africa |
| Chile | 20.8% | 4.1M | South America |
| Malaysia | 19.7% | 6.7M | Southeast Asia |
| Argentina | 19.6% | 9.0M | South America |
| Bosnia and Herzegovina | 19.5% | 624K | Europe |
| Greece | 19.1% | 2.0M | Europe |
| Japan | 19.1% | 23.7M | East Asia |
| Kuwait | 19.1% | 936K | Middle East |
| Philippines | 18.3% | 21.5M | Southeast Asia |
| Georgia | 18.2% | 673K | Central Asia |
| Mexico | 17.8% | 23.3M | North America |
| Ecuador | 17.7% | 3.2M | South America |
| Brazil | 17.1% | 36.9M | South America |
| Moldova | 17.0% | 510K | Europe |
| Albania | 16.5% | 462K | Europe |
| El Salvador | 16.2% | 1.0M | Central America |
| Romania | 16.2% | 3.1M | Europe |
| India | 15.7% | 229M | South Asia |
| Azerbaijan | 15.5% | 1.6M | Central Asia |
| Guatemala | 14.8% | 2.7M | Central America |
| Peru | 14.7% | 5.1M | South America |
| Türkiye | 14.6% | 12.5M | Middle East |
| Mongolia | 14.3% | 501K | East Asia |
| Namibia | 13.8% | 414K | Africa |
| Botswana | 13.7% | 370K | Africa |
| Kazakhstan | 13.7% | 2.8M | Central Asia |
| Libya | 13.7% | 1.0M | Africa |
| Egypt | 13.4% | 15.6M | Africa |
| Gabon | 13.4% | 335K | Africa |
| Honduras | 13.1% | 1.4M | Central America |
| Nepal | 13.0% | 4.0M | South Asia |
| Senegal | 12.9% | 2.4M | Africa |
| Indonesia | 12.7% | 35.6M | Southeast Asia |
| Tunisia | 12.7% | 1.6M | Africa |
| Zambia | 12.3% | 2.6M | Africa |
| Algeria | 12.0% | 5.6M | Africa |
| Côte d'Ivoire | 11.7% | 3.7M | Africa |
| Bolivia | 11.6% | 1.4M | South America |
| Iraq | 11.2% | 5.2M | Middle East |
| Paraguay | 11.0% | 759K | South America |
| Gambia | 10.9% | 305K | Africa |
| Morocco | 10.9% | 4.2M | Africa |
| Iran | 10.7% | 9.5M | Middle East |
| Nicaragua | 10.7% | 749K | Central America |
| Thailand | 10.7% | 7.7M | Southeast Asia |
| Pakistan | 10.3% | 25.3M | South Asia |
| Angola | 9.7% | 3.7M | Africa |
| Madagascar | 9.7% | 3.0M | Africa |
| Malawi | 9.7% | 2.1M | Africa |
| Mozambique | 9.7% | 3.4M | Africa |
| Benin | 9.3% | 1.3M | Africa |
| Burkina Faso | 9.3% | 2.2M | Africa |
| Ghana | 9.3% | 3.2M | Africa |
| Guinea | 9.3% | 1.4M | Africa |
| Guinea-Bissau | 9.3% | 205K | Africa |
| Liberia | 9.3% | 521K | Africa |
| Mali | 9.3% | 2.2M | Africa |
| Mauritania | 9.3% | 465K | Africa |
| Niger | 9.3% | 2.5M | Africa |
| Nigeria | 9.3% | 21.4M | Africa |
| Sierra Leone | 9.3% | 818K | Africa |
| Togo | 9.3% | 884K | Africa |
| Lesotho | 9.1% | 209K | Africa |
| Myanmar | 9.1% | 5.0M | Southeast Asia |
| French Guiana | 9.0% | 27K | South America |
| Guyana | 9.0% | 72K | South America |
| Suriname | 9.0% | 54K | South America |
| Ukraine | 9.0% | 3.3M | Europe |
| Venezuela | 9.0% | 2.6M | South America |
| Belarus | 8.4% | 764K | Europe |
| Kyrgyzstan | 8.2% | 590K | Central Asia |
| Kenya | 8.1% | 4.6M | Africa |
| Russia | 8.0% | 11.5M | Europe |
| Cameroon | 7.8% | 2.3M | Africa |
| Central African Republic | 7.8% | 437K | Africa |
| Chad | 7.8% | 1.5M | Africa |
| Congo | 7.8% | 491K | Africa |
| Congo (DRC) | 7.8% | 8.3M | Africa |
| Haiti | 7.6% | 904K | Caribbean |
| Zimbabwe | 7.6% | 1.3M | Africa |
| Papua New Guinea | 7.3% | 774K | Oceania |
| Bangladesh | 7.1% | 12.4M | South Asia |
| Syria | 7.1% | 1.7M | Middle East |
| Burundi | 6.8% | 898K | Africa |
| Eritrea | 6.8% | 252K | Africa |
| Ethiopia | 6.8% | 8.8M | Africa |
| Somalia | 6.8% | 1.3M | Africa |
| South Sudan | 6.8% | 782K | Africa |
| Sudan | 6.8% | 3.4M | Africa |
| Tanzania | 6.8% | 4.7M | Africa |
| Uganda | 6.8% | 3.4M | Africa |
| Laos | 6.7% | 523K | Southeast Asia |
| Armenia | 6.6% | 198K | Central Asia |
| Sri Lanka | 6.6% | 1.5M | South Asia |
| Rwanda | 6.3% | 901K | Africa |
| Uzbekistan | 6.3% | 2.3M | Central Asia |
| Cuba | 6.1% | 671K | Caribbean |
| Afghanistan | 5.6% | 2.4M | South Asia |
| Tajikistan | 5.6% | 582K | Central Asia |
| Turkmenistan | 5.6% | 420K | Central Asia |
| Cambodia | 5.1% | 887K | Southeast Asia |

</details>

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
