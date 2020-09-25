# GUI

**Table of contents**

# **⚒️ Design Structure**

## **1. Sketch file structure**

```
[Project Folder]
  ├─ <feature_1>.sketch
  ├─ <feature_2>.sketch
  ├─ ...
  └─ <project_name> Library.sketch ✱✱

```
## **2. How to naming artboard/symbols (Name convention)**

### **2.1 Artboard name**

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

### **2.2 Symbol name**

Group of symbol name is always plural and capital name.

> Icons/…Assets/…Icons/Black/…

Symbol names are written in [snake_case](https://en.wikipedia.org/wiki/Snake_case).

`type_subtype_state`

> Icons/Black/ic_email
> 
> Buttons/Default/btn_default_enabled
> 
> Buttons/Outline/btn_outline_pressed

### **2.3 Example name conventions**

Naming conventions for symbol type:

| Asset Type | Prefix | Example |
| --- | --- | --- |
| Toolbar | tb_ | tb_default |
| Button | btn_ | btn\_send_password |
| Dialog | tb_ | tb_default |
| Divider | divider_ | divider_horizontal |
| Icon | ic_ | ic_star |
| Menu | menu_ | menu\_submenu_bg |
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
| Normal | _normal | Buttons/Default/btn\_order\_normal |
| Pressed | \_pressed | Buttons/Default/btn\_order\_pressed |
| Focused | \_focused | Buttons/Default/btn\_order\_focused |
| Disabled | \_disabled | Buttons/Default/btn\_order\_disabled |
| Selected | \_selected | Buttons/Default/btn\_order\_selected |

## **3. Design system structure**

### **3.1 Library structure**

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

### **3.2 Symbol structure**

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

### **3.3 Text style**

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

## **4. Make components by features**

We split component into **common components** and **feature components** when project is big for example:

`🚀 Features/...`

![https://i.imgur.com/RCiGFNI.png](https://i.imgur.com/RCiGFNI.png)

## **5. Deprecated components**

When you want to update **the new version of components, you have to move your old components to:**

```
[Library.sketch]
 ├─ ...
 └─ Deprecated Symbols
```

and change the name to `_Deprecated/...`

**[Example]**

> Text Field/Outline/…↓_Deprecated/Text Field/Outline/…

## **6. Error state**

Don’t forget to **create all error state** from every user-generated content by linking with i18N sheet example:

- Type form
- Upload files / images
- Q&A
- Feedback / Review
- And more…

![https://i.imgur.com/LkcrBye.png](https://i.imgur.com/LkcrBye.png)

## **7. Google sheet wording (i18N)**

*Example:* [https://docs.google.com/spreadsheets/d/17sWoWSdgTzINACFAgvD6t7i_8NWMSA8b23YrwEp_Awo/](https://docs.google.com/spreadsheets/d/17sWoWSdgTzINACFAgvD6t7i_8NWMSA8b23YrwEp_Awo/)

### **7.1 Naming ID**

1. Common wording (for reuse ID)

| ID | EN | TH |
| --- | --- | --- |
| ok | OK | ตกลง |
| cancel | Cancel | ยกเลิก |
| error_empty | This field cannot be empty. | กรุณากรอกข้อมูล |
| error_empty_select | Please select information. | กรุณาเลือกข้อมูล |
| error_format | Incorrect format. | รูปแบบข้อมูลไม่ถูกต้อง |

2. Fix wording → feature_wording
| ID | EN | TH |
| --- | --- | --- |
| home_how_to_use | How to use? | วิธีการใช้งาน |

3. Error wording → feature_error_component_case

| ID | Common ID | EN | TH |
| --- | --- | --- | --- |
| register\_error\_emai\_empty | error_empty | This field cannot be empty. | กรุณากรอกข้อมูล |
| register\_error\_emai\_format | error_format | Incorrect format. | กรุณากรอกข้อมูล |

# **🚛 Deliver**

### **1. Export screens to Zeplin**

### **1. Export screens to Zeplin**

1. Upload screens and categorize into features

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/453c5c96-3b2c-411c-8509-2e9e11e248a1/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/453c5c96-3b2c-411c-8509-2e9e11e248a1/Untitled.png)

2. Upload all assets (icons, logos, images)

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/0a99160f-463a-4d53-9109-1f38e2152003/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/0a99160f-463a-4d53-9109-1f38e2152003/Untitled.png)

3. Update style guides (colors, text styles)

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/eeb39bcc-2d22-4bb6-ab65-159ac12e8ac4/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/eeb39bcc-2d22-4bb6-ab65-159ac12e8ac4/Untitled.png)

4. Upload project documentation (optional)

5. Define states and features into [tags](https://blog.zeplin.io/organizing-screens-in-zeplin-with-tags-128dc3ed0749) (optional)

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/0e409b20-8d0b-4487-9091-b42cc44e4bf0/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/0e409b20-8d0b-4487-9091-b42cc44e4bf0/Untitled.png)

Using tags is easy for screen types, states, and features sorting.

### **2. Link flow with [Overflow.io](http://overflow.io/)**

### **3. Create wording ID with Google Sheet (i18N)**

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

_comming soon..._

> Please shoot 100+⭐️ to show this section.


## Getting Help

To ask questions, please use 👇🏻 or Follow our <a href="https://www.facebook.com/TheExistingCompany" target="_blank">Facebook page</a>.

<a href="https://m.me/TheExistingCompany?ref=w12969068" target="_blank"><img src="Assets/btn_start_conversation.png" width="270"  /></a>


To report bugs, please use the GitHub project.

* Reporting Bugs: [https://github.com/THE-EXISTING/GUI/issues](https://github.com/THE-EXISTING/GUI/issues)
