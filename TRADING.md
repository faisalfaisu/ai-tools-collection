# Trading notes (saved from shared videos)

Notes, prompts and setup commands from trading videos shared for review. The trading tool repos themselves are listed in [README.md](README.md) (TradingAgents, day-trader-skill, tradingview-mcp). Nothing here is financial advice. Profit screenshots in source videos are unverified, and an AI verdict is not a buy signal.

## Stock-analysis prompt (from a shared reel)

Source: Instagram reel by @jainamjainz - https://www.instagram.com/reel/Da2ZJnWTeda/ . The reel is aimed at Indian-listed stocks and links to a paid coaching session; the prompt itself is free to use. Use it to study a company, not as a trading signal.

### The 6 documents to attach (all free)

As listed on screen in the reel (original Hindi-English wording, with plain-English meaning):

1. **Annual Report** - "last 2-3 saal (BSE/NSE ya company website se)" = last 2-3 years, from BSE/NSE or the company website.
2. **MDA Report** - "annual report ke andar hi hota hai, same PDF" = it is a section inside the annual report PDF.
3. **Concall Transcripts** - "last 2-3 quarters (Screener.in ya Tijori Finance se)" = from Screener.in or Tijori Finance.
4. **1D Technical Chart Screenshot** - "TradingView pe 50 EMA, 200 EMA, RSI, Volume ke saath" = daily chart with those indicators visible.
5. **Screener Screenshot** - P/E, ROE, Debt/Equity, Revenue growth, Profit growth, Operating Cash Flow, Promoter holding.
6. **Shareholding Pattern** - "latest quarter (BSE/NSE se)".

### The prompt (transcribed from the reel)

> "Act as a seasoned equity research analyst with 20 years of experience across fundamental analysis, technical analysis, and behavioral finance. I am providing you with the following documents for [Company Name]: annual financial statements, Management Discussion & Analysis, concall transcripts, a daily technical chart, key ratios from Screener, and the latest shareholding pattern.
>
> Tear this company apart across these dimensions:
>
> FUNDAMENTALS - Is this business genuinely healthy or just looks good on surface? Dig into revenue quality, margin trajectory, cash flow vs reported profits, debt structure, and ROE sustainability. Flag any accounting red flags.
>
> MANAGEMENT DNA - Read between the lines of the concall transcripts and MDA. Is management confident or defensive? Are they overpromising and underdelivering? Any change in language tone vs last year? Promoter pledge or stake reduction is an automatic red flag - call it out.
>
> VALUATION REALITY - Is the market pricing in perfection? Compare current P/E, EV/EBITDA against historical averages and sector peers. Tell me if I am paying a premium for growth that may never come.
>
> TECHNICAL STRUCTURE - Where is the stock in its trend cycle? Is it in accumulation, markup, distribution, or markdown phase? Key support and resistance levels. Is volume confirming price action or diverging?
>
> RISK FACTORS - What are the 3 things that could destroy this thesis? Sector risk, company-specific risk, macro risk.
>
> FINAL VERDICT - Buy, Hold, or Avoid. Conviction score out of 10. Price at which this becomes interesting if not now. One line that summarizes this stock.
>
> Do not give me a balanced, diplomatic answer. I want the truth - even if it is uncomfortable."

Note: the "do not give me a balanced, diplomatic answer" line forces a confident verdict - confidence is not accuracy.

## Cloning a tool repo (practice only)

```
gh repo clone Jakeschincariol/day-trader-skill
```

Needs GitHub CLI (`gh`) installed. Cloning only downloads the code: it does not install the Claude skills, connect a broker or place any trades. Keep broker connections, live orders, API keys and paid services off while inspecting a new repo.
