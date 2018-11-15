<!-- default file list -->
*Files to look at*:

* [MainWindow.xaml](./CS/WpfApplication20/MainWindow.xaml) (VB: [MainWindow.xaml](./VB/WpfApplication20/MainWindow.xaml))
<!-- default file list end -->
# How to: Merge Bars When They are Used in Standard Controls


<p>This example demonstrates the merging behavior of bars when they are used in controls that don't support automatic merging.</p>
The example creates a TabControl in which a Tab contains three MainMenuControls: <br>1) an empty menu called 'elementHost', <br>2) a menu with 'Cut', 'Copy' and 'Paste' commands, <br>3) a menu with 'Left', 'Center' and 'Right' commands.<br>The second and third MainMenuControls will be merged to the first MainMenuControl.<br><br>The merging feature is enabled with the <a href="https://documentation.devexpress.com/#wpf/DevExpressXpfBarsMergingProperties_ElementMergingBehaviortopic">ElementMergingBehavior</a> property attached to the Tab. This property is set to 'InternalWithInternal', which means that the Tab's internal elements are merged with other internal elements that are defined in parent name scopes. <br>The 'elementHost' MainMenuControl belongs to the name scope inherited from the Window object (a name scope is implicitly created for each Window object). The <a href="https://documentation.devexpress.com/#wpf/DevExpressXpfBarsBarNameScope_IsScopeOwnertopic">IsScopeOwner</a> properties set for the second and third MainMenuControls define child name scopes. Thus, these MainMenuControls will be merged to the 'elementHost' MainMenuControl (defined in the parent name scope).<br><br><strong>Note:</strong><br>If you want to merge the Tab's second and third MainMenuControls to the Window's topmost MainMenuControl (the one that contains 'File', 'Settings' and 'Exit' commands), replace the Tab's property setting:<br>dxb:MergingProperties.ElementMergingBehavior="InternalWithInternal"<br>with:<br>dxb:MergingProperties.ElementMergingBehavior="InternalWithExternal"<br><br>

<br/>


