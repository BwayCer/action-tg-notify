GitHub Action Telegram 推送訊息
=======


> 版本： v1.0.0

GitHub Action 的 Telegram 推送訊息工具。



## 使用方式

```
...
jobs:
  runUbuntu:
    runs-on: ubuntu-latest
    steps:
      - uses: bwaycer/action-tg-notify
        id: tgNotify
        with:
          botToken: ${{ secrets.BOT_TOKEN }}
          chatId: ${{ secrets.CHAT_ID }}
          text: 'some text'
      - name: show result
        run: echo ${{ steps.tgNotify.outputs.result }}
```

