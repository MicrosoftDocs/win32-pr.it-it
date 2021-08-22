---
title: Appendice G Active Accessibility Bridge to Automazione interfaccia utente
description: Questa appendice contiene informazioni sull'Microsoft Active Accessibility Bridge.
ms.assetid: f19036c7-5a18-4faa-a98d-564e5e63a94f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14991f869706a16c4def8fdaf49ae255e3ddf413eec416cefd1e151ee470cc02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052969"
---
# <a name="appendix-g-active-accessibility-bridge-to-ui-automation"></a>Appendice G: Active Accessibility Bridge to Automazione interfaccia utente

Questa appendice contiene informazioni sull'Microsoft Active Accessibility Bridge. Il Active Accessibility Bridge consente alle applicazioni che implementano Microsoft Active Accessibility accedere alle applicazioni che implementano Microsoft Automazione interfaccia utente. Grazie al bridging di Microsoft Active Accessibility e Automazione interfaccia utente, i client basati su Microsoft Active Accessibility, ad esempio un'utilità per la lettura dello schermo in Windows XP, possono interagire a livello di codice con i provider di Automazione interfaccia utente basati su Automazione interfaccia utente, ad esempio un'applicazione Windows Presentation Foundation (WPF). Fa parte dell'API Automazione interfaccia utente Native Core (UIAutomationCore.dll).

Il Active Accessibility Bridge esegue il mapping Automazione interfaccia utente proprietà ed eventi a quelli di Microsoft Active Accessibility. Nelle tabelle seguenti viene mappato il Microsoft Active Accessibility [**e le proprietà dell'interfaccia IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) Automazione interfaccia utente. Usare queste tabelle per determinare le procedure di codifica appropriate per lo sviluppo Microsoft Active Accessibility client basato su client.

### <a name="navigation-and-hierarchy-properties"></a>Proprietà di navigazione e gerarchia



| Proprietà IAccessible                                                     | Automazione interfaccia utente proprietà          |
|--------------------------------------------------------------------------|---------------------------------|
| [**get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)           | Non implementato                 |
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | Derivato da Automazione interfaccia utente albero |
| [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | Derivato da Automazione interfaccia utente albero |
| [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)              | Non implementato                 |



 

### <a name="descriptive-properties-and-methods"></a>Proprietà e metodi descrittivi



| Iaccessible                                                                          | Automazione interfaccia utente                                                                                                                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)            | Per informazioni dettagliate, vedere la tabella Tipi di controllo e accRole .                                                                                                                                                                                                                                                                     |
| [**get \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)       | Per informazioni dettagliate, vedere la tabella Tipi di controllo e accRole .                                                                                                                                                                                                                                                                     |
| [**get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | AccessKeyPropertyor AcceleratorKeyProperty; Se sono presenti entrambi, AccessKeyProperty ha la precedenza.                                                                                                                                                                                                                         |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | NameProperty                                                                                                                                                                                                                                                                                                             |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | Proprietà ControlType. Per informazioni dettagliate, vedere la tabella Tipi di controllo e accRole .                                                                                                                                                                                                                                                |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | Per informazioni dettagliate, vedere la tabella Tipi di controllo e accRole .                                                                                                                                                                                                                                                                     |
| [**get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)                       | ValueProperty; supportato nei tipi di controllo che supportano il pattern di controllo [Value](uiauto-implementingvalue.md) o [rangeValue.](uiauto-implementingrangevalue.md) I valori RangeValue sono coerenti Microsoft Active Accessibility comportamento predefinito (da 0 a 100). Gli elementi dei valori usano una stringa. |
| [**put \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-put_accvalue)                       | ValueProperty; supportato nei tipi di controllo che supportano il pattern di controllo [Value](uiauto-implementingvalue.md) [o RangeValue](uiauto-implementingrangevalue.md)                                                                                                                                      |
| [**get \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)                         | Proprietà HelpTextProperty                                                                                                                                                                                                                                                                                                         |
| [**get \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           | Non implementato                                                                                                                                                                                                                                                                                                          |
| [**get \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)               | Non implementato                                                                                                                                                                                                                                                                                                          |



 

### <a name="control-types-and-accrole"></a>Tipi di controllo e accRole

Il Microsoft Active Accessibility predefinito è [**ROLE \_ SYSTEM \_ CLIENT**](object-roles.md). Se non viene trovata alcuna azione predefinita per un tipo di controllo, Active Accessibility Bridge userà anche i pattern di controllo disponibili seguenti: [Invoke](uiauto-implementinginvoke.md), [ExpandCollapse](uiauto-implementingexpandcollapse.md)e [Toggle](uiauto-implementingtoggle.md). Ad esempio, un controllo groupbox non ha un'azione predefinita. Se supporta ExpandCollapse, il Active Accessibility Bridge lo userà per l'azione predefinita.



| Automazione interfaccia utente tipo di controllo                              | accRole                                                                     | Azione predefinita                                           |
|---------------------------------------------------------|-----------------------------------------------------------------------------|----------------------------------------------------------|
| [Button](uiauto-supportbuttoncontroltype.md)           | [**ROLE \_ SYSTEM \_ PUSHBUTTON**](object-roles.md)     | Premere                                                    |
| [Calendario](uiauto-supportcalendarcontroltype.md)       | [**\_CLIENT DEL SISTEMA \_ RUOLO**](object-roles.md)             | Nessuno                                                     |
| [CheckBox](uiauto-supportcheckboxcontroltype.md)       | [**ROLE \_ SYSTEM \_ CHECKBUTTON**](object-roles.md)   | Seleziona/Deseleziona (attiva/disattiva)                                   |
| [ComboBox](uiauto-supportcomboboxcontroltype.md)       | [**CASELLA \_ COMBINATA \_ SISTEMA RUOLO**](object-roles.md)         | Nessuno                                                     |
| Personalizzato                                                  | [**\_CLIENT DEL SISTEMA \_ RUOLO**](object-roles.md)             | Nessuno                                                     |
| [DataGrid](uiauto-supportdatagridcontroltype.md)       | [**ELENCO \_ DEI SISTEMI \_ RUOLO**](object-roles.md)                 | Nessuno                                                     |
| [DataItem](uiauto-supportdataitemcontroltype.md)       | [**ROLE \_ SYSTEM \_ LISTITEM**](object-roles.md)         | Nessuno                                                     |
| [Documento](uiauto-supportdocumentcontroltype.md)       | [**DOCUMENTO \_ DI SISTEMA DEL \_ RUOLO**](object-roles.md)         | Nessuno                                                     |
| [Modifica](uiauto-supporteditcontroltype.md)               | [**ROLE \_ SYSTEM \_ TEXT**](object-roles.md)                 | Nessuno                                                     |
| [Gruppo](uiauto-supportgroupcontroltype.md)             | [**RAGGRUPPAMENTO \_ DEL \_ SISTEMA DI RUOLI**](object-roles.md)         | Nessuno                                                     |
| [Intestazione](uiauto-supportheadercontroltype.md)           | [**ELENCO \_ DEI SISTEMI \_ RUOLO**](object-roles.md)                 | Nessuno                                                     |
| [HeaderItem](uiauto-supportheaderitemcontroltype.md)   | [**ROLE \_ SYSTEM \_ COLUMNHEADER**](object-roles.md) | Fare clic su                                                    |
| [Collegamento ipertestuale](uiauto-supporthyperlinkcontroltype.md)     | [**COLLEGAMENTO SISTEMA \_ \_ RUOLO**](object-roles.md)                 | Jump (esegue il mapping a Invoke)                                    |
| [Immagine](uiauto-supportimagecontroltype.md)             | [**IMMAGINE DEL \_ SISTEMA \_ RUOLO**](object-roles.md)           | Nessuno                                                     |
| [Elenco](uiauto-supportlistcontroltype.md)               | [**ELENCO \_ DI SISTEMI \_ RUOLO**](object-roles.md)                 | Nessuno                                                     |
| [ListItem](uiauto-supportlistitemcontroltype.md)       | [**ROLE \_ SYSTEM \_ LISTITEM**](object-roles.md)         | Fare doppio clic su                                             |
| [Menu](uiauto-supportmenucontroltype.md)               | [**\_MENU SISTEMA \_ RUOLOPOPUP**](object-roles.md)       | Nessuno                                                     |
| [MenuBar](uiauto-supportmenubarcontroltype.md)         | [**BARRA \_ DEI MENU DEL SISTEMA DEI \_ RUOLI**](object-roles.md)           | Nessuno                                                     |
| [MenuItem](uiauto-supportmenuitemcontroltype.md)       | [**ROLE \_ SYSTEM \_ MENUITEM**](object-roles.md)         | Eseguire o Apri/Chiudi per le voci di menu con elementi figlio. |
| [Riquadro](uiauto-supportpanecontroltype.md)               | [**RIQUADRO \_ SISTEMA \_ RUOLO**](object-roles.md)                 | Nessuno                                                     |
| [ProgressBar](uiauto-supportprogressbarcontroltype.md) | [**BARRA DI \_ STATO DEL SISTEMA DEL \_ RUOLO**](object-roles.md)   | Nessuno                                                     |
| [RadioButton](uiauto-supportradiobuttoncontroltype.md) | [**PULSANTE \_ DI OPZIONE SISTEMA \_ RUOLO**](object-roles.md)   | Controllo                                                    |
| [ScrollBar](uiauto-supportscrollbarcontroltype.md)     | [**BARRA \_ DI SCORRIMENTO \_ DEL SISTEMA RUOLO**](object-roles.md)       | Nessuno                                                     |
| [Dispositivo di scorrimento](uiauto-supportslidercontroltype.md)           | [**DISPOSITIVO DI \_ SCORRIMENTO DEL SISTEMA \_ RUOLO**](object-roles.md)             | Nessuno                                                     |
| [Spinner](uiauto-supportspinnercontroltype.md)         | [**PULSANTE \_ DI SELEZIONE SISTEMA \_ RUOLO**](object-roles.md)     | Nessuno                                                     |
| [SplitButton](uiauto-supportsplitbuttoncontroltype.md) | [**ROLE \_ SYSTEM \_ SPLITBUTTON**](object-roles.md)   | Nessuno                                                     |
| [StatusBar](uiauto-supportstatusbarcontroltype.md)     | [**BARRA \_ DI STATO DEL SISTEMA DEI \_ RUOLI**](object-roles.md)       | Nessuno                                                     |
| [TAB](uiauto-supporttabcontroltype.md)                 | [**ROLE \_ SYSTEM \_ PAGETABLIST**](object-roles.md)   | Nessuno                                                     |
| [TabItem](uiauto-supporttabitemcontroltype.md)         | [**SCHEDA \_ PAGINA \_ SISTEMA RUOLO**](object-roles.md)           | Commutatore                                                   |
| [Tabella](uiauto-supporttablecontroltype.md)             | [**TABELLA \_ DI SISTEMA DEI \_ RUOLI**](object-roles.md)               | Nessuno                                                     |
| [Text](uiauto-supporttextcontroltype.md)               | [**TESTO \_ STATICO DEL SISTEMA DEI \_ RUOLI**](object-roles.md)     | Nessuno                                                     |
| [Pollice](uiauto-supportthumbcontroltype.md)             | [**INDICATORE \_ DI SISTEMA DEL \_ RUOLO**](object-roles.md)       | Nessuno                                                     |
| [Titlebar](uiauto-supporttitlebarcontroltype.md)       | [**BARRA \_ DEL TITOLO DEL SISTEMA DI \_ RUOLI**](object-roles.md)         | Nessuno                                                     |
| [Barra degli strumenti](uiauto-supporttoolbarcontroltype.md)         | [**BARRA DEGLI \_ STRUMENTI DEL SISTEMA DEI \_ RUOLI**](object-roles.md)           | Nessuno                                                     |
| [ToolTip](uiauto-supporttooltipcontroltype.md)         | [**DESCRIZIONE \_ COMANDO DEL SISTEMA DEI \_ RUOLI**](object-roles.md)           | Nessuno                                                     |
| [Albero](uiauto-supporttreecontroltype.md)               | [**STRUTTURA \_ DEL SISTEMA DEI \_ RUOLI**](object-roles.md)           | Nessuno                                                     |
| [TreeItem](uiauto-supporttreeitemcontroltype.md)       | [**ROLE \_ SYSTEM \_ OUTLINEITEM**](object-roles.md)   | Espandere o comprimere                                       |
| [Window](uiauto-supportwindowcontroltype.md)           | [**FINESTRA \_ SISTEMA \_ RUOLO**](object-roles.md)             | Nessuno                                                     |



 

### <a name="ui-automation-properties-and-accstate"></a>Automazione interfaccia utente proprietà e accState



| accState                                                                                      | Automazione interfaccia utente proprietà                                                                                                                                                        | Modifica dello stato dei trigger |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------|
| [**STATE \_ SYSTEM \_ CHECKED**](object-state-constants.md)                 | Per ControlType = "checkbox" usare ToggleState.On. Per "radiobutton" usare [ **SelectionItemPattern::IsSelected**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-get_currentisselected) | Sì                   |
| [**STATO \_ ATTIVO \_ DEL SISTEMA**](object-state-constants.md)             | IsKeyboardFocusableProperty                                                                                                                                                   | No                    |
| [**STATO \_ ATTIVO DEL \_ SISTEMA**](object-state-constants.md)                 | HasKeyboardFocusProperty                                                                                                                                                      | No                    |
| [**STATE \_ SYSTEM \_ PROTECTED**](object-state-constants.md)             | IsPasswordProperty                                                                                                                                                            | No                    |
| [**STATE \_ SYSTEM \_ READONLY**](object-state-constants.md)               | IsReadOnlyProperty (pattern di controllo Value e pattern di controllo RangeValue)                                                                                                     | No                    |
| [**SISTEMA \_ DI STATO NON \_ DISPONIBILE**](object-state-constants.md)         | IsEnabledProperty                                                                                                                                                             | Sì                   |
| [**STATO \_ COLLEGATO AL \_ SISTEMA**](object-state-constants.md)                   | ControlTypeProperty = "hyperlink"                                                                                                                                             | No                    |
| [**STATE \_ SYSTEM \_ SELECTABLE**](object-state-constants.md)           | SelectionItemPattern è supportato                                                                                                                                             | No                    |
| [**STATE \_ SYSTEM \_ SELECTED**](object-state-constants.md)               | IsSelectedProperty (pattern di controllo SelectionItem)                                                                                                                            | No                    |
| [**SISTEMA \_ DI STATO \_ COMPRESSO**](object-state-constants.md)             | ExpandCollapseState = Compresso                                                                                                                                               | Sì                   |
| [**STATE \_ SYSTEM \_ EXPANDED**](object-state-constants.md)               | ExpandCollapseState = Expanded o PartiallyExpanded                                                                                                                           | Sì                   |
| [**STATE \_ SYSTEM \_ HASPOPUP**](object-state-constants.md)               | Voci di menu che supportano Espandi/Comprimi                                                                                                                                       | No                    |
| [**SISTEMA \_ DI STATO \_ MISTO**](object-state-constants.md)                     | ToggleState = Indeterminato                                                                                                                                                   | No                    |
| [**STATE \_ SYSTEM \_ SIZEABLE**](object-state-constants.md)               | [**IUIAutomationTransformPattern::CanResize**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtransformpattern-get_currentcanresize)                                                                     | No                    |
| [**SISTEMA \_ DI STATO \_ SPOSTABILE**](object-state-constants.md)               | [**IUIAutomationTransformPattern::CanMove**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtransformpattern-get_currentcanmove)                                                                         | No                    |
| [**STATE \_ SYSTEM \_ MULTISELECTABLE**](object-state-constants.md) | [**IUIAutomationSelectionPattern::CanSelectMultiple**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionpattern-get_currentcanselectmultiple)                                                     | No                    |



 

### <a name="selection-and-focus"></a>Selezione e stato attivo



| Iaccessible                                                            | Automazione interfaccia utente                                                                          |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)         | [**IUIAutomation::FocusedElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement)        |
| [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                | Per informazioni dettagliate, vedere la Automazione interfaccia utente proprietà e la tabella accSelect SELFLAGs.             |
| [**get \_ accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection) | [**SelectionPattern::GetSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-getselection) |



 

### <a name="ui-automation-properties-and-accselect-selflags"></a>Automazione interfaccia utente proprietà e accSelect SELFLAG



| accSelect SELFLAG                                                  | Automazione interfaccia utente proprietà                                                                                                         |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**SELFLAG \_ NONE**](selflag.md)                       | Non disponibile                                                                                                                  |
| SELFLAG \_ TAKFOCUS                                                   | [**IUIAutomationElement::SetFocus**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-setfocus)                                                 |
| [**SELFLAG \_ TAKESELECTION**](selflag.md)     | [**IUIAutomationSelectionItemPattern::Select**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-select)                           |
| [**SELFLAG \_ ADDSELECTION**](selflag.md)       | [**IUIAutomationSelectionItemPattern::AddToSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-addtoselection)           |
| SELFLAG \_ TAKEREMOVESELECTION                                        | [**IUIAutomationSelectionItemPattern::RemoveFromSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-removefromselection) |
| [**SELFLAG \_ EXTENDSELECTION**](selflag.md) | Non disponibile                                                                                                                  |



 

### <a name="spatial-mapping"></a>Mapping spaziale



| Iaccessible                                                 | Automazione interfaccia utente                                                                                                                        |
|-------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) | Proprietà BoundingRectangleProperty                                                                                                            |
| [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)   | [**IRawElementProviderFragmentRoot::ElementProviderFromPoint**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragmentroot-elementproviderfrompoint) |



 

### <a name="events"></a>Eventi



| System-Level costanti evento                                                             | Automazione interfaccia utente                                                                                                           |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**MENU \_ SISTEMA \_ EVENTIPOPUPSTART**](event-constants.md)     | [**Interfaccia \_ utente MenuOpenedEventId**](uiauto-event-ids.md) (Nota: deve verificare se si tratta di una finestra popup). |
| [**MENU \_ SISTEMA \_ EVENTIPOPUPEND**](event-constants.md)         | [**UIA \_ MenuClosedEventId**](uiauto-event-ids.md)                                                |
| [**MENU \_ SISTEMA \_ EVENTIAVVIO**](event-constants.md)               | [**UIA \_ MenuModeStartEventId**](uiauto-event-ids.md)                                          |
| [**MENU \_ DI SISTEMA \_ EVENTIEND**](event-constants.md)                   | [**UIA \_ MenuModeEndEventId**](uiauto-event-ids.md)                                              |
| [**SUONO \_ DEL SISTEMA DI \_ EVENTI**](event-constants.md)                       |                                                                                                                         |
| [**AVVISO \_ DEL SISTEMA DI \_ EVENTI**](event-constants.md)                       |                                                                                                                         |
| [**ACQUISIZIONE \_ DEL SISTEMA DI \_ EVENTIAVVIO**](event-constants.md)         |                                                                                                                         |
| [**ACQUISIZIONE \_ DEL SISTEMA DI \_ EVENTIEND**](event-constants.md)             |                                                                                                                         |
| [**FINESTRA DI \_ DIALOGO \_ SISTEMA EVENTIAVVIO**](event-constants.md)           |                                                                                                                         |
| [**FINESTRA DI \_ DIALOGO \_ SISTEMA EVENTIEND**](event-constants.md)               |                                                                                                                         |
| [**EVENT \_ SYSTEM \_ MOVESIZESTART**](event-constants.md)       |                                                                                                                         |
| [**\_MOVESIZEEND DEL SISTEMA DI \_ EVENTI**](event-constants.md)           |                                                                                                                         |
| [**CONTESTO \_ DEL SISTEMA DI \_ EVENTIHELPSTART**](event-constants.md) |                                                                                                                         |
| [**CONTESTO \_ DEL SISTEMA DI \_ EVENTIHELPEND**](event-constants.md)     | Non rilevante                                                                                                            |
| [**\_DRAGDROPSTART DEL SISTEMA DI \_ EVENTI**](event-constants.md)       |                                                                                                                         |
| [**\_DRAGDROPEND DEL SISTEMA DI \_ EVENTI**](event-constants.md)           |                                                                                                                         |
| [**SWITCH \_ DI SISTEMA \_ EVENTIAVVIO**](event-constants.md)           | Non rilevante                                                                                                            |
| [**SWITCHEND \_ DEL \_ SISTEMA DI EVENTI**](event-constants.md)               | Non rilevante                                                                                                            |
| [**RIDUZIONE AL \_ MINIMO DEL SISTEMA DI \_ EVENTIAVVIO**](event-constants.md)       |                                                                                                                         |
| [**RIDUZIONE \_ A ICONA DEL SISTEMA DI \_ EVENTIEND**](event-constants.md)           |                                                                                                                         |
| [**PRIMO \_ PIANO DEL SISTEMA DI \_ EVENTI**](event-constants.md)             |                                                                                                                         |
| [**SCORRIMENTO \_ DEL SISTEMA DI \_ EVENTIAVVIO**](event-constants.md)     | Non disponibile                                                                                                           |
| [**SCORRIMENTO \_ DEL SISTEMA \_ DI EVENTIEND**](event-constants.md)         | Non disponibile                                                                                                           |



 



| Object-Level costanti evento                                                           | Automazione interfaccia utente                                                                          |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**STATO ATTIVO \_ DELL'OGGETTO \_ EVENTO**](event-constants.md)                     | AutomationFocusChangedEvent                                                            |
| [**VALUECHANGE \_ \_ DELL'OGGETTO EVENTO**](event-constants.md)         | ValueProperty (pattern di controllo Value e pattern di controllo RangeValue)                   |
| [**SELEZIONE \_ DELL'OGGETTO \_ EVENTO**](event-constants.md)             | ElementSelectedEvent (pattern di controllo SelectionItem)                                   |
| [**SELEZIONE \_ \_ DELL'OGGETTO EVENTOAGGIUNGI**](event-constants.md)       | ElementAddedToSelectionEvent (pattern di controllo SelectionItem)                           |
| [**SELEZIONE \_ \_ DELL'OGGETTO EVENTORIMOZIONE**](event-constants.md) | ElementRemovedFromSelectionEvent                                                       |
| [**SELEZIONE \_ \_ DELL'OGGETTO EVENTOWITHIN**](event-constants.md) | EventsSelectionInvalidatedEvent                                                        |
| [**STATECHANGE \_ \_ DELL'OGGETTO EVENTO**](event-constants.md)         | Vedere Automazione interfaccia utente proprietà e la tabella accState per gli stati che attivano una modifica dello stato |



 

 

 




