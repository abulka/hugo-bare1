---
title: "Full Size"
date: 2020-09-21T13:25:43+10:00
draft: false
---


# Home

Traditional markdown image reference only works if config has `canonifyurls = true` when deploying to github project page site (which are the ones with the trailing project path in the url e.g. the `/projectname/` in 
```
baseURL = "https://user.github.io/projectname/"
canonifyurls = true
```

traditional markdown is
```
![screenshot1](/images/screenshot1.png)
```

here is the screenshot:

---

![screenshot1](/images/screenshot1.png)

---

# List

Note this use of my custom `abs-url` shortcode *not necessary* if config has `canonifyurls = true`

markdown is
```
![screenshot2]({{</* abs-url "images/screenshot2.png" */>}})
```

here is the screenshot:

---
![screenshot2]({{< abs-url "images/screenshot2.png" >}})

---

# Single

To finish off this screenshot page, here are the four techniques I've developed for showing images in Hugo. 

```
1. {{</* thumb-small "/images/screenshot3.png" */>}}

2. {{</* thumb src="/images/screenshot3.png" width=300 */>}}

3. ![screenshot3]({{</* abs-url "images/screenshot3.png" */>}})

4. ![screenshot3](/images/screenshot3.png)
```

## 1
Uses `thumb-small` shortcode which takes one positional parameter
```
<img src="{{ .Get 0 }}" width="200">
```
{{< thumb-small "/images/screenshot3.png" >}}

## 2
Uses `thumb` shortcode which takes named parameters
```
<img src="{{ .Get "src" }}" width="{{ .Get "width" }}">
```

{{< thumb src="/images/screenshot3.png" width=300 >}}

## 3
Uses image markdown but wraps the url in `abs-url` which expands the url correctly on github project pages sites.

![screenshot3]({{< abs-url "images/screenshot3.png" >}})

## 4
Traditional markdown. Simple, but needs `canonifyurls = true` when your `baseURL` is a github project pages site like `"https://user.github.io/projectname/"`

![screenshot3](/images/screenshot3.png)

---

**Note**, For this documentation page, the trick to displaying shortcodes (without them activating and expanding) inside code blocks is to add `/*` and `*/` inside the shortcode as per this [post info](https://github.com/gohugoio/hugo/issues/7561#issuecomment-674197381).

end of page
