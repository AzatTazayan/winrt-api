---
-api-id: T:Windows.UI.Xaml.Automation.Peers.FlipViewAutomationPeer
-api-type: winrt class
---

<!-- Class syntax.
public class FlipViewAutomationPeer : Windows.UI.Xaml.Automation.Peers.SelectorAutomationPeer, Windows.UI.Xaml.Automation.Peers.IFlipViewAutomationPeer
-->

# Windows.UI.Xaml.Automation.Peers.FlipViewAutomationPeer

## -description
Exposes [FlipView](../windows.ui.xaml.controls/flipview.md) types to Microsoft UI Automation.

## -remarks
The Windows Runtime  [FlipView](../windows.ui.xaml.controls/flipview.md) class creates a new [FlipViewAutomationPeer](flipviewautomationpeer.md) as its [OnCreateAutomationPeer](../windows.ui.xaml/uielement_oncreateautomationpeer.md) definition. Derive your automation peer from [FlipViewAutomationPeer](flipviewautomationpeer.md) if you are deriving a custom class from [FlipView](../windows.ui.xaml.controls/flipview.md) and want to add automation support for additional features that you enabled in your custom class. Then override [OnCreateAutomationPeer](../windows.ui.xaml/uielement_oncreateautomationpeer.md) so that it returns your custom peer.

### Default peer implementation and overrides in **FlipViewAutomationPeer**

[FlipViewAutomationPeer](flipviewautomationpeer.md) has overrides of **Core** methods such that the associated [AutomationPeer](automationpeer.md) methods provide peer-specific information to a Microsoft UI Automation client.

+ [GetPattern](automationpeer_getpattern.md) reports that the peer provides pattern support for these patterns:
+ [PatternInterface.Selection](patterninterface.md) ([ISelectionProvider](../windows.ui.xaml.automation.provider/iselectionprovider.md))
+ [PatternInterface.ItemContainer](patterninterface.md) ([IItemContainerProvider](../windows.ui.xaml.automation.provider/iitemcontainerprovider.md))
 This is the accumulated pattern support from each of the peer base classes.
+ [GetClassName](automationpeer_getclassname.md) returns "FlipView".
+ [GetAutomationControlType](automationpeer_getautomationcontroltype.md) returns [AutomationControlType.List](automationcontroltype.md).
+ [GetChildren](automationpeer_getchildren.md) returns peers ([FlipViewItemAutomationPeer](flipviewitemautomationpeer.md) instances) for the item content.
The peer also has other behaviors that are provided by the base [FrameworkElementAutomationPeer](frameworkelementautomationpeer.md) class. For more info, see "Base implementation in FrameworkElementAutomationPeer" section of [Custom automation peers](http://msdn.microsoft.com/library/aa8da53b-fe6e-40ac-9f0a-cb09637c87b4).

## -examples

## -see-also
[FlipView](../windows.ui.xaml.controls/flipview.md), [SelectorAutomationPeer](selectorautomationpeer.md), [IItemContainerProvider](../windows.ui.xaml.automation.provider/iitemcontainerprovider.md), [ISelectionProvider](../windows.ui.xaml.automation.provider/iselectionprovider.md), [Custom automation peers](http://msdn.microsoft.com/library/aa8da53b-fe6e-40ac-9f0a-cb09637c87b4)