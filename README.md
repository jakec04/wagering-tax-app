# Illinois Per-Wager Sports Betting Tax Calculator

This repository contains a fully static HTML/JavaScript interactive that illustrates how Illinois’ per-wager online sports betting tax affects individual bettors. The tool runs entirely in the browser—no Shiny server required—and can be embedded in news articles or hosted on GitHub Pages.

Users can enter their own betting habits to see how the state’s per-wager fee accumulates per bet, per week and over longer periods of time. The calculator was developed alongside reporting from DePaul University’s Center for Journalism Integrity and Excellence (CJIE) on the evolution of Illinois’ sports wagering laws, including the state’s per-wager tax enacted in 2025.

## Live Version

View the calculator on GitHub Pages: https://jakec04.github.io/wagering-tax-app/

## Background

Illinois is the first state in the United States to implement a per-wager tax on online sports bets. Under the law:

- Sportsbooks are charged $0.25 per wager for the first 20 million annual online wagers  
- After that threshold, the cost increases to $0.50 per wager  
- Many operators pass this fee directly to bettors through increased minimum wagers or per-bet charges  

This application demonstrates how the per-wager fee accumulates for an individual bettor based on:

- Number of bets per week  
- Average bet size  
- Length of betting period  

Default values reflect median betting habits reported in a 2024 Stanford study on online wagering behavior.

## Embedding

To embed the calculator in another site, use the following iframe snippet:

```html
<div id="wager-calculator-embed" style="width: 100%; margin: 0 auto;">
  <iframe
    id="wager-calculator-frame"
    src="https://jakec04.github.io/wagering-tax-app/"
    style="width: 100%; border: 0; overflow: hidden;"
    scrolling="no"
  ></iframe>
</div>

<script>
window.addEventListener("message", function(event) {
  if (event.data && event.data.type === "embedHeight") {
    var iframe = document.getElementById("wager-calculator-frame");
    if (iframe) {
      iframe.style.height = event.data.height + "px";
    }
  }
});
</script>

## Author

Developed by Jake Cox for the DePaul University Center for Journalism Integrity and Excellence.

**GitHub:** https://github.com/jakec04  
**Email:** coxja2204@gmail.com
