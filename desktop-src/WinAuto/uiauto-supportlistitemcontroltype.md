---
title: Tipo di controllo ListItem
description: In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo ListItem.
ms.assetid: 8cb579ab-92c9-4311-aad7-5363f4cf2eaf
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo ListItem
- Automazione interfaccia utente, tipo di controllo ListItem
- Automazione interfaccia utente, struttura ad albero per il tipo di controllo ListItem
- Automazione interfaccia utente, proprietà per il tipo di controllo ListItem
- Automazione interfaccia utente, pattern di controllo per il tipo di controllo ListItem
- Automazione interfaccia utente, eventi per il tipo di controllo ListItem
- strutture ad albero, tipo di controllo ListItem
- Proprietà, tipo di controllo ListItem
- pattern di controllo, tipo di controllo ListItem
- eventi, tipo di controllo ListItem
- supporto per il tipo di controllo ListItem
- Tipo di controllo ListItem
- tipi di controllo, struttura ad albero per il tipo di controllo ListItem
- tipi di controllo, pattern di controllo per il tipo di controllo ListItem
- tipi di controllo, supporto per ListItem
- tipi di controllo, ListItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5093ef62793d96a5438c27edd29e96a96cfa407
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298152"
---
# <a name="listitem-control-type"></a>Tipo di controllo ListItem

In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo **ListItem** .

I controlli elemento elenco sono un esempio di controlli che implementano il tipo di controllo **ListItem** .

Nelle sezioni seguenti vengono definiti la struttura ad albero, le proprietà, i pattern di controllo e gli eventi di automazione interfaccia utente necessari per il tipo di controllo **ListItem** . I requisiti di automazione interfaccia utente si applicano a tutti i controlli elemento elenco in cui la piattaforma/Framework dell'interfaccia utente integra il supporto di automazione interfaccia utente per i tipi di controllo e pattern di controllo

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Pattern di controllo obbligatori](#required-control-patterns)
-   [Eventi obbligatori](#required-events)
-   [Osservazioni:](#remarks)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

Nella tabella seguente viene illustrata una tipica visualizzazione del controllo e del contenuto della struttura ad albero di automazione interfaccia utente relativa ai controlli elemento elenco e viene descritto il possibile contenuto di ogni visualizzazione. Per altre informazioni sull'albero di automazione interfaccia utente, vedere [Cenni preliminari sull'albero di automazione interfaccia utente](uiauto-treeoverview.md).



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
<li>ListItem
<ul>
<li>Image (0 o più)</li>
<li>Text (0 o più)</li>
<li>Edit (0 o più)</li>
</ul></li>
</ul></td>
<td><ul>
<li>ListItem</li>
</ul></td>
</tr>
</tbody>
</table>



 

Gli elementi figlio di un controllo elemento elenco all'interno della visualizzazione contenuto dell'albero di automazione interfaccia utente devono sempre visualizzare zero elementi figlio. Se la struttura del controllo è tale che gli altri elementi sono contenuti sotto l'elemento dell'elenco, è necessario che seguano i requisiti per il supporto di automazione interfaccia utente per il tipo di controllo [TreeItem](uiauto-supporttreeitemcontroltype.md) .

## <a name="relevant-properties"></a>Proprietà rilevanti

La tabella seguente elenca le proprietà di automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per il tipo di controllo **ListItem** . Per altre informazioni sulle proprietà di automazione interfaccia utente, vedere [recupero di proprietà da elementi di automazione interfaccia utente](uiauto-propertiesforclients.md).



| Proprietà di automazione interfaccia utente                                                                                              | Valore        | Note                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_AUTOMATIONIDPROPERTYID UIA**](uiauto-automation-element-propids.md)                 | Vedere le note.   | Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata della struttura ad albero di automazione interfaccia utente. Allocare la proprietà **AutomationId** per un elemento elenco se l'elemento è noto come coerente tra istanze diverse dell'interfaccia utente. Se l'elemento elenco viene popolato in modo dinamico e non stimabile, lasciare vuota la proprietà **AutomationId** .                                                          |
| [**\_BOUNDINGRECTANGLEPROPERTYID UIA**](uiauto-automation-element-propids.md)       | Vedere le note.   | Il valore di questa proprietà include l'area dei contenuti immagine e testo dell'elemento dell'elenco.                                                                                                                                                                                                                                                                                                                              |
| [**\_CLICKABLEPOINTPROPERTYID UIA**](uiauto-automation-element-propids.md)             | Dipende da      | Se il controllo elenco ha un punto selezionabile, ovvero un punto su cui è possibile fare clic per fare in modo che l'elenco abbia lo stato attivo, tale punto deve essere esposto tramite questa proprietà. Se il controllo elenco è completamente coperto da elementi elenco discendente, restituirà l' [**errore \_ \_ NOCLICKABLEPOINT**](uiauto-error-codes.md) di gestione delle attività e per indicare che il client deve richiedere un elemento all'interno del controllo elenco per un punto selezionabile. |
| [**\_CONTROLTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md)                   | **ListItem** | Questo valore è uguale per tutti i framework dell'interfaccia utente.                                                                                                                                                                                                                                                                                                                                                                                     |
| [**\_HELPTEXTPROPERTYID UIA**](uiauto-automation-element-propids.md)                         | Vedere le note.   | Il testo della Guida per gli elenchi deve spiegare il motivo per cui all'utente viene chiesto di effettuare una selezione da un elenco di opzioni, che è in genere lo stesso tipo di informazioni visualizzate tramite una descrizione comando. Ad esempio, "selezionare un elemento per impostare la risoluzione dello schermo per il monitoraggio".                                                                                                                                                    |
| [**\_ISCONTENTELEMENTPROPERTYID UIA**](uiauto-automation-element-propids.md)         | **TRUE**     | Il controllo elenco è sempre incluso nella visualizzazione contenuto dell'albero di automazione interfaccia utente.                                                                                                                                                                                                                                                                                                                                                |
| [**\_ISCONTROLELEMENTPROPERTYID UIA**](uiauto-automation-element-propids.md)         | **TRUE**     | Il controllo elenco è sempre incluso nella visualizzazione controlli dell'albero di automazione interfaccia utente.                                                                                                                                                                                                                                                                                                                                                |
| [**\_ISKEYBOARDFOCUSABLEPROPERTYID UIA**](uiauto-automation-element-propids.md)   | Vedere le note.   | Se il contenitore può accettare input da tastiera, il valore di questa proprietà deve essere **true**.                                                                                                                                                                                                                                                                                                                                           |
| [**\_ISOFFSCREENPROPERTYID UIA**](uiauto-automation-element-propids.md)                   | Dipende da      | Questa proprietà deve restituire un valore che indica se l'elemento elenco è attualmente visualizzato in visualizzazione all'interno del contenitore padre che implementa il pattern di controllo [Scroll](uiauto-implementingscroll.md) .                                                                                                                                                                                                                                  |
| [**\_ITEMSTATUSPROPERTYID UIA**](uiauto-automation-element-propids.md)                     | Dipende da      | Se il controllo contiene uno stato aggiornato dinamicamente, è necessario che questa proprietà sia supportata in modo che una tecnologia per l'accesso facilitato possa ricevere aggiornamenti quando lo stato dell'elemento cambia.                                                                                                                                                                                                                                     |
| [**\_ITEMTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md)                         | Dipende da      | Questa proprietà deve essere esposta per i controlli elemento elenco che rappresentano un oggetto sottostante. In genere, questi controlli elemento elenco includono un'icona associato al controllo che gli utenti associano all'oggetto sottostante.                                                                                                                                                                                                   |
| [**\_LABELEDBYPROPERTYID UIA**](uiauto-automation-element-propids.md)                       | Vedere le note.   | Se è presente un'etichetta di testo statico, questa proprietà deve esporre un riferimento a tale controllo.                                                                                                                                                                                                                                                                                                                                       |
| [**\_LOCALIZEDCONTROLTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md) | Vedere le note.   | Stringa localizzata corrispondente al tipo di controllo **ListItem** . Il valore predefinito è "Item List" per en-US o English (Stati Uniti).                                                                                                                                                                                                                                                                                           |
| [**\_NAMEPROPERTYID UIA**](uiauto-automation-element-propids.md)                                 | Vedere le note.   | Il valore della proprietà Name di un controllo elemento elenco deriva dall'etichetta di testo dell'elemento.                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="required-control-patterns"></a>Pattern di controllo obbligatori

La tabella seguente elenca i pattern di controllo di automazione interfaccia utente che devono essere supportati da tutti i controlli elemento elenco. Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Pattern di controllo                                                   | Supporto | Note                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Dipende da | Se l'elemento può essere modificato per mostrare o nascondere informazioni, è necessario implementare il pattern di controllo [ExpandCollapse](uiauto-implementingexpandcollapse.md) .                                                                                                                                                                                                                        |
| [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)             | Dipende da | Se la navigazione spaziale da elemento a elemento è supportata all'interno del contenitore elenco e il contenitore viene disposto in righe e colonne, è necessario implementare il pattern di controllo [GridItem](uiauto-implementinggriditem.md) .                                                                                                                                                                  |
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)                 | Dipende da | Se l'elemento include un comando che può essere eseguito su di esso, separato dalla selezione, è necessario implementare il pattern di controllo [Invoke](uiauto-implementinginvoke.md) . In genere si tratta di un'azione associata all'esecuzione del doppio clic sul controllo elemento elenco. Ad esempio, l'avvio di un documento da Esplora risorse o la riproduzione di un file musicale in Microsoft Windows Media Player.        |
| [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider)         | Dipende da | Se l'elemento elenco è contenuto all'interno di un contenitore scorrevole, è necessario implementare il pattern di controllo [ScrollItem](uiauto-implementingscrollitem.md) .                                                                                                                                                                                                                       |
| [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)   | Dipende da | Un controllo elemento elenco che supporta la selezione deve implementare il pattern di controllo [SelectionItem](uiauto-implementingselectionitem.md) . Ciò consente ai controlli elemento elenco di indicare quando sono selezionati.                                                                                                                                                                             |
| [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)                 | Dipende da | Se l'elemento elenco è selezionabile e l'azione non esegue una modifica dello stato di selezione, è necessario implementare il pattern di controllo di [attivazione/disattivazione](uiauto-implementingtoggle.md) .                                                                                                                                                                                                            |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)                   | Dipende da | Se l'elemento può essere modificato, è necessario implementare il pattern di controllo [value](uiauto-implementingvalue.md) . Le modifiche apportate al controllo elemento elenco provocheranno modifiche ai valori delle proprietà [**\_ NamePropertyId**](uiauto-automation-element-propids.md) e [**\_ ValueValuePropertyId**](uiauto-control-pattern-propids.md) UIA. |



 

## <a name="required-events"></a>Eventi obbligatori

La tabella seguente elenca gli eventi di automazione interfaccia utente che sono necessari per supportare i controlli elemento elenco. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



| Evento di automazione interfaccia utente                                                                                                                                                | Note                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**\_AUTOMATIONFOCUSCHANGEDEVENTID UIA**](uiauto-event-ids.md)                                                                   |                                                                                                                                  |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà BoundingRectanglePropertyId.                              |                                                                                                                                  |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ExpandCollapseExpandCollapseStatePropertyId. | Se il controllo supporta il pattern di controllo [ExpandCollapse](uiauto-implementingexpandcollapse.md) , deve supportare questo evento. |
| [**\_Richiama \_ InvokedEventId**](uiauto-event-ids.md)                                                                                  | Se il controllo supporta il pattern di controllo [Invoke](uiauto-implementinginvoke.md) , deve supportare questo evento.                 |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsEnabledPropertyId.                                              | Se il controllo supporta la proprietà [**IsEnabled**](uiauto-automation-element-propids.md) , deve supportare questo evento.         |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsOffscreenPropertyId.                                          | Se il controllo supporta la proprietà [**IsOffscreen**](uiauto-automation-element-propids.md) , deve supportare questo evento.       |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà ItemStatusPropertyId.                                            | Se il controllo supporta la proprietà [**ItemStatus**](uiauto-automation-element-propids.md) , deve supportare questo evento.        |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà NamePropertyId.                                                        |                                                                                                                                  |
| [**\_ElementAddedToSelectionEventId SelectionItem di UIA \_**](uiauto-event-ids.md)                                    | Se il controllo supporta il pattern di controllo [SelectionItem](uiauto-implementingselectionitem.md) , deve supportare questo evento.   |
| [**\_ElementRemovedFromSelectionEventId SelectionItem di UIA \_**](uiauto-event-ids.md)                            | Se il controllo supporta il pattern di controllo [SelectionItem](uiauto-implementingselectionitem.md) , deve supportare questo evento.   |
| [**\_ElementSelectedEventId SelectionItem di UIA \_**](uiauto-event-ids.md)                                                    | Se il controllo supporta il pattern di controllo [SelectionItem](uiauto-implementingselectionitem.md) , deve supportare questo evento.   |
| [**\_STRUCTURECHANGEDEVENTID UIA**](uiauto-event-ids.md)                                                                               |                                                                                                                                  |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ToggleToggleStatePropertyId.                                 | Se il controllo supporta il pattern di controllo [interruttore](uiauto-implementingtoggle.md) , deve supportare questo evento.                 |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ValueValuePropertyId.                                               | Se il controllo supporta il pattern di controllo [value](uiauto-implementingvalue.md) , deve supportare questo evento.                   |



 

## <a name="remarks"></a>Commenti

Se un contenitore ospita elementi elenco, il mezzo principale di navigazione dovrebbe passare agli elementi dell'elenco. Posizionare l'attenzione sui sottoelementi tramite la navigazione con elenco può creare confusione per gli utenti e gli strumenti di accessibilità. Se il contenitore ospita un elenco verticale di elementi, premere i tasti freccia su e freccia giù per spostarsi tra gli elementi, ma la pressione della freccia destra e dei tasti di direzione sinistra può passare a sottoelementi dell'elemento con lo stato attivo, ad esempio colonne elenco o sottoelementi dell'interfaccia utente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente](uiauto-controltypesoverview.md)
</dt> <dt>

[Cenni preliminari su automazione interfaccia utente](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




