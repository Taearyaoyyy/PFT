 # PFT
 name: LINE Notify

on:
  push:
    branches:
      - main

jobs:
  notify:
    runs-on: ubuntu-latest
    steps:
      - name: Send LINE Notify
        uses: snow-actions/line-notify@v1.1.0
        with:
          access_token: ${{ secrets.LINE_ACCESS_TOKEN }}
          message: "แจ้งเตือนจาก PlugfileTu-: มีการเปลี่ยนแปลงใน repository นะ"
