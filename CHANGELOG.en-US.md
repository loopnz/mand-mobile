---
title: Change Log
toc: hidden
---

### 2.3.1

`2019-06-22`

- Feature
  - `NumberKeyboard` adds property `isHideConfirm`, used to control whether the confirmation button click action automatically hides the keyboard[#474](https://github.com/didi/mand-mobile/issues/474)
  - `NumberKeyboard` add default slot

- Fix
  - fix 'Slider` progress bar width calculation error[#472](https://github.com/didi/mand-mobile/issues/472)
  - fix the problem that the `NumberKeyboard` keys may be clicked incorrectly[#477](https://github.com/didi/mand-mobile/issues/477)
  
### 2.3.0

`2019-06-13`

- Feature
  - `Check` and `CheckList` increase the icon size, location and other related configuration properties[#383](https://github.com/didi/mand-mobile/issues/383)
  - `CheckList` slot adds `index`, `selected` field

  ```html
    <template>
      <md-check-list :options="data">
        <template slot-scope="{ option, index, selected }">
          <!-- xxx -->
        </template>
      </md-check-list>
    </template>
  ```

  - `RadioList` slot adds `index`, `selected` fields, and does not display icons when `icon` is empty
  - `Selector` adds property `multi` to support multiple selections[#296](https://github.com/didi/mand-mobile/issues/296)
  - `Toast` adds the attribute `component`, which is used and customized in component form[#445](https://github.com/didi/mand-mobile/issues/445)
  - ScrollView` adds property `is-prevent` to support setting whether to prevent the default behavior when scrolling in non-scrollable areas[#454](https://github.com/didi/mand-mobile/issues/454)

- Fix
  - Fix autoplay invalidation when `Swiper` property isLoop is true[#452](https://github.com/didi/mand-mobile/issues/452)
  - Fix error caused by closing dialog, when `Dialog` property `maskClosable` is true[#471](https://github.com/didi/mand-mobile/issues/471)
  
### 2.2.4

`2019-05-26`

- Fix
  - Fix the problem that the first and last items of `TabBar` cannot be automatically repaired after they are selected[#434](https://github.com/didi/mand-mobile/issues/434)
  - Texts of `TabBar` items cannot be selected
  
### 2.2.3

`2019-05-25`

- Fix
  - Utility style `hairline` replaces `width` and `height` with `border`
  
### 2.2.2

`2019-05-11`

- Feature
  - `TabPicker`add event `select`[#436](https://github.com/didi/mand-mobile/issues/436)

- Fix
  - When the option in the tab list of each level of `TabPicker` is selected, the internal container is reset to the top
  - `RadioList` automatically clears the filled out text box when switching to a non-text option
  - `DatePicker` prop `custom-types` support `HH`[#433](https://github.com/didi/mand-mobile/issues/433)
  - Add `onCancel` to the type declaration of `Dialog`
  - Optimize some components documentation
  
### 2.2.1

`2019-04-22`

- Feature
  - `Stepper` add slots `unreached`、`icon`[#405](https://github.com/didi/mand-mobile/issues/405)
  - `InputItem` add prop `solid`, used to set the title with unfixed width[#411](https://github.com/didi/mand-mobile/issues/411)
  - `Ruler` add props `stepTextPosition`、`stepTextRender`

- Fix
  - Fix the exception thrown by `Picker` when setting a wrong `default-index`[#416](https://github.com/didi/mand-mobile/issues/416)
  - Optimize some component styles
  
### 2.2.0

`2019-04-13`

- Feature
  - New `Ruler` Component
  - `ScrollViewRefresh` add prop `rollerColor`, used to set the progress bar color of pull-down refreshing[#399](https://github.com/didi/mand-mobile/issues/399)
  - Optimize `WaterMark` component by using `canvas` to render watermark
  - `Stepper` add `increase`, `decrease` events

- Fix
  - `Swiper` incorrect index jumping with method `goto`[#366](https://github.com/didi/mand-mobile/issues/366)
  - `Progress` hide inner circle when value is `0`[#381](https://github.com/didi/mand-mobile/issues/381)

### 2.1.7

`2019-03-22`

- Fix
  - `InputItem` not update when slots change
  - `Codebox` bottom border not shown on some devices

### 2.1.6

`2019-03-15`

- Fix
  - `Swiper` not destroy properly[#338](https://github.com/didi/mand-mobile/issues/338)
  - `InputItem` support string type `virtual-keyboard-vm` prop[#355](https://github.com/didi/mand-mobile/issues/355)

### 2.1.4

`2019-03-08`

- Feature
  - Optimize `Swiper` gestures

- Fix
  - Some build bugs
  - `ScrollView` move out screen not trigger scroll end action
  - `Popup` synchronously operate problem[#341](https://github.com/didi/mand-mobile/issues/341)

### 2.1.2

`2019-02-25`

- Fix
  - Fix `ScrollView` is not able to trigger the problem when the content is not full.[#335](https://github.com/didi/mand-mobile/issues/335)
  - Fixed a problem with the line break when the `InputItem` title floated

### 2.1.1

`2019-02-23`

- Fix
  - Fix the problem that `postcss` is not in effect at build time, causing assets such as images in `mand-mobile.css` not to be processed by url inline。

### 2.1.0

`2019-02-22`

- Feature
  - `Seletor`: `defaultValue` prop remove type limits[#305](https://github.com/didi/mand-mobile/issues/305)
  - `ScrollView`: add `immediateCheckEndReaching` prop，in order to check reach bottom immediately and emit `endReached` event[#312](https://github.com/didi/mand-mobile/issues/312)
  - `Picker` and `DatePicker`: add `lineHeight` prop, which is used to customize option line height[#323](https://github.com/didi/mand-mobile/issues/323)
  - `ScrollView`: add `touchAngle` prop, in order to control scroll angle[#326](https://github.com/didi/mand-mobile/issues/326)
  - `Amount`: use system default font

- Fix
  - Update type declaration
  - `WaterMark`: fix can not click content area[#304](https://github.com/didi/mand-mobile/issues/304)
  - `Swiper`: fix when set `isLoop` as `false` and `transition` as `slideY`, can not scroll problem[#311](https://github.com/didi/mand-mobile/issues/311)
  - `TabPicker`: fix scroll and click bug[#319](https://github.com/didi/mand-mobile/issues/319)
  - `InputItem`: fix wrong cursor position[#322](https://github.com/didi/mand-mobile/issues/322)
  - `InputItem`: fix bug at `Vue 2.6+`[#324](https://github.com/didi/mand-mobile/issues/324)
  - Update docs

### 2.0.0

`2019-01-30`

- Feature
  - `DetailItem` increase supported types of `content`[#285](https://github.com/didi/mand-mobile/issues/285)
  - `Dialog` add default value `true` of `preventScroll`[#286](https://github.com/didi/mand-mobile/issues/286)
  - `Radio` increase supported types of `value`[#289](https://github.com/didi/mand-mobile/issues/289)
  - `Icon` font type increases without prefix class name[#295](https://github.com/didi/mand-mobile/issues/295)
  - `Check`，`CheckBox`increase supported types of `name` and `value`[#297](https://github.com/didi/mand-mobile/issues/297)
  - `InputItem` add prop `virtual-keyboard-vm`, used to support external custom financial keyboards
  - `Cashier` add scoped slot `footer` and `channels` add property `img`

- Fix
  - `InputItem` remove setting cursor for native type [#268](https://github.com/didi/mand-mobile/issues/268)
  - supplement `index.d.ts`
  - fix part of components style issues

### 2.0.0-rc.5

`2019-01-04`

- Feature
  - Add `PascalCase` name to global components[#261](https://github.com/didi/mand-mobile/issues/261)
  - `ScrollView` add prop `manual-init` and method `init`
  - `TabBar`, `Tabs` add prop `immediate`
  - `Swiper` add prop `transition-duration`

- Fix
  - fix part of components style issues

### 2.0.0-rc.4

`2018-12-21`

- Feature
  - Optimize `NumberKeyboard` input experience
  - `Cashier` adds slot `scene`
  - `Picker` adds prop `default-value`[#255](https://github.com/didi/mand-mobile/issues/255)

- Fix
  - Fix `Popup` continuous "show & hide" invalidation problem
  - Fix `Steps` style compatibility issues
  - Fix `InputItem` style problem, increase close button click area
  - `setError` of `Captcha` no longer clears codes

### 2.0.0-rc.3

`2018-12-14`

🎉🎉🎉 👏👏👏 Learn more in the<a href="#/en-US/docs/migration">Migration from 1.x</a>.

### 1.x

Visit [GitHub](https://github.com/didi/mand-mobile/blob/1.x/CHANGELOG.en-US.md) to read `1.x` change logs.

