
# GitHub Pages公開チュートリアル（VS Code使用）

## 前提条件
- Webサイトのファイル（例：`index.html`など）が1つのフォルダにまとまっている
- GitHubアカウントを持っている
- VS Codeがインストールされている

---

## ① Gitのインストール（初回のみ）

まだGitがパソコンに入っていない場合は、以下からダウンロードしてインストール：

- Windows: [https://gitforwindows.org](https://gitforwindows.org)  
- macOS: Homebrewで `brew install git` または [https://git-scm.com](https://git-scm.com)

インストール後、VS Codeを再起動してください。

---

## ② Gitのユーザー情報を登録（初回のみ）

VS Codeを開いて、メニューから「ターミナル → 新しいターミナル」を開き、以下のコマンドを入力：

```bash
git config --global user.name "あなたのGitHubユーザー名"
git config --global user.email "GitHubに登録しているメールアドレス"
```

設定確認（省略可）：

```bash
git config --global --list
```

---

## ③ GitHub上で新しいリポジトリを作成

1. [https://github.com](https://github.com) にアクセスし、ログイン
2. 右上の `+` → 「New repository」をクリック
3. 次の設定で作成：

- Repository name: 任意の名前（例：`my-website`）
- Public（公開）を選択
- Initialize with README は **チェックしない**（空のリポジトリにする）

「Create repository」をクリック

---

## ④ VS Codeでリポジトリを登録

1. VS Codeであなたのプロジェクトフォルダ（`index.html`があるディレクトリ）を開いている状態で、
2. 左のメニューから「ソース管理」タブ（Gitアイコン）をクリック
3. 「リポジトリとして初期化」ボタンを押す（もしくは「Initialize Repository」）

---

## ⑤ GitHubリポジトリに接続

ターミナルで以下を実行（`your-username`と`your-repo-name`は適宜変更）：

```bash
git remote add origin https://github.com/your-username/your-repo-name.git
```

例：

```bash
git remote add origin https://github.com/yohman/my-website.git
```

---

## ⑥ 初回コミットとプッシュ（VS CodeのGUIで）

1. 左側のソース管理タブで、すべての変更ファイルが表示されていることを確認
2. 上部のメッセージ欄にコミットメッセージを入力（例：`first commit`）
3. チェックマーク（✔）をクリックしてコミット
4. 右上の「…」から「Remote → Push」を選択（もしくは「Publish Branch」ボタンが出ている場合はそれをクリック）

GitHubにログインを求められる場合は、ブラウザで認証してください。

---

## ⑦ GitHub Pagesを有効にする

1. GitHubで該当のリポジトリページを開く
2. 「Settings」→「Pages」タブを開く
3. 「Source」欄を「`main` / `master` branch」→「`/ (root)`」に設定
4. 「Save」ボタンを押す

数分後、表示される公開URL（例：`https://your-username.github.io/your-repo-name/`）にアクセスすると、Webページが表示されます。

---

## 完了

お疲れ様でした。これで、VS Codeで作成したWebサイトをGitHub Pagesで公開できました。  
今後の更新はファイルを修正後、コミット → プッシュを繰り返せば自動的にサイトが更新されます。
