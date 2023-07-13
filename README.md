# 1stdibs's `robots.txt`

We have two `robots.txt` files. One under the buyer site domain and another under the domain from where we serve our assets, e.g., images. You likely only need to update the `robots.txt` file in the `www.1stdibs.com` directory.

You can see both of these files live on production:
* https://www.1stdibs.com/robots.txt
* https://a.1stdibscdn.com/robots.txt

## Updates (Non-Technical)

Use the links below to learn how to edit the `robots.txt` files directly in Github and create a pull request.

* [Editing Files](https://docs.github.com/en/repositories/working-with-files/managing-files/editing-files)
  * If this is your first time editing a file, you may be asked to "fork" the repository. You'll have to perform that action first before you can go ahead.
* [Creating a Pull Request](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request)
  * Please add any relevant Jira ticket numbers to your commit message. 

Once you create the pull request, you'll have several reviewers automatically assigned to your pull request. They will handle reviewing, merging, and deploying your changes onto production.

## Reviews

A pull request must be reviewed before it can be merged. If you are assigned to a pull request for this repository, please review the changes and reach out to your team to coordinate when the changes should be deployed. 

Once the changes are merged, please run the Jenkins job with the `noop` flag and comment on the pull request with the output. If the output looks correct, rerun the job with the production flag. See this [pull request](https://github.com/1stdibs/robots.txt/pull/39) as an example.

## Deployment

- There is a Jenkins job configured to deploy `robots.txt` changes to production, which resides here : 
	- https://janky2.1stdibs.com/job/robots.txt-prod/
- The job features a `noop` flag allowing you to do a dry run of the deployment.
	- This outputs the diff between the current changes in master and what's on production.

**DO NOT DEPLOY WITHOUT THE EXPRESS PERMISSION OF:**
- the SEO team
- the Growth Team PM

