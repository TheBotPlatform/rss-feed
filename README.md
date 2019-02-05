# rss-feed

An example rss feed to power a carousel in The Bot Platform

## Title

It is important to make sure your rss feed has a title as this is how you are presented with the RSS feed within the bot platform itself

```xml
<title>Sample RSS Feed</title>
```

## Images

It requires `media:thumbnail` to power the image in the carousel
`media:thumbnail` is part of the yahoo search rss spec, which you can specify as an entity in your rss by using the following:

```xml
<rss version="2.0" xmlns:media="http://search.yahoo.com/mrss/">
```

## Individual items

In your RSS feed you can have any number of items, bots only have a maximum of 10 items though, but the bot platform will handle that for you.

```xml
<item>
    <title>This is the title of the first item</title>
    <description>This is the subtitle in the carousel</description>
    <link>https://thebotplatform.com/news</link>
    <guid isPermaLink="true">https://thebotplatform.com/news</guid>
    <media:thumbnail url="http://placekitten.com/600/200"/>
</item>
```

## Full example

You can access a full example file here: https://raw.githubusercontent.com/TheBotPlatform/rss-feed/master/example.xml

Or below

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<rss version="2.0" xmlns:media="http://search.yahoo.com/mrss/">
    <channel>
        <title>Sample RSS Feed</title>
        <link>https:thebotplatform.com</link>        
        <lastBuildDate>Tue, 05 Feb 2019 11:19:48 GMT</lastBuildDate>
        <item>
            <title>This is the title of the first item</title>
            <description>This is the subtitle in the carousel</description>
            <link>https://thebotplatform.com/news</link>
            <guid isPermaLink="true">https://thebotplatform.com/news/1</guid>
            <media:thumbnail url="http://placekitten.com/600/200"/>
        </item>
        <item>
            <title>This is the title of the second item</title>
            <description>This is the subtitle in the carousel</description>
            <link>https://thebotplatform.com/news</link>
            <guid isPermaLink="true">https://thebotplatform.com/news/2</guid>
            <media:thumbnail url="http://placekitten.com/600/201"/>
        </item>
        <item>
            <title>This is the title of another item</title>
            <description>This is the subtitle in the carousel</description>
            <link>https://thebotplatform.com/news</link>
            <guid isPermaLink="true">https://thebotplatform.com/news/3</guid>
            <media:thumbnail url="http://placekitten.com/600/202"/>
        </item>
    </channel>
</rss>
```
