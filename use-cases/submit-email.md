# Submit an Email

To submit an email for analysis, make the following request:

```
POST https://totalemail.io/api/v1/emails/

{
    "full_text": "<EMAIL TEXT HERE>"
}
```

This will return the following JSON data with details about the email you just created:

```
{
    "full_text": "<EMAIL TEXT HERE>",
    "id": abc123...
}
```

Now, you can [get details about the email](get-email-details.html) you just created.

## Redaction

By default, the recipient email address and name will be removed from all emails created via API.

### Adding Additional Redaction Values

If you would like to redact additional values from an email before creating it, you can provide a list of redaction values in a `redaction_values` key in the body of the POST request described above. For example, a full request with additional redaction values would look like:

```
{
    "full_text": "<EMAIL TEXT HERE>",
    "redaction_values": ["foo bar"]
}
```

If this were POSTed to the API, the phrase `foo bar` would be removed from the email.

### Disabling Redaction

If you would not like the recipient email address and name to be redacted, you can include the query parameter `redact=false` in the url of the request.
