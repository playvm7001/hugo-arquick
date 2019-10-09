# Arquick Hugo Static website

## Custom Page Layout

- add layout attr to page front matter and to themes layouts

## Translating the themes

- add to config
`
languageCode = "ar" 
DefaultContentLanguage = "ar"
`
- add ar.toml to <theme>\i18n to [translate strings](https://gohugo.io/content-management/multilingual/#translation-of-strings)

## Adding image custom type

- to do so i need to add post type dir https://gohugo.io/content-management/types/
- then loop for this custom type , see section here https://gohugo.io/templates/lists/

## Don't forget to

- specify baseURL in config

## adding analytics

- get code and add it to config.toml
- add `{{ template "_internal/google_analytics.html" . }}` to theme head

---
## package json
```
{
  "name": "arquick",
  "version": "1.0.0",
  "description": "- add layout attr to page front matter and to themes layouts",
  "main": "index.js",
  "dependencies": {
    "litecontentsync": "^1.0.9"
  },
  "devDependencies": {},
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "sync": "node ./node_modules/litecontentsync/sync"
  },
  "author": "",
  "license": "ISC"
}
```

---
## To Change Sitemap priority or listing
- I created a new sitemap.xml layout to exclude pages with private set to true in front matter
- Using Index Pages: *_index.md*  allows you to add front matter and content to your list templates
- You can set 
```
[sitemap]
  priority = "0.5"
```

## To Disable taxonomies
in config.toml `disableKinds= ["taxonomy","taxonomyTerm"]`

## To Add Comments ( Todo )
https://gohugo.io/content-management/comments/
https://binarymist.io/blog/2018/02/24/hugo-with-staticman-commenting-and-subscriptions/