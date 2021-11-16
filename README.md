# My VSCode Setup

## Terminal Setup

1) Git Bash
- https://avladov.com/blog/641/replacing-command-prompt-git-bash (Config)
- http://practicalseries.com/1002-vcs/03-03-install.html (Change default path)

2) Hyper

### MacOS

1) https://dev.to/code2rithik/how-to-install-hyper-terminal-for-macbook-8db
2) https://github.com/vercel/hyper
3) https://stackoverflow.com/questions/68884397/hyper-terminal-zsh-command-not-found-hyper
4) https://tjay.dev/howto-my-terminal-shell-setup-hyper-js-zsh-starship/
5) https://github.com/MozzarellaM/hyper-monokai-pro (Monokai Pro Theme)
6) https://github.com/lucleray/hyper-opacity (Hyper Opacity background)

### Windows

1) https://github.com/lucleray/hyper-opacity (Hyper Opacity background)

## Setup SSH for GitHub

https://help.github.com/en/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent

```
$ git config --global user.name "John Doe"
$ git config --global user.email "john@doe.org"

$ git config user.name
$ git config user.email
```

## Backup and Synchronize VSCode Settings with a GitHub Gist

https://mikefrobbins.com/2019/03/21/backup-and-synchronize-vscode-settings-with-a-github-gist/

## Extensions

- Auto Close Tag
- Auto Rename Tag
- Auto-Open Markdown Preview
- Bracket Pair Colorizer
- Color Picker
- CSS Peek
- ES7 React/Redux/GraphQL/React-Native snippets
- ESLint
- Git History
- GitLens — Git supercharged
- HTML CSS Support
- Hyper in VS Code
- indent-rainbow
- JavaScript (ES6) code snippets
- Jest Snippets
- Live Server
- Markdown PDF
- Material Icon Theme
- Monokai Pro
- Prettier - Code formatter
- Remote - WSL
- Settings Sync
- TODO Highlight
- Turbo Console Log

## VSCode user config (settings.json)
```
{
	"editor.roundedSelection": false,
	"editor.snippetSuggestions": "top",
	"editor.tabSize": 2,
	"editor.minimap.enabled": false,
	"editor.fontSize": 14,
	"editor.fontLigatures": true,
	"editor.suggestSelection": "first",
	"editor.formatOnSave": true,
	"editor.gotoLocation.multipleDefinitions": "goto",
	"editor.defaultFormatter": "esbenp.prettier-vscode",
	"explorer.openEditors.visible": 0,
	"explorer.autoReveal": false,
	"explorer.confirmDragAndDrop": false,
	"workbench.iconTheme": "material-icon-theme",
	"workbench.colorTheme": "Monokai Classic",
	"workbench.editor.enablePreviewFromQuickOpen": false,
	"workbench.startupEditor": "newUntitledFile",
	"window.zoomLevel": 1,
	"liveServer.settings.donotShowInfoMsg": true,
	"gitlens.advanced.messages": {
		"suppressCommitHasNoPreviousCommitWarning": false,
		"suppressCommitNotFoundWarning": false,
		"suppressFileNotUnderSourceControlWarning": false,
		"suppressGitVersionWarning": false,
		"suppressLineUncommittedWarning": false,
		"suppressNoRepositoryWarning": false
	},
	"gitlens.keymap": "none",
	"todohighlight.keywords": ["todo", "@todo", "fixme", "@fixme"],
	"todohighlight.isCaseSensitive": false,
	"todohighlight.defaultStyle": {
		"color": "white",
		"backgroundColor": "#ffab00",
		"overviewRulerColor": "#ffab00",
		"fontWeight": "bold"
	},
	"breadcrumbs.enabled": true,
	"javascript.updateImportsOnFileMove.enabled": "never",
	"[javascript]": {
		"editor.defaultFormatter": "esbenp.prettier-vscode"
	},
	"typescript.updateImportsOnFileMove.enabled": "never",
	"[typescriptreact]": {
		"editor.defaultFormatter": "esbenp.prettier-vscode"
	},
	"[typescript]": {
		"editor.defaultFormatter": "esbenp.prettier-vscode"
	},
	"[jsonc]": {
		"editor.defaultFormatter": "esbenp.prettier-vscode"
	},
	"eslint.alwaysShowStatus": true,
	"eslint.migration.2_x": "off",
	"eslint.validate": [
		"javascript",
		"javascriptreact",
		"typescript",
		"typescriptreact"
	],
	"prettier.singleQuote": true,
	"prettier.useTabs": true,
	"git.confirmSync": false,
	"git.autofetch": true,
	"workbench.editor.enablePreview": false,
	"terminal.external.windowsExec": "C:\\WINDOWS\\System32\\bash.exe",
	"extensions.ignoreRecommendations": true,
	"turboConsoleLog.logMessagePrefix": "",
	"sync.gist": "ca918e14a9b9ea8b6c7ffce533bc685d",
	"terminal.integrated.defaultProfile.osx": "zsh",
	"terminal.external.osxExec": "Hyper.app",
	"terminal.explorerKind": "external"
}
```

## Hyper Config (.hyper.js)
```
'use strict';
// Future versions of Hyper may add additional config options,
// which will not automatically be merged into this file.
// See https://hyper.is#cfg for all currently supported options.
module.exports = {
	config: {
		// choose either `'stable'` for receiving highly polished,
		// or `'canary'` for less polished but more frequent updates
		updateChannel: 'stable',
		// default font size in pixels for all tabs
		fontSize: 15,
		// font family with optional fallbacks
		fontFamily:
			'Menlo, "DejaVu Sans Mono", Consolas, "Lucida Console", monospace',
		// default font weight: 'normal' or 'bold'
		fontWeight: 'normal',
		// font weight for bold characters: 'normal' or 'bold'
		fontWeightBold: 'bold',
		// line height as a relative unit
		lineHeight: 1,
		// letter spacing as a relative unit
		letterSpacing: 0,
		// terminal cursor background color and opacity (hex, rgb, hsl, hsv, hwb or cmyk)
		cursorColor: 'rgba(248,28,229,0.8)',
		// terminal text color under BLOCK cursor
		cursorAccentColor: '#000',
		// `'BEAM'` for |, `'UNDERLINE'` for _, `'BLOCK'` for █
		cursorShape: 'BLOCK',
		// set to `true` (without backticks and without quotes) for blinking cursor
		cursorBlink: false,
		// color of the text
		foregroundColor: '#fff',
		// terminal background color
		// opacity is only supported on macOS
		backgroundColor: '#000',
		// terminal selection color
		selectionColor: 'rgba(248,28,229,0.3)',
		// border color (window, tabs)
		borderColor: '#333',
		// custom CSS to embed in the main window
		css: '',
		// custom CSS to embed in the terminal window
		termCSS: '',
		// set custom startup directory (must be an absolute path)
		workingDirectory: '',
		// if you're using a Linux setup which show native menus, set to false
		// default: `true` on Linux, `true` on Windows, ignored on macOS
		showHamburgerMenu: '',
		// set to `false` (without backticks and without quotes) if you want to hide the minimize, maximize and close buttons
		// additionally, set to `'left'` if you want them on the left, like in Ubuntu
		// default: `true` (without backticks and without quotes) on Windows and Linux, ignored on macOS
		showWindowControls: '',
		// custom padding (CSS format, i.e.: `top right bottom left`)
		padding: '12px 14px',
		// the full list. if you're going to provide the full color palette,
		// including the 6 x 6 color cubes and the grayscale map, just provide
		// an array here instead of a color map object
		colors: {
			black: '#000000',
			red: '#C51E14',
			green: '#1DC121',
			yellow: '#C7C329',
			blue: '#0A2FC4',
			magenta: '#C839C5',
			cyan: '#20C5C6',
			white: '#C7C7C7',
			lightBlack: '#686868',
			lightRed: '#FD6F6B',
			lightGreen: '#67F86F',
			lightYellow: '#FFFA72',
			lightBlue: '#6A76FB',
			lightMagenta: '#FD7CFC',
			lightCyan: '#68FDFE',
			lightWhite: '#FFFFFF',
			limeGreen: '#32CD32',
			lightCoral: '#F08080',
		},
		// the shell to run when spawning a new session (i.e. /usr/local/bin/fish)
		// if left empty, your system's login shell will be used by default
		//
		// Windows
		// - Make sure to use a full path if the binary name doesn't work
		// - Remove `--login` in shellArgs
		//
		// Windows Subsystem for Linux (WSL) - previously Bash on Windows
		// - Example: `C:\\Windows\\System32\\wsl.exe`
		//
		// Git-bash on Windows
		// - Example: `C:\\Program Files\\Git\\bin\\bash.exe`
		//
		// PowerShell on Windows
		// - Example: `C:\\WINDOWS\\System32\\WindowsPowerShell\\v1.0\\powershell.exe`
		//
		// Cygwin
		// - Example: `C:\\cygwin64\\bin\\bash.exe`
		shell: '/opt/homebrew/bin/zsh',
		// for setting shell arguments (i.e. for using interactive shellArgs: `['-i']`)
		// by default `['--login']` will be used
		shellArgs: ['--login'],
		// for environment variables
		env: {},
		// Supported Options:
		//  1. 'SOUND' -> Enables the bell as a sound
		//  2. false: turns off the bell
		bell: 'SOUND',
		// An absolute file path to a sound file on the machine.
		// bellSoundURL: '/path/to/sound/file',
		// if `true` (without backticks and without quotes), selected text will automatically be copied to the clipboard
		copyOnSelect: false,
		// if `true` (without backticks and without quotes), hyper will be set as the default protocol client for SSH
		defaultSSHApp: true,
		// if `true` (without backticks and without quotes), on right click selected text will be copied or pasted if no
		// selection is present (`true` by default on Windows and disables the context menu feature)
		quickEdit: false,
		// choose either `'vertical'`, if you want the column mode when Option key is hold during selection (Default)
		// or `'force'`, if you want to force selection regardless of whether the terminal is in mouse events mode
		// (inside tmux or vim with mouse mode enabled for example).
		macOptionSelectionMode: 'vertical',
		// Whether to use the WebGL renderer. Set it to false to use canvas-based
		// rendering (slower, but supports transparent backgrounds)
		webGLRenderer: false,
		// keypress required for weblink activation: [ctrl|alt|meta|shift]
		// todo: does not pick up config changes automatically, need to restart terminal :/
		webLinksActivationKey: '',
		// if `false` (without backticks and without quotes), Hyper will use ligatures provided by some fonts
		disableLigatures: true,
		// set to true to disable auto updates
		disableAutoUpdates: false,
		// for advanced config flags please refer to https://hyper.is/#cfg,
		opacity: {
			focus: 0.9,
			blur: 0.5,
		},
		hyperMonokaiPro: {
			// theme: "pro" || "octagon" || "machine" || "ristretto" || "spectrum" || "classic"
			theme: 'classic',
		},
		activeTab: '🚀',
		hyperline: {
			plugins: ['ip', 'cpu'],
		},
		paneNavigation: {
			debug: false,
			hotkeys: {
				navigation: {
					up: 'ctrl+alt+up',
					down: 'ctrl+alt+down',
					left: 'ctrl+alt+left',
					right: 'ctrl+alt+right',
				},
				jump_prefix: 'ctrl+alt', // completed with 1-9 digits
				permutation_modifier: 'shift', // Added to jump and navigation hotkeys for pane permutation
				maximize: 'meta+enter',
			},
		},
	},
	// a list of plugins to fetch and install from npm
	// format: [@org/]project[#version]
	// examples:
	//   `hyperpower`
	//   `@company/project`
	//   `project#1.0.1`
	plugins: [
		'hyper-opacity',
		'hyper-monokai-pro',
		'hyper-pane',
		'hypercwd',
		'hyper-active-tab',
		'hyperline',
	],
	// in development, you can create a directory under
	// `~/.hyper_plugins/local/` and include it here
	// to load it and avoid it being `npm install`ed
	localPlugins: [],
	keymaps: {
		// Example
		// 'window:devtools': 'cmd+alt+o',
	},
};
//# sourceMappingURL=config-default.js.map
```

## .zshrc
```
eval "$(starship init zsh)"
source /Users/witold/.zsh/fast-syntax-highlighting/fast-syntax-highlighting.plugin.zsh
source /Users/witold/.zsh/completion.zsh
source /Users/witold/.zsh/zsh-autosuggestions/zsh-autosuggestions.zsh
source /Users/witold/.zsh/history.zsh
alias ls='ls -G'
source /Users/witold/.zsh/key-bindings.zsh
source /Users/witold/.zsh/aliases.zsh
```

## aliases.zsh
```
alias ls='ls -G'                              # colorize `ls` output
alias zshreload='source ~/.zshrc'             # reload ZSH
alias shtop='sudo htop'                       # run `htop` with root rights
alias grep='grep --color=auto'                # colorize `grep` output
alias ..='cd ..'
alias ...='cd ../..'
alias ....='cd ../../..'
alias less='less -R'
alias g='git'

alias rm='rm -i'                              # confirm removal
alias cp='cp -i'                              # confirm copy
alias mv='mv -i'                              # confirm move
alias cal='gcal --starting-day=1'             # print simple calendar for current month
alias weather='curl v2.wttr.in'               # print weather for current location (https://github.com/chubin/wttr.in)
```

## .gitconfig
```
[alias]
  a = add																		# Add file contents to the index
  ai = add --interactive										# Add modified contents in the working tree interactively to the index.
  ##############
  b = branch
  ba = branch --all                     		# List both remote-tracking branches and local branches.
  bav = branch --all --verbose 							# When in list mode, show sha1 and commit subject line for each head, along with relationship to upstream branch (if any)
  bd = branch --delete 											# Delete a branch. The branch must be fully merged in its upstream branch, or in HEAD if no upstream was set with --track or --set-upstream-to.
  bdd = branch -D 													# Shortcut for --delete --force.
  bm = branch --move												# Move/rename a branch and the corresponding reflog.
  bmm = branch -M 													# Shortcut for --move --force.
  br = branch --remotes 										# List or delete (if used with -d) the remote-tracking branches.
  ##############
  c = commit 																# Record changes to the repository
  ca = commit --all													# Tell the command to automatically stage files that have been modified and deleted, but new files you have not told Git about are not affected.
  cm = commit -m 														# Use the given <msg> as the commit message.
  cam = commit -am 													# Shortcut for --all and -m
  cem = commit --allow-empty -m							# Allows to create a commit without any files modified
  cd = commit --amend												# Replace the tip of the current branch by creating a new commit.
  cad = commit --all --amend								# Shortcut for --amend and --all
  cadne = commit --all --amend --no-edit		# Amends a commit without changing its commit message.
  ##############
  cl = clone 																# Clone a repository into a new directory
  cld = clone --depth 1											# Create a shallow clone with a history truncated to the specified number of commits.
  ##############
  cp = cherry-pick													# Apply the changes introduced by some existing commits
  cpa = cherry-pick --abort									# Cancel the operation and return to the pre-sequence state.
  cpc = cherry-pick --continue 							# Continue the operation in progress using the information in .git/sequencer. Can be used to continue after resolving conflicts in a failed cherry-pick or revert.
  cps = cherry-pick --skip 									# Skip the current commit and continue with the rest of the sequence.
  ##############
  d = diff																	# Show changes between commits, commit and working tree, etc
  di = !"d() { git diff --patch-with-stat HEAD~$1; }; git diff-index --quiet HEAD -- || clear; d" 	# `git di $number` shows the diff between the state `$number` revisions ago and the current state
  dt = difftool															# Show changes using common diff tools
  ##############
  f = fetch 																# Download objects and refs from another repository
  fo = fetch origin 												# Update the remote-tracking branches
  fu = fetch upstream												# Fetch the branches and their respective commits from the upstream repository.
  ##############
  fk = fsck 																# Verifies the connectivity and validity of the objects in the database
  ##############
  g = grep -p																# Print lines matching a pattern
  ##############
  l = log --oneline													# Show commit logs, the commit message is prefixed with this information on the same line.
  lg = log --oneline --graph --decorate			# Draw a text-based graphical representation of the commit history on the left hand side of the output.
  lgs = !"git log --pretty=format:"%C(yellow)%h\\ %ad%Cred%d\\ %Creset%s%Cblue\\ [%cn]" --decorate --date=short" 													# SHA + date + Commit message + author
  lgc = !"git log --pretty=format:"%C(yellow)%h%Cred%d\\ %Creset%s%Cblue\\ [%cn]" --decorate --numstat"																		# SHA + Commit message + author + changed files
  lgt = !"git log --graph --pretty='%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit --all" # As tree: SHA + Commit message + Time ago + author
  ##############
  ls = ls-files															# Show information about files in the index and the working tree
  lsm = ls-files --modified									# Show modified files in the output
  lss = ls-files --stage										# Show staged contents' mode bits, object name and stage number in the output.
  ##############
  m = merge 																# Join two or more development histories together
  ma = merge --abort												# Abort the current conflict resolution process, and try to reconstruct the pre-merge state.
  mc = merge --continue											# After a git merge stops due to conflicts you can conclude the merge by running git merge --continue
  mq = merge --quit													# Forget about the current merge in progress. Leave the index and the working tree as-is.
  mm = merge master 												# Merge 'master' branch to the current branch.
  ##############
  o = checkout 															# Switch branches or restore working tree files.
  om = checkout master											# Switch branch to master.
  ob = checkout -b 													# Create and switch to a new branch
  ##############
  pr = prune --verbose --progress						# Prune all unreachable objects from the object database. Report all removed objects. Show progress.
  prn = prune --dry-run											# Do not remove anything; just report what it would remove.
  ##############
  ps = push 																# Update remote refs along with associated objects
  psa = push --all 													# Push all branches (i.e. refs under refs/heads/); cannot be used with other <refspec>.
  psf = push --force												# Usually, the command refuses to update a remote ref that is not an ancestor of the local ref used to overwrite it. This flag disables these checks, and can cause the remote repository to lose commits; use it with care.
  psu = push --set-upstream									# For every branch that is up to date or successfully pushed, add upstream (tracking) reference.
  ##############
  pso = push origin													# `origin` is an alias in the system for a particular remote repository. Can be checked by running `git remote -v`.
  psao = push --all origin									# Same as `push --all` but for origin.
  psfo = push --force origin								# Same as `push --force` but for origin.
  psuo = push --set-upstream origin					# Same as `push --set-upstream` but for origin.
  #############
  psom = push origin master 								# Same as `push origin` but for master branch.
  psaom = push --all origin master					# Same as `push --all origin` but for master branch.
  psfom = push --force origin master				# Same as `push --force origin` but for master branch.
  psuom = push --set-upstream origin master # Same as `push --set-upstream origin` but for master branch.
  #############
  pl = pull 																# Fetch from and integrate with another repository or a local branch.
  plr = pull --rebase 											# When true, rebase the current branch on top of the upstream branch after fetching.
  plv = pull --verbose 											# Pass --verbose to git-fetch and git-merge.
  #############
  plo = pull origin 											  # Same as `pull` but for origin.
  plro = pull --rebase origin								# Same as `pull --rebase` but for origin.
  plom = pull origin master									# Same as `pull origin` but for master branch.
  #############
  plu = pull upstream												# Same as `pull` but for upstream.
  plum = pull upstream master								# Same as `pull upstream` but for master branch.
  plrum = pull --rebase upstream master    	# Same as `pull --rebase` but for upstream and master branch.
  #############
  rb = rebase																# Reapply commits on top of another base tip.
  rba = rebase --abort											# Abort the rebase operation and reset HEAD to the original branch.
  rbc = rebase --continue 									# Restart the rebasing process after having resolved a merge conflict.
  rbi = rebase --interactive                # Make a list of the commits which are about to be rebased. Let the user edit that list before rebasing. This mode can also be used to split commits.
  rbs = rebase --skip 											# Restart the rebasing process by skipping the current patch.
  rbin = "!r() { git rebase -i HEAD~$1; }; r" # Interactive rebase with the given number of latest commits.
  #############
  re = reset																# Reset current HEAD to the specified state
  rh = reset HEAD 													# HEAD is defined explicitly
  reh = reset --hard												# Resets the index and working tree. Any changes to tracked files in the working tree since <commit> are discarded.
  rem = reset --mixed												# Resets the index but not the working tree (i.e., the changed files are preserved but not marked for commit) and reports what has not been updated. This is the default action.
  res = reset --soft                        # Does not touch the index file or the working tree at all (but resets the head to <commit>, just like all modes do). This leaves all your changed files "Changes to be committed".
  rehh = reset --hard HEAD									# HEAD is defined explicitly
  remh = reset --mixed HEAD									# HEAD is defined explicitly
  resh = reset --soft HEAD									# HEAD is defined explicitly
  rehom = reset --hard origin/master				# Throw away all my staged and unstaged changes, forget everything on my current local branch and make it exactly the same as origin/master.
  #############
  r = remote																# Manage set of tracked repositories
  ra = remote add 													# Adds a remote named <name> for the repository at <url>.
  rr = remote remove												# Remove the remote named <name>. All remote-tracking branches and configuration settings for the remote are removed.
  rv = remote --verbose											# Be a little more verbose and show remote url after name.
  rn = remote rename												# Rename the remote named <old> to <new>. All remote-tracking branches and configuration settings for the remote are updated.
  rp = remote prune 												# Deletes stale references associated with <name>. By default, stale remote-tracking branches under <name> are deleted, but depending on global configuration and the configuration of the remote we might even prune local tags that haven't been pushed there.
  rs = remote show 													# Gives some information about the remote <name>.
  rao = remote add origin 									# Add new origin.
  rau = remote add upstream									# Add new upstream.
  rro = remote remove origin								# Remove origin.
  rru = remote remove upstream              # Remove upstream.
  rso = remote show origin									# Show current origin.
  rsu = remote show upstream								# Show current upstream.
  rpo = remote prune origin                 # Prune current origin.
  rpu = remote prune upstream								# Prune current upstream.
  #############
  rmf = rm -f																# Remove files from the working tree and from the index. Override the up-to-date check.
  rmrf = rm -r -f														# Same as above + Allow recursive removal when a leading directory name is given.
  #############
  s = status																# Show the working tree status
  sb = status -s -b													# Same as above + Give the output in the short-format. Show the branch and tracking info even in short-format.
  #############
  sa = stash apply													# Like pop, but do not remove the state from the stash list.
  sc = stash clear													# Remove all the stash entries. Note that those entries will then be subject to pruning, and may be impossible to recover.
  sd = stash drop														# Remove a single stash entry from the list of stash entries. When no <stash> is given, it removes the latest one.
  sl = stash list														# List the stash entries that you currently have.
  sp = stash pop														# Remove a single stashed state from the stash list and apply it on top of the current working tree state, i.e., do the inverse operation of git stash push.
  sps = stash push 													# Save your local modifications to a new stash entry and roll them back to HEAD (in the working tree and in the index). The <message> part is optional and gives the description along with the stashed state.
  spsk = stash push -k											# All changes already added to the index are left intact.
  sw = stash show														# Show the changes recorded in the stash entry as a diff between the stashed contents and the commit back when the stash entry was first created. When no <stash> is given, it shows the latest one.
  st = !git stash list | wc -l 2>/dev/null | grep -oEi '[0-9][0-9]*'
  #############
  t = tag																		# Create, list, delete or verify a tag object signed with GPG.
  td = tag --delete													# Delete existing tags with the given names.
  tl = tag --list														# Show verbose output about tags.
  #############
  w = show                                  # Show various types of objects.
  wo = show --oneline												# This is a shorthand for "--pretty=oneline --abbrev-commit" used together.
  wf = show --format=fuller									# Print more extensive info.
  #############
  aliases = !git config -l | grep alias | cut -c 7- # List git aliases
  branches = branch --all 									# List both remote-tracking branches and local branches.
  remotes = remote --verbose 								# Be a little more verbose and show remote url after name.
  contributors = shortlog --summary --numbered	# List contributors with number of commits
  amend = commit --amend --no-edit					# Amend the currently staged files to the latest commit.
  go = "!f() { git checkout -b \"$1\" 2> /dev/null || git checkout \"$1\"; }; f"	# Switch to a branch, creating it if necessary
  fb = "!f() { git branch -a --contains $1; }; f"																	# Find branches containing commit
  ft = "!f() { git describe --always --contains $1; }; f"													# Find tags containing commit
  fc = "!f() { git log --pretty=format:'%C(yellow)%h  %Cblue%ad  %Creset%s%Cgreen  [%cn] %Cred%d' --decorate --date=short -S$1; }; f"				# Find commits by source code
  fm = "!f() { git log --pretty=format:'%C(yellow)%h  %Cblue%ad  %Creset%s%Cgreen  [%cn] %Cred%d' --decorate --date=short --grep=$1; }; f" 	# Find commits by commit message
  dm = "!git branch --merged | grep -v '\\*' | xargs -n 1 git branch -d"	# Remove branches that have already been merged with master (a.k.a. ‘delete merged’)
```
