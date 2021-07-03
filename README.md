The `new-group` tool in this repository takes a group name and a list of commits.  It checks out the `groups`
branch and then adds a commit to it whose message is the group name and whose list of parents includes all of
the specified commits. This produces a repository something like:

```
% git log --format=oneline --graph --all
*-.   10659afc2c13f9d2a7dbacdbdaeb641823e8318c (groups) new-group tool
|\ \
* \ \   657ea908f3dc942b6bd15db849964d56d628ed60 ed2e033819fe92a501d3501cca5e82aa5ac91758
|\ \ \
| | |/
| |/|
| * | c70b86c79d7968ca7d89ade3861bab638c53541b (HEAD -> main) make new-group executable
| |/
| * ed2e033819fe92a501d3501cca5e82aa5ac91758 initial new-group
| |
|  \
|   \
|    \
*---. | 042eb3fcdef8d0c6474fffbe27d70f6b217a8124 third group
|\ \ \|
| | | * f54511dfa8694aba692788adf480df2e4f39a8fb g
| | |/
| | * 0ef3c9a7436d4b205134519003e37efd0a69371f f
| |/
| * 7027077047120847fc23d8137754a478ce824127 e
* |   323d1b5365cc2962b0d33bb45190bf9eaf14cec6 second group
|\ \
| \ \
|  \ \
|   \ \
|    \ \
*---. \ \   ecf40cb20fa3878383ccd656eb900a42c503911b first group
|\ \ \ \ \
| | | |/ /
| | |/| /
| | | |/
| | | * 945153ad1088c6f0ba51871a73076b3df940ae58 d
| | | * 18e126d841e56dac46546d1ac034d39a36f369dd c
| | |/
| | * baa4c78372e7e1ec541aa2121286efc044431378 b
| |/
| * f6e4687e4c450733ca741dcb15a9a0a6d2ce2727 a
| * bfc0e809e4416fdba3249a01f231d4c054955ec9 (root)
* 157d0b38c1891eb91c00f8acf8f09250570eabf1 (group root)
```
