# Frequently Asked Questions

### Q: How to Customise Message Display?

**Text, Image, Buttons**
```js
conn.sendButton(
      jid, // jid of the user to send the message to
      text, // text to send
      foooter, // footer to send
      buffer, // buffer to send (optional), if you want to send button image, location, etc
      buttons, // buttons to send, example [['text1', 'id1'], ['text2', 'id2']]
      quoted, // quoted message to send (optional)
      options // options to send, example { asLocation: true }
)
```
```js
Code Format
conn.sendButton(jid, '<text>', '<footer>', '<buffer>',
[
['<BUTTON-1>', 'button-1'],
['<BUTTON-2>', '<button-2>'],
['<BUTTON-3>', '<button-3>']
],
<options>
)
```
```js
Example With Location Image
conn.sendButton(m.chat, 'Hello World!', 'By Valor_Bot', 'valor.jpg',
[
['Hello', 'hello'],
['Hi', 'hi'],
['Bye', 'bye']
], m, { asLocation: true })
```

**Text, Image, URL, Call, Buttons**
```js
conn.sendButton(
      jid, // jid of the user to send the message to
      text, // text to send
      foooter, // footer to send
      buffer, // buffer to send (optional), if you want to send button image, location, etc
      url-link, // url link as a button to send
      url-name, // display name of url link as a button to send
      contact-number, // contact number as a button to send
      contact-name, // display name of contact number as a button to send
      buttons, // buttons to send, example [['text1', 'id1'], ['text2', 'id2']]
      quoted, // quoted message to send (optional)
      options // options to send, example { asLocation: true }
)
```
```js
Code Format
conn.sendHydrated(m.chat, '<header>', '<footer>', '<buffer>', '<url-link>', '<url-name>', '<contact-number>', '<contact-name>',
[
['<BUTTON-1>', 'button-1'],
['<BUTTON-2>', '<button-2>'],
['<BUTTON-3>', '<button-3>']
], <options>)
```
```js
Example
conn.sendButton(m.chat, 'Hello World!', '@Valor_Bot', 'https://github.com/DineshValor/',
[
['Hello', 'hello'],
['Bye', 'bye']
], m)
```
