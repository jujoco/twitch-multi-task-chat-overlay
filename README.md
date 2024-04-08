# Twitch Multi-Task Chat Bot

<img src="./demo/preview.png" width="530" height="660">

## Why you should use this

- Free to use
- Easy setup & use
- Easy to customize
- Customizable Multi-language support
- No third-party database required

## **APP Features ✨**

- User features
  - user can create multiple tasks
  - user can edit current tasks
  - user can mark tasks as complete
  - user can delete previous tasks
- Faster performance & smaller file sizes
- Supports multiple languages translations
  - EN - English
  - ES - Español
  - FR - française
  - JP - 日本語

## Content

- [Installation](#installation)
- [Commands](#commands)
  - [Moderators only](#moderators-only)
- [Customization settings](#customization-settings)
  - [settings](#settings)
  - [fonts](#fonts)
  - [scroll](#scroll)
  - [task list](#task-list)
  - [header](#header)
  - [body](#body)
  - [task (individual tasks)](#task-individual-tasks)
  - [checkbox](#checkbox)
  - [bullet point](#bullet-point)
  - [colon](#colon)
- [Aliases](#aliases)
- [Credits](#credits)

## Installation

1. Get auth token from https://twitchapps.com/tmi
2. Copy the token
3. Put it in auth.js, like so:

```js
const oauth = "oauth:1a2b3c4d5e6f7g8h9i1j2k3l";
```

4. Fill in your channel name:

```js
const channel = "JujocoCS";
const username = "YOUR_BOT_ACCOUNT_HERE";
```

5. Fill in the bot username, or your channel's username, depending on which account you authorized in https://twitchapps.com/tmi. In most cases it is the same as your channel name.

```js
const channel = "JujocoCS";
const username = "JujocoCS";
const oauth = "oauth:1a2b3c4d5e6f7g8h9i1j2k3l";
```

6. Add & Setup a `Browser Source` in OBS studio or other streaming software with the local file source pointing to `index.html`

## Commands

### Common

- !taskadd \<task\> , \<task\> - Add a task or multiple tasks by comma separated
- !taskedit \<number\> \<newTask\> - Edit a single task
- !taskdone \<number\> - Mark a single task as done
- !taskdelete \<number\> - Delete a single task
- !taskcheck - Check your unfinished tasks

### Moderators only

- !adminclearall - Clear all tasks
- !admincleardone - Clear all done tasks
- !adminclearuser \<username\> - Remove all tasks from a user

For aliases, see [here](#aliases)

## Customization settings

### Behavior Settings

Open the `configs.js` to edit the behavior of the Task List

`crossTasksOnDone`: default **true**

- **true**: cross the tasks when they are marked as done
- **false**: don't cross the tasks when they are marked as done

`languageCode`: default **EN**

- **EN**: English translation
- **ES**: Spanish translation
- **FR**: French translation
- **JP**: Japanese translation

`maxTasksPerUser`: default **5**

- **number**: A value between 1 - 10.

`scrollSpeed`: default **40**

- **number**: A value between 1 - 100.

`testMode`: default **false**

- **false**: turn OFF test mode.
- **true**: turn ON test mode.

### Styles Settings

Open the `base.css` to edit the styles of the Task List

### Fonts Styles

Font family for the Header & Body \(supports all fonts from [Google Fonts](https://fonts.google.com/)\)

```css
/* fonts available @ https://fonts.google.com */
--header-font-family: Roboto Mono;
--card-font-family: Roboto Mono;
```

### App Styles

```css
/* App Styles */
--app-border-radius: 5px;
--app-padding: 8px;
--app-bg-image: url(../public/transparent-background.png);
--app-background-color: rgb(183, 183, 183, 0);
```

### Header Styles

```css
/* Header */
--header-border-radius: 5px;
--header-margin-bottom: 10px;
--header-background-color: rgba(0, 0, 0, 0.8);
--header-font-size: 24px;
--header-font-color: white;
--header-font-weight: lighter;
```

### Body Styles

```css
/* Body */
--body-background-color: rgba(0, 77, 0, 0);
```

### Card Styles (individual cards)

```css
/* Card */
--card-gap-between: 10px;
--card-border-radius: 5px;
--card-background-color: rgba(0, 0, 0, 0.8);

/* User Name */
--username-font-size: 22px;
--username-color: #ffffff;
--username-font-weight: lighter;

/* User Task */
--task-font-size: 18px;
--task-font-color: #ffffff;
--task-font-weight: lighter;
--task-done-font-color: #2e2e2e;
```

## Aliases

### User Commands

**add task commands:** \(add a task\)

- `!addtask`
- `!add`
- `!task`
- `!taska`
- `!taskadd`
- `!atask`
- `!todo`

**edit task commands:** \(edit a task\)

- `!edit`
- `!taskedit`
- `!edittask`
- `!taske`
- `!etask`

**finish task commands:** \(mark a task as done\)

- `!done`
- `!donetask`
- `!taskdone`

**delete task commands:** \(delete a task\)

- `!delete`
- `!taskdelete`
- `!deletetask`
- `!taskdel`
- `!deltask`

**check commands:** \(check last task of yourself or user\)

- `!check`
- `!checktask`
- `!taskcheck`
- `!mytask`

**help commands:** \(show help commands\)

- `!help`
- `!taskhelp`
- `!helptask`

### Admin Commands

**admin clear User commands:** \(clear all tasks from a user\) \(mods only\)

- `!adminclearuser`

**admin clear done commands:** \(clear all done tasks from list\) \(mods only\)

- `!admincleardone`

**admin clear all commands:** \(clear all tasks from list\) \(mods only\)

- `!adminclearall`

## Credits

**Author:** [**@JujocoCS**](https://twitch.tv/JujocoCS)

**Inspired by:** [**@RythonDev**](https://twitch.tv/RythonDev) & [**@MohFocus**](https://twitch.tv/MohFocus)
