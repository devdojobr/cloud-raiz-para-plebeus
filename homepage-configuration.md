## widget.yml
```yaml
---
# For configuration options and examples, please see:
# https://gethomepage.dev/configs/service-widgets


- logo:
    icon: https://devdojo.academy/images/LOGO_WHITE.svg

- resources:
    cpu: true
    memory: true
    disk: /
    cputemp: true
    tempmin: 0 # optional, minimum cpu temp
    tempmax: 100 # optional, maximum cpu temp
    uptime: true
    units: imperial # only used by cpu temp
    refresh: 3000 # optional, in ms
    diskUnits: bytes # optional, bytes (default) or bbytes. Only applies to disk

- openmeteo:
    label: Atlanta # optional
    units: metric # or imperial
    cache: 5 # Time in minutes to cache API responses, to stay within limits
    format: # optional, Intl.NumberFormat options
      maximumFractionDigits: 1

- search:
    provider: google
    target: _blank
```

## settings.yml

```yaml
title: DevDojo Academy

theme: dark
useEqualHeights: true
headerStyle: boxedWidgets
iconStyle: defaults
showStats: true

base: https://dashboard.scrumlio.com/homepage

background:
  image: https://wallpapers.com/images/hd/dark-samurai-ozptbd1ntlz67j3r.jpg
  blur: sm # sm, "", md, xl... see https://tailwindcss.com/docs/backdrop-blur
  saturate: 50 # 0, 50, 100... see https://tailwindcss.com/docs/backdrop-saturate
  brightness: 50 # 0, 50, 75... see https://tailwindcss.com/docs/backdrop-brightness
  opacity: 50 # 0-100

#color: indigo
layout:
  Apps:
    style: row
    columns: 4

quickLaunch:
  searchDescriptions: true
  hideInternetSearch: true
  showSearchSuggestions: true
  hideVisitURL: true
  provider: google # google, duckduckgo, bing, baidu, brave or custom
```

## services.yml

```yaml
---
# For configuration options and examples, please see:
# https://gethomepage.dev/configs/services

- Apps:
    - Grafana:
        icon: grafana.png
        href: https://grafana.scrumlio.com
        description: Monitoring and observability platform
        showStats: true

    - Portainer:
          icon: portainer.png
          href: https://portainer.scrumlio.com
          description: Docker container management tool
          showStats: true

    - Uptime Kuma:
          icon: uptime-kuma.png
          href: https://uptime.scrumlio.com
          description: Self-hosted monitoring tool
          showStats: true

    - Authentik:
          icon: authentik.png
          href: https://authentik.scrumlio.com
          description: Identity provider for authentication
          showStats: true

    - Nginx:
          icon: nginx.png
          href: https://proxy.scrumlio.com
          description: Reverse Proxy Provider
          showStats: true
```
