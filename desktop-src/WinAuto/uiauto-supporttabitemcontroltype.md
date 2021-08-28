---
title: Tipo di controllo TabItem
description: Questo argomento fornisce informazioni sul supporto di Microsoft Automazione interfaccia utente per il tipo di controllo TabItem.
ms.assetid: 97b8c043-1ac5-4e14-be80-8687300a10a2
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo TabItem
- Automazione interfaccia utente,Tipo di controllo TabItem
- Automazione interfaccia utente,struttura ad albero per il tipo di controllo TabItem
- Automazione interfaccia utente,proprietà per il tipo di controllo TabItem
- Automazione interfaccia utente,pattern di controllo per il tipo di controllo TabItem
- Automazione interfaccia utente,eventi per il tipo di controllo TabItem
- strutture ad albero, tipo di controllo TabItem
- proprietà, tipo di controllo TabItem
- pattern di controllo, tipo di controllo TabItem
- eventi, tipo di controllo TabItem
- supporto per il tipo di controllo TabItem
- Tipo di controllo TabItem
- tipi di controllo, struttura ad albero per il tipo di controllo TabItem
- tipi di controllo, pattern di controllo per il tipo di controllo TabItem
- tipi di controllo, supporto per TabItem
- tipi di controllo, TabItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f82b96f5ae64b4cb22d650d6d349f18cb68619d5
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469108"
---
# <a name="tabitem-control-type"></a>Tipo di controllo TabItem

Questo argomento fornisce informazioni sul supporto di Microsoft Automazione interfaccia utente per il **tipo di controllo TabItem.**

Un controllo voce di scheda viene usato come controllo in un controllo Struttura a schede che seleziona una pagina specifica da visualizzare in una finestra.

Le sezioni seguenti definiscono la struttura Automazione interfaccia utente struttura ad albero, le proprietà, i pattern di controllo e gli eventi per il **tipo di controllo TabItem.** I Automazione interfaccia utente si applicano a tutti i controlli elemento scheda in cui il framework o la piattaforma dell'interfaccia utente si integra Automazione interfaccia utente per i tipi di controllo e i pattern di controllo.

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Pattern di controllo obbligatori](#required-control-patterns)
-   [Eventi obbligatori](#required-events)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

La tabella seguente illustra un controllo tipico e una visualizzazione contenuto dell'albero Automazione interfaccia utente relativo ai controlli elemento scheda e descrive gli elementi che possono essere contenuti in ogni visualizzazione. Per altre informazioni sull'albero Automazione interfaccia utente, vedere Automazione interfaccia utente [Tree Overview](uiauto-treeoverview.md).




| Visualizzazione controlli | Visualizzazione contenuto | 
|--------------|--------------|
| <ul><li>TabItem<ul><li>Image (0 o 1)</li><li>Testo</li><li>Riquadro<ul><li>Vari controlli (0 o più)</li></ul></li></ul></li></ul> | <ul><li>TabItem<ul><li>Riquadro<ul><li>Vari controlli (0 o più)</li></ul></li></ul></li></ul> | 




 

## <a name="relevant-properties"></a>Proprietà rilevanti

La tabella seguente elenca le Automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per il **tipo di controllo TabItem.** Per altre informazioni sulle Automazione interfaccia utente, vedere [Recupero di proprietà da Automazione interfaccia utente elementi](uiauto-propertiesforclients.md).



| Proprietà di automazione interfaccia utente                                                                                              | valore       | Note                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|-------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Vedere le note.  | Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata dell'Automazione interfaccia utente albero.                                |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vedere le note.  | Il rettangolo più esterno che contiene l'intero controllo.                                                                                    |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vedere le note.  | Il controllo voce di scheda deve avere un punto su cui è possibile fare clic per selezionare l'elemento.                                                   |
| [**UIA \_ ControllerForPropertyId**](uiauto-automation-element-propids.md)               | Vedere le note.  | Questa proprietà può essere usata come puntatore al riquadro schede associato. Ciò risulta utile nel caso in cui non possa ospitare un riquadro come figlio dell'oggetto voce di scheda. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **TabItem** | Questo valore è uguale per tutti i framework dell'interfaccia utente.                                                                                               |
| [**\_IsContentElementPropertyId dell'interfaccia utente**](uiauto-automation-element-propids.md)         | true        | Il controllo elemento scheda è sempre incluso nella visualizzazione contenuto dell'Automazione interfaccia utente struttura ad albero.                                                      |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | true        | Il controllo elemento scheda è sempre incluso nella visualizzazione controlli dell'Automazione interfaccia utente struttura ad albero.                                                      |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Vedere le note.  | Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.                                                                   |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Null        | Il controllo voce di scheda non ha un'etichetta di testo statico.                                                                                     |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vedere le note.  | Stringa localizzata corrispondente al **tipo di controllo TabItem.** Il valore predefinito è "tab item" per en-US o English (Stati Uniti).       |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Vedere le note.  | Controllo elemento scheda auto-etichettato.                                                                                                          |



 

## <a name="required-control-patterns"></a>Pattern di controllo obbligatori

Nella tabella seguente sono elencati i Automazione interfaccia utente di controllo personalizzati che devono essere supportati da tutti i controlli Elemento scheda. Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Pattern di controllo                                                 | Supporto  | Note                                                                                                                    |
|-----------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------|
| [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider) | Obbligatoria | Il controllo Elemento scheda deve supportare [**IUIAutomationSelectionItemPattern.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationselectionitempattern) |
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)               | Mai    | Il controllo elemento scheda non supporta mai [**IUIAutomationInvokePattern.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationinvokepattern)             |



 

## <a name="required-events"></a>Eventi obbligatori

La tabella seguente elenca gli eventi Automazione interfaccia utente che i controlli Elemento scheda devono supportare. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automazione interfaccia utente eventi                                                                                                                     | Note                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                        |                                                                                                                            |
| [**Interfaccia \_ utente Evento di modifica della proprietà BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md)   |                                                                                                                            |
| [**Interfaccia \_ utente Evento di modifica della proprietà IsEnabledPropertyId.**](uiauto-automation-element-propids.md)                   | Se il controllo supporta la [**proprietà IsEnabled,**](uiauto-automation-element-propids.md) deve supportare questo evento.   |
| [**Interfaccia \_ utente Evento di modifica della proprietà IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)               | Se il controllo supporta la [**proprietà IsOffscreen,**](uiauto-automation-element-propids.md) deve supportare questo evento. |
| [**UIA \_ SelectionItem \_ ElementRemovedFromSelectionEventId**](uiauto-event-ids.md) |                                                                                                                            |
| [**UIA \_ SelectionItem \_ ElementSelectedEventId**](uiauto-event-ids.md)                         |                                                                                                                            |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                    |                                                                                                                            |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente](uiauto-controltypesoverview.md)
</dt> <dt>

[Cenni preliminari su automazione interfaccia utente](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




