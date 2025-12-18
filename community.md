---
layout: guide
title: Community Projects
description: Design projects initiated by the Bitcoin Design Community.
permalink: /community/
main_nav: false
main_classes: -no-top-padding
image: https://bitcoin.design/assets/images/projects/projects-preview.jpg
projects:
  - name: Bitcoin Design Guide
    description: The primary project we are working on, a resource for designers to create better bitcoin products faster.
    image:
      url: /assets/images/projects/design-guide.png
      width: 75
      height: 75
    links:
      - name: Site
        link: https://bitcoin.design/guide
      - name: How to contribute
        link: https://bitcoin.design/guide/contribute/

  - name: Bitcoin UI Kit
    description: A complete design system to serve as a foundation for wallet concepts, prototypes and application development.
    image:
      url: /assets/images/projects/bitcoin-ui-kit.svg
      width: 75
      height: 75
    links:
      - name: Site
        link: https://bitcoinuikit.com
      - name: Figma
        link: https://www.figma.com/community/file/916680391812923706/Bitcoin-Wallet-UI-Kit-(work-in-progress)
      - name: Github
        link: https://github.com/GBKS/bitcoin-wallet-ui-kit

  - name: Bitcoin Icon set
    description: Icons for typical needs of bitcoin applications. Includes common generic icons like arrows, and more unique ones like a wallet, keys, mining, and bitcoin symbols.
    image:
      url: /assets/images/projects/bitcoin-icon-set.svg
      width: 75
      height: 75
    links:
      - name: Site
        link: https://bitcoinicons.com
      - name: Figma
        link: https://www.figma.com/community/file/948545404023677970/Bitcoin-icon-set
      - name: Github
        link: https://github.com/BitcoinDesign/Bitcoin-Icons

  - name: Bitcoin UX Research Toolkit
    description: Build human-centric bitcoin products for everyone with this practical guide and toolbox for user research.
    image:
      url: /assets/images/projects/research-kit.svg
      width: 75
      height: 75
    links:
      - name: Site
        link: https://bitcoinresearch.xyz

  - name: Bitcoin Design Foundation
    description: An initiative to make the community and its efforts sustainable.
    image:
      url: /assets/images/projects/foundation.png
      width: 75
      height: 75
    links:
      - name: Website
        link: https://opencollective.com/bitcoin-design-foundation
      - name: Discord
        link: https://discord.gg/V4xwxTBett

  - name: When Taproot
    description: Promote broader adoption of Taproot.
    image:
      url: /assets/images/projects/whentaproot.png
      width: 75
      height: 75
    links:
      - name: More info
        link: https://whentaproot.org
      - name: Collaboration
        link: https://github.com/BitcoinDesign/Meta/issues/347

  - name: Bitcoin QR
    description: Help get unified QR codes adopted for smoother payment flows.
    image:
      url: /assets/images/projects/bitcoinqr.png
      width: 75
      height: 75
    links:
      - name: More info
        link: https://bitcoinqr.dev

  - name: BOLT 12
    description: Promoting adoption of BOLT 12 and Async Payments for better lightning experiences.
    image:
      url: /assets/images/projects/bolt12.png
      width: 75
      height: 75
    links:
      - name: Discord
        link: https://discord.gg/ZTM6qHSsJt

  - name: Designathon
    description: We organized a hackathon for designers.
    image:
      url: /assets/images/projects/designathon.png
      width: 75
      height: 75
    links:
      - name: Event site
        link: https://event.bitcoin.design

  - name: Bitcoin Design Sprints
    description: This project from 2022 was about improving lightning network wallets through applying the design guide, design thinking and problem solving.
    image:
      url: /assets/images/projects/wallet-design-sprints.png
      width: 75
      height: 75
    links:
      - name: More info
        link: https://github.com/BitcoinDesign/Meta/issues/244
      - name: Slack (Archive)
        link: https://bitcoindesign.slack.com/archives/C02VCHSQECT
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

# Community Projects

These are design projects we have initiated ourselves. Projects launched by community members often focus on creating design resources.

For more details, see our [Project](https://github.com/BitcoinDesign/Meta/blob/master/Projects.md) document. If you are interested in getting involved, reach out directly to the projects below, or reach out in our [Discord]({{ site.discord_invite_url }}).

<div class="project-grid">
  {% for item in page.projects %}
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
