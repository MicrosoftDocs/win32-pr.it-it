---
title: Tipo di controllo Calendar
description: In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo Calendar. Un controllo Calendar consente all'utente di determinare facilmente la data e selezionare altre date.
ms.assetid: 886cf1a4-0e6f-4ae1-9dc4-e97ac6a22359
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo Calendar
- Automazione interfaccia utente, tipo di controllo Calendar
- Automazione interfaccia utente, struttura ad albero per il tipo di controllo Calendar
- Automazione interfaccia utente, proprietà per il tipo di controllo Calendar
- Automazione interfaccia utente, pattern di controllo per il tipo di controllo Calendar
- Automazione interfaccia utente, eventi per il tipo di controllo Calendar
- strutture ad albero, tipo di controllo Calendar
- Proprietà, tipo di controllo Calendar
- pattern di controllo, tipo di controllo Calendar
- eventi, tipo di controllo Calendar
- supporto per il tipo di controllo Calendar
- Calendar (tipo di controllo)
- tipi di controllo, struttura ad albero per il tipo di controllo Calendar
- tipi di controllo, pattern di controllo per il tipo di controllo Calendar
- tipi di controllo, supporto per Calendar
- tipi di controllo, calendario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef936848f764c6937bfe36e6ed919f0a88dac78c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045370"
---
# <a name="calendar-control-type"></a>Tipo di controllo Calendar

In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo **Calendar** . Un controllo Calendar consente all'utente di determinare facilmente la data e selezionare altre date.

Nelle sezioni seguenti vengono definiti la struttura ad albero, le proprietà, i pattern di controllo e gli eventi di automazione interfaccia utente necessari per il tipo di controllo **Calendar** . I requisiti di automazione interfaccia utente si applicano a tutti i controlli calendario in cui il Framework dell'interfaccia utente/piattaforma integra il supporto di automazione interfaccia utente per i tipi di controllo e i pattern

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Pattern di controllo obbligatori](#required-control-patterns)
-   [Eventi obbligatori](#required-events)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

Nella tabella seguente viene illustrata una tipica visualizzazione del controllo e del contenuto dell'albero di automazione interfaccia utente relativo ai controlli calendario e viene descritto il possibile contenuto di ogni visualizzazione. Per altre informazioni sull'albero di automazione interfaccia utente, vedere [Cenni preliminari sull'albero di automazione interfaccia utente](uiauto-treeoverview.md).



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
<li>Calendario
<ul>
<li>DataGrid
<ul>
<li>Header (0 o 1)
<ul>
<li>HeaderItem (0 o 7, la quantità dipende dal numero di giorni visualizzati nelle colonne)</li>
</ul></li>
<li>ListItem (la quantità dipende dal numero di giorni visualizzati)</li>
<li>Button (0 o 2; per la visualizzazione delle diverse pagine del calendario)</li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li>Calendario
<ul>
<li>ListItem (la quantità dipende dal numero di giorni visualizzati)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

I controlli Calendario possono essere rappresentati in formati diversi all'interno dell'interfaccia utente. Gli unici controlli garantiti nella visualizzazione controlli dell'albero di automazione interfaccia utente sono i controlli griglia dati, intestazione, elemento intestazione ed elemento elenco.

## <a name="relevant-properties"></a>Proprietà rilevanti

La tabella seguente elenca le proprietà di automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per il tipo di controllo **Calendar** . Per altre informazioni sulle proprietà di automazione interfaccia utente, vedere [recupero di proprietà da elementi di automazione interfaccia utente](uiauto-propertiesforclients.md).



| Proprietà di automazione interfaccia utente                                                                                              | Valore        | Note                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_AUTOMATIONIDPROPERTYID UIA**](uiauto-automation-element-propids.md)                 | Vedere le note.   | Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata della struttura ad albero di automazione interfaccia utente.                                                                                         |
| [**\_BOUNDINGRECTANGLEPROPERTYID UIA**](uiauto-automation-element-propids.md)       | Vedere le note.   | Il rettangolo più esterno che contiene l'intero controllo.                                                                                                                                             |
| [**\_CLICKABLEPOINTPROPERTYID UIA**](uiauto-automation-element-propids.md)             | Vedere le note.   | Supportata se è presente un rettangolo di delimitazione. Se non tutti i punti all'interno del rettangolo di delimitazione sono selezionabili e l'elemento esegue un hit testing specializzato, eseguire l'override e fornire un punto selezionabile. |
| [**\_CONTROLTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md)                   | **Calendario** | Questo valore è uguale per tutti i framework dell'interfaccia utente.                                                                                                                                                        |
| [**\_ISCONTENTELEMENTPROPERTYID UIA**](uiauto-automation-element-propids.md)         | true         | Il controllo Calendar viene sempre incluso nella visualizzazione contenuto dell'albero di automazione interfaccia utente.                                                                                                               |
| [**\_ISCONTROLELEMENTPROPERTYID UIA**](uiauto-automation-element-propids.md)         | true         | Il controllo Calendar viene sempre incluso nella visualizzazione controlli dell'albero di automazione interfaccia utente.                                                                                                               |
| [**\_ISKEYBOARDFOCUSABLEPROPERTYID UIA**](uiauto-automation-element-propids.md)   | Vedere le note.   | Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.                                                                                                                            |
| [**\_LABELEDBYPROPERTYID UIA**](uiauto-automation-element-propids.md)                       | Vedere le note.   | Il valore di questa proprietà deve essere l'etichetta del controllo documento. In genere, viene usato il titolo del documento.                                                                                |
| [**\_LOCALIZEDCONTROLTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md) | Vedere le note.   | Stringa localizzata corrispondente al tipo di controllo **Calendar** . Il valore predefinito è "Calendar" per en-US o inglese (Stati Uniti).                                                               |
| [**\_NAMEPROPERTYID UIA**](uiauto-automation-element-propids.md)                                 | Vedere le note.   | Il controllo Calendar in genere ottiene il nome dalla data corrente.                                                                                                                                  |



 

## <a name="required-control-patterns"></a>Pattern di controllo obbligatori

La tabella seguente elenca i pattern di controllo di automazione interfaccia utente che devono essere supportati da tutti i controlli calendario. Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Pattern di controllo/proprietà del pattern                        | Supporto/valore | Note                                                                                                                                                                                                                                                                                                                          |
|---------------------------------------------------------|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider)           | Necessario      | Il controllo calendario supporta sempre il pattern di controllo [Grid](uiauto-implementinggrid.md) perché i giorni all'interno di un mese sono elementi che possono essere spostati a livello spaziale.                                                                                                                                                        |
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)       | Dipende da       | La maggior parte dei controlli Calendario supporta lo scorrimento della visualizzazione per pagina. Il pattern di controllo [Scroll](uiauto-implementingscroll.md) è consigliato per supportare la navigazione di paging.                                                                                                                                                    |
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) | Dipende da       | La maggior parte dei controlli calendario mantiene un giorno, un mese o un anno specifico come selezione del sottoelemento. Alcuni calendari sono multiselezionabili e altri solo selezionabili singolarmente. Il controllo Calendar con sottoelementi selezionabili deve supportare il pattern di controllo [Selection](uiauto-implementingselection.md) .                         |
| [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider)         | Necessario      | Poiché il controllo Calendar include sempre un'intestazione all'interno del relativo sottoalbero per i giorni della settimana, il pattern di controllo [Table](uiauto-implementingtable.md) deve essere supportato.                                                                                                                                                     |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)         | No            | Il pattern di controllo [value](uiauto-implementingvalue.md) non è necessario per i controlli Calendar perché l'elemento non può impostare il valore direttamente nel controllo. Se al controllo è associata una data specifica, le informazioni devono essere fornite dal pattern di controllo [Selection](uiauto-implementingselection.md) . |



 

## <a name="required-events"></a>Eventi obbligatori

La tabella seguente elenca gli eventi di automazione interfaccia utente necessari per supportare i controlli calendario. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



| Evento di automazione interfaccia utente                                                                                                                                        | Note                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_AUTOMATIONFOCUSCHANGEDEVENTID UIA**](uiauto-event-ids.md)                                                           |                                                                                                                                                                                                              |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà BoundingRectanglePropertyId.                      |                                                                                                                                                                                                              |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsEnabledPropertyId.                                      | Se il controllo supporta la proprietà [**IsEnabled**](uiauto-automation-element-propids.md) , deve supportare questo evento.                                                                                     |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsOffscreenPropertyId.                                  | Se il controllo supporta la proprietà [**IsOffscreen**](uiauto-automation-element-propids.md) , deve supportare questo evento.                                                                                   |
| [**\_LAYOUTINVALIDATEDEVENTID UIA**](uiauto-event-ids.md)                                                                     |                                                                                                                                                                                                              |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà MultipleViewCurrentViewPropertyId.             | Se il controllo supporta la proprietà [**CurrentView**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-get_currentview) del pattern di controllo [MultipleView](uiauto-implementingmultipleview.md) , deve supportare questo evento. |
| [**\_STRUCTURECHANGEDEVENTID UIA**](uiauto-event-ids.md)                                                                       |                                                                                                                                                                                                              |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ScrollHorizontallyScrollablePropertyId.   | Se il controllo supporta il pattern di controllo [Scroll](uiauto-implementingscroll.md) , deve supportare questo evento.                                                                                             |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ScrollHorizontalScrollPercentPropertyId. | Se il controllo supporta il pattern di controllo [Scroll](uiauto-implementingscroll.md) , deve supportare questo evento.                                                                                             |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ScrollHorizontalViewSizePropertyId.           | Se il controllo supporta il pattern di controllo [Scroll](uiauto-implementingscroll.md) , deve supportare questo evento.                                                                                             |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ScrollVerticalScrollPercentPropertyId.     | Se il controllo supporta il pattern di controllo [Scroll](uiauto-implementingscroll.md) , deve supportare questo evento.                                                                                             |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ScrollVerticallyScrollablePropertyId.       | Se il controllo supporta il pattern di controllo [Scroll](uiauto-implementingscroll.md) , deve supportare questo evento.                                                                                             |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ScrollVerticalViewSizePropertyId.               | Se il controllo supporta il pattern di controllo [Scroll](uiauto-implementingscroll.md) , deve supportare questo evento.                                                                                             |
| [**\_InvalidatedEventId selezione \_ UIA**](uiauto-event-ids.md)                                                            |                                                                                                                                                                                                              |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente](uiauto-controltypesoverview.md)
</dt> <dt>

[Cenni preliminari su automazione interfaccia utente](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




