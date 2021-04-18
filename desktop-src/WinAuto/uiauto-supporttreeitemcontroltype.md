---
title: Tipo di controllo TreeItem
description: In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo TreeItem.
ms.assetid: 03d8a2a7-0b9a-41f8-a9d3-cebba9c25c63
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo TreeItem
- Automazione interfaccia utente, tipo di controllo TreeItem
- Automazione interfaccia utente, struttura ad albero per il tipo di controllo TreeItem
- Automazione interfaccia utente, proprietà per il tipo di controllo TreeItem
- Automazione interfaccia utente, pattern di controllo per il tipo di controllo TreeItem
- Automazione interfaccia utente, eventi per il tipo di controllo TreeItem
- strutture ad albero, tipo di controllo TreeItem
- Proprietà, tipo di controllo TreeItem
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
ms.openlocfilehash: 4c837428a0aeef900779cfccf0a28b46aa276369
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298667"
---
# <a name="treeitem-control-type"></a>Tipo di controllo TreeItem

In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo **TreeItem** .

Il tipo di controllo **TreeItem** rappresenta un nodo all'interno di un contenitore dell'albero. Ciascun nodo può contenere altri nodi, denominati nodi figlio. I nodi padre, ovvero i nodi contenenti nodi figlio, possono essere visualizzati in formato espanso o compresso.

Nelle sezioni seguenti vengono definiti la struttura ad albero, le proprietà, i pattern di controllo e gli eventi di automazione interfaccia utente necessari per il tipo di controllo **TreeItem** . I requisiti di automazione interfaccia utente si applicano a tutti i controlli elemento della struttura ad albero in cui la piattaforma/Framework dell'interfaccia utente integra il supporto di automazione interfaccia utente per i tipi di controllo e

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Pattern di controllo obbligatori](#required-control-patterns)
-   [Eventi obbligatori](#required-events)
-   [Osservazioni:](#remarks)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

Nella tabella seguente viene illustrata una tipica visualizzazione del controllo e del contenuto dell'albero di automazione interfaccia utente relativo ai controlli elemento della struttura ad albero e viene descritto il possibile contenuto di ogni visualizzazione. Per altre informazioni sull'albero di automazione interfaccia utente, vedere [Cenni preliminari sull'albero di automazione interfaccia utente](uiauto-treeoverview.md).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Visualizzazione controlli</th>
<th>Visualizzazione contenuto</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li>TreeItem
<ul>
<li>CheckBox (0 o 1)</li>
<li>Image (0 o 1)</li>
<li>Button (0 o 1)</li>
<li>TreeItem (0 o più)</li>
</ul></li>
</ul></td>
<td><ul>
<li>TreeItem
<ul>
<li>TreeItem (0 o più)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

I controlli elemento albero possono avere zero o più elementi figlio dell'elemento Tree nella visualizzazione contenuto dell'albero di automazione interfaccia utente. Se il controllo elemento della struttura ad albero presenta funzionalità superiori a quelle esposte nei pattern di controllo elencati di seguito, il controllo deve essere basato sul tipo di controllo [DataItem](uiauto-supportdataitemcontroltype.md) .

Gli elementi compressi dell'albero non vengono visualizzati nella visualizzazione controlli o nella visualizzazione contenuto fino a quando non vengono espansi e visibili (oppure è possibile scorrere la visualizzazione).

La visualizzazione controlli può contenere dettagli aggiuntivi per un controllo, tra cui un'immagine associata o un pulsante. Ad esempio, un elemento in una visualizzazione Struttura potrebbe contenere un'immagine e un pulsante per espandere o comprimere la struttura. Questi oggetti dettagliati non vengono visualizzati nella visualizzazione contenuto perché le informazioni sono già rappresentate dall'elemento padre dell'albero.

Gli elementi della struttura ad albero di cui è stato eseguito lo scorrimento sullo schermo vengono visualizzati sia nella visualizzazione del controllo che nella visualizzazione del contenuto dell'albero di automazione interfaccia utente e la proprietà [**IUIAutomationElement:: CurrentIsOffscreen**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentisoffscreen) (o [**CachedIsOffscreen**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedisoffscreen)) è impostata su **true**.

## <a name="relevant-properties"></a>Proprietà rilevanti

La tabella seguente elenca le proprietà di automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per il tipo di controllo **TreeItem** . Per altre informazioni sulle proprietà di automazione interfaccia utente, vedere [recupero di proprietà da elementi di automazione interfaccia utente](uiauto-propertiesforclients.md).



| Proprietà di automazione interfaccia utente                                                                                              | Valore        | Note                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_AUTOMATIONIDPROPERTYID UIA**](uiauto-automation-element-propids.md)                 | Vedere le note.   | Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata della struttura ad albero di automazione interfaccia utente.                                                                                  |
| [**\_BOUNDINGRECTANGLEPROPERTYID UIA**](uiauto-automation-element-propids.md)       | Vedere le note.   | Il rettangolo più esterno che contiene l'intero controllo.                                                                                                                                      |
| [**\_CLICKABLEPOINTPROPERTYID UIA**](uiauto-automation-element-propids.md)             | Vedere le note.   | Questa proprietà deve restituire un percorso che determina la modifica dello stato di selezione dell'elemento dell'albero o lo stato attivo.                                                                                   |
| [**\_CONTROLTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md)                   | **TreeItem** | Questo valore è uguale per tutti i framework dell'interfaccia utente.                                                                                                                                                 |
| [**\_ISCONTENTELEMENTPROPERTYID UIA**](uiauto-automation-element-propids.md)         | **TRUE**     | Il controllo elemento albero viene sempre incluso nella visualizzazione contenuto dell'albero di automazione interfaccia utente.                                                                                                       |
| [**\_ISCONTROLELEMENTPROPERTYID UIA**](uiauto-automation-element-propids.md)         | **TRUE**     | Il controllo elemento albero viene sempre incluso nella visualizzazione controlli dell'albero di automazione interfaccia utente.                                                                                                       |
| [**\_ISKEYBOARDFOCUSABLEPROPERTYID UIA**](uiauto-automation-element-propids.md)   | Vedere le note.   | Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.                                                                                                                     |
| [**\_ISOFFSCREENPROPERTYID UIA**](uiauto-automation-element-propids.md)                   | Vedere le note.   | Questa proprietà indica se un controllo elemento della struttura ad albero viene spostato fuori dallo schermo.                                                                                                               |
| [**\_ITEMSTATUSPROPERTYID UIA**](uiauto-automation-element-propids.md)                     | Vedere le note.   | Se il controllo contiene uno stato aggiornato dinamicamente, è necessario che questa proprietà sia supportata in modo che una tecnologia per l'accesso facilitato possa ricevere aggiornamenti quando lo stato dell'elemento cambia. |
| [**\_ITEMTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md)                         | Vedere le note.   | Se il controllo elemento della struttura ad albero utilizza un'icona visiva per indicare che è un tipo particolare di elemento, questa proprietà deve essere supportata e deve indicare il tipo di elemento.                                   |
| [**\_LABELEDBYPROPERTYID UIA**](uiauto-automation-element-propids.md)                       | **NULL**     | Per i controlli TreeItem l'etichetta viene definita automaticamente.                                                                                                                                                         |
| [**\_LOCALIZEDCONTROLTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md) | Vedere le note.   | Stringa localizzata corrispondente al tipo di controllo TreeItem. Il valore predefinito è "Tree Item" per en-US o English (Stati Uniti).                                                           |
| [**\_NAMEPROPERTYID UIA**](uiauto-automation-element-propids.md)                                 | Vedere le note.   | Questa proprietà espone il testo visualizzato per ogni controllo TreeItem.                                                                                                                          |



 

## <a name="required-control-patterns"></a>Pattern di controllo obbligatori

La tabella seguente elenca i pattern di controllo di automazione interfaccia utente che devono essere supportati da tutti i controlli elemento della struttura ad albero. Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Pattern di controllo/proprietà del pattern                                                  | Supporto/valore                     | Note                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider)                 | Necessario                          | Tutti gli elementi dell'albero devono supportare il pattern di controllo [ExpandCollapse](uiauto-implementingexpandcollapse.md) perché tutti gli elementi possono essere espansi o compressi.                                           |
| [**ExpandCollapseState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate) | Espanso, compresso o nodo foglia | Gli elementi dell'albero sono nodi foglia quando non sono espansi o compressi.                                                                                                                                |
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)                                 | Dipende da                           | Implementare il pattern di controllo [Invoke](uiauto-implementinginvoke.md) se l'elemento della struttura ad albero può eseguire un comando.                                                                                     |
| [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider)                         | Dipende da                           | Implementare il pattern di controllo [ScrollItem](uiauto-implementingscrollitem.md) se il contenitore dell'albero supporta il pattern di controllo [Scroll](uiauto-implementingscroll.md) .                         |
| [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)                   | Dipende da                           | Implementare il pattern di controllo [SelectionItem](uiauto-implementingselectionitem.md) se è possibile disporre di una selezione attiva che viene mantenuta quando l'utente torna al contenitore dell'albero. |
| [**SelectionContainer**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_selectioncontainer)    | Necessario                          | Questa proprietà espone lo stesso contenitore per tutti gli elementi all'interno del contenitore.                                                                                                                      |



 

## <a name="required-events"></a>Eventi obbligatori

La tabella seguente elenca gli eventi di automazione interfaccia utente necessari per supportare i controlli degli elementi di struttura ad albero. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



| Evento di automazione interfaccia utente                                                                                                                                                | Note                                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**\_AUTOMATIONFOCUSCHANGEDEVENTID UIA**](uiauto-event-ids.md)                                                                   |                                                                                                                                |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà BoundingRectanglePropertyId.                              |                                                                                                                                |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ExpandCollapseExpandCollapseStatePropertyId. |                                                                                                                                |
| [**\_Richiama \_ InvokedEventId**](uiauto-event-ids.md)                                                                                  | Se il controllo supporta il pattern di controllo [Invoke](uiauto-implementinginvoke.md) , deve supportare questo evento.               |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsEnabledPropertyId.                                              | Se il controllo supporta la proprietà [**IsEnabled**](uiauto-automation-element-propids.md) , deve supportare questo evento.       |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsOffscreenPropertyId.                                          | Se il controllo supporta la proprietà [**IsOffscreen**](uiauto-automation-element-propids.md) , deve supportare questo evento.     |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà ItemStatusPropertyId.                                            | Se il controllo supporta la proprietà [**ItemStatus**](uiauto-automation-element-propids.md) , deve supportare questo evento.      |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà MultipleViewCurrentViewPropertyId.                     | Se il controllo supporta il pattern di controllo [MultipleView](uiauto-implementingmultipleview.md) , deve supportare questo evento.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà NamePropertyId.                                                        |                                                                                                                                |
| [**\_ElementAddedToSelectionEventId SelectionItem di UIA \_**](uiauto-event-ids.md)                                    | Se il controllo supporta il pattern di controllo [SelectionItem](uiauto-implementingselectionitem.md) , deve supportare questo evento. |
| [**\_ElementRemovedFromSelectionEventId SelectionItem di UIA \_**](uiauto-event-ids.md)                            | Se il controllo supporta il pattern di controllo [SelectionItem](uiauto-implementingselectionitem.md) , deve supportare questo evento. |
| [**\_ElementSelectedEventId SelectionItem di UIA \_**](uiauto-event-ids.md)                                                    | Se il controllo supporta il pattern di controllo [SelectionItem](uiauto-implementingselectionitem.md) , deve supportare questo evento. |
| [**\_STRUCTURECHANGEDEVENTID UIA**](uiauto-event-ids.md)                                                                               |                                                                                                                                |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ToggleToggleStatePropertyId.                                 | Se il controllo supporta il pattern di controllo [interruttore](uiauto-implementingtoggle.md) , deve supportare questo evento.               |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ValueValuePropertyId.                                               | Se il controllo supporta il pattern di controllo [value](uiauto-implementingvalue.md) , deve supportare questo evento.                 |



 

## <a name="remarks"></a>Commenti

Se un elemento della struttura ad albero presenta sottoelementi diversi dai nodi della struttura figlio, il provider deve gestire le informazioni sull'oggetto figlio in modo accurato e chiaro. Nell'automazione dell'interfaccia utente, la struttura ad albero viene gestita dalla gerarchia della struttura ad albero. Grazie alla presenza di uno o più elementi figlio non strutturati, le differenze tra di essi e i nodi effettivi della struttura figlio diventano seriamente ambigui.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente](uiauto-controltypesoverview.md)
</dt> <dt>

[Cenni preliminari su automazione interfaccia utente](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




