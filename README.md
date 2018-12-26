# Dwango_report
- 実装内容
  - 与えられた文章に対して似た意味と反対の意味を持つ文章を返す
- 実装方法
  - 文章を分解するため(形態素解析)mecabを使用
  - 同じ意味を持つ単語を検索するためword2vecを使用して実装する
  - 反対の意味を持つ単語を検索するために何かしらをしなくてはいけない(negative="単語"の方法では無理だった)
- 実行方法
  - pipで mecab-pythonと gensimのインストールを行う
  - execute.pyを実行する
- モデル作成のために行ったこと
  - wikipedia(https://dumps.wikimedia.org/jawiki/latest/)からテキストデータを持ってくる
  - wikiextractorで使いやすいデータにする
  - type text/*/* > jawiki.txtで１つのファイルにまとめる
  - wiki_mol.pyを実行させまとめたファイルに対して形態素解析を行い動詞と名詞の単語をwikidata.txtにまとめる
  - まとめたファイルに対してword2vecを用いてモデル化する
