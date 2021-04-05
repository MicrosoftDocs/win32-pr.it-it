---
title: Linee guida per l'implementazione di IAccessibleEx
description: Il nucleo di automazione interfaccia utente Microsoft può recuperare tutte le proprietà di Microsoft Active Accessibility per qualsiasi oggetto accessibile esposto da un server tramite l'interfaccia IAccessible.
ms.assetid: d047127c-1be2-4f34-bb97-330b5509ca0d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82403a51e4848142a26194a98dce3922619b06f4
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "103719993"
---
# <a name="iaccessibleex-implementation-guidelines"></a>Linee guida per l'implementazione di IAccessibleEx

Il nucleo di automazione interfaccia utente Microsoft può recuperare tutte le proprietà di Microsoft Active Accessibility per qualsiasi oggetto accessibile esposto da un server tramite l'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) . Quando si implementa [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex), è necessario esporre solo gli aspetti delle funzionalità dell'interfaccia utente che altrimenti non possono essere esposti tramite le proprietà esistenti di Microsoft Active Accessibility. In questo argomento vengono identificate le proprietà e i pattern di controllo di automazione interfaccia utente che rappresentano la funzionalità dell'interfaccia utente senza controparte in Microsoft Active Accessibility, ovvero le proprietà e i pattern di controllo che è possibile esporre in un'implementazione di **IAccessibleEx** .

In questo argomento sono incluse le sezioni seguenti:

-   [Proprietà](#properties)
-   [Pattern di controllo](#control-patterns)
-   [WinEvents per eventi di modifica proprietà di automazione interfaccia utente](#winevents-for-ui-automation-property-changed-events)
-   [Argomenti correlati](#related-topics)

## <a name="properties"></a>Proprietà

Le seguenti proprietà di automazione interfaccia utente non si sovrappongono con la funzionalità Microsoft Active Accessibility. Possono essere usati in un'implementazione di [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) :

-   AriaProperties
-   AriaRole
-   AutomationId
-   ClassName
-   ClickablePoint
-   ControllerFor
-   culture
-   DescribedBy
-   FlowsTo
-   FrameworkId
-   IsContentElement
-   IsControlElement
-   IsDataValidForForm
-   IsRequiredForForm
-   ItemStatus
-   ItemType
-   LabeledBy
-   LocalizedControlType
-   Orientamento

Sebbene le proprietà di automazione interfaccia utente AcceleratorKey e AccessKey si sovrappongano alla proprietà accKeyboardShortcut Active Accessibility Microsoft, è comunque possibile usarle in un'implementazione [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) per i controlli che dispongono sia di una chiave di accesso sia di un acceleratore. Analogamente, la proprietà di automazione interfaccia utente ControlType si sovrappone alla proprietà Microsoft Active Accessibility accRole, ma è comunque possibile utilizzarla in un'implementazione **IAccessibleEx** per definire un ruolo più specifico per un controllo.

Poiché le proprietà degli elementi di automazione interfaccia utente seguenti sono già coperte dalle proprietà di Microsoft Active Accessibility, non è necessario utilizzarle in un'implementazione di [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) .



| Proprietà di automazione interfaccia utente | Microsoft Active Accessibility equivalente                                                                                                                                     |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BoundingRectangle      | accLocation                                                                                                                                                                   |
| HasKeyboardFocus       | accState, [ **stato \_ \_ attivo sistema**](object-state-constants.md)                                                                                       |
| IsEnabled              | accState, [ **sistema di stato non \_ \_ disponibile**](object-state-constants.md)                                                                               |
| IsKeyboardFocusable    | accState, [ **stato \_ \_ attivo del sistema di stato**](object-state-constants.md)                                                                                   |
| IsPassword             | accState, [ **stato \_ \_ protetto dal sistema**](object-state-constants.md)                                                                                   |
| HelpText               | accHelp                                                                                                                                                                       |
| Nome                   | accName                                                                                                                                                                       |
| NativeWindowHandle     | [**WindowFromAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-windowfromaccessibleobject)                                                                                                              |
| IsOffscreen            | accState, sistema di stato [**\_ \_ invisibile**](object-state-constants.md) / [**allo stato del sistema \_ \_ Offscreen**](object-state-constants.md) |
| ProcessId              | Fornito dal core di automazione interfaccia utente                                                                                                                                                |



 

Per qualsiasi proprietà di automazione interfaccia utente non supportata, l'implementazione del metodo [**IRawElementProviderSimple:: GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue) deve impostare il parametro *pRetVal* su VT \_ Empty e restituire S \_ OK. Se si restituisce l'interfaccia [**\_ \_ NotSupported E**](uiauto-error-codes.md) il proxy MSAA-to-UIA, il mapping predefinito per la proprietà corrispondente verrà rimosso.

## <a name="control-patterns"></a>Pattern di controllo

I pattern di controllo di automazione interfaccia utente seguenti non si sovrappongono alla funzionalità Microsoft Active Accessibility. Possono essere usati in un'implementazione di [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) :

-   Ancora
-   ExpandCollapse
-   Pannello Grid
-   GridItem
-   MultipleView
-   RangeValue
-   Scroll
-   ScrollItem
-   SynchronizedInput
-   Tabella
-   TableItem
-   Trasformare

Per i pattern di controllo RangeValue e Transform, alcuni metodi si sovrappongono tra il pattern di controllo di automazione interfaccia utente e i metodi di Microsoft Active Accessibility. In questi casi, entrambi devono essere implementati. Ad esempio, entrambi i metodi di Microsoft Active Accessibility [**IAccessible:: Get \_ AccValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) e [**IAccessible::p UT \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-put_accvalue) devono essere implementati, come i metodi di automazione interfaccia utente [**IRangeValueProvider:: value**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_value) e [**IRangeValueProvider::**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-setvalue) SetValue. Internamente, un'implementazione può condividere il codice per questi. Questo requisito per implementare entrambi i set evita di avere un'implementazione parziale di un'interfaccia del modello mantenendo l'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) utilizzabile dai client Microsoft Active Accessibility esistenti.

I pattern di controllo di automazione interfaccia utente seguenti non sono necessari quando il controllo ha uno dei ruoli descritti di seguito. in caso contrario, devono essere supportati in modo esplicito se pertinente.



| Pattern di controllo di automazione interfaccia utente | Ruolo Microsoft Active Accessibility                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| InvokePattern                 | [**Ruolo \_ di \_Pulsante di sistema**](object-roles.md), [**\_ \_ MenuItem del sistema dei ruoli**](object-roles.md), sistema del [**ruolo \_ \_ BUTTONDROPDOWN**](object-roles.md), [**sistema del ruolo \_ \_ SPLITBUTTON**](object-roles.md)e qualsiasi altro ruolo in cui il valore della proprietà accDefaultAction non è **null**. |
| SelectionItemPattern          | [**Ruolo \_ di System \_ ListItem**](object-roles.md), [ **\_ \_ RadioButton del sistema di ruolo**](object-roles.md)                                                                                                                                                                                                                                                 |
| SelectionPattern              | [**\_elenco sistema \_ ruoli**](object-roles.md)                                                                                                                                                                                                                                                                                                                                    |
| TogglePattern                 | [**\_CHECKBUTTON di sistema ruolo \_**](object-roles.md)                                                                                                                                                                                                                                                                                                                      |
| ValuePattern                  | [**Ruolo \_ di \_Testo di sistema**](object-roles.md) (se non è di sola lettura), [**\_ \_ PROGRESSBAR del sistema dei ruoli**](object-roles.md), [**\_ \_ casella combinata del sistema del ruolo**](object-roles.md)e qualsiasi altro ruolo quando il valore della Proprietà accValue non è **null**.                                                                            |
| WindowPattern                 | Supportato automaticamente in **HWND** Microsoft Win32 di primo livello.                                                                                                                                                                                                                                                                                                                                |



 

## <a name="winevents-for-ui-automation-property-changed-events"></a>WinEvents per eventi di modifica proprietà di automazione interfaccia utente

Oltre agli eventi definiti per [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), vengono definiti anche gli identificatori di evento seguenti e possono essere usati con un'implementazione di [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) come eventi di modifica delle proprietà per le proprietà di automazione interfaccia utente corrispondenti. Questi utilizzano lo stesso meccanismo degli eventi definiti per **IAccessible**. Per ulteriori informazioni, vedere [winEvents](winevents-infrastructure.md).



| ID WinEvent per le implementazioni di IAccessibleEx                                                                                              | ID WinEvent correlato da Microsoft Active Accessibility                                |
|--------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**\_ARIAPROPERTIESPROPERTYID UIA**](uiauto-automation-element-propids.md)                                    | nessuno                                                                                   |
| [**\_ARIAROLEPROPERTYID UIA**](uiauto-automation-element-propids.md)                                                | nessuno                                                                                   |
| [**\_CONTROLLERFORPROPERTYID UIA**](uiauto-automation-element-propids.md)                                      | nessuno                                                                                   |
| [**\_DESCRIBEDBYPROPERTYID UIA**](uiauto-automation-element-propids.md)                                          | nessuno                                                                                   |
| [**\_EXPANDCOLLAPSEEXPANDCOLLAPSESTATEPROPERTYID UIA**](uiauto-control-pattern-propids.md) | [**\_oggetto evento \_ STATECHANGE**](event-constants.md)         |
| [**\_FLOWSTOPROPERTYID UIA**](uiauto-automation-element-propids.md)                                                  | nessuno                                                                                   |
| [**\_INPUTDISCARDEDEVENTID UIA**](uiauto-event-ids.md)                                                           | nessuno                                                                                   |
| [**\_INPUTREACHEDOTHERELEMENTEVENTID UIA**](uiauto-event-ids.md)                                       | nessuno                                                                                   |
| [**\_INPUTREACHEDTARGETEVENTID UIA**](uiauto-event-ids.md)                                                   | nessuno                                                                                   |
| [**\_ISDATAVALIDFORFORMPROPERTYID UIA**](uiauto-automation-element-propids.md)                            | nessuno                                                                                   |
| [**\_ISENABLEDPROPERTYID UIA**](uiauto-automation-element-propids.md)                                              | [**\_oggetto evento \_ STATECHANGE**](event-constants.md)         |
| [**\_ITEMSTATUSPROPERTYID UIA**](uiauto-automation-element-propids.md)                                            | nessuno                                                                                   |
| [**\_MULTIPLEVIEWCURRENTVIEWPROPERTYID UIA**](uiauto-control-pattern-propids.md)                     | nessuno                                                                                   |
| [**\_SCROLLHORIZONTALLYSCROLLABLEPROPERTYID UIA**](uiauto-control-pattern-propids.md)           | nessuno                                                                                   |
| [**\_SCROLLHORIZONTALSCROLLPERCENTPROPERTYID UIA**](uiauto-control-pattern-propids.md)         | [**\_oggetto evento \_ CONTENTSCROLLED**](event-constants.md) |
| [**\_SCROLLHORIZONTALVIEWSIZEPROPERTYID UIA**](uiauto-control-pattern-propids.md)                   | nessuno                                                                                   |
| [**\_SCROLLVERTICALLYSCROLLABLEPROPERTYID UIA**](uiauto-control-pattern-propids.md)               | nessuno                                                                                   |
| [**\_SCROLLVERTICALSCROLLPERCENTPROPERTYID UIA**](uiauto-control-pattern-propids.md)             | [**\_oggetto evento \_ CONTENTSCROLLED**](event-constants.md) |
| [**\_SCROLLVERTICALVIEWSIZEPROPERTYID UIA**](uiauto-control-pattern-propids.md)                       | nessuno                                                                                   |
| [**\_TOGGLETOGGLESTATEPROPERTYID UIA**](uiauto-control-pattern-propids.md)                                 | [**\_oggetto evento \_ STATECHANGE**](event-constants.md)         |



 

Per gli eventi precedenti che hanno un \_ valore di oggetto evento \_ elencato dopo di essi, l'implementazione di [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) deve generare questo evento oltre all'evento modificato elencato. In questo modo il codice client **IAccessibleEx** esistente continuerà a funzionare, fornendo al contempo informazioni più dettagliate sugli eventi ai client interessati.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[WinEvents](winevents-infrastructure.md)
</dt> <dt>

[Interfaccia IAccessibleEx](iaccessibleex.md)
</dt> </dl>

 

 




