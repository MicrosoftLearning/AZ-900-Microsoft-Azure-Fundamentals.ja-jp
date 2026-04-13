---
lab:
  title: 演習 - Azure リソースを作成する
  module: Module 01 - Describe the core architectural components of Azure
  description: この演習では、Azure portal を使ってリソースを作成します。 演習の焦点は、Azure リソース グループで作成されたリソースをどのように設定するかを確認することです。
  duration: 15 minutes
  level: 100
  islab: true
  primarytopics:
    - Azure
    - Azure Portal
---

<!--
Edit the metadata above to manage the list of exercises in the home page of the GitHub site that gets generated.
You can delete the module and edit index.md in the root of the repo to customize the display so that only the exercises are listed
To enable GitHub page publishing, edit the Page settings for the repo and publish from the main branch
-->

# Microsoft Azure リソースを作成する <!-- match title in metadata above (and Learn Exercise unit and ILT slide)-->

この演習では、Azure portal を使用してリソースを作成します。 演習の焦点は、Azure リソース グループで作成されたリソースをどのように設定するかを確認することです。

この演習の所要時間は約 **15** 分です。 <!-- update with estimated duration -->

> [!IMPORTANT]
> この演習を終えるには、リソース グループと仮想マシンを作成するための十分なアクセス許可を持って Azure サブスクリプションにアクセスする必要があります。

## タスク 1: リソース グループを作成する
このタスクでは、リソース グループを作成します。 この演習用のリソース グループを作成すると、完了時に演習をクリーンアップしやすくなります。

1. [Azure Portal](https://portal.azure.com/?azure-portal=true) にログインします。
1. **[リソース グループ]** を選択します。
1. **［作成］** を選択します
1. **[サブスクリプション]** ドロップダウン リストから、この演習に使うサブスクリプションを選びます。
1. リソース グループ名に「`IntroAzureRG`」と入力します。
1. ご自分のサブスクリプションまたはコース環境で使用できる Azure リージョンを選びます。
1. **[Review + create](レビュー + 作成)** を選択します。
1. **［作成］** を選択します
1. **[ホーム]** を選択して、Azure portal のホーム画面に戻ります。

## タスク 2: 仮想マシンを作成する

このタスクでは、Azure portal を使用して仮想マシンを作成します。

1. **[リソースの作成]** を選択します。
1. [カテゴリ] メニューから **[インフラストラクチャ サービス]** を選びます。
1. 仮想マシンの見出しの下にある **[作成]** を選びます。
1. [仮想マシンの作成] ペインが開き、[基本] タブが開きます。
1. 各設定に対して次の値を入力します。 設定が指定されていない場合は、既定値のままにします。
    
    **[基本] タブ**
    
    | **設定**                  | **Value**                                       |
    | ---------------------------- | ----------------------------------------------- |
    | サブスクリプション                 | タスク 1 で選んだサブスクリプションを選びます。 |
    | リソース グループ               | IntroAzureRG                                    |
    | 仮想マシン名         | `my-vm`                                         |
    | リージョン                       | IntroAzureRG と同じ                            |
    | ゾーンのオプション​​                 | 既定値のままにする                                   |
    | 可用性ゾーン            | 既定値のままにする                                   |
    | セキュリティの種類                | 既定値のままにする                                   |
    | Image                        | 既定値のままにする                                   |
    | VMアーキテクチャ              | 既定値のままにする                                   |
    | Azure Spot 割引で実行する | Unchecked                                       |
    | サイズ                         | 既定値のままにする                                   |
    | 認証               | Password                                        |
    | Username (ユーザー名)                     | `azureuser`                                     |
    | Password (パスワード)                     | カスタム パスワードを入力する                         |
    | パスワードの確認             | カスタム パスワードを再入力する                     |
    | パブリック受信ポート         | なし                                            |

6.  **[確認と作成]** を選択します。
6.  **[作成] を選択する。**

VM がプロビジョニングされるのを待ちます。 デプロイが進行中の場合は、VM の準備ができたら [配置完了] に変わります。

## タスク 3: 作成されたリソースを確認する

デプロイが作成されたら、VM だけでなく、VM に必要なすべての関連リソースが Azure によって作成されたことを確認できます。

1.  **[ホーム]** を選びます
2.  **[リソース グループ]** を選択します
3.  **[IntroAzureRG]** リソース グループを選びます

リソース グループ内のリソースの一覧が表示されます。 既定で、関連付けに役立つように同様の名前が Azure によってすべて付けられ、それらが同じリソース グループにグループ化されました。

おめでとうございます。 Azure でリソースを作成し、作成時にリソースがどのようにグループ化されるかを確認しました。

## クリーンアップ
1. Azure のホーム ページで、[Azure サービス] の下にある **[リソース グループ]** を選びます。
1. **[IntroAzureRG]** リソース グループを選びます。
1. **[リソース グループの削除]** を選択します。
1. **[選択した仮想マシンと仮想マシン スケール セットに対して強制削除を適用する]** が表示されている場合は、それがオンになっていることを確認します。
1. 「`IntroAzureRG`」と入力してリソース グループの削除を確認します。
1. **[削除]** を選択します。
1. [削除の確認] ポップアップ ウィンドウで、**[削除]** を選びます。
