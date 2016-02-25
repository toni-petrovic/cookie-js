# Usage #

Here a very simple example of how you can use this script:

## HTML ##

```

<input id="ctest" type="button" value="Click me" onclick="testCookie();" />

```

## Javascript ##

```

function testCookie() {
  if (Cookie.test()) {
    if (Cookie.get('testCookie')) {
      alert('Cookie was set, now unsetting.');
      Cookie.unset('testCookie');
      $('ctest').value = "Click me";
    }
    else {
      alert('Cookie was not set, now setting test cookie.');
      Cookie.set('testCookie','true');
      $('ctest').value = "Click me again !";
    }
  }
}

```

# Methods #

| `Cookie.get` | Get a cookie's value |
|:-------------|:---------------------|
| `Cookie.set` | Set a cookie         |
| `Cookie.unset` | Unset a cookie       |
| `Cookie.test` | Return true if cookie functionnalities are available |
| `Cookie.dump` | If Firebug JavaScript console is present, it will dump cookie string to console. |
| `Cookie.hoursToExpireDate` | Return GTM date string of "now" + time to live |