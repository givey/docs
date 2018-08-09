---
title: Authentication
order: 2
---

<p>
  The Givey API uses <code>access tokens</code> in order to validate requests.
</p>

<p>
  You can obtain an access token by creating an application at <a href="https://www.givey.com/developers" target="_blank">https://www.givey.com/developers</a>.
</p>

<p>
  Once you have an access token, you can use it in your requests. The preferred method
  of authentication is via the request headers:

<pre class="code" style="display: block">
$ curl https://api.givey.com/v4/charities \
  -H "Authorization: Bearer {access token}"
</pre>
</p>
