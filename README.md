<img src="https://cdn.glowmedia.es/upload/uploads/d53f37cookies-preview.png" data-canonical-src="https://cdn.glowmedia.es/upload/uploads/d53f37cookies-preview.png" width="100%" />


![Badge-glow](https://img.shields.io/badge/GlowCookies-v.3.0.1-blue) ![jsDelivr hits (GitHub)](https://img.shields.io/jsdelivr/gh/hm/manucaralmo/GlowCookies) ![GitHub repo size](https://img.shields.io/github/repo-size/manucaralmo/GlowCookies) ![GitHub Repo stars](https://img.shields.io/github/stars/manucaralmo/GlowCookies?style=social)

# GlowCookies - Cookie Consent Banner In JavaScript for Google Analytics, Facebook Pixel & more
Simple and full automated cookies banner for any website. Complies with the new European regulations with GlowCookies. Activate and deactivate Google Analytics, Facebook Pixel, Hotjar (and coming soon) cookies whenever the user wishes, with just 1 click.

[![Foo](https://cdn.glowmedia.es/upload/uploads/ed1952btn.svg)](https://manucaralmo.github.io/glow-cookies-web/)


## The cookies banner
<img src="https://cdn.glowmedia.es/upload/uploads/90c82dbanner.png" data-canonical-src="https://cdn.glowmedia.es/upload/uploads/90c82dbanner.png" width="375" />

## How it works
You just have to install the code. When the user clicks on accept cookies, the google analytics tracking code, Facebook Pixel and/or Hotjar starts tracking. If the user rejects cookies, the tracking code will not start working.

## How to use
Add this code to your html `<head>` or `<body>` tag.
```html
<script src="https://cdn.jsdelivr.net/gh/manucaralmo/GlowCookies@3.0.1/src/glowCookies.min.js"></script>
<script>
    glowCookies.start('en', { 
        analytics: 'G-FH87DE17XF', 
        facebookPixel: '990955817632355',
        policyLink: 'https://google.es'
    });
</script>
```

## Languages `New`
Now you can choose between two available languages: English and Spanish.
In the first parameter of the start() method add `'es'` for Spanish or `'en'` for English.

## Tracking options
These are the parameters that you can modify to add your tracking codes or custom scripts.

| Parameter | Type | Values |
| ------------- | ------------- | ------------- |
| `analytics` | String  | Example: `"G-FH87DE17XF"` (Analytics tracking code) |
| `facebookPixel` | String  | Example: `"990955817632355"` (Facebook Pixel code) |
| `HotjarTrackingCode` | String  | Example: `"990955817632355"` (Hotjar tracking code) |
| `customScript` (Inline) | Object  | Example: `[{ type: 'custom', position: 'body', content: 'console.log('custom script');' }]` |
| `customScript` (src) | Object  | Example: `[{ type: 'src', position: 'head', content: 'https://www.googletagmanager.com/gtag/js?id=G-FH87DE17XF' }]` |

## Config Banner
These are the parameters that you can modify to change certain banner options

| Parameter | Type | Values |
| ------------- | ------------- | ------------- |
| `policyLink` | String  | Example: `"https://yourlink.com"` (Your cookies policy link) |
| `hideAfterClick` | Boolean  | (`true` or `false`) Default: `true` (Hide banner after Accept or Reject cookies) |


## Customize Banner
Now there are certain parameters that you can change to customize your banner.

| Parameter | Type | Values |
| ------------- | ------------- | ------------- |
| `border` | String | (`"border"` or `"none"`) Default: `"border"` |
| `position` | String | (`"left"` or `"right"`) Default: `"left"` |
| `bannerDescription` | String  | Example: `"We use our own and third-party cookies to personalize content and to analyze web traffic."` |
| `bannerLinkText` | String  | Example: `"Read more about cookies"` |
| `bannerBackground` | String  | Example: `"#FAFAFA"` Example: `"lightblue"` |
| `bannerColor` | String  | Example: `"#000"` Example: `"blue"` |
| `bannerHeading` | String  | Example: `"Use of cookies"` Default: None |
| `acceptBtnText` | String  | Example: `"Accept cookies"` |
| `acceptBtnColor` | String  | Example: `"#000"` Example: `"blue"` |
| `acceptBtnBackground` | String  | Example: `"#fff"` Example: `"white"` |
| `rejectBtnText` | String  | Example: `"Reject"` |
| `rejectBtnBackground` | String  | Example: `"#000"` Example: `"blue"` |
| `rejectBtnColor` | String  | Example: `"#fff"` Example: `"white"` |
| `manageColor` | String  | Example: `"#fff"` Example: `"white"` |
| `manageBackground` | String  | Example: `"#f2f2f2"` Example: `"blue"` |
| `manageText` | String  | Example: `"Manage cookies"` |


## Fully customized banner
```html
<script src="https://cdn.jsdelivr.net/gh/manucaralmo/GlowCookies@3.0.1/src/glowCookies.min.js"></script>
<script>
    glowCookies.start('en', { 
        analytics: 'G-FH87DE17XF', 
        facebookPixel: '990955817632355',
        hideAfterClick: true,
        border: 'none',
        position: 'right',
        policyLink: 'https://google.es',
        customScript: [{ type: 'custom', position: 'body', content: `console.log('my custom js');` }],
        bannerDescription: 'banner desc',
        bannerLinkText: 'banner link text',
        bannerBackground: '#000',
        bannerColor: '#fafafa',
        bannerHeading: '<h2>Cookies</h2>',
        acceptBtnText: 'accept btn text',
        acceptBtnColor: 'green',
        acceptBtnBackground: 'red',
        rejectBtnText: 'reject btn text',
        rejectBtnBackground: 'lightblue',
        rejectBtnColor: 'blue',
        manageColor: 'white',
        manageBackground: 'blue',
        manageText: 'cookies text'
    });
</script>
```

## Next steps
- [ ] Advanced cookies management
- [ ] Banner templates
- [ ] Custom cookies icon

### Request features
info@glowmedia.es
