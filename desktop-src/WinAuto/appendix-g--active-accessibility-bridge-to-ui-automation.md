---
title: Appendice G Active Accessibility Bridge per l'automazione interfaccia utente
description: Questa appendice contiene informazioni su Microsoft Active Accessibility Bridge.
ms.assetid: f19036c7-5a18-4faa-a98d-564e5e63a94f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df5fdc1ebc4d6e17781e383463974f78bb9334aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298177"
---
# <a name="appendix-g-active-accessibility-bridge-to-ui-automation"></a>Appendice G: Active Accessibility Bridge per l'automazione interfaccia utente

Questa appendice contiene informazioni su Microsoft Active Accessibility Bridge. Il Bridge Active Accessibility consente alle applicazioni che implementano Microsoft Active Accessibility di accedere alle applicazioni che implementano l'automazione interfaccia utente Microsoft. Grazie al bridging di Microsoft Active Accessibility e dell'automazione dell'interfaccia utente, i client basati su Microsoft Active Accessibility, ad esempio Screenreader su Windows XP, possono interagire a livello di programmazione con i provider di automazione interfaccia utente basati sull'automazione interfaccia utente, ad esempio un'applicazione Windows Presentation Foundation (WPF). Fa parte dell'API di base nativa di automazione interfaccia utente (UIAutomationCore.dll).

Il Bridge Active Accessibility mappa le proprietà e gli eventi di automazione interfaccia utente a quelli di Microsoft Active Accessibility. Le tabelle seguenti consentono di eseguire il mapping dei metodi e delle proprietà dell'interfaccia Microsoft Active Accessibility [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) all'automazione interfaccia utente. Usare queste tabelle per determinare le procedure di codifica appropriate per lo sviluppo di client basati su Microsoft Active Accessibility.

### <a name="navigation-and-hierarchy-properties"></a>Proprietà di navigazione e gerarchia



| IAccessible (proprietà)                                                     | Proprietà di automazione interfaccia utente          |
|--------------------------------------------------------------------------|---------------------------------|
| [**ottenere \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)           | Non implementato                 |
| [**ottenere \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | Derivato dall'albero di automazione interfaccia utente |
| [**ottenere \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | Derivato dall'albero di automazione interfaccia utente |
| [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)              | Non implementato                 |



 

### <a name="descriptive-properties-and-methods"></a>Proprietà e metodi descrittivi



| IAccessible                                                                          | Automazione interfaccia utente                                                                                                                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)            | Per informazioni dettagliate, vedere i tipi di controllo e la tabella accRole.                                                                                                                                                                                                                                                                     |
| [**ottenere \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)       | Per informazioni dettagliate, vedere i tipi di controllo e la tabella accRole.                                                                                                                                                                                                                                                                     |
| [**ottenere \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | AccessKeyPropertyor AcceleratorKeyProperty; Se sono presenti entrambi, AccessKeyProperty ha la precedenza.                                                                                                                                                                                                                         |
| [**ottenere \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | NameProperty                                                                                                                                                                                                                                                                                                             |
| [**ottenere \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | ControlTypeProperty. Per informazioni dettagliate, vedere i tipi di controllo e la tabella accRole.                                                                                                                                                                                                                                                |
| [**ottenere \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | Per informazioni dettagliate, vedere i tipi di controllo e la tabella accRole.                                                                                                                                                                                                                                                                     |
| [**ottenere \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)                       | ValueProperty supportato su tipi di controllo che supportano il pattern di controllo [value](uiauto-implementingvalue.md) o pattern di controllo [RangeValue](uiauto-implementingrangevalue.md) . I valori RangeValue sono coerenti con il comportamento di Microsoft Active Accessibility (da 0 a 100). Gli elementi dei valori usano una stringa. |
| [**Inserisci \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-put_accvalue)                       | ValueProperty supportato sui tipi di controllo che supportano il pattern di controllo [value](uiauto-implementingvalue.md) o il pattern di controllo [RangeValue](uiauto-implementingrangevalue.md)                                                                                                                                      |
| [**ottenere \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)                         | Proprietà HelpTextProperty                                                                                                                                                                                                                                                                                                         |
| [**ottenere \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           | Non implementato                                                                                                                                                                                                                                                                                                          |
| [**ottenere \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)               | Non implementato                                                                                                                                                                                                                                                                                                          |



 

### <a name="control-types-and-accrole"></a>Tipi di controllo e accRole

Il ruolo predefinito Microsoft Active Accessibility è [**\_ \_ client di sistema del ruolo**](object-roles.md). Se non viene trovata alcuna azione predefinita per un tipo di controllo, il Bridge di Active Accessibility utilizzerà anche i pattern di controllo disponibili seguenti: [Invoke](uiauto-implementinginvoke.md), [ExpandCollapse](uiauto-implementingexpandcollapse.md)e l' [interruttore](uiauto-implementingtoggle.md). Ad esempio, un controllo GroupBox non ha un'azione predefinita. Se supporta ExpandCollapse, il Bridge Active Accessibility lo utilizzerà per l'azione predefinita.



| Tipo di controllo di automazione interfaccia utente                              | accRole                                                                     | Azione predefinita                                           |
|---------------------------------------------------------|-----------------------------------------------------------------------------|----------------------------------------------------------|
| [Button](uiauto-supportbuttoncontroltype.md)           | [**\_pulsante sistema \_ ruolo**](object-roles.md)     | Premere                                                    |
| [Calendario](uiauto-supportcalendarcontroltype.md)       | [**\_client di sistema ruolo \_**](object-roles.md)             | nessuno                                                     |
| [CheckBox](uiauto-supportcheckboxcontroltype.md)       | [**\_CHECKBUTTON di sistema ruolo \_**](object-roles.md)   | Selezionare/deselezionare (interruttore)                                   |
| [ComboBox](uiauto-supportcomboboxcontroltype.md)       | [**\_ \_ casella combinata sistema ruolo**](object-roles.md)         | nessuno                                                     |
| Personalizzato                                                  | [**\_client di sistema ruolo \_**](object-roles.md)             | nessuno                                                     |
| [DataGrid](uiauto-supportdatagridcontroltype.md)       | [**\_elenco sistema \_ ruoli**](object-roles.md)                 | nessuno                                                     |
| [DataItem](uiauto-supportdataitemcontroltype.md)       | [**\_ListItem del sistema di ruolo \_**](object-roles.md)         | nessuno                                                     |
| [Documento](uiauto-supportdocumentcontroltype.md)       | [**\_documento di sistema del ruolo \_**](object-roles.md)         | nessuno                                                     |
| [Modifica](uiauto-supporteditcontroltype.md)               | [**\_testo del sistema ruolo \_**](object-roles.md)                 | nessuno                                                     |
| [Gruppo](uiauto-supportgroupcontroltype.md)             | [**\_raggruppamento del sistema di ruoli \_**](object-roles.md)         | nessuno                                                     |
| [Intestazione](uiauto-supportheadercontroltype.md)           | [**\_elenco sistema \_ ruoli**](object-roles.md)                 | nessuno                                                     |
| [HeaderItem](uiauto-supportheaderitemcontroltype.md)   | [**\_COLUMNHEADER del sistema di ruolo \_**](object-roles.md) | Fare clic su                                                    |
| [Collegamento ipertestuale](uiauto-supporthyperlinkcontroltype.md)     | [**\_collegamento del sistema ruolo \_**](object-roles.md)                 | Jump (mapping da richiamare)                                    |
| [Immagine](uiauto-supportimagecontroltype.md)             | [**\_rappresentazione grafica del sistema di ruoli \_**](object-roles.md)           | nessuno                                                     |
| [Elenco](uiauto-supportlistcontroltype.md)               | [**\_elenco sistema \_ ruoli**](object-roles.md)                 | nessuno                                                     |
| [ListItem](uiauto-supportlistitemcontroltype.md)       | [**\_ListItem del sistema di ruolo \_**](object-roles.md)         | Doppio clic                                             |
| [Menu](uiauto-supportmenucontroltype.md)               | [**\_MENUPOPUP di sistema ruolo \_**](object-roles.md)       | nessuno                                                     |
| [MenuBar](uiauto-supportmenubarcontroltype.md)         | [**\_barra dei \_ menu sistema ruolo**](object-roles.md)           | nessuno                                                     |
| [MenuItem](uiauto-supportmenuitemcontroltype.md)       | [**\_MenuItem del sistema di ruolo \_**](object-roles.md)         | Eseguire o aprire/chiudere le voci di menu che dispongono di elementi figlio. |
| [Riquadro](uiauto-supportpanecontroltype.md)               | [**\_riquadro sistema \_ ruoli**](object-roles.md)                 | nessuno                                                     |
| [ProgressBar](uiauto-supportprogressbarcontroltype.md) | [**\_PROGRESSBAR del sistema di ruolo \_**](object-roles.md)   | nessuno                                                     |
| [RadioButton](uiauto-supportradiobuttoncontroltype.md) | [**\_RadioButton sistema \_ ruolo**](object-roles.md)   | Controllo                                                    |
| [ScrollBar](uiauto-supportscrollbarcontroltype.md)     | [**\_barra di \_ scorrimento sistema ruolo**](object-roles.md)       | nessuno                                                     |
| [Dispositivo di scorrimento](uiauto-supportslidercontroltype.md)           | [**\_dispositivo di \_ scorrimento sistema ruolo**](object-roles.md)             | nessuno                                                     |
| [Spinner](uiauto-supportspinnercontroltype.md)         | [**\_SPINBUTTON di sistema ruolo \_**](object-roles.md)     | nessuno                                                     |
| [SplitButton](uiauto-supportsplitbuttoncontroltype.md) | [**\_SPLITBUTTON di sistema ruolo \_**](object-roles.md)   | nessuno                                                     |
| [StatusBar](uiauto-supportstatusbarcontroltype.md)     | [**\_StatusBar del sistema ruolo \_**](object-roles.md)       | nessuno                                                     |
| [TAB](uiauto-supporttabcontroltype.md)                 | [**\_PAGETABLIST di sistema ruolo \_**](object-roles.md)   | nessuno                                                     |
| [TabItem](uiauto-supporttabitemcontroltype.md)         | [**\_PaginaScheda di sistema ruolo \_**](object-roles.md)           | Opzione                                                   |
| [Tabella](uiauto-supporttablecontroltype.md)             | [**\_tabella di sistema del ruolo \_**](object-roles.md)               | nessuno                                                     |
| [Text](uiauto-supporttextcontroltype.md)               | [**\_STATICTEXT di sistema ruolo \_**](object-roles.md)     | nessuno                                                     |
| [Thumb](uiauto-supportthumbcontroltype.md)             | [**\_indicatore del sistema di ruolo \_**](object-roles.md)       | nessuno                                                     |
| [TitleBar](uiauto-supporttitlebarcontroltype.md)       | [**barra di titolo \_ sistema ruolo \_**](object-roles.md)         | nessuno                                                     |
| [Barra degli strumenti](uiauto-supporttoolbarcontroltype.md)         | [**\_ \_ barra degli strumenti del sistema di ruolo**](object-roles.md)           | nessuno                                                     |
| [ToolTip](uiauto-supporttooltipcontroltype.md)         | [**\_ \_ Descrizione comando sistema ruolo**](object-roles.md)           | nessuno                                                     |
| [Albero](uiauto-supporttreecontroltype.md)               | [**\_struttura del sistema di ruolo \_**](object-roles.md)           | nessuno                                                     |
| [TreeItem](uiauto-supporttreeitemcontroltype.md)       | [**\_OUTLINEITEM di sistema ruolo \_**](object-roles.md)   | Espandi o Comprimi                                       |
| [Window](uiauto-supportwindowcontroltype.md)           | [**\_finestra del sistema di ruolo \_**](object-roles.md)             | nessuno                                                     |



 

### <a name="ui-automation-properties-and-accstate"></a>Proprietà di automazione interfaccia utente e accState



| accState                                                                                      | Proprietà di automazione interfaccia utente                                                                                                                                                        | Modifica stato trigger |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------|
| [**sistema di stato \_ \_ selezionato**](object-state-constants.md)                 | Per ControlType = "checkbox" usare ToggleState. on. Per "RadioButton" utilizzare [ **SelectionItemPattern:: IsSelected**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-get_currentisselected) | Sì                   |
| [**STATO \_ attivo del sistema di stato \_**](object-state-constants.md)             | IsKeyboardFocusableProperty                                                                                                                                                   | No                    |
| [**STATO \_ \_ attivo sistema**](object-state-constants.md)                 | HasKeyboardFocusProperty                                                                                                                                                      | No                    |
| [**\_protetto dal sistema di stato \_**](object-state-constants.md)             | IsPasswordProperty                                                                                                                                                            | No                    |
| [**sistema di stato \_ \_ ReadOnly**](object-state-constants.md)               | IsReadOnlyProperty (pattern di controllo Value e pattern di controllo RangeValue)                                                                                                     | No                    |
| [**sistema di stato non \_ \_ disponibile**](object-state-constants.md)         | IsEnabledProperty                                                                                                                                                             | Sì                   |
| [**sistema di stato \_ \_ collegato**](object-state-constants.md)                   | ControlTypeProperty = "Hyperlink"                                                                                                                                             | No                    |
| [**sistema di stato \_ \_ selezionabile**](object-state-constants.md)           | SelectionItemPattern è supportato                                                                                                                                             | No                    |
| [**sistema di stato \_ \_ selezionato**](object-state-constants.md)               | IsSelectedProperty (pattern di controllo SelectionItem)                                                                                                                            | No                    |
| [**sistema di stato \_ \_ compresso**](object-state-constants.md)             | ExpandCollapseState = compresso                                                                                                                                               | Sì                   |
| [**sistema di stato \_ \_ espanso**](object-state-constants.md)               | ExpandCollapseState = espanso o PartiallyExpanded                                                                                                                           | Sì                   |
| [**\_HASPOPUP sistema di stato \_**](object-state-constants.md)               | Voci di menu che supportano l'espansione o la compressione                                                                                                                                       | No                    |
| [**sistema di stato \_ \_ misto**](object-state-constants.md)                     | ToggleState = indeterminato                                                                                                                                                   | No                    |
| [**\_dimensioni del sistema di stato \_**](object-state-constants.md)               | [**IUIAutomationTransformPattern:: CanResize**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtransformpattern-get_currentcanresize)                                                                     | No                    |
| [**sistema di stato \_ \_ mobile**](object-state-constants.md)               | [**IUIAutomationTransformPattern:: CanMove**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtransformpattern-get_currentcanmove)                                                                         | No                    |
| [**sistema di stato \_ \_ multiselezionabile**](object-state-constants.md) | [**IUIAutomationSelectionPattern:: CanSelectMultiple**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionpattern-get_currentcanselectmultiple)                                                     | No                    |



 

### <a name="selection-and-focus"></a>Selezione e stato attivo



| IAccessible                                                            | Automazione interfaccia utente                                                                          |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**ottenere \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)         | [**IUIAutomation:: FocusedElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement)        |
| [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                | Per informazioni dettagliate, vedere le proprietà di automazione interfaccia utente e la tabella SELFLAGs accSelect.             |
| [**ottenere \_ accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection) | [**SelectionPattern:: GetSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-getselection) |



 

### <a name="ui-automation-properties-and-accselect-selflags"></a>Proprietà di automazione interfaccia utente e accSelect SELFLAGs



| SELFLAGs accSelect                                                  | Proprietà di automazione interfaccia utente                                                                                                         |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**SELFLAG \_ None**](selflag.md)                       | Non disponibile                                                                                                                  |
| \_TAKFOCUS SELFLAG                                                   | [**IUIAutomationElement:: SetFocus**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-setfocus)                                                 |
| [**\_TAKESELECTION SELFLAG**](selflag.md)     | [**IUIAutomationSelectionItemPattern:: Select**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-select)                           |
| [**\_ADDSELECTION SELFLAG**](selflag.md)       | [**IUIAutomationSelectionItemPattern:: AddToSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-addtoselection)           |
| \_TAKEREMOVESELECTION SELFLAG                                        | [**IUIAutomationSelectionItemPattern:: RemoveFromSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-removefromselection) |
| [**\_EXTENDSELECTION SELFLAG**](selflag.md) | Non disponibile                                                                                                                  |



 

### <a name="spatial-mapping"></a>Mapping spaziale



| IAccessible                                                 | Automazione interfaccia utente                                                                                                                        |
|-------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) | BoundingRectangleProperty                                                                                                            |
| [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)   | [**IRawElementProviderFragmentRoot:: ElementProviderFromPoint**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragmentroot-elementproviderfrompoint) |



 

### <a name="events"></a>Eventi



| Costanti evento System-Level                                                             | Automazione interfaccia utente                                                                                                           |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**\_MENUPOPUPSTART sistema \_ eventi**](event-constants.md)     | [**UIA \_ MenuOpenedEventId**](uiauto-event-ids.md) (Nota: è necessario controllare se si tratta di una finestra popup). |
| [**\_MENUPOPUPEND sistema \_ eventi**](event-constants.md)         | [**\_MENUCLOSEDEVENTID UIA**](uiauto-event-ids.md)                                                |
| [**\_l'MenuStart sistema \_ eventi**](event-constants.md)               | [**\_MENUMODESTARTEVENTID UIA**](uiauto-event-ids.md)                                          |
| [**\_MENUEND sistema \_ eventi**](event-constants.md)                   | [**\_MENUMODEENDEVENTID UIA**](uiauto-event-ids.md)                                              |
| [**\_audio sistema \_ eventi**](event-constants.md)                       |                                                                                                                         |
| [**\_avviso sistema \_ eventi**](event-constants.md)                       |                                                                                                                         |
| [**\_CAPTURESTART sistema \_ eventi**](event-constants.md)         |                                                                                                                         |
| [**\_CAPTUREEND sistema \_ eventi**](event-constants.md)             |                                                                                                                         |
| [**\_DIALOGSTART sistema \_ eventi**](event-constants.md)           |                                                                                                                         |
| [**\_DIALOGEND sistema \_ eventi**](event-constants.md)               |                                                                                                                         |
| [**\_MOVESIZESTART sistema \_ eventi**](event-constants.md)       |                                                                                                                         |
| [**\_MOVESIZEEND sistema \_ eventi**](event-constants.md)           |                                                                                                                         |
| [**\_CONTEXTHELPSTART sistema \_ eventi**](event-constants.md) |                                                                                                                         |
| [**\_CONTEXTHELPEND sistema \_ eventi**](event-constants.md)     | Non rilevante                                                                                                            |
| [**\_DRAGDROPSTART sistema \_ eventi**](event-constants.md)       |                                                                                                                         |
| [**\_DRAGDROPEND sistema \_ eventi**](event-constants.md)           |                                                                                                                         |
| [**\_SWITCHSTART sistema \_ eventi**](event-constants.md)           | Non rilevante                                                                                                            |
| [**\_SWITCHEND sistema \_ eventi**](event-constants.md)               | Non rilevante                                                                                                            |
| [**\_MINIMIZESTART sistema \_ eventi**](event-constants.md)       |                                                                                                                         |
| [**\_MINIMIZEEND sistema \_ eventi**](event-constants.md)           |                                                                                                                         |
| [**\_primo piano del sistema di eventi \_**](event-constants.md)             |                                                                                                                         |
| [**\_SCROLLINGSTART sistema \_ eventi**](event-constants.md)     | Non disponibile                                                                                                           |
| [**\_SCROLLINGEND sistema \_ eventi**](event-constants.md)         | Non disponibile                                                                                                           |



 



| Costanti evento Object-Level                                                           | Automazione interfaccia utente                                                                          |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**\_ \_ stato attivo oggetto evento**](event-constants.md)                     | AutomationFocusChangedEvent                                                            |
| [**\_oggetto evento \_ VALUECHANGE**](event-constants.md)         | ValueProperty (pattern di controllo Value e pattern di controllo RangeValue)                   |
| [**\_selezione oggetti \_ evento**](event-constants.md)             | ElementSelectedEvent (pattern di controllo SelectionItem)                                   |
| [**\_oggetto evento \_ SELECTIONADD**](event-constants.md)       | ElementAddedToSelectionEvent (pattern di controllo SelectionItem)                           |
| [**\_oggetto evento \_ SELECTIONREMOVE**](event-constants.md) | ElementRemovedFromSelectionEvent                                                       |
| [**\_oggetto evento \_ SELECTIONWITHIN**](event-constants.md) | EventsSelectionInvalidatedEvent                                                        |
| [**\_oggetto evento \_ STATECHANGE**](event-constants.md)         | Vedere Proprietà di automazione interfaccia utente e tabella accState per gli Stati che attivano una modifica dello stato |



 

 

 




