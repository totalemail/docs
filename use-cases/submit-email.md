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
