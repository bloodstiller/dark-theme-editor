# Dark Theme Editor | Hugo 
[![Example Site](https://github.com/JingWangTW/dark-theme-editor/actions/workflows/hugo.yml/badge.svg)](https://github.com/JingWangTW/dark-theme-editor/actions/workflows/hugo.yml)

> **Dark Theme Editor** is a blog theme for [Hugo](https://gohugo.io/).

DEMO - https://jingwangtw.github.io/dark-theme-editor/

⚠️ The theme needs at least Hugo v0.112.x.

---

## Main Features
* An editor-like theme for Hugo
* Draggable Sidebar
* Fully Responsive
* Fully based on Hugo ecosystem
* Goolge/Bing SEO Support
* Better Code Block
* Multilingual Support

## Usage
### Download manually
You can simply download the theme from [GitGub Repo](https://github.com/JingWangTW/dark-theme-editor) and paste it into the `themes/dark-theme-editor` directory in the root directory of your Hugo site.

### Install theme locally
```
# Under the root directory of your Hugo site.

git clone https://github.com/JingWangTW/dark-theme-editor.git themes/dark-theme-editor
```

This will clone the theme repository directly into the `themes/dark-theme-editor` directory.

### Install theme as submodule
```
# Under the root directory of your Hugo site.

git submodule add -f https://github.com/JingWangTW/dark-theme-editor.git themes/dark-theme-editor
```

This will install the theme repository as a sumbodule in the `themes/dark-theme-editor` directory.

## Configuration
* When using `dark-theme-editor` as the theme for your Hugo site, please remember to set the [theme field in your `hugo.toml` file](https://gohugo.io/getting-started/configuration/#theme).
* Additionally, the theme provides many custom fields for you to configure as needed. Please refer to the [`hugo.toml` file in the theme](https://github.com/JingWangTW/dark-theme-editor/blob/main/config.toml) to find all available options. You can override these values by adding them to your own `hugo.toml` file or by directly modifying the file in the theme directory.
    <details>
    <summary>Click to toggle the full list of configurations.</summary>

    ```toml
    # Theme parameters
    [params]

        # Parameters applied in HTML <head>
        [params.site]
            # Website ICON
            faviconUrl = ""

            # Do you have any CSS in local? List them in an array.
            # They should be placed inside "/assets" dir.
            # And don't named the file as "index.css" and "style.css".
            # These two files are used by the theme.
            localCss = []

            # Do you need to add any external CSS? List them in an array.
            externalCss = []

            # Do you have any script in local? List them in an array.
            # They should be placed inside "/assets" dir.
            # And don't named the file as "index.js"
            # Theis file is used by the theme.
            localJs = []

            # Do you have any external Script need to add on? List them in an array.
            externalJs = []

            # The code you could get from Google Search Console.
            # Please patse the value of content xxx in the following items
            # <meta name="google-site-verification" content="xxxxxxxxxxxxxxxxxxxxxxxxxx" />
            googleVerification = ""

            # The code you could get from Microsoft Bing Webmater
            # Please patse the value of content xxx in the following items
            # <meta name="msvalidate.01" content="xxxxxxxxxxxxxxxxxxxx" />
            bingVerifivation = ""

        # Customized info shown in header of the page
        [params.header]
            # Website title for header banner.
            title = "My New Hugo Site"

            # Subtitle for this site, used in homepage only
            subtitle = "A Site Built by Hugo"

            # Config about your's site logo, remove this item to hide the logo
            [params.header.logo]
                # Where is your site's URL
                imgUrl = ""

                # If the logo is clickable, where should it be linked?
                # In default, it will linked to the homepage of the site.
                logoLink = ""

        # Customized info shown in footer of the page
        [params.footer]
            # CopyRight string shown in the footer. Keep it an empty string or remove this item will hide it from the page.
            copyrightStr = "All Rights Reserved ®."

            # Should show the counter in the footer or not
            # In the home page, it will show the numbers of all pages
            # In the sections pages, it will show the numbers of pages within the section
            # In the taxonomy pages, it will show the numbers of pages belong to the taxonomy.
            # In the regular content pages, it will show the word count.
            counter = true

            # Should show the language of the page or not
            language = true

            # Should show the hugo version or not
            hugoVersion = true

            # Should show the theme info or not
            theme = true

            # Should show the edited time of the page or not
            modifiedTime = true

            # The format of the `modifiedTime`.
            # Refer to page https://gohugo.io/functions/format/ for more detail.
            # Below is the default format, please do not remove it, unless you set `false` in `modifiedTime` field.
            dateFormat = "Jan 02 2006 15:04:05"

            # Should show the current git HEAD hash or not
            # To make this show up correctly, please follow the prerequisites in page
            # https://gohugo.io/variables/git/
            gitHash = true

            # Social link in the footer, listed items are supported, delete unwanted items to hide it.
            [params.footer.socialLink]
                github = ""
                facebook = ""
                twitter = ""
                email = ""
                linkedin = ""
                instagram = ""
                telegram = ""
                medium = ""
                vimeo = ""
                youtube = ""

        # Metadata of the site, value will be used in HTML <header>
        # These value would be used when they didn't appear in the frontmatter of a single page.
        # In other words, these value will be overwritten by the frontmatter in the single page.
        [params.globalFrontmatter]
            # The author of this site. This will be shown in 
            # 1. the footer of all page
            # 2. the author filed in the single page. (this could be overwritten by the frontmatter of the single page.)
            # Keep it an empty string or remove this item will hide it from the page
            author = "Jing Wang"
            
            # Website description for RSS and SEO. Theme will generate a <meta> tag for this item
            description = "This is my new hugo site"

            # Website keywords. Theme will generate a <meta> tag for this item.
            keywords = "hugo,site,new"

        # Parameters applied in the homepage only
        [params.homePage]
            # Long Descripition shown in home page "Start Block". Is is recommended to have the paragraph shorter than 100 words.        
            siteLongDescription = "Hugo is a fast and easy-to-use static website generator written in Go. It renders a complete HTML website from content and templates in a directory, utilizing Markdown files for metadata. It's optimized for speed and suitable for various website types."

            # If you don't like the title of "siteLongDescription" be "Start" (default), 
            # you may change the value of this item to "Description" or something you like.
            siteLongDescriptionTitle = "Start"

            # Param to decide whether to show the most recent blog posts or not. (Default: true)
            showRecentPostsBlock = true

            # Param to decide how many recent posts to show in the home page. (Default: 5)
            numOfRecentPosts = 5

            # Parameter to decide whether to show the URL behind the title.
            # It will be more like an editor if it is shown. However, in general, it can be messy if it is displayed.        
            # (Default: true)
            recentPostShowUrl = true
        
        
        # Paramater applied in the single page
        # These values could be overwritten by the frontmatter in the single page.
        [params.page]
            # Should include Table of Content in front of the page or not.
            includeToc = true

            # Should show the author of the page or not.
            # The author name will be shown in the single page if and only if 
            #   1. this items been set as true and
            #   2. "aurthor" filed been provided in the 
            #       A. single page frontmatter or
            #       B. "author" filed in above "globalFrontmatter" block
            showAuthor = true

            # Should show the date of the page or not
            showDate = true

            # The format of the date.
            # Refer to page https://gohugo.io/functions/format/ for more detail.
            # Below is the default format, please do not remove it, unless you set `false` in `showDate` field.
            dateFormat = "2006.01.02"

            # Should show the estimate reading time in front of the page or not.
            showTimeToRead = true

            # Should show the breadcrumb in front of the page or not.
            showBreadcrumb = true

            # Should show the "copy" button in the codeblock or not.
            codeBlockCopible = true
    ```
    </details>

## Multilingual
* If your site is in [multilingual mode](https://gohugo.io/content-management/multilingual/), there will be a language select icon at the footer of the site. Additionally, there will be a navigator on each translated page.
* Please move the configuration fields that need to be translated under the corresponding language configuration blocks in your `hugo.toml`. There is an example `hugo.multilang.toml` file you could reference. Remember to rename it to `hugo.toml` when needed.
    <details>
    <summary>Click to toggle example <code>hugo.multilang.toml</code> file</summary>

    ```toml
    # Multilingual Setting
    [languages]
        
        [languages.en]
            
            # hugo multilingual setting
            languageCode = 'en-US'
            languageDirection = 'ltr'
            languageName = 'English'
            weight = 1
            
            # Configs that were originally in the "params" section but need to be translated.
            [languages.en.params]
                
                [languages.en.params.header]
                    # Website title for header banner.
                    title = "My New Hugo Site"

                    # Subtitle for this site, used in homepage only
                    subtitle = 'A Site Built by Hugo'
                
                [languages.en.params.footer]
                    # CopyRight string shown in the footer. Keep it an empty string or remove this item will hide it from the page.
                    copyrightStr = "All Rights Reserved ®."

                [languages.en.params.globalFrontmatter]
                    # The author of this site. This will be shown in 
                    # 1. the footer of all page
                    # 2. the author filed in the single page. (this could be overwritten by the frontmatter of the single page.)
                    # Keep it an empty string or remove this item will hide it from the page
                    author = "Jing Wang"
                    
                    # Website description for RSS and SEO. Theme will generate a <meta> tag for this item
                    description = "This is my new hugo site"

                    # Website keywords. Theme will generate a <meta> tag for this item.
                    keywords = "hugo,site,new"

                [languages.en.params.homePage]

                    # Long Descripition shown in home page "Start Block". Is is recommended to have the paragraph shorter than 100 words.        
                    siteLongDescription = "Hugo is a fast and easy-to-use static website generator written in Go. It renders a complete HTML website from content and templates in a directory, utilizing Markdown files for metadata. It's optimized for speed and suitable for various website types."

                    # If you don't like the title of "siteLongDescription" be "Start" (default), 
                    # you may change the value of this item to "Description" or something you like.
                    siteLongDescriptionTitle = "Start"

        # 設定為繁體中文
        [languages.zh]

            # Hugo 多語言設定
            languageCode = 'zh-Hant-TW'
            languageDirection = 'ltr'
            languageName = '繁體中文'
            weight = 2

            # 原本位於 "params" 區段但需要翻譯的設定
            [languages.zh.params]
                
                [languages.zh.params.header]
                    # 頁首橫幅的網站標題。
                    title = "我的新 Hugo 網站"

                    # 本站的副標題，僅用於首頁
                    subtitle = '由 Hugo 建立的網站'

                [languages.zh.params.footer]
                    # 在頁尾顯示的版權字串。將其保留為空字串或刪除此項目可將其從頁面中隱藏。
                    copyrightStr = "版權所有 ®."

                [languages.zh.params.globalFrontmatter]
                    # 本站的作者。將顯示於
                    # 1. 所有頁面的頁尾
                    # 2. 單頁的作者欄位中（可被單頁的前置資料覆寫）
                    # 將其保留為空字串或刪除此項目可將其從頁面中隱藏
                    author = "王靖"

                    # 用於 RSS 和 SEO 的網站描述。主題將為此項目生成 <meta> 標籤
                    description = "這是我的新 Hugo 網站"

                    # 網站關鍵字。主題將為此項目生成 <meta> 標籤
                    keywords = "hugo,網站,新"

                [languages.zh.params.homePage]

                    # 在首頁「開始區塊」中顯示的詳細描述。建議段落長度不超過 100 個字。
                    siteLongDescription = "Hugo 是一個快速且易於使用的靜態網站產生器，用 Go 語言編寫。它可以從目錄中的內容和模板呈現完整的 HTML 網站，利用 Markdown 檔案進行元數據。它針對速度進行了優化，適用於各種類型的網站。"

                    # 如果您不喜歡 "siteLongDescription" 的標題是「開始」（默認值），
                    # 您可以將此項目的值更改為「描述」或您喜歡的其他內容。
                    siteLongDescriptionTitle = "開始"


        # Spracheinstellung für Deutsch
        [languages.de]

            languageCode = 'de-DE'
            languageDirection = 'ltr'
            languageName = 'Deutsch'
            title = 'Projekt Dokumentation'
            weight = 3

            # Konfigurationen, die ursprünglich im Abschnitt "params" waren, aber übersetzt werden müssen.
            [languages.de.params]
                
                [languages.de.params.header]
                    # Website-Titel für den Kopfzeilenbanner.
                    title = "Meine neue Hugo-Website"

                    # Untertitel für diese Seite, nur auf der Startseite verwendet
                    subtitle = 'Eine Website erstellt von Hugo'
                
                [languages.de.params.footer]
                    # Urheberrechtszeichenfolge im Footer angezeigt. Lassen Sie es leer oder entfernen Sie diesen Eintrag, um sie von der Seite auszublenden.
                    copyrightStr = "Alle Rechte vorbehalten ®."

                [languages.de.params.globalFrontmatter]
                    # Der Autor dieser Website. Dies wird angezeigt in 
                    # 1. im Footer auf allen Seiten
                    # 2. dem Autorenfeld auf der Einzelseite. (dies kann durch das Frontmatter der Einzelseite überschrieben werden.)
                    # Lassen Sie es leer oder entfernen Sie diesen Eintrag, um ihn von der Seite auszublenden.
                    author = "Jing Wang"
                    
                    # Website-Beschreibung für RSS und SEO. Das Theme generiert ein <meta>-Tag für diesen Eintrag
                    description = "Das ist meine neue Hugo-Website"

                    # Website-Schlüsselwörter. Das Theme generiert ein <meta>-Tag für diesen Eintrag.
                    keywords = "hugo,website,neu"

                [languages.de.params.homePage]
                    # Lange Beschreibung im "Start Block" auf der Startseite angezeigt. Es wird empfohlen, den Absatz kürzer als 100 Wörter zu halten.        
                    siteLongDescription = "Hugo ist ein schneller und benutzerfreundlicher statischer Website-Generator, der in Go geschrieben ist. Er rendert eine vollständige HTML-Website aus Inhalten und Vorlagen in einem Verzeichnis und verwendet Markdown-Dateien für Metadaten. Er ist optimiert für Geschwindigkeit und für verschiedene Arten von Websites geeignet."

                    # Wenn Ihnen der Titel von "siteLongDescription" nicht gefällt, der standardmäßig "Start" ist, 
                    # können Sie den Wert dieses Elements in "Beschreibung" oder etwas ähnliches ändern, das Ihnen gefällt.
                    siteLongDescriptionTitle = "Start"

    # Theme parameters
    [params]

        # Parameters applied in HTML <head>
        [params.site]
            # Website ICON
            faviconUrl = ""

            # Do you have any CSS in local? List them in an array.
            # They should be placed inside "/assets" dir.
            # And don't named the file as "index.css" and "style.css".
            # These two files are used by the theme.
            localCss = []

            # Do you need to add any external CSS? List them in an array.
            externalCss = []

            # Do you have any script in local? List them in an array.
            # They should be placed inside "/assets" dir.
            # And don't named the file as "index.js"
            # Theis file is used by the theme.
            localJs = []

            # Do you have any external Script need to add on? List them in an array.
            externalJs = []

            # The code you could get from Google Search Console.
            # Please patse the value of content xxx in the following items
            # <meta name="google-site-verification" content="xxxxxxxxxxxxxxxxxxxxxxxxxx" />
            googleVerification = ""

            # The code you could get from Microsoft Bing Webmater
            # Please patse the value of content xxx in the following items
            # <meta name="msvalidate.01" content="xxxxxxxxxxxxxxxxxxxx" />
            bingVerifivation = ""

        # Customized info shown in header of the page
        [params.header]
            # Config about your's site logo, remove this item to hide the logo
            [params.header.logo]
                # Where is your site's URL
                imgUrl = ""

                # If the logo is clickable, where should it be linked?
                # In default, it will linked to the homepage of the site.
                logoLink = ""

        # Customized info shown in footer of the page
        [params.footer]
            # Should show the counter in the footer or not
            # In the home page, it will show the numbers of all pages
            # In the sections pages, it will show the numbers of pages within the section
            # In the taxonomy pages, it will show the numbers of pages belong to the taxonomy.
            # In the regular content pages, it will show the word count.
            counter = true

            # Should show the language of the page or not
            language = true

            # Should show the hugo version or not
            hugoVersion = true

            # Should show the theme info or not
            theme = true

            # Should show the edited time of the page or not
            modifiedTime = true

            # The format of the `modifiedTime`.
            # Refer to page https://gohugo.io/functions/format/ for more detail.
            # Below is the default format, please do not remove it, unless you set `false` in `modifiedTime` field.
            dateFormat = "Jan 02 2006 15:04:05"

            # Should show the current git HEAD hash or not
            # To make this show up correctly, please follow the prerequisites in page
            # https://gohugo.io/variables/git/
            gitHash = true

            # Social link in the footer, listed items are supported, delete unwanted items to hide it.
            [params.footer.socialLink]
                github = ""
                facebook = ""
                twitter = ""
                email = ""
                linkedin = ""
                instagram = ""
                telegram = ""
                medium = ""
                vimeo = ""
                youtube = ""

        # Parameters applied in the homepage only
        [params.homePage]
            # Param to decide whether to show the most recent blog posts or not. (Default: true)
            showRecentPostsBlock = true

            # Param to decide how many recent posts to show in the home page. (Default: 5)
            numOfRecentPosts = 5

            # Parameter to decide whether to show the URL behind the title.
            # It will be more like an editor if it is shown. However, in general, it can be messy if it is displayed.        
            # (Default: true)
            recentPostShowUrl = true
        
        
        # Paramater applied in the single page
        # These values could be overwritten by the frontmatter in the single page.
        [params.page]
            # Should include Table of Content in front of the page or not.
            includeToc = true

            # Should show the author of the page or not.
            # The author name will be shown in the single page if and only if 
            #   1. this items been set as true and
            #   2. "aurthor" filed been provided in the 
            #       A. single page frontmatter or
            #       B. "author" filed in above "globalFrontmatter" block
            showAuthor = true

            # Should show the date of the page or not
            showDate = true

            # The format of the date.
            # Refer to page https://gohugo.io/functions/format/ for more detail.
            # Below is the default format, please do not remove it, unless you set `false` in `showDate` field.
            dateFormat = "2006.01.02"

            # Should show the estimate reading time in front of the page or not.
            showTimeToRead = true

            # Should show the breadcrumb in front of the page or not.
            showBreadcrumb = true

            # Should show the "copy" button in the codeblock or not.
            codeBlockCopible = true
    ```
    </details>
* Also, please [add the corresponding i18n translation table](https://gohugo.io/functions/lang/translate/) according to the language you use, so the theme can translate to the language you use properly. I have placed an example file for English containing all the words required by the theme under the `i18n` folder. You should copy it and translate it to the language you need.

## Run & Build
### Develop
```
hugo server
```
Then, you should be able to see your site at `localhost:1313`. From now on, all changes made locally will be reflected on the site, without the need to refresh your browser each time. Additionally, all files will not be minified or merged in this development mode, making it easier to debug any issues.

### Release
```
hugo
```
This will build your site in release mode, where all `.html`, `.css`, and `.js` files will be minified and merged when possible.

## Feature Plan
* Share to Social Media Button
* Emoji Support
* Better Code Block Highlight
* Mermaid Support
* Tab View Support
* Store custom note in local storage.
* Accessiblity Support
* LaTex Math Support

## Acknowledgement
This theme was originally inspired by the [theme `edidor`](https://github.com/sfengyuan/edidor).

## License
This theme was released under the Apache License 2.0.
