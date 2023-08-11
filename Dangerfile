fail 'Pull Request descriptionの記載をお願いします' if github.pr_body.length < 5

warn 'deployする課題の場合はherokuにdeployかつpull requestのdescriptionにdeployしたURL(herokuapp.com)を記載してください' unless github.pr_body.include?('herokuapp.com')

fail 'reviewersを指定して下さい' if github.pr_json[:requested_reviewers].empty?

fail "assigneesが未指定です" unless github.pr_json["assignee"]

if git.added_files.include?(".env")
  fail <<~TEXT
    .envファイルをコミットしないでください。
    .gitignoreに.envを追加してください。
    .env.exampleで設定する環境変数例を記載するとよいでしょう。
  TEXT
end
#2023.8.11追記
