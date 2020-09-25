# GUI

# **Table of contents**

[⚒️ Design Structures](#design-structures)

1. [Sketch file structures](#sketch-file-structures)

2. [How to naming artboard/symbols (Name convention)](#name-convention)

	2.1 [Artboard name](#artboard-name)
	
	2.2 [Symbol name](#symbol-name)
	
	2.3 [Example name conventions](#example-name-conventions)
	
3. [Design system structures](#design-system-structures)

	3.1 [Library structures](#library-structures)
	
	3.2 [Symbol structures](#symbol-structures)
	
	3.3 [Text styles](#text-structures)
	
4. [Make components by features](#make-components-by-features)

5. [Deprecated components](#deprecated-components)

6. [Error state](#error-state)

7. [Google sheet wording (i18N)](#i18n)

	7.1 [Naming ID](#naming-id)
	
[🚛 Deliver](#deliver)

1. [Export screens to Zeplin](#export-screens-to-zeplin)

2. [Link flow with Overflow.io](#link-flow-with-overflow)

3. [Create wording ID with Google Sheet (i18N)](#create-wording-id)


# <a name="design-structures"></a> **⚒️ Design Structures**

## <a name="sketch-file-structures"></a> **1. Sketch file structures**

```
[Project Folder]
  ├─ <feature_1>.sketch
  ├─ <feature_2>.sketch
  ├─ ...
  └─ <project_name> Library.sketch ✱✱

```
## <a name="name-convention"></a> **2. How to naming artboards/symbols (Name convention)**

### <a name="artboard-name"></a> **2.1 Artboard name**

`Platform/Feature/Feature — State`

**[Example]**

> Mobile/Register/Register — Ideal
> 
> Desktop/Register/Cancel dialog

| State | Description |
| --- | --- |
| Ideal | All fields filled state |
| Empty |All fields empty state |
| Loading |Components loading state |
| Error |All fields error state |

### <a name="symbol-name"></a> **2.2 Symbol name**

Group of symbol name is always plural and capital name.

**[Example]**

> Icons/…Assets/…Icons/Black/…

Symbol names are written in [snake_case](https://en.wikipedia.org/wiki/Snake_case).

`type_subtype_state`

**[Example]**

> Icons/Black/ic_email
> 
> Buttons/Default/btn\_default\_enabled
> 
> Buttons/Outline/btn_outline\_pressed

### <a name="example-name-conventions"></a> **2.3 Example name conventions**

Naming conventions for symbol type:

| Asset Type | Prefix | Example |
| --- | --- | --- |
| Toolbar | tb_ | tb_default |
| Button | btn_ | btn\_send\_password |
| Dialog | tb_ | tb_default |
| Divider | divider_ | divider_horizontal |
| Icon | ic_ | ic_star |
| Menu | menu_ | menu\_submenu\_bg |
| Notification | noti_ | noti_bg |
| Tabs | tab_ | tab_pressed |

Naming conventions for icons:

| Asset Type | Prefix | Example |
| --- | --- | --- |
| Icons | ic_ | Icons/_Icons/ic\_star |
| Launcher icons | ic_launcher | Icons/_Icons/ic\_launcher\_calendar |
| Menu icons and action bar icons | ic_menu | Icons/_Icons/ic\_menu\_archive |
| Status bar icons | ic\_stat_notify | Icons/_Icons/ic\_stat\_notify\_msg |
| Tab icons | ic_tab | Icons/_Icons/ic\_tab\_recent |
| Dialog icons | ic_dialog | Icons/_Icons/ic\_dialog\_info |

Naming conventions for selector states:

| Asset Type | Prefix | Example |
| --- | --- | --- |
| Normal | \_normal | Buttons/Default/btn\_order\_normal |
| Pressed | \_pressed | Buttons/Default/btn\_order\_pressed |
| Focused | \_focused | Buttons/Default/btn\_order\_focused |
| Disabled | \_disabled | Buttons/Default/btn\_order\_disabled |
| Selected | \_selected | Buttons/Default/btn\_order\_selected |

## <a name="design-system-structures"></a> **3. Design system structures**

### <a name="library-structures"></a> **3.1 Library structures**

```
[Library.sketch]
 ├─ Components ➡ Overview of Colors/Typepography/All components
 ├─ Preview ➡ Google search result/Preview link
 ├─ Typography 
 ├─ Icons & Logos ➡ Including Launcher/fav.ico
 ├─ Colors
 ├─ Symbols
 └─ Deprecated Symbols
```

**Reuse components concept** is very important to us because:

1. Team can control components in one direction. ✱✱
2. Easy to use just a few click.
3. Easy to control design system with developer.

### <a name="symbol-structures"></a> **3.2 Symbol structures**

```
[Symbols]
 ├─ ✱ ➡ config of project
 │  ├─ Colors
 │  ├─ CURSOR
 │  ├─ STATE OVERLAY
 │  └─ ...
 ├─ App
 ├─ Assets
 ├─ Background
 ├─ Buttons
 ├─ Dialog
 ├─ Divider
 ├─ Footer
 ├─ Icons
 ├─ Logos
 ├─ Text Field
 ├─  ...
```

### <a name="text-styles"></a> **3.3 Text styles**

```
EN/TH/CN/...
├─ Primary
│  └─ ...
│     ├─ Center
│     ├─ Left
│     └─ Right
│  ...
└─ Secondary
   └─ ...
      ├─ Center
      ├─ Left
      └─ Right
```

## <a name="make-components-by-features"></a> **4. Make components by features**

We split component into **common components** and **feature components** when project is large. For example:

`🚀 Features/...`

![https://i.imgur.com/RCiGFNI.png](https://i.imgur.com/RCiGFNI.png)

## <a name="deprecated-components"></a> **5. Deprecated components**

When you want to update **the new version of components, you have to move your old components to:**

```
[Library.sketch]
 ├─ ...
 └─ Deprecated Symbols
```

and change the name to `_Deprecated/...`

**[Example]**

> Text Field/Outline/…↓_Deprecated/Text Field/Outline/…

## <a name="error-state"></a> **6. Error state**

Don’t forget to **create all error state** from every user-generated content by linking with i18N sheet example:

- Type form
- Upload files / images
- Q&A
- Feedback / Review
- And more…

![https://i.imgur.com/LkcrBye.png](https://i.imgur.com/LkcrBye.png)

## <a name="i18n"></a> **7. Google sheet wording (i18N)**

*Example:* [https://docs.google.com/spreadsheets/d/17sWoWSdgTzINACFAgvD6t7i\_8NWMSA8b23YrwEp\_Awo/](https://docs.google.com/spreadsheets/d/17sWoWSdgTzINACFAgvD6t7i_8NWMSA8b23YrwEp_Awo/)

### <a name="naming-id"></a> **7.1 Naming ID**

1. Common wording (for reuse ID)

| ID | EN | TH |
| --- | --- | --- |
| ok | OK | ตกลง |
| cancel | Cancel | ยกเลิก |
| error_empty | This field cannot be empty. | กรุณากรอกข้อมูล |
| error\_empty_select | Please select information. | กรุณาเลือกข้อมูล |
| error_format | Incorrect format. | รูปแบบข้อมูลไม่ถูกต้อง |

2. Fix wording → feature_wording

| ID | EN | TH |
| --- | --- | --- |
| home\_how\_to\_use | How to use? | วิธีการใช้งาน |

3. Error wording → feature\_error\_component\_case

| ID | Common ID | EN | TH |
| --- | --- | --- | --- |
| register\_error\_emai\_empty | error_empty | This field cannot be empty. | กรุณากรอกข้อมูล |
| register\_error\_emai\_format | error_format | Incorrect format. | กรุณากรอกข้อมูล |

# <a name="deliver"></a> **🚛 Deliver**

### <a name="export-screens-to-zeplin"></a> **1. Export screens to Zeplin**

1. Upload screens and categorize into features
![https://github.com/THE-EXISTING/GUI/blob/master/Assets/Images/export1.png?raw=true](https://github.com/THE-EXISTING/GUI/blob/master/Assets/Images/export1.png?raw=true)

2. Upload all assets (icons, logos, images)
![https://github.com/THE-EXISTING/GUI/blob/master/Assets/Images/export2.png?raw=true](https://github.com/THE-EXISTING/GUI/blob/master/Assets/Images/export2.png?raw=true)

3. Update style guides (colors, text styles)
![https://github.com/THE-EXISTING/GUI/blob/master/Assets/Images/export3.png?raw=true](https://github.com/THE-EXISTING/GUI/blob/master/Assets/Images/export3.png?raw=true)

4. Upload project documentation (optional)

5. Define states and features into [tags](https://blog.zeplin.io/organizing-screens-in-zeplin-with-tags-128dc3ed0749) (optional)
![https://github.com/THE-EXISTING/GUI/blob/master/Assets/Images/export5.png?raw=true](https://github.com/THE-EXISTING/GUI/blob/master/Assets/Images/export5.png?raw=true)

Using tags is easy for screen types, states, and features sorting.

### <a name="link-flow-with-overflow"></a> **2. Link flow with [Overflow.io](http://overflow.io/)**

### <a name="create-wording-id"></a> **3. Create wording ID with Google Sheet (i18N)**

## Funding

You can also support this project by becoming a sponsor. Your logo will show up here with a link to your website.


### Sponsors

<img src="https://opencollective.com/gui-ui-guideline/tiers/sponsor/badge.svg?label=sponsor&color=brightgreen" />

<a href="https://opencollective.com/gui-ui-guideline#support" target="_blank">
  <img src="https://opencollective.com/gui-ui-guideline/tiers/sponsor.svg?width=890"/>
</a>

### Backers

Thank you to all our backers! 🙏

<img src="https://opencollective.com/gui-ui-guideline/tiers/backer/badge.svg?label=backer&color=brightgreen" />


<a href="https://opencollective.com/mockk#backers" target="_blank">
  <img src="https://opencollective.com/gui-ui-guideline/tiers/backer.svg?width=890"/>
</a>

### Contributors

_coming soon..._

> Please shoot 100+⭐️ to show this section.


## Getting Help

To ask questions, please use 👇🏻 or Follow our <a href="https://www.facebook.com/TheExistingCompany" target="_blank">Facebook page</a>.

<a href="https://m.me/TheExistingCompany?ref=w12969068" target="_blank"><img src="Assets/btn_start_conversation.png" width="270"  /></a>


To report bugs, please use the GitHub project.

* Reporting Bugs: [https://github.com/THE-EXISTING/GUI/issues](https://github.com/THE-EXISTING/GUI/issues)
