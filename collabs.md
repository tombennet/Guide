---
layout: guide
title: Collaborations
description: Projects we collaborate with to improve bitcoin design and user experience.
permalink: /collabs/
main_nav: false
main_classes: -no-top-padding
image: https://bitcoin.design/assets/images/projects/projects-preview.jpg
collaborations:
  - name: Wallet Scrutiny
    description: Redesign of an important security resource.
    image:
      url: /assets/images/projects/wallet-scrutiny.png
      width: 75
      height: 75
    links:
      - name: More info
        link: https://walletscrutiny.com
      - name: Collaboration
        link: https://github.com/BitcoinDesign/Meta/issues/415

  - name: Saving Satoshi
    description: A sci-fi epic that teaches you bitcoin coding.
    image:
      url: /assets/images/projects/saving-satoshi.png
      width: 75
      height: 75
    links:
      - name: More info
        link: https://savingsatoshi.com

  - name: Summer of Bitcoin
    description: We support and mentor students in this educational initiative.
    image:
      url: /assets/images/projects/summer-of-bitcoin.png
      width: 75
      height: 75
    links:
      - name: More info
        link: https://summerofbitcoin.org

  - name: Alby
    description: Alby brings Bitcoin to the web with in-browser payments and identity, no account required.
    image:
      url: /assets/images/projects/alby.png
      width: 75
      height: 75
    links:
      - name: Site
        link: https://getalby.com/
      - name: Collaboration
        link: https://github.com/BitcoinDesign/Meta/issues/113
      - name: Telegram
        link: https://t.me/getAlby

  - name: Bitcoin Core app
    description: Building an application that lets users easily run full bitcoin nodes.
    image:
      url: /assets/images/projects/bitcoin-core.png
      width: 75
      height: 75
    links:
      - name: Design docs
        link: https://bitcoincore.app
      - name: Collaboration
        link: https://github.com/BitcoinDesign/Meta/issues/238

  - name: Bitcoin Smiles
    description: Raising bitcoin for dentistry treatments.
    image:
      url: /assets/images/projects/bitcoin-smiles.png
      width: 75
      height: 75
    links:
      - name: Site
        link: https://bitcoinsmiles.org/
      - name: Twitter
        link: https://twitter.com/BitcoinSmiles

  - name: Jam
    description: A web UI for JoinMarket, for creating private bitcoin transactions called CoinJoins.
    image:
      url: /assets/images/projects/joinmarket.png
      width: 75
      height: 75
    links:
      - name: Site
        link: https://jamapp.org
      - name: Collaboration
        link: https://github.com/BitcoinDesign/Meta/issues/239
      - name: Telegram
        link: https://t.me/JoinMarketWebUI

  - name: Zeus
    description: Zeus is an open-source, non-custodial bitcoin wallet that gives you full control over how you make payments.
    image:
      url: /assets/images/projects/zeus.png
      width: 75
      height: 75
    links:
      - name: Site
        link: https://zeusln.app/
      - name: Collaboration
        link: https://github.com/BitcoinDesign/Meta/issues/70
      - name: Telegram
        link: https://t.me/zeusLN

  - name: Bolt.fun
    description: Learn about the lightning network, post your apps on the market, and join our hackathons.
    image:
      url: /assets/images/projects/bolt-fun.png
      width: 75
      height: 75
    links:
      - name: Site
        link: https://bolt.fun/

  - name: Stratum V2
    description: Stratum V2 is the next generation protocol for pooled mining.
    image:
      url: /assets/images/projects/stratum-v2.png
      width: 75
      height: 75
    links:
      - name: Site
        link: https://stratumprotocol.org/
      - name: Twitter
        link: https://twitter.com/StratumV2

  - name: Hello Bitcoin
    description: Hello Bitcoin is a volunteer-run project with the simple goal of helping people learn about bitcoin in a way that is friendly and accessible.
    image:
      url: /assets/images/projects/hello-bitcoin.png
      width: 75
      height: 75
    links:
      - name: Site
        link: https://hellobitco.in/
      - name: Collaboration
        link: https://github.com/BitcoinDesign/Meta/issues/170
      - name: Discord
        link: https://discord.gg/j64t8xdwEA
---

{% include picture.html
   image = "/assets/images/projects/projects.jpg"
   retina = "/assets/images/projects/projects@2x.jpg"
   mobile = "/assets/images/projects/projects-mobile.jpg"
   mobileRetina = "/assets/images/projects/projects-mobile@2x.jpg"
   alt-text = "Strong handshake"
   width = 1600
   height = 900
   layout = "full-width"
%}

# Collaborations

Some of us try to help other bitcoin projects improve their products' design and user experience. For more details, see our [Collaboration](https://github.com/BitcoinDesign/Meta/blob/master/Collaboration.md) document.

For a more complete list of current and past collaborations, see our [collaboration board](https://github.com/BitcoinDesign/Meta/projects/2).

If you are interested in getting involved, reach out directly to the projects below, or reach out in our [Discord]({{ site.discord_invite_url }}).

<div class="project-grid">
  {% for item in page.collaborations %}
    <div class="project-grid-item">
      <a class="project-grid-item-image" href="{{- item.links[0].link -}}" target="_blank" rel="noopener">
        <img src="{{ item.image.url | relative_url }}" width="{{ item.image.width }}" height="{{ item.image.height }}" alt="" />
      </a>
      <h3>
        <a href="{{- item.links[0].link -}}" target="_blank" rel="noopener">{{- item.name -}}</a>
      </h3>
      <p>{{- item.description -}}</p>
      <div class="links">
        {% for link in item.links %}
          <a href="{{- link.link -}}" target="_blank" rel="noopener">{{ link.name }}</a>
        {% endfor %}
      </div>
    </div>
  {% endfor %}
</div>

---

[Back to Projects](/projects/)
