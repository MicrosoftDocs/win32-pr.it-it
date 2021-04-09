---
title: Tipo di controllo DataItem
description: In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo DataItem.
ms.assetid: def52fe7-9f05-4cd0-8a46-af4e2e3ba03e
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo DataItem
- Automazione interfaccia utente, tipo di controllo DataItem
- Automazione interfaccia utente, struttura ad albero per il tipo di controllo DataItem
- Automazione interfaccia utente, proprietà per il tipo di controllo DataItem
- Automazione interfaccia utente, pattern di controllo per il tipo di controllo DataItem
- Automazione interfaccia utente, eventi per il tipo di controllo DataItem
- Automazione interfaccia utente, elenchi di grandi dimensioni e tipo di controllo DataItem
- strutture ad albero, tipo di controllo DataItem
- Proprietà, tipo di controllo DataItem
- pattern di controllo, tipo di controllo DataItem
- eventi, tipo di controllo DataItem
- elenchi di grandi dimensioni
- supporto per il tipo di controllo DataItem
- Tipo di controllo DataItem
- tipi di controllo, struttura ad albero per il tipo di controllo DataItem
- tipi di controllo, pattern di controllo per il tipo di controllo DataItem
- tipi di controllo, elenchi di grandi dimensioni e tipo di controllo DataItem
- tipi di controllo, supporto per DataItem
- tipi di controllo, DataItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0902cc593ec7f9104ed27031caa2785b7cb9756
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044609"
---
# <a name="dataitem-control-type"></a>Tipo di controllo DataItem

In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo **DataItem** .

Una voce in un elenco Contatti, ad esempio, è un controllo elemento dati. Un controllo elemento dati contiene informazioni di interesse per un utente finale. È più complicato del semplice elemento elenco poiché contiene informazioni più dettagliate.

Nelle sezioni seguenti vengono definiti la struttura ad albero, le proprietà, i pattern di controllo e gli eventi di automazione interfaccia utente necessari per il tipo di controllo **DataItem** . I requisiti di automazione interfaccia utente si applicano a tutti i controlli elemento dati in cui la piattaforma/Framework dell'interfaccia utente integra il supporto di automazione interfaccia utente per i tipi di controllo e pattern di controllo

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Pattern di controllo obbligatori](#required-control-patterns)
-   [Utilizzo di oggetti dataItems in elenchi di grandi dimensioni](#working-with-dataitems-in-large-lists)
-   [Eventi obbligatori](#required-events)
-   [Esempio del tipo di controllo DataItem](#dataitem-control-type-example)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

Nella tabella seguente viene illustrata una tipica visualizzazione del controllo e del contenuto dell'albero di automazione interfaccia utente relativo ai controlli elemento dati e viene descritto il possibile contenuto di ogni visualizzazione. Per altre informazioni sull'albero di automazione interfaccia utente, vedere [Cenni preliminari sull'albero di automazione interfaccia utente](uiauto-treeoverview.md).



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
<li>DataItem
<ul>
<li>Varia (0 o più, può essere strutturato in una gerarchia)</li>
</ul></li>
</ul></td>
<td><ul>
<li>DataItem
<ul>
<li>Varia (0 o più, può essere strutturato in una gerarchia)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

Un elemento dati in una griglia di dati può contenere vari tipi di oggetti, incluso un altro livello di elementi dati o specifici elementi di griglia quali testo, immagini o controlli di modifica. Se l'elemento dati dispone di un ruolo di oggetto specifico, l'elemento deve essere esposto come tipo di controllo specifico; ad esempio, un tipo di controllo [ListItem](uiauto-supportlistitemcontroltype.md) per un elemento di dati selezionabile nella griglia.

## <a name="relevant-properties"></a>Proprietà rilevanti

La tabella seguente elenca le proprietà di automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per il tipo di controllo DataItem. Per altre informazioni sulle proprietà di automazione interfaccia utente, vedere [recupero di proprietà da elementi di automazione interfaccia utente](uiauto-propertiesforclients.md).



| Proprietà di automazione interfaccia utente                                                                                              | Valore        | Note                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_AUTOMATIONIDPROPERTYID UIA**](uiauto-automation-element-propids.md)                 | Vedere le note.   | Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata della struttura ad albero di automazione interfaccia utente.                                                                                         |
| [**\_BOUNDINGRECTANGLEPROPERTYID UIA**](uiauto-automation-element-propids.md)       | Vedere le note.   | Il rettangolo più esterno che contiene l'intero controllo.                                                                                                                                             |
| [**\_CLICKABLEPOINTPROPERTYID UIA**](uiauto-automation-element-propids.md)             | Vedere le note.   | Supportata se è presente un rettangolo di delimitazione. Se non tutti i punti all'interno del rettangolo di delimitazione sono selezionabili e l'elemento esegue un hit testing specializzato, eseguire l'override e fornire un punto selezionabile. |
| [**\_CONTROLTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md)                   | **DataItem** |                                                                                                                                                                                                      |
| [**\_ISCONTENTELEMENTPROPERTYID UIA**](uiauto-automation-element-propids.md)         | true         | Il controllo elemento dati deve essere sempre un contenuto.                                                                                                                                                        |
| [**\_ISCONTROLELEMENTPROPERTYID UIA**](uiauto-automation-element-propids.md)         | true         | Il controllo elemento dati deve essere sempre un controllo.                                                                                                                                                      |
| [**\_ISKEYBOARDFOCUSABLEPROPERTYID UIA**](uiauto-automation-element-propids.md)   | Vedere le note.   | Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.                                                                                                                            |
| [**\_ITEMSTATUSPROPERTYID UIA**](uiauto-automation-element-propids.md)                     | Vedere le note.   | Se il controllo contiene uno stato aggiornato dinamicamente, è necessario che questa proprietà sia supportata in modo che una tecnologia per l'accesso facilitato possa ricevere aggiornamenti quando lo stato dell'elemento cambia.        |
| [**\_ITEMTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md)                         | Vedere le note.   | Si tratta del valore della stringa che indica all'utente finale l'oggetto sottostante rappresentato dall'elemento, Gli esempi includono "file multimediale" e "contatto".                                                   |
| [**\_LABELEDBYPROPERTYID UIA**](uiauto-automation-element-propids.md)                       | Null         | I controlli elemento dati non hanno un'etichetta di testo statico.                                                                                                                                                  |
| [**\_LOCALIZEDCONTROLTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md) | Vedere le note.   | Stringa localizzata corrispondente al tipo di controllo **DataItem** . Il valore predefinito è "elemento dati" per en-US o inglese (Stati Uniti).                                                              |
| [**\_NAMEPROPERTYID UIA**](uiauto-automation-element-propids.md)                                 | Vedere le note.   | Il controllo elemento dati contiene sempre un elemento di testo primario che l'utente riconosce come identificatore per l'elemento.                                                                           |



 

## <a name="required-control-patterns"></a>Pattern di controllo obbligatori

La tabella seguente elenca i pattern di controllo di automazione interfaccia utente che devono essere supportati da tutti i controlli elemento dati. Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Pattern di controllo                                                   | Supporto | Note                                                                                                                                                                                                                 |
|-------------------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Dipende da | Se è possibile espandere o comprimere l'elemento dati per visualizzare e nascondere le informazioni, è necessario supportare il pattern di controllo [ExpandCollapse](uiauto-implementingexpandcollapse.md) .                                            |
| [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)             | Dipende da | Gli elementi di dati supporteranno il pattern di controllo [GridItem](uiauto-implementinggriditem.md) quando una raccolta di elementi di dati è disponibile all'interno di un contenitore che può essere spostata a livello spaziale da elemento a elemento.                 |
| [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider)         | Dipende da | Tutti gli elementi di dati supportano la possibilità di scorrere la visualizzazione con il pattern di controllo [ScrollItem](uiauto-implementingscrollitem.md) quando il relativo contenitore di dati contiene più elementi rispetto a quelli che possono essere visualizzati sullo schermo.             |
| [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)   | Dipende da | La possibilità di selezionare gli elementi di dati dipende dal contenuto.                                                                                                                                                          |
| [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider)           | Dipende da | Se l'elemento dati è contenuto all'interno di un tipo di controllo [DataGrid](uiauto-supportdatagridcontroltype.md) che dispone di un elemento header, deve supportare il pattern di controllo [TableItem](uiauto-implementingtableitem.md) . |
| [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)                 | Dipende da | Se l'elemento dati contiene uno stato che può essere ciclito tramite, deve supportare il pattern di controllo di [alternanza](uiauto-implementingtoggle.md) .                                                                          |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)                   | Dipende da | Se il testo primario dell'elemento dati è modificabile, il pattern di controllo [value](uiauto-implementingvalue.md) deve essere supportato.                                                                                             |



 

## <a name="working-with-dataitems-in-large-lists"></a>Utilizzo di oggetti dataItems in elenchi di grandi dimensioni

Poiché gli elenchi di grandi dimensioni sono spesso virtualizzati nei framework dell'interfaccia utente per facilitare le prestazioni, un client di automazione interfaccia utente non può usare la funzionalità di query di automazione interfaccia utente per cercare il contenuto dell'albero completo nello stesso modo in cui è possibile in altri contenitori di elementi. Un client deve scorrere l'elemento nella visualizzazione (oppure espandere il controllo per visualizzare tutte le opzioni disponibili) prima di accedere al set completo di informazioni dell'elemento dati.

Quando si chiama [**SetFocus**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-setfocus) sull'elemento di automazione interfaccia utente per l'elemento di dati, Esplora risorse di Microsoft Windows viene restituito correttamente e causa l'impostazione dello stato attivo sul controllo di modifica all'interno del sottoalbero dell'elemento dati.

## <a name="required-events"></a>Eventi obbligatori

La tabella seguente elenca gli eventi di automazione interfaccia utente necessari per supportare i controlli elemento dati. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



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



 

## <a name="dataitem-control-type-example"></a>Esempio del tipo di controllo DataItem

Nell'immagine seguente viene illustrato un tipo di controllo DataItem in un controllo visualizzazione elenco.

![screenshot del controllo visualizzazione elenco con il tipo di controllo DataItem](images/dataitemxmpl.jpg)

La visualizzazione controlli e la visualizzazione contenuto dell'albero di automazione interfaccia utente che riguarda il controllo elemento dati sono visualizzate di seguito. I pattern di controllo per ogni elemento di automazione sono indicati tra parentesi. Il **gruppo** "contoso" fa inoltre parte della griglia del controllo host della griglia dati. Per un esempio di una struttura di griglia di livello superiore, vedere [tipo di controllo DataGrid](uiauto-supportdatagridcontroltype.md).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Albero di automazione interfaccia utente-visualizzazione controlli</th>
<th>Albero di automazione interfaccia utente-visualizzazione contenuto</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li>Gruppo &quot; Contoso &quot; (tabella, griglia)
<ul>
<li>DataItem &quot; accounts Receivable.doc&quot; (TableItem, GridItem, SelectionItem, Invoke)
<ul>
<li>&quot;Receivable.docdi account immagine&quot;</li>
<li>Modifica &quot; nome &quot; (TableItem, GridItem, valore &quot; accounts Receivable.doc&quot; )</li>
<li>Modifica &quot; Data modifica &quot; (TableItem, GridItem, valore &quot; 8/25/2006 3:29 PM &quot; )</li>
<li>Modifica &quot; dimensioni &quot; (GridItem, TableItem, valore &quot; 11,0 KB &quot; )</li>
</ul></li>
<li>DataItem &quot; accounts Payable.doc&quot; (TableItem, GridItem, SelectionItem, Invoke)
<ul>
<li>...</li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li>Gruppo &quot; Contoso &quot; (tabella, griglia)
<ul>
<li>DataItem &quot; accounts Receivable.doc&quot; (TableItem, GridItem, SelectionItem, Invoke)
<ul>
<li>&quot;Receivable.docdi account immagine&quot;</li>
<li>Modifica &quot; nome &quot; (TableItem, GridItem, valore &quot; accounts Receivable.doc&quot; )</li>
<li>Modifica &quot; Data modifica &quot; (TableItem, GridItem, valore &quot; 8/25/2006 3:29 PM &quot; )</li>
<li>Modifica &quot; dimensioni &quot; (GridItem, TableItem, valore &quot; 11,0 KB &quot; )</li>
</ul></li>
<li>DataItem &quot; accounts Payable.doc&quot; (TableItem, GridItem, SelectionItem, Invoke)
<ul>
<li>...</li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

Se una griglia rappresenta un elenco di elementi selezionabili, è possibile esporre gli elementi dell'interfaccia utente selezionabili corrispondenti con il tipo di controllo [ListItem](uiauto-supportlistitemcontroltype.md) anziché con il tipo di controllo DataItem. Nell'esempio precedente, gli elementi **DataItem** ("accounts Receivable.doc" e "accounts Payable.doc") in **Group** ("contoso") possono essere migliorati esponendoli come tipi di controllo ListItem, perché il tipo già supporta il pattern di controllo [SelectionItem](uiauto-implementingselectionitem.md) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente](uiauto-controltypesoverview.md)
</dt> <dt>

[Cenni preliminari su automazione interfaccia utente](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




