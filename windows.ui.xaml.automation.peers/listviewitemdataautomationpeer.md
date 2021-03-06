---
-api-id: T:Windows.UI.Xaml.Automation.Peers.ListViewItemDataAutomationPeer
-api-type: winrt class
---

<!-- Class syntax.
public class ListViewItemDataAutomationPeer : Windows.UI.Xaml.Automation.Peers.SelectorItemAutomationPeer, Windows.UI.Xaml.Automation.Peers.IListViewItemDataAutomationPeer, Windows.UI.Xaml.Automation.Provider.IScrollItemProvider
-->

# Windows.UI.Xaml.Automation.Peers.ListViewItemDataAutomationPeer

## -description
Exposes [ListView](../windows.ui.xaml.controls/listview.md) items to Microsoft UI Automation, using a data representation of the item so that the peer supports scrolling to that item with data awareness.

## -remarks
 [ListViewItemDataAutomationPeer](listviewitemdataautomationpeer.md) is generated from [ListViewAutomationPeer](listviewautomationpeer.md) logic, not an associated control class.

### Default peer implementation and overrides in **ListViewItemDataAutomationPeer**

[ListViewItemDataAutomationPeer](listviewitemdataautomationpeer.md) has overrides of **Core** methods such that the associated [AutomationPeer](automationpeer.md) methods provide peer-specific information to a Microsoft UI Automation client.

+ [GetPattern](automationpeer_getpattern.md) reports that the peer supports [PatternInterface.ScrollItem](patterninterface.md) ([IScrollItemProvider](../windows.ui.xaml.automation.provider/iscrollitemprovider.md)). The base [SelectorItemAutomationPeer](selectoritemautomationpeer.md) supports [PatternInterface.SelectionItem](patterninterface.md) ([ISelectionItemProvider](../windows.ui.xaml.automation.provider/iselectionitemprovider.md)) and the base [ItemAutomationPeer](itemautomationpeer.md) supports [PatternInterface.VirtualizedItem](patterninterface.md) ([IVirtualizedItemProvider](../windows.ui.xaml.automation.provider/ivirtualizeditemprovider.md)).
+ [GetClassName](automationpeer_getclassname.md) returns "ListViewItem".
+ [GetAutomationControlType](automationpeer_getautomationcontroltype.md) returns [AutomationControlType.ListItem](automationcontroltype.md).

<!--TODO investigate whether there is a default Name forwarding. There was something sticky with data bound items not being able to add Name into a tree, but maybe that is separate from the 'data' concept here-->
The peer also has other behaviors that are provided by the base [FrameworkElementAutomationPeer](frameworkelementautomationpeer.md) class. For more info, see "Base implementation in FrameworkElementAutomationPeer" section of [Custom automation peers](http://msdn.microsoft.com/library/aa8da53b-fe6e-40ac-9f0a-cb09637c87b4).

## -examples

## -see-also
[ListViewItemAutomationPeer](listviewitemautomationpeer.md), [SelectorItemAutomationPeer](selectoritemautomationpeer.md), [ListView](../windows.ui.xaml.controls/listview.md), [IVirtualizedItemProvider](../windows.ui.xaml.automation.provider/ivirtualizeditemprovider.md), [ISelectionItemProvider](../windows.ui.xaml.automation.provider/iselectionitemprovider.md), [IScrollItemProvider](../windows.ui.xaml.automation.provider/iscrollitemprovider.md), [Custom automation peers](http://msdn.microsoft.com/library/aa8da53b-fe6e-40ac-9f0a-cb09637c87b4)