# TryHackMe - Neighbor CTF

In this CTF we are dealing with IDOR. We have to find the flag of the user `admin` which is hidden in the website.

## How to solve this CTF:

```bash
1. Go to the website. Here you will se a login page.
```

![Login page](./neighbor/login.png)

```bash
2. Let's look at the source code of the page. We can gather some valuable information from here.
```

![Source code](./neighbor/source_code.png)

```bash
3. We can use the username:password, `guest:guest` to login. We will be redirected to the home page.
```

```bash
4. In the url we can see that we are dealing with a `id` parameter, i.e. "guest". Let's try to change it to "admin".
```

![Admin](./neighbor/change_url.png)

```bash
5. We are now logged in as admin. We can see the flag in the home page.
```

![Flag](./neighbor/flag.png)

```bash
By using IDOR vulnerability we were able to bypass authentication and get the flag. Hurrah!
```
