---
title: "Screenshots"
date: 2020-09-21T13:25:43+10:00
draft: false
---


# Home

<!-- traditional markdown image reference only works if config has canonifyurls = true when deploying to github project page site (which are the ones with the trailing project path in the url e.g. the /projectname/ in baseURL = "https://user.github.io/projectname/" ) -->
![Image](/images/screenshot1.png)

# List

<!-- Note this use of abs-url shortcode not necessary if config has canonifyurls = true -->
![screenshot2]({{< abs-url "images/screenshot2.png" >}})

# Single

{{< thumb-small "/images/screenshot3.png" >}}

{{< thumb src="/images/screenshot3.png" width=300 >}}

end of page
