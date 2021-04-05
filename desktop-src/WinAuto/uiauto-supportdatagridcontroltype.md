---
title: Tipo di controllo DataGrid
description: In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo DataGrid.
ms.assetid: 2381b302-37d6-4159-bb7d-862ae41af695
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo DataGrid
- Automazione interfaccia utente, tipo di controllo DataGrid
- Automazione interfaccia utente, struttura ad albero per il tipo di controllo DataGrid
- Automazione interfaccia utente, proprietà per il tipo di controllo DataGrid
- Automazione interfaccia utente, pattern di controllo per il tipo di controllo DataGrid
- Automazione interfaccia utente, eventi per il tipo di controllo DataGrid
- strutture ad albero, tipo di controllo DataGrid
- Proprietà, tipo di controllo DataGrid
- pattern di controllo, tipo di controllo DataGrid
- eventi, tipo di controllo DataGrid
- supporto per il tipo di controllo DataGrid
- Tipo di controllo DataGrid
- tipi di controllo, struttura ad albero per il tipo di controllo DataGrid
- tipi di controllo, pattern di controllo per il tipo di controllo DataGrid
- tipi di controllo, supporto per DataGrid
- tipi di controllo, DataGrid
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8af1e35e062c778285d1cb7edcca9ac6192792b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955405"
---
# <a name="datagrid-control-type"></a>Tipo di controllo DataGrid

In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo **DataGrid** .

Il tipo di controllo **DataGrid** consente a un utente di usare facilmente gli elementi contenenti dati o elementi di automazione presentati in colonne o righe. I controlli griglia dati contengono righe di elementi e colonne di informazioni su tali elementi. Un controllo visualizzazione elenco in Esplora risorse di Windows Vista è un esempio che supporta il tipo di controllo **DataGrid** .

Nelle sezioni seguenti vengono definiti la struttura ad albero, le proprietà, i pattern di controllo e gli eventi di automazione interfaccia utente necessari per il tipo di controllo **DataGrid** . I requisiti di automazione interfaccia utente si applicano a tutti i controlli griglia di dati in cui la piattaforma/Framework dell'interfaccia utente integra il supporto di automazione interfaccia utente per i tipi di controllo e i pattern

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Pattern di controllo obbligatori](#required-control-patterns)
-   [Eventi obbligatori](#required-events)
-   [Esempio di tipo di controllo DataGrid](#datagrid-control-type-example)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

Nella tabella seguente viene illustrata una tipica visualizzazione del controllo e del contenuto dell'albero di automazione interfaccia utente relativo ai controlli griglia dati e viene descritto il possibile contenuto di ogni visualizzazione. Per altre informazioni sull'albero di automazione interfaccia utente, vedere [Cenni preliminari sull'albero di automazione interfaccia utente](uiauto-treeoverview.md).



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
<li>DataGrid
<ul>
<li>Header (0, 1 o 2)
<ul>
<li>HeaderItem (numero di colonne o righe)</li>
</ul></li>
<li>DataItem (0 o più, può essere strutturato in una gerarchia)</li>
</ul></li>
</ul></td>
<td><ul>
<li>DataGrid
<ul>
<li>DataItem (0 o più, può essere strutturato in una gerarchia)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a>Proprietà rilevanti

La tabella seguente elenca le proprietà di automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per il tipo di controllo **DataGrid** . Per altre informazioni sulle proprietà di automazione interfaccia utente, vedere [recupero di proprietà da elementi di automazione interfaccia utente](uiauto-propertiesforclients.md).



| Proprietà di automazione interfaccia utente                                                                                              | Valore        | Note                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_AUTOMATIONIDPROPERTYID UIA**](uiauto-automation-element-propids.md)                 | Vedere le note.   | Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata della struttura ad albero di automazione interfaccia utente.                                                                                                                                                                                                 |
| [**\_BOUNDINGRECTANGLEPROPERTYID UIA**](uiauto-automation-element-propids.md)       | Vedere le note.   | Il rettangolo più esterno che contiene l'intero controllo.                                                                                                                                                                                                                                                     |
| [**\_CLICKABLEPOINTPROPERTYID UIA**](uiauto-automation-element-propids.md)             | Vedere le note.   | Supportata se è presente un rettangolo di delimitazione. Se non tutti i punti all'interno del rettangolo di delimitazione sono selezionabili e l'elemento esegue un hit testing specializzato, eseguire l'override e fornire un punto selezionabile.                                                                                                         |
| [**\_CONTROLTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md)                   | **DataGrid** |                                                                                                                                                                                                                                                                                                              |
| [**\_ISCONTENTELEMENTPROPERTYID UIA**](uiauto-automation-element-propids.md)         | true         | Il valore di questa proprietà deve essere sempre **true**. Ciò significa che il controllo griglia dati deve essere sempre presente nella visualizzazione contenuto dell'albero di automazione interfaccia utente.                                                                                                                                                      |
| [**\_ISCONTROLELEMENTPROPERTYID UIA**](uiauto-automation-element-propids.md)         | true         | Il valore di questa proprietà deve sempre essere **true**. Questo significa che il controllo griglia dati deve essere sempre incluso nella visualizzazione controlli dell'albero di automazione interfaccia utente.                                                                                                                                                |
| [**\_ISKEYBOARDFOCUSABLEPROPERTYID UIA**](uiauto-automation-element-propids.md)   | Vedere le note.   | Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.                                                                                                                                                                                                                                    |
| [**\_LABELEDBYPROPERTYID UIA**](uiauto-automation-element-propids.md)                       | Vedere le note.   | Se è presente un'etichetta di testo statico, questa proprietà deve esporre un riferimento a tale controllo.                                                                                                                                                                                                                      |
| [**\_LOCALIZEDCONTROLTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md) | Vedere le note.   | Stringa localizzata corrispondente al tipo di controllo **DataGrid** . Il valore predefinito è "griglia dati" per en-US o inglese (Stati Uniti).                                                                                                                                                                      |
| [**\_NAMEPROPERTYID UIA**](uiauto-automation-element-propids.md)                                 | Vedere le note.   | Il controllo griglia dati in genere ottiene il valore per la proprietà **Name** da un'etichetta di testo statico. Se non è presente un'etichetta di testo statico, lo sviluppatore dell'applicazione deve assegnare un valore a per la proprietà **Name** . Il valore della proprietà **Name** non deve mai essere il contenuto testuale del controllo di modifica. |



 

## <a name="required-control-patterns"></a>Pattern di controllo obbligatori

La tabella seguente elenca i pattern di controllo di automazione interfaccia utente che devono essere supportati da tutti i controlli griglia dati. Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Pattern di controllo                                         | Supporto  | Note                                                                                                                                                                             |
|---------------------------------------------------------|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider)           | Necessario | Il controllo griglia dati stesso supporta sempre il pattern di controllo [Grid](uiauto-implementinggrid.md) perché gli elementi che contiene contengono metadati disposti in una griglia. |
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)       | Dipende da  | La possibilità di scorrere la griglia dati dipende dal contenuto e dalla presenza o meno delle barre di scorrimento.                                                                                       |
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) | Dipende da  | La possibilità di selezionare la griglia dati dipende dal contenuto.                                                                                                                           |
| [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider)         | Dipende da  | Un controllo griglia di dati che dispone di un'intestazione deve supportare il pattern di controllo [Table](uiauto-implementingtable.md) .                                                                   |



 

Gli elementi di dati nei contenitori di griglia dati supporteranno almeno:

-   Pattern di controllo [SelectionItem](uiauto-implementingselectionitem.md) (se la griglia dati è selezionabile)
-   Pattern di controllo [ScrollItem](uiauto-implementingscrollitem.md) (se la griglia dati è scorrevole)
-   Pattern di controllo [GridItem](uiauto-implementinggriditem.md)
-   Pattern di controllo [TableItem](uiauto-implementingtableitem.md) (se la griglia dati ha un'intestazione)

## <a name="required-events"></a>Eventi obbligatori

La tabella seguente elenca gli eventi di automazione interfaccia utente necessari per supportare i controlli griglia dati. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



| Evento di automazione interfaccia utente                                                                                                                                        | Note                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_AUTOMATIONFOCUSCHANGEDEVENTID UIA**](uiauto-event-ids.md)                                                           |                                                                                                                                                          |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà BoundingRectanglePropertyId.                      |                                                                                                                                                          |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsEnabledPropertyId.                                      | Se il controllo supporta la proprietà [**IsEnabled**](uiauto-automation-element-propids.md) , deve supportare questo evento.                                 |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsOffscreenPropertyId.                                  | Se il controllo supporta la proprietà [**IsOffscreen**](uiauto-automation-element-propids.md) , deve supportare questo evento.                               |
| [**\_LAYOUTINVALIDATEDEVENTID UIA**](uiauto-event-ids.md)                                                                     |                                                                                                                                                          |
| [**\_STRUCTURECHANGEDEVENTID UIA**](uiauto-event-ids.md)                                                                       |                                                                                                                                                          |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà MultipleViewCurrentViewPropertyId.             | Se il controllo supporta la proprietà CurrentView del pattern di controllo [MultipleView](uiauto-implementingmultipleview.md) , deve supportare questo evento. |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ScrollHorizontallyScrollablePropertyId.   | Se il controllo supporta il pattern di controllo [Scroll](uiauto-implementingscroll.md) , deve supportare questo evento.                                         |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ScrollHorizontalScrollPercentPropertyId. | Se il controllo supporta il pattern di controllo [Scroll](uiauto-implementingscroll.md) , deve supportare questo evento.                                         |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ScrollHorizontalViewSizePropertyId.           | Se il controllo supporta il pattern di controllo [Scroll](uiauto-implementingscroll.md) , deve supportare questo evento.                                         |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ScrollVerticalScrollPercentPropertyId.     | Se il controllo supporta il pattern di controllo [Scroll](uiauto-implementingscroll.md) , deve supportare questo evento.                                         |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ScrollVerticallyScrollablePropertyId.       | Se il controllo supporta il pattern di controllo [Scroll](uiauto-implementingscroll.md) , deve supportare questo evento.                                         |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ScrollVerticalViewSizePropertyId.               | Se il controllo supporta il pattern di controllo [Scroll](uiauto-implementingscroll.md) , deve supportare questo evento.                                         |
| [**\_InvalidatedEventId selezione \_ UIA**](uiauto-event-ids.md)                                                            |                                                                                                                                                          |



 

## <a name="datagrid-control-type-example"></a>Esempio di tipo di controllo DataGrid

Nell'immagine seguente viene illustrato un controllo visualizzazione elenco che implementa il tipo di controllo **DataGrid** .

![screenshot del controllo visualizzazione elenco con il tipo di controllo DataGrid](images/datagridxmpl.jpg)

La visualizzazione controlli e la visualizzazione contenuto dell'albero di automazione interfaccia utente che riguarda il controllo visualizzazione elenco sono visualizzate di seguito. I pattern di controllo per ogni elemento di automazione sono indicati tra parentesi.



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
<td>DataGrid (ordinamento, tabella, selezione, griglia)
<ul>
<li>Intestazione
<ul>
<li>&quot;Nome HeaderItem &quot; (Invoke)</li>
<li>Data di HeaderItem &quot; modificata &quot; (Invoke)</li>
<li>&quot;Dimensioni HeaderItem &quot; (Invoke)</li>
</ul></li>
<li>Gruppo &quot; Contoso &quot; (TableItem, GridItem, SelectionItem, Table *, Grid*)
<ul>
<li>&quot;Receivable.docdegli account DataItem &quot; (SelectionItem, Invoke, TableItem *, GridItem*)</li>
<li>&quot;Payable.docdegli account DataItem &quot; (SelectionItem, Invoke, TableItem *, GridItem*)</li>
</ul></li>
</ul></td>
<td>DataGrid (Table, Grid, Selection)
<ul>
<li>Gruppo &quot; Contoso &quot; (TableItem, GridItem, SelectionItem, Table *, Grid*)
<ul>
<li>&quot;Receivable.docdegli account DataItem &quot; (SelectionItem, Invoke, TableItem *, GridItem*)</li>
<li>&quot;Payable.docdegli account DataItem &quot; (SelectionItem, Invoke, TableItem *, GridItem*)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

\*Nell'esempio precedente viene illustrata una griglia di dati che contiene più livelli di controlli. Il controllo **Group** ("contoso") contiene due controlli **DataItem** ("Accounts Receivable.doc" e "Accounts Payable.doc"). Una  / coppia di **GridItem** DataGrid è indipendente da una coppia in un altro livello. I controlli **DataItem** in un **gruppo** possono essere esposti anche come tipo di controllo [ListItem](uiauto-supportlistitemcontroltype.md) , consentendo loro di essere presentati più chiaramente come oggetti selezionabili, anziché come elementi dati semplici. Questo esempio non include i sottoelementi degli elementi di dati raggruppati. Per un altro esempio di più livelli di controlli, vedere il tipo di controllo [DataItem](uiauto-supportdataitemcontroltype.md) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente](uiauto-controltypesoverview.md)
</dt> <dt>

[Cenni preliminari su automazione interfaccia utente](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




