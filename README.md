# geofs-website-content

Repository for all dynamic content shown at geofs homepage.

## How to update content

- TODO

## Troubleshoot

### Website does not update after content was pushed/merged on main successfully

- In github, go to Settings -> Webhooks -> select the webhook -> Deliveries -> select latest delivery (that failed)
- If Status Code is 403, this means that the reverse proxy has most likely blocked the request. 
- We only allow github's IPs to access this endpoint
- Check in nginx.conf if github's IP addresses are still up to date with [api.github.com](https://api.github.com/meta) (tag "hooks")
