# clasp-template

## 利用手順

1. [https://github.com/sekine-1113/clasp-template] を `git clone`
    - httpsの場合：`git clone https://github.com/sekine-1113/clasp-template.git`
    - sshの場合：`git clone git@github.com:sekine-1113/clasp-template.git`
1. cloneしたディレクトリで `npm install`
1. `npm run login` で `clasp` にログイン
1. Google Apps Script APIの設定をオンに変更
     - [https://script.google.com/home/usersettings:title]
1. スプレッドシートの作成または紐づけ
    - 作成の場合：`clasp create <プロジェクト名>`
    - 紐づけの場合：`clasp clone <スクリプトID>`
        - スクリプトIDは Google Apps Scriptのエディタから「プロジェクトの設定」→「ID」に記載
1. GCPと紐づけ
    1. Google Cloud Platform のコンソールにアクセス
    1. 新しいプロジェクトを作成、画面の案内に沿ってプロジェクトの構成を設定（すでに作成している場合はスキップ）
        - 新規作成の場合：「指標」→「OAuthクライアントを作成」でOAuthクライアントIDを作成
        - 既存の場合：「APIとサービス」→「認証情報」→「認証情報を作成」→「OAuthクライアントID」→「ウェブアプリケーション」でOAuthクライアントIDを作成
    1. 「APIとサービス」→「OAuth同意画面」→「対象」→「テストユーザー」に自身のメールアドレスを入力
1. エディタ（VSCode）でコードを書く
1. `npm run deploy` でリモートに push
1. `clasp run <関数名>` で実行可能
