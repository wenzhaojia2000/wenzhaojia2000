<!--
## Hi there 👋
**wenzhaojia2000/wenzhaojia2000** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->

Here's a useful command to list all commits made by you in the current working repository at a certain date. Just stick the following at the end of your `.bashrc` file:

```bash
# Logs git commits by you on a certain date
commitsMade () {
        git log --pretty='format:%C(yellow)%h %Creset%s%Cred%d' --branches \
    --after="$1 0:00" --before="$1 23:59" --author "`git config user.name`";
}
```

Now both these commands list commits made today:
```sh
$ commitsMade today
$ commitsMade
```

This command lists commits made yesterday:
```sh
$ commitsMade yesterday
```

And this on an arbitrary date:
```sh
$ commitsMade 2024-08-02
```
