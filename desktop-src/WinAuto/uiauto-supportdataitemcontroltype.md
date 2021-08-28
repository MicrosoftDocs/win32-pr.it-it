---
title: Tipo di controllo DataItem
description: In questo argomento vengono fornite informazioni sul supporto Automazione interfaccia utente microsoft per il tipo di controllo DataItem.
ms.assetid: def52fe7-9f05-4cd0-8a46-af4e2e3ba03e
keywords:
- Automazione interfaccia utente,supporto per il tipo di controllo DataItem
- Automazione interfaccia utente, tipo di controllo DataItem
- Automazione interfaccia utente struttura ad albero per il tipo di controllo DataItem
- Automazione interfaccia utente,proprietà per il tipo di controllo DataItem
- Automazione interfaccia utente,pattern di controllo per il tipo di controllo DataItem
- Automazione interfaccia utente,eventi per il tipo di controllo DataItem
- Automazione interfaccia utente, elenchi di grandi dimensioni e tipo di controllo DataItem
- strutture ad albero, tipo di controllo DataItem
- proprietà, tipo di controllo DataItem
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
ms.openlocfilehash: 49840dbe2aeed9200ebf02b80e270cd8fa3e0747
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468188"
---
# <a name="dataitem-control-type"></a>Tipo di controllo DataItem

In questo argomento vengono fornite informazioni sul supporto Automazione interfaccia utente Microsoft per il **tipo di controllo DataItem.**

Una voce in un elenco Contatti, ad esempio, è un controllo elemento dati. Un controllo elemento dati contiene informazioni di interesse per un utente finale. È più complicato del semplice elemento elenco poiché contiene informazioni più dettagliate.

Le sezioni seguenti definiscono la struttura ad Automazione interfaccia utente struttura ad albero, le proprietà, i pattern di controllo e gli eventi per il **tipo di controllo DataItem.** I Automazione interfaccia utente si applicano a tutti i controlli elemento dati in cui il framework o la piattaforma dell'interfaccia utente si integra Automazione interfaccia utente per i tipi di controllo e i pattern di controllo.

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Pattern di controllo obbligatori](#required-control-patterns)
-   [Uso di Elementi dati in elenchi di grandi dimensioni](#working-with-dataitems-in-large-lists)
-   [Eventi obbligatori](#required-events)
-   [Esempio del tipo di controllo DataItem](#dataitem-control-type-example)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

La tabella seguente illustra un controllo tipico e una visualizzazione contenuto dell'albero Automazione interfaccia utente relativo ai controlli elemento dati e descrive gli elementi che possono essere contenuti in ogni visualizzazione. Per altre informazioni sull'albero Automazione interfaccia utente, vedere panoramica [Automazione interfaccia utente albero.](uiauto-treeoverview.md)




| Visualizzazione controlli | Visualizzazione contenuto | 
|--------------|--------------|
| <ul><li>DataItem<ul><li>Varia (0 o più, può essere strutturato in una gerarchia)</li></ul></li></ul> | <ul><li>DataItem<ul><li>Varia (0 o più, può essere strutturato in una gerarchia)</li></ul></li></ul> | 




 

Un elemento dati in una griglia di dati può contenere vari tipi di oggetti, incluso un altro livello di elementi dati o specifici elementi di griglia quali testo, immagini o controlli di modifica. Se l'elemento dell'elemento dati ha un ruolo oggetto specifico, l'elemento deve essere esposto come tipo di controllo specifico. ad esempio un [tipo di controllo ListItem](uiauto-supportlistitemcontroltype.md) per un elemento dati selezionabile nella griglia.

## <a name="relevant-properties"></a>Proprietà rilevanti

La tabella seguente elenca le Automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per il tipo di controllo DataItem. Per altre informazioni sulle Automazione interfaccia utente, vedere [Recupero di proprietà da Automazione interfaccia utente elementi](uiauto-propertiesforclients.md).



| Proprietà di automazione interfaccia utente                                                                                              | valore        | Note                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Vedere le note.   | Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata dell'Automazione interfaccia utente albero.                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vedere le note.   | Il rettangolo più esterno che contiene l'intero controllo.                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vedere le note.   | Supportata se è presente un rettangolo di delimitazione. Se non tutti i punti all'interno del rettangolo di delimitazione sono selezionabili e l'elemento esegue hit testing specializzati, eseguire l'override e fornire un punto selezionabile. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **DataItem** |                                                                                                                                                                                                      |
| [**\_IsContentElementPropertyId dell'interfaccia utente**](uiauto-automation-element-propids.md)         | true         | Il controllo elemento dati deve essere sempre un contenuto.                                                                                                                                                        |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | true         | Il controllo elemento dati deve essere sempre un controllo.                                                                                                                                                      |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Vedere le note.   | Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.                                                                                                                            |
| [**UIA \_ ItemStatusPropertyId**](uiauto-automation-element-propids.md)                     | Vedere le note.   | Se il controllo contiene lo stato che viene aggiornato dinamicamente, questa proprietà deve essere supportata in modo che un assistive technology possa ricevere aggiornamenti quando lo stato dell'elemento cambia.        |
| [**UIA \_ ItemTypePropertyId**](uiauto-automation-element-propids.md)                         | Vedere le note.   | Si tratta del valore della stringa che indica all'utente finale l'oggetto sottostante rappresentato dall'elemento, Ad esempio, "File multimediale" e "Contatto".                                                   |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Null         | I controlli elemento dati non hanno un'etichetta di testo statico.                                                                                                                                                  |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vedere le note.   | Stringa localizzata corrispondente al **tipo di controllo DataItem.** Il valore predefinito è "data item" per en-US o English (Stati Uniti).                                                              |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Vedere le note.   | Il controllo elemento dati contiene sempre un elemento di testo primario che l'utente riconoscerebbe come identificatore per l'elemento.                                                                           |



 

## <a name="required-control-patterns"></a>Pattern di controllo obbligatori

Nella tabella seguente sono elencati i Automazione interfaccia utente di controllo che devono essere supportati da tutti i controlli elemento dati. Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Pattern di controllo                                                   | Supporto | Note                                                                                                                                                                                                                 |
|-------------------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Dipende da | Se l'elemento di dati può essere espanso o compresso per mostrare e nascondere le informazioni, il pattern di controllo [ExpandCollapse](uiauto-implementingexpandcollapse.md) deve essere supportato.                                            |
| [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)             | Dipende da | Gli elementi di dati supporteranno il pattern di [controllo GridItem](uiauto-implementinggriditem.md) quando una raccolta di elementi di dati è disponibile all'interno di un contenitore che può essere esplorato in modo spaziale da elemento a elemento.                 |
| [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider)         | Dipende da | Tutti gli elementi di dati supportano la possibilità di scorrere nella visualizzazione con il pattern di [controllo ScrollItem](uiauto-implementingscrollitem.md) quando il contenitore di dati contiene più elementi di quelli che possono essere visualizzati sullo schermo.             |
| [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)   | Dipende da | La possibilità di selezionare gli elementi di dati dipende dal contenuto.                                                                                                                                                          |
| [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider)           | Dipende da | Se l'elemento di dati è contenuto in un [tipo di controllo DataGrid](uiauto-supportdatagridcontroltype.md) con un elemento intestazione, deve supportare il pattern [di controllo TableItem.](uiauto-implementingtableitem.md) |
| [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)                 | Dipende da | Se l'elemento di dati contiene uno stato che può essere scorrendo, deve supportare il pattern di controllo [Toggle.](uiauto-implementingtoggle.md)                                                                          |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)                   | Dipende da | Se il testo primario dell'elemento dati è modificabile, il pattern [di](uiauto-implementingvalue.md) controllo Valore deve essere supportato.                                                                                             |



 

## <a name="working-with-dataitems-in-large-lists"></a>Uso di Elementi dati in elenchi di grandi dimensioni

Poiché gli elenchi di grandi dimensioni vengono spesso virtualizzati all'interno dei framework dell'interfaccia utente per facilitare le prestazioni, un client Automazione interfaccia utente non può usare la funzionalità di query Automazione interfaccia utente per cercare il contenuto dell'albero completo nello stesso modo possibile in altri contenitori di elementi. Un client deve scorrere l'elemento nella visualizzazione (o espandere il controllo per visualizzare tutte le opzioni disponibili) prima di accedere al set completo di informazioni dall'elemento dati.

Quando si chiama [**SetFocus**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-setfocus) sull'elemento Automazione interfaccia utente per l'elemento di dati, Microsoft Windows Explorer restituisce correttamente e fa sì che lo stato attivo sia impostato sul controllo Edit all'interno del sottoalbero dell'elemento di dati.

## <a name="required-events"></a>Eventi obbligatori

Nella tabella seguente sono elencati Automazione interfaccia utente eventi che i controlli elemento dati devono supportare. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automazione interfaccia utente evento                                                                                                                                                | Note                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                                   |                                                                                                                                  |
| [**Interfaccia \_ utente Evento di modifica della proprietà BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md)                              |                                                                                                                                  |
| [**Interfaccia \_ utente Evento di modifica della proprietà ExpandCollapseExpandCollapseStatePropertyId.**](uiauto-control-pattern-propids.md) | Se il controllo supporta il [pattern di controllo ExpandCollapse,](uiauto-implementingexpandcollapse.md) deve supportare questo evento. |
| [**UIA \_ Invoke \_ InvokedEventId**](uiauto-event-ids.md)                                                                                  | Se il controllo supporta il [pattern di controllo Invoke,](uiauto-implementinginvoke.md) deve supportare questo evento.                 |
| [**Interfaccia \_ utente Evento di modifica della proprietà IsEnabledPropertyId.**](uiauto-automation-element-propids.md)                                              | Se il controllo supporta la [**proprietà IsEnabled,**](uiauto-automation-element-propids.md) deve supportare questo evento.         |
| [**Interfaccia \_ utente Evento di modifica della proprietà IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)                                          | Se il controllo supporta la [**proprietà IsOffscreen,**](uiauto-automation-element-propids.md) deve supportare questo evento.       |
| [**Interfaccia \_ utente Evento di modifica della proprietà ItemStatusPropertyId.**](uiauto-automation-element-propids.md)                                            | Se il controllo supporta la [**proprietà ItemStatus,**](uiauto-automation-element-propids.md) deve supportare questo evento.        |
| [**Interfaccia \_ utente Evento di modifica**](uiauto-automation-element-propids.md) della proprietà NamePropertyId.                                                        |                                                                                                                                  |
| [**Elemento \_ UiA \_ SelectionItemAddedToSelectionEventId**](uiauto-event-ids.md)                                    | Se il controllo supporta il pattern [di controllo SelectionItem,](uiauto-implementingselectionitem.md) deve supportare questo evento.   |
| [**UIA \_ SelectionItem \_ ElementRemovedFromSelectionEventId**](uiauto-event-ids.md)                            | Se il controllo supporta il pattern [di controllo SelectionItem,](uiauto-implementingselectionitem.md) deve supportare questo evento.   |
| [**UIA \_ SelectionItem \_ ElementSelectedEventId**](uiauto-event-ids.md)                                                    | Se il controllo supporta il pattern [di controllo SelectionItem,](uiauto-implementingselectionitem.md) deve supportare questo evento.   |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                               |                                                                                                                                  |
| [**Interfaccia \_ utente Evento di modifica della proprietà ToggleToggleStatePropertyId.**](uiauto-control-pattern-propids.md)                                 | Se il controllo supporta il pattern di controllo [Toggle,](uiauto-implementingtoggle.md) deve supportare questo evento.                 |
| [**Interfaccia \_ utente Evento di modifica della proprietà ValueValuePropertyId.**](uiauto-control-pattern-propids.md)                                               | Se il controllo supporta il pattern [di controllo Value,](uiauto-implementingvalue.md) deve supportare questo evento.                   |



 

## <a name="dataitem-control-type-example"></a>Esempio del tipo di controllo DataItem

L'immagine seguente illustra un tipo di controllo DataItem in un controllo visualizzazione elenco.

![Screenshot del controllo visualizzazione elenco con tipo di controllo dataitem](images/dataitemxmpl.jpg)

La visualizzazione controlli e la visualizzazione contenuto dell'Automazione interfaccia utente albero dei dati che riguardano il controllo elemento di dati vengono visualizzate di seguito. I pattern di controllo per ogni elemento di automazione sono indicati tra parentesi. Il **gruppo** "Contoso" fa anche parte della griglia del controllo host griglia dati. Per un esempio di una struttura griglia di livello superiore, vedere [Tipo di controllo DataGrid](uiauto-supportdatagridcontroltype.md).




| Automazione interfaccia utente struttura ad albero - Visualizzazione controlli | Automazione interfaccia utente struttura ad albero - Visualizzazione contenuto | 
|-----------------------------------|-----------------------------------|
| <ul><li>Group "Contoso" (Table, Grid)<ul><li>DataItem "Accounts Receivable.doc" (TableItem, GridItem, SelectionItem, Invoke)<ul><li>Image "Accounts Receivable.doc"</li><li>Edit "Name" (TableItem, GridItem, Value "Accounts Receivable.doc")</li><li>Edit "Date modified" (TableItem, GridItem, Value "8/25/2006 3:29 PM")</li><li>Modificare "Size" (GridItem, TableItem, Value "11.0 KB")</li></ul></li><li>DataItem "Accounts Payable.doc" (TableItem, GridItem, SelectionItem, Invoke)<ul><li>...</li></ul></li></ul></li></ul> | <ul><li>Group "Contoso" (Table, Grid)<ul><li>DataItem "Accounts Receivable.doc" (TableItem, GridItem, SelectionItem, Invoke)<ul><li>Image "Accounts Receivable.doc"</li><li>Edit "Name" (TableItem, GridItem, Value "Accounts Receivable.doc")</li><li>Edit "Date modified" (TableItem, GridItem, Value "8/25/2006 3:29 PM")</li><li>Modificare "Size" (GridItem, TableItem, Value "11.0 KB")</li></ul></li><li>DataItem "Accounts Payable.doc" (TableItem, GridItem, SelectionItem, Invoke)<ul><li>...</li></ul></li></ul></li></ul> | 




 

Se una griglia rappresenta un elenco di elementi selezionabili, gli elementi dell'interfaccia utente selezionabili corrispondenti possono essere esposti con il tipo di controllo [ListItem](uiauto-supportlistitemcontroltype.md) anziché con il tipo di controllo DataItem. Nell'esempio precedente, gli elementi **DataItem** ("Accounts Receivable.doc" e "Accounts Payable.doc") in **Group** ("Contoso") possono essere migliorati esponendoli come tipi di controllo ListItem perché tale tipo supporta già il pattern di [controllo SelectionItem.](uiauto-implementingselectionitem.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente](uiauto-controltypesoverview.md)
</dt> <dt>

[Cenni preliminari su automazione interfaccia utente](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




