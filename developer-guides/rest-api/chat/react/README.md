# Chat Message Reactions

Toggles the authenciated user's reaction to the provided message.

| URL | Requires Auth | HTTP Method |
| :--- | :--- | :--- |
| `/api/v1/chat.react` | `yes` | `POST` |

## Payload

| Argument | Example | Required | Description |
| :--- | :--- | :--- | :--- |
| `emoji` | `smile` | Required | The emoji to react with. |
| `messageId` | `7aDSXtjMA3KPLxLjt` | Required | The message id to react to. |

The `emoji` does not have to contain the `:`'s. However, the emoji *does* have to exist.

## Example Call

```bash
curl -H "X-Auth-Token: 9HqLlyZOugoStsXCUfD_0YdwnNnunAJF8V47U3QHXSq" \
     -H "X-User-Id: aobEdbYhXfu5hkeqG" \
     -H "Content-type:application/json" \
     http://localhost:3000/api/v1/chat.react \
     -d '{ "messageId": "7aDSXtjMA3KPLxLjt", "emoji": "smile" }'
```

## Example Result

```json
{
    "success": true
}
```

## Change Log

| Version | Description |
| :--- | :--- |
| 0.63.0 | Emoji has to exist now |
| 0.62.2 | Added |
