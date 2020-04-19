# work
■機能  
・sakura_grep.xlsmにgrepしたいキーワードを記載しマクロを実行することで、サクラエディタを実行するバッチスクリプトを作成する。  
・サクラエディタのgrep時に使用できるオプションを選択できるようにする 　※仕事に使いそうなもののみ  
・grep結果は1つのファイルに追記していくか、各キーワード毎にファイルを作成するか選択できるようにする  

■動作確認環境  
・Windows10 home  
・サクラエディタ Ver. 2.2.0.1  
・Microsoft Excel2016 32bit  

■使い方  
①sakura_grep.xlsmを起動し、以下を設定する。  
  * sakuraエディタのパス (例.C:\Program Files (x86)\sakura\sakura.exe)  
  * 検索フォルダ (例.C:\Users\taka6\Desktop\work_repo\hoge)  
  * 検索ファイル種別 (例.!\*.xlsx,\*.\*)  
  * サブフォルダ検索 (サブフォルダ検索する場合は"○"、しない場合はそれ以外の文字)  
  * 大文字小文字区別 (区別する場合は"○"、しない場合はそれ以外の文字)
  * 正規表現 (正規表現を使用する場合は"○"、しない場合はそれ以外の文字)  
  * 単語単位 (単語単位で検索する場合は"○"、しない場合はそれ以外の文字)  
  * 標準出力 (標準出力する場合は"○"、しない場合はそれ以外の文字)  
  * grep結果出力フォルダ (例.C:\Users\taka6\Desktop\work_repo\output\)  
  * grep結果をまとめるか(result_all.txt) (例.まとめる場合は"○"、まとめない場合はそれ以外の文字)  
  * バッチスクリプト名(パス名も記載) (例.C:\Users\taka6\Desktop\work_repo\grep.bat)  
  
②[開発]タブ-[マクロ]を選択し、"Sample"を実行する  

③"バッチスクリプト名(パス名も記載)"にバッチスクリプトが作成される
  
■現在分かっていること(2020/04/19)
  * 入力のチェック処理がない。  
    標準出力しない場合は、サクラエディタのウィンドウにgrep結果が表示されるため以下設定は無駄となってしまう。
    "grep結果出力フォルダ"、"grep結果をまとめるか(result_all.txt)"
  * "grep出力結果フォルダ"は末尾に\\をつける必要がある
  
