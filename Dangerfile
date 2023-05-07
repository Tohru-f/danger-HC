fail 'Pull Request descriptionの記載をお願いします' if github.pr_body.length < 5

fail 'pull requestのdescriptionにherokuapp.comのURLを記載してください' unless github.pr_body.include?('herokuapp.com')

fail 'reviewerを指定して下さい' if github.pr_json[:requested_reviewers].empty?

fail "assigneesが未指定です" unless github.pr_json["assignee"]
