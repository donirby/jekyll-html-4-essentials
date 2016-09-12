---
layout: page
title: Links
---

Perhaps the most important aspect of HTML is the ability to link from one document to another. This is the basic concept underlying the web and without this functionality the World Wide Web would not exist. 

### Link syntax
Creating links is relatively straightforward, and the syntax provides a lot of flexibility in where and how links are applied. To create a link, you&rsquo;ll use the anchor element &rang;a&lang; to wrap the content you wish to convert to a link.&nbsp; Attributes inside the anchor tag tell the browser where the page is linking to, or point to an external resource that the browser should download.
Take the following link example:

~~~~~~~
<a href=&rdquo;syntax.htm&rdquo; title=&rdquo;learn more about syntax&rdquo;>HTML syntax</a>
~~~~~~~

Here the text &ldquo;HTML syntax&rdquo; would now appear as a clickable link. The `href` attribute tells the browser how to *resolve* the link; that is where the user should be directed when the link is clicked. The optional `title` attribute provides a description of the link and is helpful in making the link more accessible.

### Link types
There are three basic types of link: `absolute`, `site-root relative`, and `document relative`. Each of these types refers to the value of the `href` attribute, which directs how the browser should resolve a link once the link has been clicked. 

#### Absolute links 
These links contain the entire URL necessary to resolve a link, including the protocol. This is usually done for external links, which are links to pages outside of the current site. Here&rsquo;s an example of an absolute link:

~~~~~~~
<a href=&rdquo;http://www.lynda.com&rdquo; title=&rdquo;You can learn it at lynda.com!&rdquo;>lynda.com</a>
~~~~~~~

#### Document relative links 
These links are commonly used to navigate internally within a site. For example, if you were on the home page of your site, and wanted to navigate to the contact page, you simply provide the path from the home page to the contact page for the `href` value. Doing this requires you to understand the directory structure of your site, and when you need to navigate into, or out of, folders. Take the following example:

~~~~~~~
<a href=&rdquo;contact.htm&rdquo; title=&rdquo;our contact page&rdquo;>Contact us</a>
~~~~~~~

This link assumes that the contact page and the current page are in the same directory. If the contact page were located in a directory below the current page, the link would look like this:

~~~~~~~
<a href=&rdquo;resources/contact.htm&rdquo; title=&rdquo;our contact page&rdquo;>Contact us</a>
~~~~~~~

This assumes the contact page is in a directory titled &ldquo;resources&rdquo; and is one level below the current page. To move `out` of a directory, you precede the page with the &ldquo;../&rdquo; characters. In this case of our contact link it would look like this:

~~~~~~~
<a href=&rdquo;../contact.htm&rdquo; title=&rdquo;our contact page&rdquo;>Contact us</a>
~~~~~~~

This link would move up from the current directory and find the contact.htm page in the parent directory. You can use as many of these &ldquo;../&rdquo; as you need to move up and properly resolve the link.

#### Site-Root Relative Links
These are similar to document relative links, but start at the root folder for the site and then move down through directories to the desired page. Unlike document relative links, which depend on the current location of the page to properly resolve links, site-root relative links are written the same no matter the current location within your site. All links are preceded by a forward slash (/) that refers to the root directory. Here&rsquo;s an example:

~~~~~~~
<a href=&rdquo;/contact.htm&rdquo; title=&rdquo;our contact page&rdquo;>Contact us</a>
~~~~~~~

In this example, the link is resolved by going directly into the site&rsquo;s root folder and finding the contact page. If the contact page were located deeper within the site, the link would look like this:

~~~~~~~
<a href=&rdquo;/resources/contact.htm&rdquo; title=&rdquo;our contact page&rdquo;>Contact us</a>
~~~~~~~

### Fragment identifiers 
Occasionally you&rsquo;ll want a link to refer to a specific location within a page. This can be done using a special kind of link called a fragment identifier. These links point to elements with a specific `ID` attribute. Let&rsquo;s say, for example, you have a long list of <b>FAQs</b> on a page organized by categories and you had a heading at the top of each category. If you assigned each heading an ID attribute, you could use those IDs to create a links that jump to specific categories. For example, you could format the Camping FAQs heading like this:

~~~~~~~
<h2 id=&rdquo;camp&rdquo;>Camping</h2>
~~~~~~~

Elsewhere on the page you could link to this section by creating the following link:
~~~~~~~
<a href=&rdquo;#camp&rdquo;>Learn more about camping</a>
~~~~~~~
Note the hash symbol (#) prior to the ID value. This tells the browser to look for an element with the ID value that follows.You can link to fragment identifiers on external pages as well. Simply append the fragment identifier to the URL and the link will jump to not only to that page, but that specific section as well.

~~~~~~~
<a href=&rdquo;faq.htm#camp&rdquo;>Read our FAQ on camping.</a>
~~~~~~~

June, 2016

