---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: page
---
A long time ago, I wanted to document the little things that come up naturally in life that remind me how wonderful my wife is. Some time ago, I started listing things using Evernote and a utility called Postach.io to publish them.

Since I never really committed to the practice, I never shared it with her. I plan to unveil it at our next anniversary, which is a big one.

I hope she likes it in spite of the very few entries. Hopefully I have the rest of my life to add to them.

---

### The most recent one:
<ul class="latest-post-list">
    {%- for post in site.posts limit:1 -%}
    <li class="list-inline">
    {%- assign date_format = site.minima.date_format | default: "%Y-%m-%d" -%}
        <div class="smaller underline">{{ post.date | date: date_format }}</div>
        <div><a class="hero-link" href="{{ post.url | relative_url }}">{{ post.title | escape }}</a></div>
    </li>
    {%- endfor -%}
</ul>