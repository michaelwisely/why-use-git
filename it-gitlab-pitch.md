I think our best option would be to host a local instance of GitLab. 
GitLab is a Ruby on Rails web application that provides a friendly web interface for viewing and interacting with git repositories.
It can be configured to authenticate users against the campus LDAP server, so we can be sure it is only used by students, staff, and faculty.
 
It uses Gitolite to host the git repositories and manage access control. 
Gitolite allows users to clone over SSH or HTTP(S). 
If users want to clone over SSH, they will be required to upload an SSH public key. 
If they want to clone over HTTP(S), they can use their SSO password (assuming that GitLab is configured to use the campus LDAP server). 
For this reason, it would be imperative to set up HTTPS on a GitLab installation.
 
GitLab's biggest selling point is its user-friendliness. 
If you try out the demo at http://demo.gitlabhq.com, you'll notice that it looks a lot like GitHub.
It makes collaboration simpler, and can automate some of the processes which required an IT ticket in the past. 
IT could configure GitLab to let users create repositories on their own, which would alleviate trivial tickets like "Please make me a repository". 
If they want to limit users to a certain number of repositories each or disable repo creation, that's also possible.
 
TL;DR...

GitLab (http://gitlab.org):
- It's open source
- It's pretty 
- It feels familiar (like GitHub)
    - Easy collaboration
    - Code review through pull requests
- It can authenticate users against campus's LDAP server
- Git over SSH and HTTPS
    - Public/private key authentication over SSH
- Configure user access/abilities through a web interface
- Michigan State University is using it
- It is an actively developed project
    - It's a Rails app, so it may require occasional security updates.
