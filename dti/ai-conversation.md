
# AI Conversation History Export

This format is intended for interoperable export/import of AI conversation history.
It may be useful in personal data portability scenarios, where a user wishing to 
transfer their history to a new service can have the new service ingest their 
conversation history with a previous service.  It may also be useful simply for 
users to back up their important conversations.

## Using this format

All senders of messages in the "messages" section are identified in the "identifiers"
section, except "AI" if there is only one AI in the conversation.

Comments and suggestions may be sent to DTI via dtinit.org.

## Example

```json
{
  "details": {
    "createdBy": "ChatExample AI",
    "createdAt": "2026-05-14T18:00:00Z",
    "startTime": "2026-05-14T17:42:00Z",
    "endTime": "2026-05-14T17:47:30Z",
    "modality": "text"
  },
  "identifiers": [
    {
      "name": "Jordan Rivera",
      "type": "email",
      "identifier": "jordan.rivera@example.com"
    }
  ],
  "messages": [
    {
      "sentAt": "2026-05-14T17:42:00Z",
      "sender": "jordan.rivera@example.com",
      "text": "I need to plan dinners for the week but I only have about 30 minutes to cook each night. Any ideas?",
      "channel": "Web"
    },
    {
      "sentAt": "2026-05-14T17:42:08Z",
      "sender": "AI",
      "text": "Here are a few 30-minute dinner ideas:\n\n1. **Stir-fry** — chicken or tofu with frozen vegetables over rice\n2. **Pasta with marinara** — use store-bought sauce and add ground beef or sausage\n3. **Sheet-pan salmon** — salmon fillets with broccoli and lemon, roasted at 400°F for 20 minutes\n4. **Black bean tacos** — canned beans, cheese, and salsa in warm tortillas\n5. **Fried rice** — great for using up leftover rice and vegetables\n\nWould you like recipes for any of these?",
      "channel": "Web"
    },
    {
      "sentAt": "2026-05-14T17:45:12Z",
      "sender": "jordan.rivera@example.com",
      "text": "The sheet-pan salmon sounds great, can you give me the full recipe?",
      "channel": "Web"
    },
    {
      "sentAt": "2026-05-14T17:45:20Z",
      "sender": "AI",
      "text": "**Sheet-Pan Salmon with Broccoli**\n\nIngredients (serves 2):\n- 2 salmon fillets\n- 2 cups broccoli florets\n- 2 tbsp olive oil\n- Salt, pepper, garlic powder\n- 1 lemon, sliced\n\nInstructions:\n1. Preheat oven to 400°F.\n2. Toss broccoli with 1 tbsp olive oil, salt, and pepper on a sheet pan.\n3. Place salmon on the same pan, drizzle with remaining olive oil, and season with salt, pepper, and garlic powder.\n4. Lay lemon slices on top of salmon.\n5. Roast 18–20 minutes until salmon flakes easily.\n\nTotal time: about 25 minutes. Enjoy!",
      "channel": "Web"
    }
  ]
}
```