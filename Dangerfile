raise 'Pull Request descriptionの記載をお願いします' if github.pr_body.length < 5

raise 'pull requestのdescriptionにherokuapp.comのURLを記載してください' unless github.pr_body.include?('herokuapp.com')

raise 'reviewerを指定して下さい' if github.pr_json[:requested_reviewers].empty?
