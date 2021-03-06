---
layout: document
category: Tags
published: true
title: Comment time
description: The comment_time tag is used to display the time and date the comment was submitted.
tags:
  - Comment tags
---

# Comment time

On this page:

* [Syntax](#syntax)
* [Attributes](#attributes)
* [Examples](#examples)

## Syntax

~~~ html
<txp:comment_time />
~~~

The **comment_time** tag is a *single* tag which is used to display the time and date the comment was submitted. Should be used in Textpattern 'comment' type [Form templates](https://docs.textpattern.io/themes/form-templates-explained).

## Attributes

This tag will accept the following attributes (**case-sensitive**):

`format="format string"`
: Override the default date format set in the [Preferences panel](https://docs.textpattern.io/administration/preferences-panel).
: **Values:** any valid [strftime](https://secure.php.net/strftime) string values, `since`, `iso8601` ([ISO 8601 reference](https://en.wikipedia.org/wiki/ISO_8601)), `w3cdtf` ([W3CDTF reference](https://www.w3.org/TR/NOTE-datetime)), or `rfc822` ([RFC 822 reference](https://www.w3.org/Protocols/rfc822/#z28)).
: **Default:** the 'Date format' set in preferences.

`gmt="boolean"`
: Return either local time (according to the set time zone preferences) or GMT.
: **Values:** `0` (local time) or `1` (GMT).
: **Default:** `0`.

`lang="ISO language code"`
: Format time string suitable for the specified language (locale).
: **Values:** locales adhere to [ISO-639](https://en.wikipedia.org/wiki/ISO_639-2).
: **Default:** unset (time format set in the [Preferences panel](https://docs.textpattern.io/administration/preferences-panel).

## Examples

### Example 1: Comments display form

~~~ html
<txp:comment_message />
<p>
    <txp:comment_name />
    <txp:comment_time />
    <txp:comment_permlink>
        <txp:comment_id />
    </txp:comment_permlink>
</p>
~~~

Other tags used: [comment_id](comment_id), [comment_message](comment_message), [comment_name](comment_name), [comment_permlink](comment_permlink).
