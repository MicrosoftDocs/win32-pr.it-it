---
title: Tipo di controllo TreeItem
description: In questo argomento vengono fornite informazioni sul supporto Automazione interfaccia utente microsoft per il tipo di controllo TreeItem.
ms.assetid: 03d8a2a7-0b9a-41f8-a9d3-cebba9c25c63
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo TreeItem
- Automazione interfaccia utente, tipo di controllo TreeItem
- Automazione interfaccia utente,struttura ad albero per il tipo di controllo TreeItem
- Automazione interfaccia utente,properties per il tipo di controllo TreeItem
- Automazione interfaccia utente,pattern di controllo per il tipo di controllo TreeItem
- Automazione interfaccia utente,eventi per il tipo di controllo TreeItem
- strutture ad albero, tipo di controllo TreeItem
- proprietà, tipo di controllo TreeItem
- pattern di controllo, tipo di controllo TreeItem
- eventi, tipo di controllo TreeItem
- supporto per il tipo di controllo TreeItem
- Tipo di controllo TreeItem
- tipi di controllo, struttura ad albero per il tipo di controllo TreeItem
- tipi di controllo, pattern di controllo per il tipo di controllo TreeItem
- tipi di controllo, supporto per TreeItem
- tipi di controllo, TreeItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c07f55ab6d9df8af46253a2428964bdf4ded64c4
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482927"
---
# <a name="treeitem-control-type"></a>Tipo di controllo TreeItem

In questo argomento vengono fornite informazioni sul supporto Automazione interfaccia utente microsoft per il **tipo di controllo TreeItem.**

Il **tipo di controllo TreeItem** rappresenta un nodo all'interno di un contenitore albero. Ciascun nodo può contenere altri nodi, denominati nodi figlio. I nodi padre, ovvero i nodi contenenti nodi figlio, possono essere visualizzati in formato espanso o compresso.

Nelle sezioni seguenti vengono definiti i Automazione interfaccia utente struttura ad albero, le proprietà, i pattern di controllo e gli eventi per il **tipo di controllo TreeItem.** I Automazione interfaccia utente si applicano a tutti i controlli elemento della struttura ad albero in cui il framework o la piattaforma dell'interfaccia utente si integra Automazione interfaccia utente per i tipi di controllo e i pattern di controllo.

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Pattern di controllo obbligatori](#required-control-patterns)
-   [Eventi obbligatori](#required-events)
-   [Osservazioni:](#remarks)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

La tabella seguente illustra un controllo tipico e una visualizzazione contenuto dell'albero Automazione interfaccia utente che riguarda i controlli elemento della struttura ad albero e descrive gli elementi che possono essere contenuti in ogni visualizzazione. Per altre informazioni sull'albero Automazione interfaccia utente, vedere Automazione interfaccia utente [Tree Overview](uiauto-treeoverview.md).




| Visualizzazione controlli | Visualizzazione contenuto | 
|--------------|--------------|
| <ul><li>TreeItem<ul><li>CheckBox (0 o 1)</li><li>Image (0 o 1)</li><li>Button (0 o 1)</li><li>TreeItem (0 o più)</li></ul></li></ul> | <ul><li>TreeItem<ul><li>TreeItem (0 o più)</li></ul></li></ul> | 




 

I controlli tree item possono avere zero o più elementi figlio della struttura ad albero nella visualizzazione contenuto dell'Automazione interfaccia utente albero. Se il controllo elemento della struttura ad albero dispone di funzionalità oltre a quanto esposto nei pattern di controllo elencati di seguito, il controllo deve essere basato sul [tipo di controllo DataItem.](uiauto-supportdataitemcontroltype.md)

Gli elementi della struttura ad albero compressa non vengono visualizzati nella visualizzazione controlli o nella visualizzazione contenuto fino a quando non diventano espansi e visibili (o possono essere scorreti nella visualizzazione).

La visualizzazione controlli può contenere dettagli aggiuntivi per un controllo, tra cui un'immagine associata o un pulsante. Ad esempio, un elemento in una visualizzazione Struttura potrebbe contenere un'immagine e un pulsante per espandere o comprimere la struttura. Questi oggetti dettaglio non vengono visualizzati nella visualizzazione contenuto perché le informazioni sono già rappresentate dall'elemento della struttura ad albero padre.

Gli elementi della struttura ad albero che vengono scorreti dalla schermata vengono visualizzati sia nella visualizzazione controlli che nelle visualizzazioni contenuto dell'albero di Automazione interfaccia utente e la proprietà [**IUIAutomationElement::CurrentIsOffscreen**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentisoffscreen) (o [**CachedIsOffscreen)**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedisoffscreen)deve essere impostata su **TRUE.**

## <a name="relevant-properties"></a>Proprietà rilevanti

Nella tabella seguente sono elencate le Automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per il **tipo di controllo TreeItem.** Per altre informazioni sulle Automazione interfaccia utente, vedere [Recupero di proprietà da Automazione interfaccia utente elementi](uiauto-propertiesforclients.md).



| Proprietà di automazione interfaccia utente                                                                                              | valore        | Note                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Vedere le note.   | Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata dell'Automazione interfaccia utente albero.                                                                                  |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vedere le note.   | Il rettangolo più esterno che contiene l'intero controllo.                                                                                                                                      |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vedere le note.   | Questa proprietà deve restituire una posizione che fa sì che l'elemento della struttura ad albero cambi lo stato di selezione o diventi attivo.                                                                                   |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **TreeItem** | Questo valore è uguale per tutti i framework dell'interfaccia utente.                                                                                                                                                 |
| [**\_IsContentElementPropertyId dell'interfaccia utente**](uiauto-automation-element-propids.md)         | **TRUE**     | Il controllo elemento della struttura ad albero è sempre incluso nella visualizzazione contenuto dell'Automazione interfaccia utente albero.                                                                                                       |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | **TRUE**     | Il controllo elemento della struttura ad albero è sempre incluso nella visualizzazione controlli dell'Automazione interfaccia utente albero.                                                                                                       |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Vedere le note.   | Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.                                                                                                                     |
| [**UIA \_ IsOffscreenPropertyId**](uiauto-automation-element-propids.md)                   | Vedere le note.   | Questa proprietà indica se lo scorrimento di un controllo elemento della struttura ad albero viene disattivato dalla schermata.                                                                                                               |
| [**UIA \_ ItemStatusPropertyId**](uiauto-automation-element-propids.md)                     | Vedere le note.   | Se il controllo contiene lo stato che viene aggiornato dinamicamente, questa proprietà deve essere supportata in modo che un assistive technology possa ricevere aggiornamenti quando lo stato dell'elemento cambia. |
| [**UIA \_ ItemTypePropertyId**](uiauto-automation-element-propids.md)                         | Vedere le note.   | Se il controllo elemento della struttura ad albero usa un'icona visiva per indicare che è un particolare tipo di elemento, questa proprietà deve essere supportata e deve indicare il tipo di elemento.                                   |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | **NULL**     | Per i controlli TreeItem l'etichetta viene definita automaticamente.                                                                                                                                                         |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vedere le note.   | Stringa localizzata corrispondente al tipo di controllo TreeItem. Il valore predefinito è "tree item" per en-US o English (Stati Uniti).                                                           |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Vedere le note.   | Questa proprietà espone il testo visualizzato per ogni controllo TreeItem.                                                                                                                          |



 

## <a name="required-control-patterns"></a>Pattern di controllo obbligatori

Nella tabella seguente sono elencati i Automazione interfaccia utente che devono essere supportati da tutti i controlli elemento della struttura ad albero. Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Pattern di controllo/proprietà del pattern                                                  | Supporto/valore                     | Note                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider)                 | Obbligatoria                          | Tutti gli elementi della struttura ad albero devono supportare il pattern di controllo [ExpandCollapse](uiauto-implementingexpandcollapse.md) perché tutti gli elementi possono essere espansi o compressi.                                           |
| [**ExpandCollapseState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate) | Espanso, compresso o nodo foglia | Gli elementi della struttura ad albero sono nodi foglia quando non sono espansi o compressi.                                                                                                                                |
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)                                 | Dipende da                           | Implementare [il pattern di](uiauto-implementinginvoke.md) controllo Invoke se l'elemento della struttura ad albero può eseguire un comando.                                                                                     |
| [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider)                         | Dipende da                           | Implementare il pattern [di controllo ScrollItem](uiauto-implementingscrollitem.md) se il contenitore della struttura ad albero supporta il pattern [di controllo Scroll.](uiauto-implementingscroll.md)                         |
| [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)                   | Dipende da                           | Implementare il pattern [di controllo SelectionItem](uiauto-implementingselectionitem.md) se è possibile mantenere una selezione attiva quando l'utente torna al contenitore dell'albero. |
| [**Selectioncontainer**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_selectioncontainer)    | Obbligatoria                          | Questa proprietà espone lo stesso contenitore per tutti gli elementi all'interno del contenitore.                                                                                                                      |



 

## <a name="required-events"></a>Eventi obbligatori

La tabella seguente elenca gli eventi Automazione interfaccia utente che i controlli tree item devono supportare. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automazione interfaccia utente eventi                                                                                                                                                | Note                                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                                   |                                                                                                                                |
| [**Interfaccia \_ utente Evento di modifica della proprietà BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md)                              |                                                                                                                                |
| [**Interfaccia \_ utente Evento di modifica della proprietà ExpandCollapseExpandCollapseStatePropertyId.**](uiauto-control-pattern-propids.md) |                                                                                                                                |
| [**\_ \_ InvokedEventId dell'interfaccia utente**](uiauto-event-ids.md)                                                                                  | Se il controllo supporta il pattern [di controllo Invoke,](uiauto-implementinginvoke.md) deve supportare questo evento.               |
| [**Interfaccia \_ utente Evento di modifica della proprietà IsEnabledPropertyId.**](uiauto-automation-element-propids.md)                                              | Se il controllo supporta la [**proprietà IsEnabled,**](uiauto-automation-element-propids.md) deve supportare questo evento.       |
| [**Interfaccia \_ utente Evento di modifica della proprietà IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)                                          | Se il controllo supporta la [**proprietà IsOffscreen,**](uiauto-automation-element-propids.md) deve supportare questo evento.     |
| [**Interfaccia \_ utente Evento di modifica della proprietà ItemStatusPropertyId.**](uiauto-automation-element-propids.md)                                            | Se il controllo supporta la [**proprietà ItemStatus,**](uiauto-automation-element-propids.md) deve supportare questo evento.      |
| [**Interfaccia \_ utente Evento di modifica della proprietà MultipleViewCurrentViewPropertyId.**](uiauto-control-pattern-propids.md)                     | Se il controllo supporta il pattern [di controllo MultipleView,](uiauto-implementingmultipleview.md) deve supportare questo evento.   |
| [**Interfaccia \_ utente Evento di modifica**](uiauto-automation-element-propids.md) della proprietà NamePropertyId.                                                        |                                                                                                                                |
| [**Elemento \_ SelectionItem \_ dell'interfaccia utenteAddedToSelectionEventId**](uiauto-event-ids.md)                                    | Se il controllo supporta il pattern [di controllo SelectionItem,](uiauto-implementingselectionitem.md) deve supportare questo evento. |
| [**UIA \_ SelectionItem \_ ElementRemovedFromSelectionEventId**](uiauto-event-ids.md)                            | Se il controllo supporta il pattern [di controllo SelectionItem,](uiauto-implementingselectionitem.md) deve supportare questo evento. |
| [**UIA \_ SelectionItem \_ ElementSelectedEventId**](uiauto-event-ids.md)                                                    | Se il controllo supporta il pattern [di controllo SelectionItem,](uiauto-implementingselectionitem.md) deve supportare questo evento. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                               |                                                                                                                                |
| [**Interfaccia \_ utente Evento di modifica della proprietà ToggleToggleStatePropertyId.**](uiauto-control-pattern-propids.md)                                 | Se il controllo supporta il pattern [di controllo Toggle,](uiauto-implementingtoggle.md) deve supportare questo evento.               |
| [**Interfaccia \_ utente Evento di modifica della proprietà ValueValuePropertyId.**](uiauto-control-pattern-propids.md)                                               | Se il controllo supporta il pattern [di controllo Value,](uiauto-implementingvalue.md) deve supportare questo evento.                 |



 

## <a name="remarks"></a>Commenti

Se un elemento della struttura ad albero include sottoelementi diversi da nodi figlio della struttura, il provider deve gestire con attenzione e chiaramente le informazioni sull'oggetto figlio. In Automazione interfaccia utente, la struttura ad albero viene gestita dalla gerarchia dell'albero stessa. Con uno o più nodi figlio non di struttura, le differenze tra di essi e i nodi della struttura figlio effettivi diventano molto ambigue.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente](uiauto-controltypesoverview.md)
</dt> <dt>

[Cenni preliminari su automazione interfaccia utente](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




