# Java HarmonyOS API for Android developers - cheatsheet

## Basic Applications Elements

| Android       | HarmonyOS                   | Notes / Usage                                                                                                                                                                                                                                                                                                                                                                                     |
| ------------- | --------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `Application` | `AbilityPackage`            |                                                                                                                                                                                                                                                                                                                                                                                                   |
| `Activity`    | `Ability` (Page Ability)    | An ability is an abstraction of a functionality that an application can provide. Abilities are classified into Feature Abilities (FAs) and Particle Abilities (PAs). `Ability` class can be used similar to `Activity`, then it is FA and uses `Page` template. Docs: https://developer.harmonyos.com/en/docs/documentation/doc-guides/ability-page-concept-0000000000033573                      |
| `Fragment`    | `AbilitySlice`              | `AbilitySlice` represents a single screen and its control logic.                                                                                                                                                                                                                                                                                                                                  |
| `Service`     | `Ability` (Service Ability) | `Ability` class can be used similar to `Service`. Docs: https://developer.harmonyos.com/en/docs/documentation/doc-guides/ability-service-concept-0000000000044457                                                                                                                                                                                                                                 |
|               | `Ability` (Data Abilty)     | A Data ability helps applications manage access to data stored by themselves and other applications, and provides methods for sharing data with other applications. Data abilities can be used for data sharing between applications on the same device or across different devices. Docs: https://developer.harmonyos.com/en/docs/documentation/doc-guides/ability-data-concept-0000000000043058 |
| `Intent`      | `Intent`                    | Docs: https://developer.harmonyos.com/en/docs/documentation/doc-guides/ability-intent-0000000000038799                                                                                                                                                                                                                                                                                            |
| `Context`     | `Context`                   |                                                                                                                                                                                                                                                                                                                                                                                                   |

## UI Basics
Overview docs: https://developer.harmonyos.com/en/docs/documentation/doc-guides/ui-java-overview-0000000000500404
| Android                  | HarmonyOS                         |
| ------------------------ | --------------------------------- |
| `View`                   | `Component`                       |
| `ViewGroup`              | `ComponentContainer`              |
| `ViewGroup.LayoutParams` | `ComponentContainer.LayoutConfig` |

## Views / Components
| Android                                   | HarmonyOS                                    | Notes / Usage                                                                                                                                                                                                                          |
| ----------------------------------------- | -------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `TextView`                                | `TextView`                                   | https://developer.harmonyos.com/en/docs/documentation/doc-guides/ui-java-component-text-0000001050729534                                                                                                                               |
| `Button`                                  | `Button`                                     | https://developer.harmonyos.com/en/docs/documentation/doc-guides/ui-java-component-button-0000001051009585                                                                                                                             |
| `EditText`                                | `TextField`                                  | https://developer.harmonyos.com/en/docs/documentation/doc-guides/ui-java-component-textfield-0000001061125582                                                                                                                          |
| `ImageView`                               | `Image`                                      | https://developer.harmonyos.com/en/docs/documentation/doc-guides/ui-java-component-image-0000001058976860                                                                                                                              |
| `TabLayout` / `TabItem`                   | `TabList` / `Tab`                            | https://developer.harmonyos.com/en/docs/documentation/doc-guides/ui-java-component-tablist-tab-0000001062229749                                                                                                                        |
| `DatePickerDialog`                        | `DatePicker` (Component)                     | https://developer.harmonyos.com/en/docs/documentation/doc-guides/ui-java-component-datepicker-0000001060237839                                                                                                                         |
| `TimePickerDialog`                        | `TimePicker` (Component)                     | https://developer.harmonyos.com/en/docs/documentation/doc-guides/ui-java-component-timepicker-0000001060648140                                                                                                                         |
| `Switch`                                  | `Switch`                                     | https://developer.harmonyos.com/en/docs/documentation/doc-guides/ui-java-component-switch-0000001060806006                                                                                                                             |
| `RadioButton`                             | `RadioButton`                                | https://developer.harmonyos.com/en/docs/documentation/doc-guides/ui-java-component-radiobutton-0000001060647792                                                                                                                        |
| `RadioGroup`                              | `RadioContainer`                             | https://developer.harmonyos.com/en/docs/documentation/doc-guides/ui-java-component-radiocontainer-0000001063470429                                                                                                                     |
| `CheckBox`                                | `CheckBox`                                   | https://developer.harmonyos.com/en/docs/documentation/doc-guides/ui-java-component-checkbox-0000001060487804                                                                                                                           |
| `ProgressBar` / `LinearProgressIndicator` | `ProgressBar`                                | https://developer.harmonyos.com/en/docs/documentation/doc-guides/ui-java-component-progressbar-0000001060379891                                                                                                                        |
| `CircularProgressIndicator` (material)    | `RoundProgressBar`                           | https://developer.harmonyos.com/en/docs/documentation/doc-guides/ui-java-component-roundprogressbar-0000001062558057                                                                                                                   |
| `ScrollView`                              | `ScrollView`                                 | https://developer.harmonyos.com/en/docs/documentation/doc-guides/ui-java-component-scrollview-0000001060965602                                                                                                                         |
| `ListView` / `RecyclerView`               | `ListContiner` (works similar to `ListView`) | https://developer.harmonyos.com/en/docs/documentation/doc-guides/ui-java-component-listcontainer-0000001060007847                                                                                                                      |
| `ViewPager`                               | `PageSlider` (with `PageSliderIndicator`)    | https://developer.harmonyos.com/en/docs/documentation/doc-guides/ui-java-component-pageslider-0000001091933258 https://developer.harmonyos.com/en/docs/documentation/doc-guides/ui-java-component-pagesliderindicator-0000001091773342 |
| `WebView`                                 | `WebView`                                    | https://developer.harmonyos.com/en/docs/documentation/doc-guides/ui-java-component-webview-0000001092715158                                                                                                                            |

## Layouts / ViewGroups
| Android                               | HarmonyOS                                             | Notes / Usage                                                                                                      |
| ------------------------------------- | ----------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------ |
| `LinearLayout`                        | `DirectionaLayout`                                    | https://developer.harmonyos.com/en/docs/documentation/doc-guides/ui-java-layout-directionallayout-0000001050769565 |
| `RelativeLayout` / `ConstraintLayout` | `DependentLayout` (works similar to `RelativeLayout`) | https://developer.harmonyos.com/en/docs/documentation/doc-guides/ui-java-layout-dependentlayout-0000001050729536   |
| `FrameLayout`                         | `StackLayout`                                         | https://developer.harmonyos.com/en/docs/documentation/doc-guides/ui-java-layout-stacklayout-0000001060357540       |
| `GridLayout`                          | `TableLayout`                                         | https://developer.harmonyos.com/en/docs/documentation/doc-guides/ui-java-layout-tablelayout-0000001060379893       |
| `AbsoluteLayout`                      | `PositionLayout`                                      | https://developer.harmonyos.com/en/docs/documentation/doc-guides/ui-java-layout-positionlayout-0000001062250815    |
|                                       | `AdaptiveBoxLayout`                                   | https://developer.harmonyos.com/en/docs/documentation/doc-guides/ui-java-layout-adaptiveboxlayout-0000001104341118 |



## Dialogs, popups, toasts

| Android       | HarmonyOS      | Notes / Usage                                                                                                                                                         |
| ------------- | -------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `Toast`       | `ToastDialog`  | https://developer.harmonyos.com/en/docs/documentation/doc-guides/ui-java-component-toastdialog-0000001060125963                                                       |
| `PopupWindow` | `PopupDialog`  | `PopupDialog` can be attached to a `Component`. Docs: https://developer.harmonyos.com/en/docs/documentation/doc-guides/ui-java-component-popupdialog-0000001150714408 |
| `AlertDialog` | `CommonDialog` | https://developer.harmonyos.com/en/docs/documentation/doc-guides/ui-java-component-commondialog-0000001150874228                                                      |

## Custom Views / Components
Docs: https://developer.harmonyos.com/en/docs/documentation/doc-guides/ui-java-custom-component-layout-overview-0000001139508543
| Android          | HarmonyOS        | Notes / Usage                                                                                |
| ---------------- | ---------------- | -------------------------------------------------------------------------------------------- |
| `onMeasure`      | `onEstimateSize` |                                                                                              |
| `onLayout`       | `onArrange`      |                                                                                              |
| `AttributeSet`   | `AttrSet`        |                                                                                              |
| `onDraw`         | `onDraw`         |
| `LayoutInflater` | `LayoutScatter`  | `LayoutScatter.getInstance(context).parse(ResourceTable.Layout_title_bar, component, true);` |

## Lifecycle
### Application / AbilityPackage
| Android                                                               | HarmonyOS                |
| --------------------------------------------------------------------- | ------------------------ |
| `onCreate`                                                            | `onInitialize`           |
| `onTerminate`                                                         | `onEnd`                  |
| `onConfigurationChanged`                                              | `onConfigurationUpdated` |
| `onTrimMemory` / `onLowMemory`                                        | `onMemoryLevel`          |
| `registerActivityLifecycleCallbacks` / `registerComponentCallbacks`   | `registerCallbacks`      |
| `unregisterActivityLifecycleCallbacks` / `registerComponentCallbacks` | `unregisterCallbacks`    |

### Activity / Ability
Docs: https://developer.harmonyos.com/en/docs/documentation/doc-guides/ability-page-lifecycle-0000000000029840
| Android     | HarmonyOS      |
| ----------- | -------------- |
| `onCreate`  | `onStart`      |
| `onStart`   | ----           |
| `onResume`  | `onActive`     |
| `onPause`   | `onInactive`   |
| `onStop`    | `onBackground` |
| `onRestart` | `onForeground` |
| `onDestroy` | `onStop`       |

### Service / Ability
Docs: https://developer.harmonyos.com/en/docs/documentation/doc-guides/ability-service-creating-0000000000044464
| Android          | HarmonyOS   |
| ---------------- | ----------- |
| `onCreate`       | `onStart`   |
| `onStartCommand` | `onCommand` |
| `onBind`         | `onConnect` |
| `onDestroy`      | `onStop`    |

### Fragment / AbilitySlice
An ability slice's lifecycle is bound to the Page ability that hosts it. An ability slice has the same lifecycle states and lifecycle callbacks as its host Page ability. Once the lifecycle state of a Page ability changes, its ability slices undergo the same change. An ability slice can also have its own lifecycle state changes, which occur during the switching between the ability slices within the Page ability. Such a switching does not affect the host ability's lifecycle.

Docs: https://developer.harmonyos.com/en/docs/documentation/doc-guides/ability-page-lifecycle-0000000000029840

## XML Layouts
Docs: https://developer.harmonyos.com/en/docs/documentation/doc-guides/ui-java-component-layout-xml-0000000000500395
| Android                        | HarmonyOS             |
| ------------------------------ | --------------------- |
| `android:id="@+id/text"`       | `ohos:id="$+id:text"` |
| `android:layout_width="20dp"`  | `ohos:width="20vp"`   |
| `android:layout_height="20dp"` | `ohos:height="20vp"`  |
| `match_parent`                 | `match_parent`        |
| `wrap_content`                 | `match_content`       |

## AndroidManifest.xml / config.json
In HarmonyOS there is a config.json file instead of AndroidManifest.xml. Docs: https://developer.harmonyos.com/en/docs/documentation/doc-guides/basic-config-file-overview-0000000000011951

## Resources
All the application resource files, such as strings, images, and audio files, are stored in the resources directory, allowing you to easily access, use, and maintain them. The resources directory consists of two types of sub-directories: the `base` sub-directory and `qualifiers` sub-directories, and the `rawfile` sub-directory.

Example:
```
resources
|---base  // Default directory
|   |---element
|   |   |---string.json
|   |---media
|   |   |---icon.png
|---en_GB-vertical-car-mdpi // Example of a qualifiers sub-directory, which needs to be created on your own
|   |---element
|   |   |---string.json
|   |---media
|   |   |---icon.png
|---rawfile  // Default directory
```
Docs: https://developer.harmonyos.com/en/docs/documentation/doc-guides/basic-resource-file-categories-0000001052066099#EN-US_TOPIC_0000001062847941__table1324121514614

### Referencing Resource Files
Resource files are referenced in a Java file in the following format: `ResourceTable.type_name`. Specifically, a system resource is referenced using `ohos.global.systemres.ResourceTable.type_name`.

Resource files are referenced in an XML file in the following format: `$type:name`. Specifically, a system resource is referenced using `$ohos:type:name`.

Docs: https://developer.harmonyos.com/en/docs/documentation/doc-guides/basic-resource-file-example-0000001051733014

Examples:

| Android                                      | HarmonyOS                                                                 |
| -------------------------------------------- | ------------------------------------------------------------------------- |
| `findViewById(R.id.textView)`                | `findComponentById(ResourceTable.Id_textView)`                            |
| `setContentView(R.layout.activity_main)`     | `setUIContent(ResourceTable.Layout_ability_main)`                         |
| `<ImageView android:src="@drawable/plant"/>` | `<Image ohos:image_src="$media:plant" />`                                 |
| `getString(R.string.hello)`                  | `getResourceManager().getElement(ResourceTable.String_hello).getString()` |


## Permissiosns
Docs: https://developer.harmonyos.com/en/docs/documentation/doc-guides/security-permissions-overview-0000000000029883

- permissions are definied in `config.json`
- sensitive permissions must be dynamically requested with users' acknowledgement (https://developer.harmonyos.com/en/docs/documentation/doc-guides/security-permissions-guidelines-0000000000029886#section7431121314439)


| Android                             | HarmonyOS                                |
| ----------------------------------- | ---------------------------------------- |
| `checkSelfPermission(..)`           | `verifySelfPermission(..)`               |
| `requestPermissions(..)`            | `requestPermissionsFromUser(..)`         |
| `onRequestPermissionsResult(..)`    | `onRequestPermissionsFromUserResult(..)` |
| `PackageManager.PERMISSION_GRANTED` | `IBundleManager.PERMISSION_GRANTED`      |

## Contributing
If you think there could be more items in this cheatsheat please open an issue or a PR. Repository: https://github.com/burnoo/HarmonyOSAndroidCheatsheet/
