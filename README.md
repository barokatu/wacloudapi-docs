#Whatsapp Cloud API Request Messages Documentation

## Request Send Text Message to Whatsapp Cloud API

```
POST https://graph.facebook.com/{{Version}}/{{Phone-Number-ID}}/messages:
```
```
{
    "messaging_product": "whatsapp",    
    "recipient_type": "individual",
    "to": "{{Recipient-Phone-Number}}",
    "type": "text",
    "text": {
        "preview_url": false,
        "body": "text-message-content"
    }
}
```
SUCCESS RESPONSE:
```
{
"messaging_product": "whatsapp",
"contacts": [
    {
        "input": "48XXXXXXXXX",
        "wa_id": "48XXXXXXXXX "
    }
],
"messages": [
    {
        "id": "wamid.gBGGSFcCNEOPAgkO_KJ55r4w_ww"
    }
]
}
```
ERROR RESPONSE:
```
{
  "statuses": [
    {
      "errors": [
        {
          "code": 1026,
          "href": "https://developers.facebook.com/docs/whatsapp/api/errors/",
          "title": "Receiver Incapable"
        }
      ],
      "id": "gBGGFlAwCWFvAgkyHMGKnRu4JeA",
      "message": {
        "recipient_id": "+91xxxxxxxxxx"
      },
      "recipient_id": "91xxxxxxxxxx",
      "status": "failed",
      "timestamp": "1670394125",
      "type": "message"
    }
  ]
}
```
## Request Send Reply to Text Message to Whatsapp Cloud API

```
POST https://graph.facebook.com/{{Version}}/{{Phone-Number-ID}}/messages:
```
```
{
    "messaging_product": "whatsapp",
    "recipient_type": "individual",
    "to": "{{Recipient-Phone-Number}}",
    "context": {
        "message_id": "<MSGID_OF_PREV_MSG>"
    },
    "type": "text",
    "text": {
        "preview_url": false,
        "body": "<TEXT_MSG_CONTENT>"
    }
}
```
SUCCESS RESPONSE:
```
{
    "messaging_product": "whatsapp",
    "contacts": [
        {
            "input": "48XXXXXXXXX",
            "wa_id": "48XXXXXXXXX "
        }
    ],
    "messages": [
        {
            "id": "wamid.gBGGSFcCNEOPAgkO_KJ55r4w_ww"
        }
    ]
}
```
ERROR RESPONSE:
```
{
  "statuses": [
    {
      "errors": [
        {
          "code": 1026,
          "href": "https://developers.facebook.com/docs/whatsapp/api/errors/",
          "title": "Receiver Incapable"
        }
      ],
      "id": "gBGGFlAwCWFvAgkyHMGKnRu4JeA",
      "message": {
        "recipient_id": "+91xxxxxxxxxx"
      },
      "recipient_id": "91xxxxxxxxxx",
      "status": "failed",
      "timestamp": "1670394125",
      "type": "message"
    }
  ]
}
```
## Request Send Text Message with Preview URL to Whatsapp Cloud API

```
POST https://graph.facebook.com/{{Version}}/{{Phone-Number-ID}}/messages:
```
```
{
    "messaging_product": "whatsapp",
    "to": "{{Recipient-Phone-Number}}",
    "text": {
        "preview_url": true,
        "body": "Please visit https://youtu.be/hpltvTEiRrY to inspire your day!"
    }
}
```
SUCCESS RESPONSE:
```
{
  "messaging_product": "whatsapp",
  "contacts": [{
      "input": "15555551234",
      "wa_id": "<WHATSAPP_ID>"
    }],
  "messages": [{
      "id": "wamid.ID"
    }]
}
```
ERROR RESPONSE:
```
{
  "statuses": [
    {
      "errors": [
        {
          "code": 1026,
          "href": "https://developers.facebook.com/docs/whatsapp/api/errors/",
          "title": "Receiver Incapable"
        }
      ],
      "id": "gBGGFlAwCWFvAgkyHMGKnRu4JeA",
      "message": {
        "recipient_id": "+91xxxxxxxxxx"
      },
      "recipient_id": "91xxxxxxxxxx",
      "status": "failed",
      "timestamp": "1670394125",
      "type": "message"
    }
  ]
}
```
## Request Send Reply with Reaction Message to Whatsapp Cloud API

```
POST https://graph.facebook.com/{{Version}}/{{Phone-Number-ID}}/messages:
```
```
{
    "messaging_product": "whatsapp",
    "recipient_type": "individual",
    "to": "{{Recipient-Phone-Number}}",
    "type": "reaction",
    "reaction": {
        "message_id": "<WAM_ID>",
        "emoji": "<EMOJI>"
    }
}
```
SUCCESS RESPONSE:
```
{
    "messaging_product": "whatsapp",
    "contacts": [
        {
            "input": "<PHONE_NUMBER>",
            "wa_id": "<WHATSAPP_ID>"
        }
    ],
    "messages": [
        {
            "id": "wamid.HBgLM..."
        }
    ]
}
```
ERROR RESPONSE:
```
{
  "statuses": [
    {
      "errors": [
        {
          "code": 1026,
          "href": "https://developers.facebook.com/docs/whatsapp/api/errors/",
          "title": "Receiver Incapable"
        }
      ],
      "id": "gBGGFlAwCWFvAgkyHMGKnRu4JeA",
      "message": {
        "recipient_id": "+91xxxxxxxxxx"
      },
      "recipient_id": "91xxxxxxxxxx",
      "status": "failed",
      "timestamp": "1670394125",
      "type": "message"
    }
  ]
}
```
## Request Send Image Message by ID to Whatsapp Cloud API

```
POST https://graph.facebook.com/{{Version}}/{{Phone-Number-ID}}/messages:
```
```
{
    "messaging_product": "whatsapp",
    "recipient_type": "individual",
    "to": "{{Recipient-Phone-Number}}",
    "type": "image",
    "image": {
        "id": "<IMAGE_OBJECT_ID>"
    }
}
```
SUCCESS RESPONSE:
```
{
    "messaging_product": "whatsapp",
    "contacts": [
        {
            "input": "48XXXXXXXXX",
            "wa_id": "48XXXXXXXXX "
        }
    ],
    "messages": [
        {
            "id": "wamid.gBGGSFcCNEOPAgkO_KJ55r4w_ww"
        }
    ]
}
```
ERROR RESPONSE:
```
{
  "statuses": [
    {
      "errors": [
        {
          "code": 1026,
          "href": "https://developers.facebook.com/docs/whatsapp/api/errors/",
          "title": "Receiver Incapable"
        }
      ],
      "id": "gBGGFlAwCWFvAgkyHMGKnRu4JeA",
      "message": {
        "recipient_id": "+91xxxxxxxxxx"
      },
      "recipient_id": "91xxxxxxxxxx",
      "status": "failed",
      "timestamp": "1670394125",
      "type": "message"
    }
  ]
}
```
## Request Send Reply to Image Message by ID to Whatsapp Cloud API
```
POST https://graph.facebook.com/{{Version}}/{{Phone-Number-ID}}/messages:
```
```
{
    "messaging_product": "whatsapp",
    "recipient_type": "individual",
    "to": "{{Recipient-Phone-Number}}",
    "context": {
        "message_id": "<MSGID_OF_PREV_MSG>"
    },
    "type": "image",
    "image": {
        "id": "<IMAGE_OBJECT_ID>"
    }
}
```
SUCCESS RESPONSE:
```
{
    "messaging_product": "whatsapp",
    "contacts": [
        {
            "input": "48XXXXXXXXX",
            "wa_id": "48XXXXXXXXX "
        }
    ],
    "messages": [
        {
            "id": "wamid.gBGGSFcCNEOPAgkO_KJ55r4w_ww"
        }
    ]
}
```
ERROR RESPONSE:
```
{
  "statuses": [
    {
      "errors": [
        {
          "code": 1026,
          "href": "https://developers.facebook.com/docs/whatsapp/api/errors/",
          "title": "Receiver Incapable"
        }
      ],
      "id": "gBGGFlAwCWFvAgkyHMGKnRu4JeA",
      "message": {
        "recipient_id": "+91xxxxxxxxxx"
      },
      "recipient_id": "91xxxxxxxxxx",
      "status": "failed",
      "timestamp": "1670394125",
      "type": "message"
    }
  ]
}
```
## Request Send Image Message by URL to Whatsapp Cloud API
```
POST https://graph.facebook.com/{{Version}}/{{Phone-Number-ID}}/messages:
```
```
{
    "messaging_product": "whatsapp",
    "recipient_type": "individual",
    "to": "{{Recipient-Phone-Number}}",
    "type": "image",
    "image": {
        "link": "http(s)://image-url"
    }
}
```
SUCCESS RESPONSE:
```
{
    "messaging_product": "whatsapp",
    "contacts": [
        {
            "input": "48XXXXXXXXX",
            "wa_id": "48XXXXXXXXX "
        }
    ],
    "messages": [
        {
            "id": "wamid.gBGGSFcCNEOPAgkO_KJ55r4w_ww"
        }
    ]
}
```
ERROR RESPONSE:
```
{
  "statuses": [
    {
      "errors": [
        {
          "code": 1026,
          "href": "https://developers.facebook.com/docs/whatsapp/api/errors/",
          "title": "Receiver Incapable"
        }
      ],
      "id": "gBGGFlAwCWFvAgkyHMGKnRu4JeA",
      "message": {
        "recipient_id": "+91xxxxxxxxxx"
      },
      "recipient_id": "91xxxxxxxxxx",
      "status": "failed",
      "timestamp": "1670394125",
      "type": "message"
    }
  ]
}
```
## Request Send Reply to Image Message by URL to Whatsapp Cloud API
```
POST https://graph.facebook.com/{{Version}}/{{Phone-Number-ID}}/messages:
```
```
{
    "messaging_product": "whatsapp",
    "recipient_type": "individual",
    "to": "{{Recipient-Phone-Number}}",
    "context": {
        "message_id": "<MSGID_OF_PREV_MSG>"
    },
    "type": "image",
    "image": {
        "link": "http(s)://image-url"
    }
}
```
SUCCESS RESPONSE:
```
{
    "messaging_product": "whatsapp",
    "contacts": [
        {
            "input": "48XXXXXXXXX",
            "wa_id": "48XXXXXXXXX "
        }
    ],
    "messages": [
        {
            "id": "wamid.gBGGSFcCNEOPAgkO_KJ55r4w_ww"
        }
    ]
}
```
ERROR RESPONSE:
```
{
  "statuses": [
    {
      "errors": [
        {
          "code": 1026,
          "href": "https://developers.facebook.com/docs/whatsapp/api/errors/",
          "title": "Receiver Incapable"
        }
      ],
      "id": "gBGGFlAwCWFvAgkyHMGKnRu4JeA",
      "message": {
        "recipient_id": "+91xxxxxxxxxx"
      },
      "recipient_id": "91xxxxxxxxxx",
      "status": "failed",
      "timestamp": "1670394125",
      "type": "message"
    }
  ]
}
```
## Request Send Audio Message by ID to Whatsapp Cloud API
```
POST https://graph.facebook.com/{{Version}}/{{Phone-Number-ID}}/messages:
```
```
{
    "messaging_product": "whatsapp",
    "recipient_type": "individual",
    "to": "{{Recipient-Phone-Number}}",
    "type": "audio",
    "audio": {
        "id": "<AUDIO_OBJECT_ID>"
    }
}
```
SUCCESS RESPONSE:
```
{
    "messaging_product": "whatsapp",
    "contacts": [
        {
            "input": "48XXXXXXXXX",
            "wa_id": "48XXXXXXXXX "
        }
    ],
    "messages": [
        {
            "id": "wamid.gBGGSFcCNEOPAgkO_KJ55r4w_ww"
        }
    ]
}
```
ERROR RESPONSE:
```
{
  "statuses": [
    {
      "errors": [
        {
          "code": 1026,
          "href": "https://developers.facebook.com/docs/whatsapp/api/errors/",
          "title": "Receiver Incapable"
        }
      ],
      "id": "gBGGFlAwCWFvAgkyHMGKnRu4JeA",
      "message": {
        "recipient_id": "+91xxxxxxxxxx"
      },
      "recipient_id": "91xxxxxxxxxx",
      "status": "failed",
      "timestamp": "1670394125",
      "type": "message"
    }
  ]
}
```
## Request Send Reply to Audio Message by ID to Whatsapp Cloud API
```
POST https://graph.facebook.com/{{Version}}/{{Phone-Number-ID}}/messages:
```
```
{
    "messaging_product": "whatsapp",
    "recipient_type": "individual",
    "to": "{{Recipient-Phone-Number}}",
    "context": {
        "message_id": "<MSGID_OF_MSG_YOU_ARE_REPLYING_TO>"
    },
    "type": "audio",
    "audio": {
        "id": "<AUDIO_OBJECT_ID>"
    }
}
```
SUCCESS RESPONSE:
```
{
    "messaging_product": "whatsapp",
    "contacts": [
        {
            "input": "48XXXXXXXXX",
            "wa_id": "48XXXXXXXXX "
        }
    ],
    "messages": [
        {
            "id": "wamid.gBGGSFcCNEOPAgkO_KJ55r4w_ww"
        }
    ]
}
```
ERROR RESPONSE:
```
{
  "statuses": [
    {
      "errors": [
        {
          "code": 1026,
          "href": "https://developers.facebook.com/docs/whatsapp/api/errors/",
          "title": "Receiver Incapable"
        }
      ],
      "id": "gBGGFlAwCWFvAgkyHMGKnRu4JeA",
      "message": {
        "recipient_id": "+91xxxxxxxxxx"
      },
      "recipient_id": "91xxxxxxxxxx",
      "status": "failed",
      "timestamp": "1670394125",
      "type": "message"
    }
  ]
}
```
## Request Send Audio Message by URL to Whatsapp Cloud API
```
POST https://graph.facebook.com/{{Version}}/{{Phone-Number-ID}}/messages:
```
```
{
    "messaging_product": "whatsapp",
    "recipient_type": "individual",
    "to": "{{Recipient-Phone-Number}}",
    "type": "audio",
    "audio": {
        "link": "http(s)://audio-url"
    }
}
```
SUCCESS RESPONSE:
```
{
    "messaging_product": "whatsapp",
    "contacts": [
        {
            "input": "48XXXXXXXXX",
            "wa_id": "48XXXXXXXXX "
        }
    ],
    "messages": [
        {
            "id": "wamid.gBGGSFcCNEOPAgkO_KJ55r4w_ww"
        }
    ]
}
```
ERROR RESPONSE:
```
{
  "statuses": [
    {
      "errors": [
        {
          "code": 1026,
          "href": "https://developers.facebook.com/docs/whatsapp/api/errors/",
          "title": "Receiver Incapable"
        }
      ],
      "id": "gBGGFlAwCWFvAgkyHMGKnRu4JeA",
      "message": {
        "recipient_id": "+91xxxxxxxxxx"
      },
      "recipient_id": "91xxxxxxxxxx",
      "status": "failed",
      "timestamp": "1670394125",
      "type": "message"
    }
  ]
}
```
## Request Send Reply to Audio Message by URL to Whatsapp Cloud API
```
POST https://graph.facebook.com/{{Version}}/{{Phone-Number-ID}}/messages:
```
```
{
    "messaging_product": "whatsapp",
    "recipient_type": "individual",
    "to": "{{Recipient-Phone-Number}}",
    "context": {
        "message_id": "<MSGID_OF_MSG_YOU_ARE_REPLYING_TO>"
    },
    "type": "audio",
    "audio": {
        "link": "http(s)://audio-url"
    }
}
```
SUCCESS RESPONSE:
```
{
    "messaging_product": "whatsapp",
    "contacts": [
        {
            "input": "48XXXXXXXXX",
            "wa_id": "48XXXXXXXXX "
        }
    ],
    "messages": [
        {
            "id": "wamid.gBGGSFcCNEOPAgkO_KJ55r4w_ww"
        }
    ]
}
```
ERROR RESPONSE:
```
{
  "statuses": [
    {
      "errors": [
        {
          "code": 1026,
          "href": "https://developers.facebook.com/docs/whatsapp/api/errors/",
          "title": "Receiver Incapable"
        }
      ],
      "id": "gBGGFlAwCWFvAgkyHMGKnRu4JeA",
      "message": {
        "recipient_id": "+91xxxxxxxxxx"
      },
      "recipient_id": "91xxxxxxxxxx",
      "status": "failed",
      "timestamp": "1670394125",
      "type": "message"
    }
  ]
}
```
## Request Send Document Message by ID to Whatsapp Cloud API
```
POST https://graph.facebook.com/{{Version}}/{{Phone-Number-ID}}/messages:
```
```
{
    "messaging_product": "whatsapp",
    "recipient_type": "individual",
    "to": "{{Recipient-Phone-Number}}",
    "type": "document",
    "document": {
        "id": "<DOCUMENT_OBJECT_ID>",
        "caption": "<DOCUMENT_CAPTION_TO_SEND>",
        "filename": "<DOCUMENT_FILENAME>"
    }
}
```
SUCCESS RESPONSE:
```
{
    "messaging_product": "whatsapp",
    "contacts": [
        {
            "input": "48XXXXXXXXX",
            "wa_id": "48XXXXXXXXX "
        }
    ],
    "messages": [
        {
            "id": "wamid.gBGGSFcCNEOPAgkO_KJ55r4w_ww"
        }
    ]
}
```
ERROR RESPONSE:
```
{
  "statuses": [
    {
      "errors": [
        {
          "code": 1026,
          "href": "https://developers.facebook.com/docs/whatsapp/api/errors/",
          "title": "Receiver Incapable"
        }
      ],
      "id": "gBGGFlAwCWFvAgkyHMGKnRu4JeA",
      "message": {
        "recipient_id": "+91xxxxxxxxxx"
      },
      "recipient_id": "91xxxxxxxxxx",
      "status": "failed",
      "timestamp": "1670394125",
      "type": "message"
    }
  ]
}
```
## Request Send Reply to Document Message by ID to Whatsapp Cloud API
```
POST https://graph.facebook.com/{{Version}}/{{Phone-Number-ID}}/messages:
```
```
{
    "messaging_product": "whatsapp",
    "recipient_type": "individual",
    "to": "{{Recipient-Phone-Number}}",
    "context": {
        "message_id": "<MSGID_OF_MSG_YOU_ARE_REPLYING_TO>"
    },
    "type": "document",
    "document": {
        "id": "<DOCUMENT_OBJECT_ID>",
        "caption": "<DOCUMENT_CAPTION_TO_SEND>",
        "filename": "<DOCUMENT_FILENAME>"
    }
}
```
SUCCESS RESPONSE:
```
{
    "messaging_product": "whatsapp",
    "contacts": [
        {
            "input": "48XXXXXXXXX",
            "wa_id": "48XXXXXXXXX "
        }
    ],
    "messages": [
        {
            "id": "wamid.gBGGSFcCNEOPAgkO_KJ55r4w_ww"
        }
    ]
}
```
ERROR RESPONSE:
```
{
  "statuses": [
    {
      "errors": [
        {
          "code": 1026,
          "href": "https://developers.facebook.com/docs/whatsapp/api/errors/",
          "title": "Receiver Incapable"
        }
      ],
      "id": "gBGGFlAwCWFvAgkyHMGKnRu4JeA",
      "message": {
        "recipient_id": "+91xxxxxxxxxx"
      },
      "recipient_id": "91xxxxxxxxxx",
      "status": "failed",
      "timestamp": "1670394125",
      "type": "message"
    }
  ]
}
```
## Request Send Document Message by URL to Whatsapp Cloud API
```
POST https://graph.facebook.com/{{Version}}/{{Phone-Number-ID}}/messages:
```
```
{
    "messaging_product": "whatsapp",
    "recipient_type": "individual",
    "to": "{{Recipient-Phone-Number}}",
    "type": "document",
    "document": {
        "link": "<http(s)://document-url>",
        "caption": "<DOCUMENT_CAPTION_TEXT>"
    }
}
```
SUCCESS RESPONSE:
```
{
    "messaging_product": "whatsapp",
    "contacts": [
        {
            "input": "48XXXXXXXXX",
            "wa_id": "48XXXXXXXXX "
        }
    ],
    "messages": [
        {
            "id": "wamid.gBGGSFcCNEOPAgkO_KJ55r4w_ww"
        }
    ]
}
```
ERROR RESPONSE:
```
{
  "statuses": [
    {
      "errors": [
        {
          "code": 1026,
          "href": "https://developers.facebook.com/docs/whatsapp/api/errors/",
          "title": "Receiver Incapable"
        }
      ],
      "id": "gBGGFlAwCWFvAgkyHMGKnRu4JeA",
      "message": {
        "recipient_id": "+91xxxxxxxxxx"
      },
      "recipient_id": "91xxxxxxxxxx",
      "status": "failed",
      "timestamp": "1670394125",
      "type": "message"
    }
  ]
}
```
## Request Send Reply to Document Message by URL to Whatsapp Cloud API
```
POST https://graph.facebook.com/{{Version}}/{{Phone-Number-ID}}/messages:
```
```
{
    "messaging_product": "whatsapp",
    "recipient_type": "individual",
    "to": "{{Recipient-Phone-Number}}",
    "context": {
        "message_id": "<MSGID_OF_MSG_YOU_ARE_REPLYING_TO>"
    },
    "type": "document",
    "document": {
        "link": "<http(s)://document-url>",
        "caption": "<DOCUMENT_CAPTION_TEXT>"
    }
}
```
SUCCESS RESPONSE:
```
{
    "messaging_product": "whatsapp",
    "contacts": [
        {
            "input": "48XXXXXXXXX",
            "wa_id": "48XXXXXXXXX "
        }
    ],
    "messages": [
        {
            "id": "wamid.gBGGSFcCNEOPAgkO_KJ55r4w_ww"
        }
    ]
}
```
ERROR RESPONSE:
```
{
  "statuses": [
    {
      "errors": [
        {
          "code": 1026,
          "href": "https://developers.facebook.com/docs/whatsapp/api/errors/",
          "title": "Receiver Incapable"
        }
      ],
      "id": "gBGGFlAwCWFvAgkyHMGKnRu4JeA",
      "message": {
        "recipient_id": "+91xxxxxxxxxx"
      },
      "recipient_id": "91xxxxxxxxxx",
      "status": "failed",
      "timestamp": "1670394125",
      "type": "message"
    }
  ]
}
```
## Request Send Sticker Message by ID to Whatsapp Cloud API
```
POST https://graph.facebook.com/{{Version}}/{{Phone-Number-ID}}/messages:
```
```
{
    "messaging_product": "whatsapp",
    "recipient_type": "individual",
    "to": "{{Recipient-Phone-Number}}",
    "type": "sticker",
    "sticker": {
        "id": "<MEDIA_OBJECT_ID>"
    }
}
```
SUCCESS RESPONSE:
```
{
    "messaging_product": "whatsapp",
    "contacts": [
        {
            "input": "48XXXXXXXXX",
            "wa_id": "48XXXXXXXXX "
        }
    ],
    "messages": [
        {
            "id": "wamid.gBGGSFcCNEOPAgkO_KJ55r4w_ww"
        }
    ]
}
```
ERROR RESPONSE:
```
{
  "statuses": [
    {
      "errors": [
        {
          "code": 1026,
          "href": "https://developers.facebook.com/docs/whatsapp/api/errors/",
          "title": "Receiver Incapable"
        }
      ],
      "id": "gBGGFlAwCWFvAgkyHMGKnRu4JeA",
      "message": {
        "recipient_id": "+91xxxxxxxxxx"
      },
      "recipient_id": "91xxxxxxxxxx",
      "status": "failed",
      "timestamp": "1670394125",
      "type": "message"
    }
  ]
}
```
## Request Send Reply to Sticker Message by ID to Whatsapp Cloud API
```
POST https://graph.facebook.com/{{Version}}/{{Phone-Number-ID}}/messages:
```
```
{
    "messaging_product": "whatsapp",
    "recipient_type": "individual",
    "to": "{{Recipient-Phone-Number}}",
    "context": {
        "message_id": "<MSGID_OF_MSG_YOU_ARE_REPLYING_TO>"
    },
    "type": "sticker",
    "sticker": {
        "id": "<MEDIA_OBJECT_ID>"
    }
}
```
SUCCESS RESPONSE:
```
{
    "messaging_product": "whatsapp",
    "contacts": [
        {
            "input": "48XXXXXXXXX",
            "wa_id": "48XXXXXXXXX "
        }
    ],
    "messages": [
        {
            "id": "wamid.gBGGSFcCNEOPAgkO_KJ55r4w_ww"
        }
    ]
}
```
ERROR RESPONSE:
```
{
  "statuses": [
    {
      "errors": [
        {
          "code": 1026,
          "href": "https://developers.facebook.com/docs/whatsapp/api/errors/",
          "title": "Receiver Incapable"
        }
      ],
      "id": "gBGGFlAwCWFvAgkyHMGKnRu4JeA",
      "message": {
        "recipient_id": "+91xxxxxxxxxx"
      },
      "recipient_id": "91xxxxxxxxxx",
      "status": "failed",
      "timestamp": "1670394125",
      "type": "message"
    }
  ]
}
```
## Request Send Sticker Message by URL to Whatsapp Cloud API
```
POST https://graph.facebook.com/{{Version}}/{{Phone-Number-ID}}/messages:
```
```
{
    "messaging_product": "whatsapp",
    "recipient_type": "individual",
    "to": "{{Recipient-Phone-Number}}",
    "type": "sticker",
    "sticker": {
        "link": "<http(s)://sticker-url>"
    }
}
```
SUCCESS RESPONSE:
```
{
    "messaging_product": "whatsapp",
    "contacts": [
        {
            "input": "48XXXXXXXXX",
            "wa_id": "48XXXXXXXXX "
        }
    ],
    "messages": [
        {
            "id": "wamid.gBGGSFcCNEOPAgkO_KJ55r4w_ww"
        }
    ]
}
```
ERROR RESPONSE:
```
{
  "statuses": [
    {
      "errors": [
        {
          "code": 1026,
          "href": "https://developers.facebook.com/docs/whatsapp/api/errors/",
          "title": "Receiver Incapable"
        }
      ],
      "id": "gBGGFlAwCWFvAgkyHMGKnRu4JeA",
      "message": {
        "recipient_id": "+91xxxxxxxxxx"
      },
      "recipient_id": "91xxxxxxxxxx",
      "status": "failed",
      "timestamp": "1670394125",
      "type": "message"
    }
  ]
}
```
## Request Send Reply to Sticker Message by URL to Whatsapp Cloud API
```
POST https://graph.facebook.com/{{Version}}/{{Phone-Number-ID}}/messages:
```
```
{
    "messaging_product": "whatsapp",
    "recipient_type": "individual",
    "to": "{{Recipient-Phone-Number}}",
    "context": {
        "message_id": "<MSGID_OF_MSG_YOU_ARE_REPLYING_TO>"
    },
    "type": "sticker",
    "sticker": {
        "link": "<http(s)://sticker-url>"
    }
}
```
SUCCESS RESPONSE:
```
{
    "messaging_product": "whatsapp",
    "contacts": [
        {
            "input": "48XXXXXXXXX",
            "wa_id": "48XXXXXXXXX "
        }
    ],
    "messages": [
        {
            "id": "wamid.gBGGSFcCNEOPAgkO_KJ55r4w_ww"
        }
    ]
}
```
ERROR RESPONSE:
```
{
  "statuses": [
    {
      "errors": [
        {
          "code": 1026,
          "href": "https://developers.facebook.com/docs/whatsapp/api/errors/",
          "title": "Receiver Incapable"
        }
      ],
      "id": "gBGGFlAwCWFvAgkyHMGKnRu4JeA",
      "message": {
        "recipient_id": "+91xxxxxxxxxx"
      },
      "recipient_id": "91xxxxxxxxxx",
      "status": "failed",
      "timestamp": "1670394125",
      "type": "message"
    }
  ]
}
```
## Request Send Video Message by ID to Whatsapp Cloud API
```
POST https://graph.facebook.com/{{Version}}/{{Phone-Number-ID}}/messages:
```
```
{
    "messaging_product": "whatsapp",
    "recipient_type": "individual",
    "to": "{{Recipient-Phone-Number}}",
    "type": "video",
    "video": {
        "caption": "<VIDEO_CAPTION_TEXT>",
        "id": "<VIDEO_OBJECT_ID>"
    }
}
```
SUCCESS RESPONSE:
```
{
    "messaging_product": "whatsapp",
    "contacts": [
        {
            "input": "48XXXXXXXXX",
            "wa_id": "48XXXXXXXXX "
        }
    ],
    "messages": [
        {
            "id": "wamid.gBGGSFcCNEOPAgkO_KJ55r4w_ww"
        }
    ]
}
```
ERROR RESPONSE:
```
{
  "statuses": [
    {
      "errors": [
        {
          "code": 1026,
          "href": "https://developers.facebook.com/docs/whatsapp/api/errors/",
          "title": "Receiver Incapable"
        }
      ],
      "id": "gBGGFlAwCWFvAgkyHMGKnRu4JeA",
      "message": {
        "recipient_id": "+91xxxxxxxxxx"
      },
      "recipient_id": "91xxxxxxxxxx",
      "status": "failed",
      "timestamp": "1670394125",
      "type": "message"
    }
  ]
}
```
## Request Send Reply to Video Message by ID to Whatsapp Cloud API
```
POST https://graph.facebook.com/{{Version}}/{{Phone-Number-ID}}/messages:
```
```
{
    "messaging_product": "whatsapp",
    "recipient_type": "individual",
    "to": "{{Recipient-Phone-Number}}",
    "context": {
        "message_id": "<MSGID_OF_MSG_YOU_ARE_REPLYING_TO>"
    },
    "type": "video",
    "video": {
        "caption": "<VIDEO_CAPTION_TEXT>",
        "id": "<VIDEO_OBJECT_ID>"
    }
}
```
SUCCESS RESPONSE:
```
{
    "messaging_product": "whatsapp",
    "contacts": [
        {
            "input": "48XXXXXXXXX",
            "wa_id": "48XXXXXXXXX "
        }
    ],
    "messages": [
        {
            "id": "wamid.gBGGSFcCNEOPAgkO_KJ55r4w_ww"
        }
    ]
}
```
ERROR RESPONSE:
```
{
  "statuses": [
    {
      "errors": [
        {
          "code": 1026,
          "href": "https://developers.facebook.com/docs/whatsapp/api/errors/",
          "title": "Receiver Incapable"
        }
      ],
      "id": "gBGGFlAwCWFvAgkyHMGKnRu4JeA",
      "message": {
        "recipient_id": "+91xxxxxxxxxx"
      },
      "recipient_id": "91xxxxxxxxxx",
      "status": "failed",
      "timestamp": "1670394125",
      "type": "message"
    }
  ]
}
```


## Request Send Video Message by URL to Whatsapp Cloud API
```
POST https://graph.facebook.com/{{Version}}/{{Phone-Number-ID}}/messages:
```
```
{
    "messaging_product": "whatsapp",
    "recipient_type": "individual",
    "to": "{{Recipient-Phone-Number}}",
    "type": "video",
    "video": {
        "link": "<http(s)://video-url>",
        "caption": "<VIDEO_CAPTION_TEXT>"
    }
}
```
SUCCESS RESPONSE:
```
{
    "messaging_product": "whatsapp",
    "contacts": [
        {
            "input": "48XXXXXXXXX",
            "wa_id": "48XXXXXXXXX "
        }
    ],
    "messages": [
        {
            "id": "wamid.gBGGSFcCNEOPAgkO_KJ55r4w_ww"
        }
    ]
}
```
ERROR RESPONSE:
```
{
  "statuses": [
    {
      "errors": [
        {
          "code": 1026,
          "href": "https://developers.facebook.com/docs/whatsapp/api/errors/",
          "title": "Receiver Incapable"
        }
      ],
      "id": "gBGGFlAwCWFvAgkyHMGKnRu4JeA",
      "message": {
        "recipient_id": "+91xxxxxxxxxx"
      },
      "recipient_id": "91xxxxxxxxxx",
      "status": "failed",
      "timestamp": "1670394125",
      "type": "message"
    }
  ]
}
```
## Request Send Reply to Video Message by URL to Whatsapp Cloud API
```
POST https://graph.facebook.com/{{Version}}/{{Phone-Number-ID}}/messages:
```
```
{
    "messaging_product": "whatsapp",
    "recipient_type": "individual",
    "to": "{{Recipient-Phone-Number}}",
    "context": {
        "message_id": "<MSGID_OF_MSG_YOU_ARE_REPLYING_TO>"
    },
    "type": "video",
    "video": {
        "link": "<http(s)://video-url>",
        "caption": "<VIDEO_CAPTION_TEXT>"
    }
}
```
SUCCESS RESPONSE:
```
{
    "messaging_product": "whatsapp",
    "contacts": [
        {
            "input": "48XXXXXXXXX",
            "wa_id": "48XXXXXXXXX "
        }
    ],
    "messages": [
        {
            "id": "wamid.gBGGSFcCNEOPAgkO_KJ55r4w_ww"
        }
    ]
}
```
ERROR RESPONSE:
```
{
  "statuses": [
    {
      "errors": [
        {
          "code": 1026,
          "href": "https://developers.facebook.com/docs/whatsapp/api/errors/",
          "title": "Receiver Incapable"
        }
      ],
      "id": "gBGGFlAwCWFvAgkyHMGKnRu4JeA",
      "message": {
        "recipient_id": "+91xxxxxxxxxx"
      },
      "recipient_id": "91xxxxxxxxxx",
      "status": "failed",
      "timestamp": "1670394125",
      "type": "message"
    }
  ]
}
```
## Request Send Contact Message to Whatsapp Cloud API
```
POST https://graph.facebook.com/{{Version}}/{{Phone-Number-ID}}/messages:
```
```
{
    "messaging_product": "whatsapp",
    "to": "{{Recipient-Phone-Number}}",
    "type": "contacts",
    "contacts": [
        {
            "addresses": [
                {
                    "street": "<ADDRESS_STREET>",
                    "city": "<ADDRESS_CITY>",
                    "state": "<ADDRESS_STATE>",
                    "zip": "<ADDRESS_ZIP>",
                    "country": "<ADDRESS_COUNTRY>",
                    "country_code": "<ADDRESS_COUNTRY_CODE>",
                    "type": "<HOME|WORK>"
                }
            ],
            "birthday": "<CONTACT_BIRTHDAY>",
            "emails": [
                {
                    "email": "<CONTACT_EMAIL>",
                    "type": "<WORK|HOME>"
                }
            ],
            "name": {
                "formatted_name": "<CONTACT_FORMATTED_NAME>",
                "first_name": "<CONTACT_FIRST_NAME>",
                "last_name": "<CONTACT_LAST_NAME>",
                "middle_name": "<CONTACT_MIDDLE_NAME>",
                "suffix": "<CONTACT_SUFFIX>",
                "prefix": "<CONTACT_PREFIX>"
            },
            "org": {
                "company": "<CONTACT_ORG_COMPANY>",
                "department": "<CONTACT_ORG_DEPARTMENT>",
                "title": "<CONTACT_ORG_TITLE>"
            },
            "phones": [
                {
                    "phone": "<CONTACT_PHONE>",
                    "wa_id": "<CONTACT_WA_ID>",
                    "type": "<HOME|WORK>"
                }
            ],
            "urls": [
                {
                    "url": "<CONTACT_URL>",
                    "type": "<HOME|WORK>"
                }
            ]
        }
    ]
}
```
SUCCESS RESPONSE:
```
{
    "messaging_product": "whatsapp",
    "contacts": [
        {
            "input": "48XXXXXXXXX",
            "wa_id": "48XXXXXXXXX "
        }
    ],
    "messages": [
        {
            "id": "wamid.gBGGSFcCNEOPAgkO_KJ55r4w_ww"
        }
    ]
}
```
ERROR RESPONSE:
```
{
  "statuses": [
    {
      "errors": [
        {
          "code": 1026,
          "href": "https://developers.facebook.com/docs/whatsapp/api/errors/",
          "title": "Receiver Incapable"
        }
      ],
      "id": "gBGGFlAwCWFvAgkyHMGKnRu4JeA",
      "message": {
        "recipient_id": "+91xxxxxxxxxx"
      },
      "recipient_id": "91xxxxxxxxxx",
      "status": "failed",
      "timestamp": "1670394125",
      "type": "message"
    }
  ]
}
```
## Request Send Reply to Contact Message to Whatsapp Cloud API
```
POST https://graph.facebook.com/{{Version}}/{{Phone-Number-ID}}/messages:
```
```
{
    "messaging_product": "whatsapp",
    "to": "{{Recipient-Phone-Number}}",
    "context": {
        "message_id": "<MSGID_OF_PREV_MSG>"
    },
    "type": "contacts",
    "contacts": [
        {
            "addresses": [
                {
                    "street": "<ADDRESS_STREET>",
                    "city": "<ADDRESS_CITY>",
                    "state": "<ADDRESS_STATE>",
                    "zip": "<ADDRESS_ZIP>",
                    "country": "<ADDRESS_COUNTRY>",
                    "country_code": "<ADDRESS_COUNTRY_CODE>",
                    "type": "<HOME|WORK>"
                }
            ],
            "birthday": "<CONTACT_BIRTHDAY>",
            "emails": [
                {
                    "email": "<CONTACT_EMAIL>",
                    "type": "<WORK|HOME>"
                }
            ],
            "name": {
                "formatted_name": "<CONTACT_FORMATTED_NAME>",
                "first_name": "<CONTACT_FIRST_NAME>",
                "last_name": "<CONTACT_LAST_NAME>",
                "middle_name": "<CONTACT_MIDDLE_NAME>",
                "suffix": "<CONTACT_SUFFIX>",
                "prefix": "<CONTACT_PREFIX>"
            },
            "org": {
                "company": "<CONTACT_ORG_COMPANY>",
                "department": "<CONTACT_ORG_DEPARTMENT>",
                "title": "<CONTACT_ORG_TITLE>"
            },
            "phones": [
                {
                    "phone": "<CONTACT_PHONE>",
                    "wa_id": "<CONTACT_WA_ID>",
                    "type": "<HOME|WORK>"
                }
            ],
            "urls": [
                {
                    "url": "<CONTACT_URL>",
                    "type": "<HOME|WORK>"
                }
            ]
        }
    ]
}
```
SUCCESS RESPONSE:
```
{
    "messaging_product": "whatsapp",
    "contacts": [
        {
            "input": "48XXXXXXXXX",
            "wa_id": "48XXXXXXXXX "
        }
    ],
    "messages": [
        {
            "id": "wamid.gBGGSFcCNEOPAgkO_KJ55r4w_ww"
        }
    ]
}
```
ERROR RESPONSE:
```
{
  "statuses": [
    {
      "errors": [
        {
          "code": 1026,
          "href": "https://developers.facebook.com/docs/whatsapp/api/errors/",
          "title": "Receiver Incapable"
        }
      ],
      "id": "gBGGFlAwCWFvAgkyHMGKnRu4JeA",
      "message": {
        "recipient_id": "+91xxxxxxxxxx"
      },
      "recipient_id": "91xxxxxxxxxx",
      "status": "failed",
      "timestamp": "1670394125",
      "type": "message"
    }
  ]
}
```
## Request Send Location Message to Whatsapp Cloud API
```
POST https://graph.facebook.com/{{Version}}/{{Phone-Number-ID}}/messages:
```
```
{
    "messaging_product": "whatsapp",
    "recipient_type": "individual",
    "to": "{{Recipient-Phone-Number}}",
    "type": "location",
    "location": {
        "latitude": "<LOCATION_LATITUDE>",
        "longitude": "<LOCATION_LONGITUDE>",
        "name": "<LOCATION_NAME>",
        "address": "<LOCATION_ADDRESS>"
    }
}
```
SUCCESS RESPONSE:
```
{
    "messaging_product": "whatsapp",
    "contacts": [
        {
            "input": "48XXXXXXXXX",
            "wa_id": "48XXXXXXXXX "
        }
    ],
    "messages": [
        {
            "id": "wamid.gBGGSFcCNEOPAgkO_KJ55r4w_ww"
        }
    ]
}
```
ERROR RESPONSE:
```
{
  "statuses": [
    {
      "errors": [
        {
          "code": 1026,
          "href": "https://developers.facebook.com/docs/whatsapp/api/errors/",
          "title": "Receiver Incapable"
        }
      ],
      "id": "gBGGFlAwCWFvAgkyHMGKnRu4JeA",
      "message": {
        "recipient_id": "+91xxxxxxxxxx"
      },
      "recipient_id": "91xxxxxxxxxx",
      "status": "failed",
      "timestamp": "1670394125",
      "type": "message"
    }
  ]
}
```
## Request Send Reply to Location Message to Whatsapp Cloud API
```
POST https://graph.facebook.com/{{Version}}/{{Phone-Number-ID}}/messages:
```
```
{
    "messaging_product": "whatsapp",
    "recipient_type": "individual",
    "to": "{{Recipient-Phone-Number}}",
    "context": {
        "message_id": "<MSGID_OF_PREV_MSG>"
    },
    "type": "location",
    "location": {
        "latitude": "<LOCATION_LATITUDE>",
        "longitude": "<LOCATION_LONGITUDE>",
        "name": "<LOCATION_NAME>",
        "address": "<LOCATION_ADDRESS>"
    }
}
```
SUCCESS RESPONSE:
```
{
    "messaging_product": "whatsapp",
    "contacts": [
        {
            "input": "48XXXXXXXXX",
            "wa_id": "48XXXXXXXXX "
        }
    ],
    "messages": [
        {
            "id": "wamid.gBGGSFcCNEOPAgkO_KJ55r4w_ww"
        }
    ]
}
```
ERROR RESPONSE:
```
{
  "statuses": [
    {
      "errors": [
        {
          "code": 1026,
          "href": "https://developers.facebook.com/docs/whatsapp/api/errors/",
          "title": "Receiver Incapable"
        }
      ],
      "id": "gBGGFlAwCWFvAgkyHMGKnRu4JeA",
      "message": {
        "recipient_id": "+91xxxxxxxxxx"
      },
      "recipient_id": "91xxxxxxxxxx",
      "status": "failed",
      "timestamp": "1670394125",
      "type": "message"
    }
  ]
}
```
## Request Send Message Template Text to Whatsapp Cloud API
```
POST https://graph.facebook.com/{{Version}}/{{Phone-Number-ID}}/messages:
```
```
{
    "messaging_product": "whatsapp",
    "recipient_type": "individual",
    "to": "{{Recipient-Phone-Number}}",
    "type": "template",
    "template": {
        "name": "template-name",
        "language": {
            "code": "language-and-locale-code"
        },
        "components": [
            {
                "type": "body",
                "parameters": [
                    {
                        "type": "text",
                        "text": "text-string"
                    },
                    {
                        "type": "currency",
                        "currency": {
                            "fallback_value": "$100.99",
                            "code": "USD",
                            "amount_1000": 100990
                        }
                    },
                    {
                        "type": "date_time",
                        "date_time": {
                            "fallback_value": "February 25, 1977",
                            "day_of_week": 5,
                            "year": 1977,
                            "month": 2,
                            "day_of_month": 25,
                            "hour": 15,
                            "minute": 33,
                            "calendar": "GREGORIAN"
                        }
                    }
                ]
            }
        ]
    }
}
```
SUCCESS RESPONSE:
```
{
    "messaging_product": "whatsapp",
    "contacts": [
        {
            "input": "48XXXXXXXXX",
            "wa_id": "48XXXXXXXXX "
        }
    ],
    "messages": [
        {
            "id": "wamid.gBGGSFcCNEOPAgkO_KJ55r4w_ww"
        }
    ]
}
```
ERROR RESPONSE:
```
{
  "statuses": [
    {
      "errors": [
        {
          "code": 1026,
          "href": "https://developers.facebook.com/docs/whatsapp/api/errors/",
          "title": "Receiver Incapable"
        }
      ],
      "id": "gBGGFlAwCWFvAgkyHMGKnRu4JeA",
      "message": {
        "recipient_id": "+91xxxxxxxxxx"
      },
      "recipient_id": "91xxxxxxxxxx",
      "status": "failed",
      "timestamp": "1670394125",
      "type": "message"
    }
  ]
}
```
## Request Send Message Template Media to Whatsapp Cloud API
```
POST https://graph.facebook.com/{{Version}}/{{Phone-Number-ID}}/messages:
```
```
{
    "messaging_product": "whatsapp",
    "recipient_type": "individual",
    "to": "{{Recipient-Phone-Number}}",
    "type": "template",
    "template": {
        "name": "template-name",
        "language": {
            "code": "language-and-locale-code"
        },
        "components": [
            {
                "type": "header",
                "parameters": [
                    {
                        "type": "image",
                        "image": {
                            "link": "http(s)://the-image-url"
                        }
                    }
                ]
            },
            {
                "type": "body",
                "parameters": [
                    {
                        "type": "text",
                        "text": "text-string"
                    },
                    {
                        "type": "currency",
                        "currency": {
                            "fallback_value": "$100.99",
                            "code": "USD",
                            "amount_1000": 100990
                        }
                    },
                    {
                        "type": "date_time",
                        "date_time": {
                            "fallback_value": "February 25, 1977",
                            "day_of_week": 5,
                            "year": 1977,
                            "month": 2,
                            "day_of_month": 25,
                            "hour": 15,
                            "minute": 33,
                            "calendar": "GREGORIAN"
                        }
                    }
                ]
            }
        ]
    }
}
```
SUCCESS RESPONSE:
```
{
    "messaging_product": "whatsapp",
    "contacts": [
        {
            "input": "48XXXXXXXXX",
            "wa_id": "48XXXXXXXXX "
        }
    ],
    "messages": [
        {
            "id": "wamid.gBGGSFcCNEOPAgkO_KJ55r4w_ww"
        }
    ]
}
```
ERROR RESPONSE:
```
{
  "statuses": [
    {
      "errors": [
        {
          "code": 1026,
          "href": "https://developers.facebook.com/docs/whatsapp/api/errors/",
          "title": "Receiver Incapable"
        }
      ],
      "id": "gBGGFlAwCWFvAgkyHMGKnRu4JeA",
      "message": {
        "recipient_id": "+91xxxxxxxxxx"
      },
      "recipient_id": "91xxxxxxxxxx",
      "status": "failed",
      "timestamp": "1670394125",
      "type": "message"
    }
  ]
}
```
## Request Send Message Template Interactive to Whatsapp Cloud API
```
POST https://graph.facebook.com/{{Version}}/{{Phone-Number-ID}}/messages:
```
```
{
    "messaging_product": "whatsapp",
    "recipient_type": "individual",
    "to": "{{Recipient-Phone-Number}}",
    "type": "template",
    "template": {
        "name": "template-name",
        "language": {
            "code": "language-and-locale-code"
        },
        "components": [
            {
                "type": "header",
                "parameters": [
                    {
                        "type": "image",
                        "image": {
                            "link": "http(s)://the-image-url"
                        }
                    }
                ]
            },
            {
                "type": "body",
                "parameters": [
                    {
                        "type": "text",
                        "text": "text-string"
                    },
                    {
                        "type": "currency",
                        "currency": {
                            "fallback_value": "$100.99",
                            "code": "USD",
                            "amount_1000": 100990
                        }
                    },
                    {
                        "type": "date_time",
                        "date_time": {
                            "fallback_value": "February 25, 1977",
                            "day_of_week": 5,
                            "year": 1977,
                            "month": 2,
                            "day_of_month": 25,
                            "hour": 15,
                            "minute": 33,
                            "calendar": "GREGORIAN"
                        }
                    }
                ]
            },
            {
                "type": "button",
                "sub_type": "quick_reply",
                "index": "0",
                "parameters": [
                    {
                        "type": "payload",
                        "payload": "aGlzIHRoaXMgaXMgY29v"
                    }
                ]
            },
            {
                "type": "button",
                "sub_type": "quick_reply",
                "index": "1",
                "parameters": [
                    {
                        "type": "payload",
                        "payload": "9rwnB8RbYmPF5t2Mn09x4h"
                    }
                ]
            }
        ]
    }
}
```
SUCCESS RESPONSE:
```
{
    "messaging_product": "whatsapp",
    "contacts": [
        {
            "input": "48XXXXXXXXX",
            "wa_id": "48XXXXXXXXX "
        }
    ],
    "messages": [
        {
            "id": "wamid.gBGGSFcCNEOPAgkO_KJ55r4w_ww"
        }
    ]
}
```
ERROR RESPONSE:
```
{
  "statuses": [
    {
      "errors": [
        {
          "code": 1026,
          "href": "https://developers.facebook.com/docs/whatsapp/api/errors/",
          "title": "Receiver Incapable"
        }
      ],
      "id": "gBGGFlAwCWFvAgkyHMGKnRu4JeA",
      "message": {
        "recipient_id": "+91xxxxxxxxxx"
      },
      "recipient_id": "91xxxxxxxxxx",
      "status": "failed",
      "timestamp": "1670394125",
      "type": "message"
    }
  ]
}
```
## Request Send List Message to Whatsapp Cloud API
```
POST https://graph.facebook.com/{{Version}}/{{Phone-Number-ID}}/messages:
```
```
{
    "messaging_product": "whatsapp",
    "recipient_type": "individual",
    "to": "{{Recipient-Phone-Number}}",
    "type": "interactive",
    "interactive": {
        "type": "list",
        "header": {
            "type": "text",
            "text": "<HEADER_TEXT>"
        },
        "body": {
            "text": "<BODY_TEXT>"
        },
        "footer": {
            "text": "<FOOTER_TEXT>"
        },
        "action": {
            "button": "<BUTTON_TEXT>",
            "sections": [
                {
                    "title": "<LIST_SECTION_1_TITLE>",
                    "rows": [
                        {
                            "id": "<LIST_SECTION_1_ROW_1_ID>",
                            "title": "<SECTION_1_ROW_1_TITLE>",
                            "description": "<SECTION_1_ROW_1_DESC>"
                        },
                        {
                            "id": "<LIST_SECTION_1_ROW_2_ID>",
                            "title": "<SECTION_1_ROW_2_TITLE>",
                            "description": "<SECTION_1_ROW_2_DESC>"
                        }
                    ]
                },
                {
                    "title": "<LIST_SECTION_2_TITLE>",
                    "rows": [
                        {
                            "id": "<LIST_SECTION_2_ROW_1_ID>",
                            "title": "<SECTION_2_ROW_1_TITLE>",
                            "description": "<SECTION_2_ROW_1_DESC>"
                        },
                        {
                            "id": "<LIST_SECTION_2_ROW_2_ID>",
                            "title": "<SECTION_2_ROW_2_TITLE>",
                            "description": "<SECTION_2_ROW_2_DESC>"
                        }
                    ]
                }
            ]
        }
    }
}
```
SUCCESS RESPONSE:
```
{
    "messaging_product": "whatsapp",
    "contacts": [{
        "input": "15555551234",
        "wa_id": "<WHATSAPP_ID>"
      }],
    "messages": [{
        "id": "wamid.ID"
      }]
  }
```
ERROR RESPONSE:
```
{
  "statuses": [
    {
      "errors": [
        {
          "code": 1026,
          "href": "https://developers.facebook.com/docs/whatsapp/api/errors/",
          "title": "Receiver Incapable"
        }
      ],
      "id": "gBGGFlAwCWFvAgkyHMGKnRu4JeA",
      "message": {
        "recipient_id": "+91xxxxxxxxxx"
      },
      "recipient_id": "91xxxxxxxxxx",
      "status": "failed",
      "timestamp": "1670394125",
      "type": "message"
    }
  ]
}
```
## Request Send Reply to List Message to Whatsapp Cloud API
```
POST https://graph.facebook.com/{{Version}}/{{Phone-Number-ID}}/messages:
```
```
{
    "messaging_product": "whatsapp",
    "recipient_type": "individual",
    "to": "{{Recipient-Phone-Number}}",
    "context": {
        "message_id": "<MSGID_OF_PREV_MSG>"
    },
    "type": "interactive",
    "interactive": {
        "type": "list",
        "header": {
            "type": "text",
            "text": "<HEADER_TEXT>"
        },
        "body": {
            "text": "<BODY_TEXT>"
        },
        "footer": {
            "text": "<FOOTER_TEXT>"
        },
        "action": {
            "button": "<BUTTON_TEXT>",
            "sections": [
                {
                    "title": "<LIST_SECTION_1_TITLE>",
                    "rows": [
                        {
                            "id": "<LIST_SECTION_1_ROW_1_ID>",
                            "title": "<SECTION_1_ROW_1_TITLE>",
                            "description": "<SECTION_1_ROW_1_DESC>"
                        },
                        {
                            "id": "<LIST_SECTION_1_ROW_2_ID>",
                            "title": "<SECTION_1_ROW_2_TITLE>",
                            "description": "<SECTION_1_ROW_2_DESC>"
                        }
                    ]
                },
                {
                    "title": "<LIST_SECTION_2_TITLE>",
                    "rows": [
                        {
                            "id": "<LIST_SECTION_2_ROW_1_ID>",
                            "title": "<SECTION_2_ROW_1_TITLE>",
                            "description": "<SECTION_2_ROW_1_DESC>"
                        },
                        {
                            "id": "<LIST_SECTION_2_ROW_2_ID>",
                            "title": "<SECTION_2_ROW_2_TITLE>",
                            "description": "<SECTION_2_ROW_2_DESC>"
                        }
                    ]
                }
            ]
        }
    }
}
```
SUCCESS RESPONSE:
```
{
    "messaging_product": "whatsapp",
    "contacts": [{
        "input": "15555551234",
        "wa_id": "<WHATSAPP_ID>"
      }],
    "messages": [{
        "id": "wamid.ID"
      }]
  }
```
ERROR RESPONSE:
```
{
  "statuses": [
    {
      "errors": [
        {
          "code": 1026,
          "href": "https://developers.facebook.com/docs/whatsapp/api/errors/",
          "title": "Receiver Incapable"
        }
      ],
      "id": "gBGGFlAwCWFvAgkyHMGKnRu4JeA",
      "message": {
        "recipient_id": "+91xxxxxxxxxx"
      },
      "recipient_id": "91xxxxxxxxxx",
      "status": "failed",
      "timestamp": "1670394125",
      "type": "message"
    }
  ]
}
```
## Request Send Reply Button to Whatsapp Cloud API
```
POST https://graph.facebook.com/{{Version}}/{{Phone-Number-ID}}/messages:
```
```
{
    "messaging_product": "whatsapp",
    "recipient_type": "individual",
    "to": "{{Recipient-Phone-Number}}",
    "type": "interactive",
    "interactive": {
        "type": "button",
        "body": {
            "text": "<BUTTON_TEXT>"
        },
        "action": {
            "buttons": [
                {
                    "type": "reply",
                    "reply": {
                        "id": "<UNIQUE_BUTTON_ID_1>",
                        "title": "<BUTTON_TITLE_1>"
                    }
                },
                {
                    "type": "reply",
                    "reply": {
                        "id": "<UNIQUE_BUTTON_ID_2>",
                        "title": "<BUTTON_TITLE_2>"
                    }
                }
            ]
        }
    }
}
```
SUCCESS RESPONSE:
```
{
    "messaging_product": "whatsapp",
    "contacts": [{
        "input": "PHONE_NUMBER",
        "wa_id": "WHATSAPP_ID"
      }],
    "messages": [{
        "id": "wamid.ID"
      }]
  }
```
ERROR RESPONSE:
```
{
  "statuses": [
    {
      "errors": [
        {
          "code": 1026,
          "href": "https://developers.facebook.com/docs/whatsapp/api/errors/",
          "title": "Receiver Incapable"
        }
      ],
      "id": "gBGGFlAwCWFvAgkyHMGKnRu4JeA",
      "message": {
        "recipient_id": "+91xxxxxxxxxx"
      },
      "recipient_id": "91xxxxxxxxxx",
      "status": "failed",
      "timestamp": "1670394125",
      "type": "message"
    }
  ]
}
```
## Request Mark Message As Read to Whatsapp Cloud API
```
PUT https://graph.facebook.com/{{Version}}/{{Phone-Number-ID}}/messages:
```
```
{
    "messaging_product": "whatsapp",
    "status": "read",
    "message_id": "<INCOMING_MSG_ID>"
}
```
SUCCESS RESPONSE:
```
{
    "success": true
}
```
ERROR RESPONSE:
```
{
  "statuses": [
    {
      "errors": [
        {
          "code": 1026,
          "href": "https://developers.facebook.com/docs/whatsapp/api/errors/",
          "title": "Receiver Incapable"
        }
      ],
      "id": "gBGGFlAwCWFvAgkyHMGKnRu4JeA",
      "message": {
        "recipient_id": "+91xxxxxxxxxx"
      },
      "recipient_id": "91xxxxxxxxxx",
      "status": "failed",
      "timestamp": "1670394125",
      "type": "message"
    }
  ]
}
```
## Request Send Single Product Message to Whatsapp Cloud API
```
POST https://graph.facebook.com/{{Version}}/{{Phone-Number-ID}}/messages:
```
```
{
    "messaging_product": "whatsapp",
    "recipient_type": "individual",
    "to": "{{Recipient-Phone-Number}}",
    "type": "interactive",
    "interactive": {
        "type": "product",
        "body": {
            "text": "<OPTIONAL_BODY_TEXT>"
        },
        "footer": {
            "text": "<OPTIONAL_FOOTER_TEXT>"
        },
        "action": {
            "catalog_id": "367025965434465",
            "product_retailer_id": "<ID_TEST_ITEM_1>"
        }
    }
}
```
SUCCESS RESPONSE:
```
{
    "messaging_product": "whatsapp",
    "contacts": [
        {
            "input": "+1-631-555-5555",
            "wa_id": "16315555555"
        }
    ],
    "messages": [
        {
            "id": "wamid.gBGGFlaCGg0xcvAdgmZ9plHrf2Mh-o"
        }
    ]
}
```
ERROR RESPONSE:
```
{
  "statuses": [
    {
      "errors": [
        {
          "code": 1026,
          "href": "https://developers.facebook.com/docs/whatsapp/api/errors/",
          "title": "Receiver Incapable"
        }
      ],
      "id": "gBGGFlAwCWFvAgkyHMGKnRu4JeA",
      "message": {
        "recipient_id": "+91xxxxxxxxxx"
      },
      "recipient_id": "91xxxxxxxxxx",
      "status": "failed",
      "timestamp": "1670394125",
      "type": "message"
    }
  ]
}
```
## Request Send Multi-Product Message to Whatsapp Cloud API
```
POST https://graph.facebook.com/{{Version}}/{{Phone-Number-ID}}/messages:
```
```
{
    "messaging_product": "whatsapp",
    "recipient_type": "individual",
    "to": "{{Recipient-Phone-Number}}",
    "type": "interactive",
    "interactive": {
        "type": "product_list",
        "header": {
            "type": "<HEADER_TYPE>",
            "text": "<YOUR_TEXT_HEADER_CONTENT>"
        },
        "body": {
            "text": "<YOUR_TEXT_BODY_CONTENT>"
        },
        "footer": {
            "text": "<YOUR_TEXT_FOOTER_CONTENT>"
        },
        "action": {
            "catalog_id": "146265584024623",
            "sections": [
                {
                    "title": "<SECTION1_TITLE>",
                    "product_items": [
                        {
                            "product_retailer_id": "<YOUR_PRODUCT1_SKU_IN_CATALOG>"
                        },
                        {
                            "product_retailer_id": "<YOUR_SECOND_PRODUCT1_SKU_IN_CATALOG>"
                        }
                    ]
                },
                {
                    "title": "<SECTION2_TITLE>",
                    "product_items": [
                        {
                            "product_retailer_id": "<YOUR_PRODUCT2_SKU_IN_CATALOG>"
                        },
                        {
                            "product_retailer_id": "<YOUR_SECOND_PRODUCT2_SKU_IN_CATALOG>"
                        }
                    ]
                }
            ]
        }
    }
}
```
SUCCESS RESPONSE:
```
{
    "messaging_product": "whatsapp",
    "contacts": [
        {
            "input": "+1-631-555-5555",
            "wa_id": "16315555555"
        }
    ],
    "messages": [
        {
            "id": "wamid.gBGGFlaCGg0xcvAdgmZ9plHrf2Mh-o"
        }
    ]
}
```
ERROR RESPONSE:
```
{
  "statuses": [
    {
      "errors": [
        {
          "code": 1026,
          "href": "https://developers.facebook.com/docs/whatsapp/api/errors/",
          "title": "Receiver Incapable"
        }
      ],
      "id": "gBGGFlAwCWFvAgkyHMGKnRu4JeA",
      "message": {
        "recipient_id": "+91xxxxxxxxxx"
      },
      "recipient_id": "91xxxxxxxxxx",
      "status": "failed",
      "timestamp": "1670394125",
      "type": "message"
    }
  ]
}
```
## Request Send Catalog Message to Whatsapp Cloud API
```
POST https://graph.facebook.com/{{Version}}/{{Phone-Number-ID}}/messages:
```
```
{
    "messaging_product": "whatsapp",
    "recipient_type": "individual",
    "to": "{{Recipient-Phone-Number}}",
    "type": "interactive",
    "interactive": {
        "type": "catalog_message",
        "body": {
            "text": "Hello! Thanks for your interest. Ordering is easy. Just visit our catalog and add items to purchase."
        },
        "action": {
            "name": "catalog_message",
            "parameters": {
                "thumbnail_product_retailer_id": "2lc20305pt"
            }
        },
        "footer": {
            "text": "Best grocery deals on WhatsApp!"
        }
    }
}
```
SUCCESS RESPONSE:
```
{
    "messaging_product": "whatsapp",
    "contacts": [
        {
            "input": "+16505551234",
            "wa_id": "16505551234"
        }
    ],
    "messages": [
        {
            "id": "wamid.HBgLMTY1MDM4Nzk0MzkVAgARGBI3NDMzMjc2N0VDNUVFNURBQzQA"
        }
    ]
}
```
ERROR RESPONSE:
```
{
  "statuses": [
    {
      "errors": [
        {
          "code": 1026,
          "href": "https://developers.facebook.com/docs/whatsapp/api/errors/",
          "title": "Receiver Incapable"
        }
      ],
      "id": "gBGGFlAwCWFvAgkyHMGKnRu4JeA",
      "message": {
        "recipient_id": "+91xxxxxxxxxx"
      },
      "recipient_id": "91xxxxxxxxxx",
      "status": "failed",
      "timestamp": "1670394125",
      "type": "message"
    }
  ]
}
```
## Request Send Catalog Template Message to Whatsapp Cloud API
```
POST https://graph.facebook.com/{{Version}}/{{Phone-Number-ID}}/messages:
```
```
{
    "messaging_product": "whatsapp",
    "recipient_type": "individual",
    "to": "{{Recipient-Phone-Number}}",
    "type": "template",
    "template": {
        "name": "intro_catalog_offer",
        "language": {
            "code": "en_US"
        },
        "components": [
            {
                "type": "body",
                "parameters": [
                    {
                        "type": "text",
                        "text": "100"
                    },
                    {
                        "type": "text",
                        "text": "400"
                    },
                    {
                        "type": "text",
                        "text": "3"
                    }
                ]
            },
            {
                "type": "button",
                "sub_type": "CATALOG",
                "index": 0,
                "parameters": [
                    {
                        "type": "action",
                        "action": {
                            "thumbnail_product_retailer_id": "2lc20305pt"
                        }
                    }
                ]
            }
        ]
    }
}
```
SUCCESS RESPONSE:
```
{
    "messaging_product": "whatsapp",
    "contacts": [
        {
            "input": "+16505551234",
            "wa_id": "16505551234"
        }
    ],
    "messages": [
        {
            "id": "wamid.HBgLMTY1MDM4Nzk0MzkVAgARGBJCOTY3NDc0NDFDRUI3NTA0Q0UA"
        }
    ]
}
```
ERROR RESPONSE:
```
{
  "statuses": [
    {
      "errors": [
        {
          "code": 1026,
          "href": "https://developers.facebook.com/docs/whatsapp/api/errors/",
          "title": "Receiver Incapable"
        }
      ],
      "id": "gBGGFlAwCWFvAgkyHMGKnRu4JeA",
      "message": {
        "recipient_id": "+91xxxxxxxxxx"
      },
      "recipient_id": "91xxxxxxxxxx",
      "status": "failed",
      "timestamp": "1670394125",
      "type": "message"
    }
  ]
}
```
/* template of request doc */
Request  to Whatsapp Cloud API
```
// here method and url [ex: POST https://site.com/send]
```
```
// here json
```

## All Of Request Documentation is Referred from 
https://www.postman.com/meta/workspace/whatsapp-business-platform/folder/13382743-1f4f7644-cc97-40b5-b8e4-c19da268fff1
