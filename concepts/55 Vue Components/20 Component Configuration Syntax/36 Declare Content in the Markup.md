The following UI components allow you to declare their content directly in the markup:

- [Drawer](/api-reference/10%20UI%20Components/dxDrawer '/Documentation/ApiReference/UI_Components/dxDrawer/')
- [DropDownBox](/api-reference/10%20UI%20Components/dxDropDownBox '/Documentation/ApiReference/UI_Components/dxDropDownBox/')
- [HtmlEditor](/api-reference/10%20UI%20Components/dxHtmlEditor '/Documentation/ApiReference/UI_Components/dxHtmlEditor/')
- [Popover](/api-reference/10%20UI%20Components/dxPopover '/Documentation/ApiReference/UI_Components/dxPopover/')
- [Popup](/api-reference/10%20UI%20Components/dxPopup '/Documentation/ApiReference/UI_Components/dxPopup/')
- [Resizable](/api-reference/10%20UI%20Components/dxResizable '/Documentation/ApiReference/UI_Components/dxResizable/')
- [ScrollView](/api-reference/10%20UI%20Components/dxScrollView '/Documentation/ApiReference/UI_Components/dxScrollView/')
- [Tooltip](/api-reference/10%20UI%20Components/dxTooltip '/Documentation/ApiReference/UI_Components/dxTooltip/')
- [ValidationGroup](/api-reference/10%20UI%20Components/dxValidationGroup '/Documentation/ApiReference/UI_Components/dxValidationGroup/')

The following is an example with ScrollView:

    <!-- tab: App.vue -->
    <template>
        <DxScrollView>
            <div>Some scrollable content</div>
        </DxScrollView>
    </template>

    <script>
    import DxScrollView from 'devextreme-vue/scroll-view';

    export default {
        components: {
            DxScrollView
        }
    }
    </script>

[important]

These UI components do not support dynamically or conditionally rendered content in their root element. For example, the following code **does not work**:

    <!-- tab: App.vue -->
    <template>
        <DxDrawer ... >
            <router-view></router-view>
        </DxDrawer>
    </template>

Wrap the content in a static element:

    <!-- tab: App.vue -->
    <template>
        <DxDrawer ... >
            <div>
                <router-view></router-view>
            </div>
        </DxDrawer>
    </template>

[/important]