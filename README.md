# Receptar Skeleton for Grav ПЕРЕВОД

![Receptar](assets/readme_1.png)

Receptar — это простая, современная, отзывчивая, полностью настраиваемая, стильная тема блога Grav с высоким разрешением от [WebMan Design](http://themedemos.webmandesign.eu/). Он имеет книжный дизайн с разделенным экраном, вдохновленный современной кулинарной книгой, с акцентом на красивые изображения и типографику.

# Функции

* Меню навигации включено
* Книжный дизайн с разделенным экраном
* Складная боковая панель
* Макет блога с поддержкой рецептов
* Красивые изображения и типографика.
* Социальный обмен
* Совместимость с браузером
* Поддерживает YouTube
* Поддерживает СаундКлауд
* Поддерживает видео
* Поддержка простого поиска
* Фиды
* Поддержка плагина RelatedPosts
* Поддержка плагинов архивов
* Поддержка плагина JComments
* Поддержка плагинов комментариев и форм
* Базовые переводы на 14 языков



## Basic Setup for a new Grav site

The simplest way to install Receptar theme for Grav is to download and install the Receptar Skeleton package:

1. [Download Receptar Skeleton](http://getgrav.org/downloads/skeletons#extras)
2. Simply unzip the package into your web root folder.
3. Point your browser at the folder, job done!

**TIP:** Check out the [general Grav installation instructions](http://learn.getgrav.org/basics/installation) for more details on this process.

---

## Existing Grav site

It is possible to install just the theme, but page content will need to reference the [Receptar theme](https://github.com/getgrav/grav-theme-receptar)'s supported templates.  It is strongly advised to at least install the Receptar Skeleton package to see the theme's capabilities in action.

To install  **just** the theme:

```
$ bin/gpm install receptar
```
---

## Configuration

In Receptar, you have few unique features which you can configure easily:

### Translations

Take a look at theme's **language.yaml**. Polish and English versions contains all variables which you can translate to your language.

### Adding recipes to blog page

In item.md page header you have to add something like that:

```yaml
ingredients_title: Ingredients
ingredients:
  - title: Corpus:
    list:
      - Lorem ipsum, 200g
      - Dolor sit amet 20dl
      - 80g sugar
      - 1 yolk
      - Salt
      - Water 0.5l
      - Milk 1l
  - title: Corpus:
    list:
      - Lorem ipsum, 200g
      - Dolor sit amet 20dl
      - 80g sugar
      - 1 yolk
      - Salt
      - Water 0.5l
      - Milk 1l
```

### Adding advanced description

Add code like that to page header:

```yaml
description:
  - option: Dificulty:
    value: simple
  - option: Serving:
    value: 4
  - option: Preparation time:
    value: 1 hour 30 minutes
  - option: What we need:
    value: oven, tart form, jar
```

### Adding video and SoundCloud

You have to add direct iframe url to page header. For example for Vimeo files, it's going to be:

```yaml
vimeo: https://player.vimeo.com/video/63451562?title=0&amp;byline=0&amp;portrait=0
```

### Slideshow

Add or modify this code in site.yaml:

```yaml
slider:
  - image: slide3.jpg
    title: A very delicious blog
    url: "#"
  - image: slide1.jpg
    title: Duis autem
    url: "#"
  - image: slide2.jpg
    title: Pumpkin recipe
    url: "#"
```

Slideshow images must be placed inside user theme **images/slideshow** directory.

### Featured image

To customize featured image, add or modify following variable in site.yaml:

```yaml
global_featured_image: featured.jpg
```

Featured images must be placed inside user theme **images** directory. Featured images is used on empty blog image posts and on posts without image (due to split-screen layout concept).
