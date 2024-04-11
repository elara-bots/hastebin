# Selfhosted Hastebin (Cloudflare Worker)

1) Go to your [Cloudflae Workers page](https://dash.cloudflare.com) and sign in. 
2) Click on the `Workers & Pages` tab on the left. 
3) Click on `KV` tab below `Workers & Pages` tab.
4) Click on `Create namespace` on the page, then use the name `HASTES` then press `Add`
5) Go back to `Workers & Pages` tab, then click `Create application`. 
6) Click on `Create worker` and enter the name of what you want the site to be called, then scroll down to `Deploy`
7) Now open both `Configure Worker` and `Edit Code` buttons. 

## For: Configure Worker: 
- Click on `Settings` then `Variables`
- Scroll down to `KV Namespace Bindings`
- Click on `Add Binding`
- Set `Variable name` to `HASTES` and point the `KV Namespace` to the one you just created. 

## For: Edit Code: 
- Copy the [worker.js](https://github.com/elara-bots/hastebin/blob/main/worker.js) file in this repo. 
- Paste it into the editor.
- Change the details you want to in the options object at the top of the file. 
- After you're done with that now press on `Deploy` on the top right and your site should be working! 

------

# Features: 
- Create & View Hastes on the site.
- API support

# API: 
- POST: `https://<website_url>/documents` with `text/plain` header and send the string in the body of the request.
- GET: `https://<website_url>/documents/:id` to get the info 
