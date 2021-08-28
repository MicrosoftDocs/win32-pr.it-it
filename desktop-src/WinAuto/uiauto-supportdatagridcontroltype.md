---
title: Tipo di controllo DataGrid
description: Questo argomento fornisce informazioni sul supporto di Microsoft Automazione interfaccia utente per il tipo di controllo DataGrid.
ms.assetid: 2381b302-37d6-4159-bb7d-862ae41af695
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo DataGrid
- Automazione interfaccia utente, tipo di controllo DataGrid
- Automazione interfaccia utente,struttura ad albero per il tipo di controllo DataGrid
- Automazione interfaccia utente,proprietà per il tipo di controllo DataGrid
- Automazione interfaccia utente,pattern di controllo per il tipo di controllo DataGrid
- Automazione interfaccia utente,eventi per il tipo di controllo DataGrid
- strutture ad albero, tipo di controllo DataGrid
- proprietà, tipo di controllo DataGrid
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
ms.openlocfilehash: 7fa37093402fc3c4c195b4b68ecc74652af2d6a6
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475597"
---
# <a name="datagrid-control-type"></a>Tipo di controllo DataGrid

Questo argomento fornisce informazioni sul supporto di Microsoft Automazione interfaccia utente per il **tipo di controllo DataGrid.**

Il **tipo di controllo DataGrid** consente a un utente di usare facilmente elementi che contengono dati o elementi di automazione presentati in colonne o righe. I controlli griglia dati contengono righe di elementi e colonne di informazioni su tali elementi. Un controllo visualizzazione elenco in Windows Vista Explorer è un esempio che supporta il **tipo di controllo DataGrid.**

Le sezioni seguenti definiscono la struttura ad Automazione interfaccia utente struttura ad albero, le proprietà, i pattern di controllo e gli eventi per il **tipo di controllo DataGrid.** I Automazione interfaccia utente si applicano a tutti i controlli griglia dati in cui il framework o la piattaforma dell'interfaccia utente si integra Automazione interfaccia utente per i tipi di controllo e i pattern di controllo.

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Pattern di controllo obbligatori](#required-control-patterns)
-   [Eventi obbligatori](#required-events)
-   [Esempio di tipo di controllo DataGrid](#datagrid-control-type-example)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

La tabella seguente illustra un controllo tipico e una visualizzazione contenuto dell'albero Automazione interfaccia utente relativo ai controlli griglia dati e descrive gli elementi che possono essere contenuti in ogni visualizzazione. Per altre informazioni sull'albero Automazione interfaccia utente, vedere Automazione interfaccia utente [Tree Overview](uiauto-treeoverview.md).




| Visualizzazione controlli | Visualizzazione contenuto | 
|--------------|--------------|
| <ul><li>DataGrid<ul><li>Header (0, 1 o 2)<ul><li>HeaderItem (numero di colonne o righe)</li></ul></li><li>DataItem (0 o più; può essere strutturato in una gerarchia)</li></ul></li></ul> | <ul><li>DataGrid<ul><li>DataItem (0 o più; può essere strutturato in una gerarchia)</li></ul></li></ul> | 




 

## <a name="relevant-properties"></a>Proprietà rilevanti

La tabella seguente elenca le Automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per il **tipo di controllo DataGrid.** Per altre informazioni sulle Automazione interfaccia utente, vedere [Recupero di proprietà da Automazione interfaccia utente elementi](uiauto-propertiesforclients.md).



| Proprietà di automazione interfaccia utente                                                                                              | valore        | Note                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Vedere le note.   | Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata dell'Automazione interfaccia utente albero.                                                                                                                                                                                                 |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vedere le note.   | Il rettangolo più esterno che contiene l'intero controllo.                                                                                                                                                                                                                                                     |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vedere le note.   | Supportata se è presente un rettangolo di delimitazione. Se non tutti i punti all'interno del rettangolo di delimitazione sono selezionabili e l'elemento esegue hit testing specializzati, eseguire l'override e fornire un punto selezionabile.                                                                                                         |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **DataGrid** |                                                                                                                                                                                                                                                                                                              |
| [**\_IsContentElementPropertyId dell'interfaccia utente**](uiauto-automation-element-propids.md)         | true         | Il valore di questa proprietà deve essere sempre **TRUE.** Ciò significa che il controllo griglia dati deve essere sempre nella visualizzazione contenuto dell'Automazione interfaccia utente dati.                                                                                                                                                      |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | true         | Il valore di questa proprietà deve essere sempre **TRUE.** Ciò significa che il controllo Griglia dati deve essere sempre incluso nella visualizzazione controlli dell'Automazione interfaccia utente dati.                                                                                                                                                |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Vedere le note.   | Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.                                                                                                                                                                                                                                    |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Vedere le note.   | Se è presente un'etichetta di testo statico, questa proprietà deve esporre un riferimento a tale controllo.                                                                                                                                                                                                                      |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vedere le note.   | Stringa localizzata corrispondente al **tipo di controllo DataGrid.** Il valore predefinito è "griglia dati" per en-US o inglese (Stati Uniti).                                                                                                                                                                      |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Vedere le note.   | Il controllo Griglia dati in genere ottiene il valore per la relativa **proprietà Name** da un'etichetta di testo statico. Se non è presente un'etichetta di testo statico, uno sviluppatore di applicazioni deve assegnare un valore a per la **proprietà** Name. Il valore della **proprietà Name** non deve mai essere il contenuto testuale del controllo di modifica. |



 

## <a name="required-control-patterns"></a>Pattern di controllo obbligatori

Nella tabella seguente sono elencati i Automazione interfaccia utente che devono essere supportati da tutti i controlli griglia dati. Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Pattern di controllo                                         | Supporto  | Note                                                                                                                                                                             |
|---------------------------------------------------------|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider)           | Obbligatoria | Il controllo griglia dati stesso supporta sempre il pattern di controllo [Grid](uiauto-implementinggrid.md) perché gli elementi in esso contenuti hanno metadati disposti in una griglia. |
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)       | Dipende da  | La possibilità di scorrere la griglia dati dipende dal contenuto e dalla presenza o meno delle barre di scorrimento.                                                                                       |
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) | Dipende da  | La possibilità di selezionare la griglia dati dipende dal contenuto.                                                                                                                           |
| [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider)         | Dipende da  | Un controllo Griglia dati con un'intestazione deve supportare il [pattern di controllo](uiauto-implementingtable.md) Tabella.                                                                   |



 

Gli elementi di dati nei contenitori di griglia dati supporteranno almeno:

-   [Pattern di controllo SelectionItem](uiauto-implementingselectionitem.md) (se la griglia dei dati è selezionabile)
-   [Pattern di controllo ScrollItem](uiauto-implementingscrollitem.md) (se la griglia dei dati è scorrevole)
-   [Pattern di controllo GridItem](uiauto-implementinggriditem.md)
-   [Pattern di controllo TableItem](uiauto-implementingtableitem.md) (se la griglia dei dati ha un'intestazione)

## <a name="required-events"></a>Eventi obbligatori

Nella tabella seguente sono elencati Automazione interfaccia utente eventi che i controlli Griglia dati devono supportare. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automazione interfaccia utente evento                                                                                                                                        | Note                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                           |                                                                                                                                                          |
| [**Interfaccia \_ utente Evento di modifica della proprietà BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md)                      |                                                                                                                                                          |
| [**Interfaccia \_ utente Evento di modifica della proprietà IsEnabledPropertyId.**](uiauto-automation-element-propids.md)                                      | Se il controllo supporta la [**proprietà IsEnabled,**](uiauto-automation-element-propids.md) deve supportare questo evento.                                 |
| [**Interfaccia \_ utente Evento di modifica della proprietà IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)                                  | Se il controllo supporta la [**proprietà IsOffscreen,**](uiauto-automation-element-propids.md) deve supportare questo evento.                               |
| [**UIA \_ LayoutInvalidatedEventId**](uiauto-event-ids.md)                                                                     |                                                                                                                                                          |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                       |                                                                                                                                                          |
| [**Interfaccia \_ utente Evento di modifica della proprietà MultipleViewCurrentViewPropertyId.**](uiauto-control-pattern-propids.md)             | Se il controllo supporta la proprietà CurrentView del pattern [di controllo MultipleView,](uiauto-implementingmultipleview.md) deve supportare questo evento. |
| [**Interfaccia \_ utente Evento di modifica della proprietà ScrollHorizontallyScrollablePropertyId.**](uiauto-control-pattern-propids.md)   | Se il controllo supporta il pattern [di controllo Scroll,](uiauto-implementingscroll.md) deve supportare questo evento.                                         |
| [**Interfaccia \_ utente Evento di modifica della proprietà ScrollHorizontalScrollPercentPropertyId.**](uiauto-control-pattern-propids.md) | Se il controllo supporta il pattern [di controllo Scroll,](uiauto-implementingscroll.md) deve supportare questo evento.                                         |
| [**Interfaccia \_ utente Evento di modifica della proprietà ScrollHorizontalViewSizePropertyId.**](uiauto-control-pattern-propids.md)           | Se il controllo supporta il pattern [di controllo Scroll,](uiauto-implementingscroll.md) deve supportare questo evento.                                         |
| [**Interfaccia \_ utente Evento di modifica della proprietà ScrollVerticalScrollPercentPropertyId.**](uiauto-control-pattern-propids.md)     | Se il controllo supporta il pattern [di controllo Scroll,](uiauto-implementingscroll.md) deve supportare questo evento.                                         |
| [**Interfaccia \_ utente Evento di modifica della proprietà ScrollVerticallyScrollablePropertyId.**](uiauto-control-pattern-propids.md)       | Se il controllo supporta il pattern [di controllo Scroll,](uiauto-implementingscroll.md) deve supportare questo evento.                                         |
| [**Interfaccia \_ utente Evento di modifica della proprietà ScrollVerticalViewSizePropertyId.**](uiauto-control-pattern-propids.md)               | Se il controllo supporta il pattern [di controllo Scroll,](uiauto-implementingscroll.md) deve supportare questo evento.                                         |
| [**UIA \_ Selection \_ InvalidatedEventId**](uiauto-event-ids.md)                                                            |                                                                                                                                                          |



 

## <a name="datagrid-control-type-example"></a>Esempio di tipo di controllo DataGrid

L'immagine seguente illustra un controllo di visualizzazione elenco che implementa il **tipo di controllo DataGrid.**

![Screenshot del controllo visualizzazione elenco con tipo di controllo datagrid](images/datagridxmpl.jpg)

La visualizzazione controlli e la visualizzazione contenuto dell'Automazione interfaccia utente struttura ad albero che riguarda il controllo visualizzazione elenco vengono visualizzate di seguito. I pattern di controllo per ogni elemento di automazione sono indicati tra parentesi.




| Automazione interfaccia utente struttura ad albero - Visualizzazione controlli | Automazione interfaccia utente albero - Visualizzazione contenuto | 
|-----------------------------------|-----------------------------------|
| DataGrid (ordinamento, tabella, selezione, griglia)<ul><li>Intestazione<ul><li>HeaderItem "Nome" (Invoke)</li><li>HeaderItem "Ultima modifica" (Invoke)</li><li>HeaderItem "Dimensione" (Invoke)</li></ul></li><li>Gruppo "Contoso" (TableItem, GridItem, SelectionItem, Table *, Grid*)<ul><li>DataItem "Accounts Receivable.doc" (SelectionItem, Invoke,*TableItem, GridItem*)</li><li>DataItem "Accounts Payable.doc" (SelectionItem, Invoke,*TableItem, GridItem*)</li></ul></li></ul> | DataGrid (Table, Grid, Selection)<ul><li>Gruppo "Contoso" (TableItem, GridItem, SelectionItem, Table *, Grid*)<ul><li>DataItem "Accounts Receivable.doc" (SelectionItem, Invoke,*TableItem, GridItem*)</li><li>DataItem "Accounts Payable.doc" (SelectionItem, Invoke,*TableItem, GridItem*)</li></ul></li></ul> | 




 

\*Nell'esempio precedente viene illustrata una griglia dei dati che contiene più livelli di controlli. Il **controllo Group** ("Contoso") contiene due controlli **DataItem** ("Accounts Receivable.doc" e "Accounts Payable.doc"). Una **coppia DataGrid** / **GridItem** è indipendente da una coppia a un altro livello. I **controlli DataItem** in **un gruppo** possono anche essere esposti come tipo di controllo [ListItem,](uiauto-supportlistitemcontroltype.md) consentendone la presentazione più chiaramente come oggetti selezionabili, anziché come elementi di dati semplici. Questo esempio non include i sottoelementi degli elementi di dati raggruppati. Per un altro esempio di più livelli di controlli, vedere il [tipo di controllo DataItem.](uiauto-supportdataitemcontroltype.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente](uiauto-controltypesoverview.md)
</dt> <dt>

[Cenni preliminari su automazione interfaccia utente](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




