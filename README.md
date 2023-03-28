# plep.link
Retake on the HTML/JS version of a website that hosts Destiny 2 infographics compilation. 

Built again from scratch using Hugo and custom theme.

Uploaded to S3, delivered to CloudFront (for SSL), and forwarded to https://plep.link using Route53. Uses GitHub Action to automate the deploy process. 

All rights to the images on https://plep.link belong to their original creators. 

- Hugo Boilerplate Theme from retrolog.io [tutorial](https://retrolog.io/blog/creating-a-hugo-theme-from-scratch/)


- How to:
    - Deploying to S3 and cache invalidation should be handled automatically, but S3 objects have to be marked public manually. <-- Need to check if workaround exists 
    - Add an entry in config.toml to add menu item
    - Add a post that matches the newly added menu item
    - Add an entry in resources.toml that matches the key in bracket
    - Add a corresponding image file in the static/webp folder (.gitignored), manually tracked in S3 for obvious reasons 
    
- GH Action notes 
    - configured to automatically build, deploy to S3, and invalidate CF cache on every push
    - AWS key has to be fetched from the IAM console, if deploy fails check credentials first 
