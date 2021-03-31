# Send mail Action
## Usage

```yaml
- name: Send mail
  uses: stopstopstop/mail-action@master
  with:
    server_address: smtp.gmail.com
    server_port: 465
    username: ${{secrets.MAIL_USERNAME}}
    password: ${{secrets.MAIL_PASSWORD}}
    subject: Github Actions job result
    # Read file contents as body:
    body: file://README.md
    to: obiwan@example.com,yoda@example.com
    from: Luke Skywalker # <user@example.com>
    # Optional carbon copy recipients
    cc: test@example.com,test1@example.com
    # Optional blind carbon copy recipients
    bcc: test@example.com,test2@example.com
    # Optional content type (defaults to text/plain):
    content_type: text/html
    # Optional converting Markdown to HTML (set content_type to text/html too):
    convert_markdown: true
    # Optional attachments:
    attachments: attachments.zip,git.diff,./dist/static/main.js
```
