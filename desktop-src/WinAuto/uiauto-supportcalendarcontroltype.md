---
title: Tipo di controllo Calendar
description: Questo argomento fornisce informazioni sul supporto di Microsoft Automazione interfaccia utente per il tipo di controllo Calendar. Un controllo calendario consente all'utente di determinare facilmente la data e selezionare altre date.
ms.assetid: 886cf1a4-0e6f-4ae1-9dc4-e97ac6a22359
keywords:
- Automazione interfaccia utente,supporto per il tipo di controllo Calendar
- Automazione interfaccia utente,Tipo di controllo Calendar
- Automazione interfaccia utente,struttura ad albero per il tipo di controllo Calendar
- Automazione interfaccia utente,proprietà per il tipo di controllo Calendar
- Automazione interfaccia utente,pattern di controllo per il tipo di controllo Calendar
- Automazione interfaccia utente,eventi per il tipo di controllo Calendar
- strutture ad albero, tipo di controllo Calendar
- proprietà,tipo di controllo Calendar
- pattern di controllo, tipo di controllo Calendar
- eventi, tipo di controllo Calendar
- supporto per il tipo di controllo Calendar
- Calendar (tipo di controllo)
- tipi di controllo, struttura ad albero per il tipo di controllo Calendar
- tipi di controllo, pattern di controllo per il tipo di controllo Calendar
- tipi di controllo, supporto per Calendar
- tipi di controllo,Calendar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d51271fb2e9526bc293b9c5d36acc0a65b3b639
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482947"
---
# <a name="calendar-control-type"></a>Tipo di controllo Calendar

Questo argomento fornisce informazioni sul supporto di Microsoft Automazione interfaccia utente per il **tipo di controllo** Calendar. Un controllo calendario consente all'utente di determinare facilmente la data e selezionare altre date.

Le sezioni seguenti definiscono la struttura ad Automazione interfaccia utente, le proprietà, i pattern di controllo e gli eventi necessari per il **tipo di controllo** Calendar. I Automazione interfaccia utente si applicano a tutti i controlli calendario in cui il framework o la piattaforma dell'interfaccia utente Automazione interfaccia utente supporto per i tipi di controllo e i pattern di controllo.

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Pattern di controllo obbligatori](#required-control-patterns)
-   [Eventi obbligatori](#required-events)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

La tabella seguente illustra un controllo tipico e una visualizzazione contenuto dell'albero Automazione interfaccia utente che riguarda i controlli calendario e descrive cosa può essere contenuto in ogni visualizzazione. Per altre informazioni sull'albero Automazione interfaccia utente, vedere panoramica Automazione interfaccia utente [albero](uiauto-treeoverview.md).




| Visualizzazione controlli | Visualizzazione contenuto | 
|--------------|--------------|
| <ul><li>Calendario<ul><li>DataGrid<ul><li>Header (0 o 1)<ul><li>HeaderItem (0 o 7, la quantità dipende dal numero di giorni visualizzati nelle colonne)</li></ul></li><li>ListItem (la quantità dipende dal numero di giorni visualizzati)</li><li>Button (0 o 2; per la visualizzazione delle diverse pagine del calendario)</li></ul></li></ul></li></ul> | <ul><li>Calendario<ul><li>ListItem (la quantità dipende dal numero di giorni visualizzati)</li></ul></li></ul> | 




 

I controlli Calendario possono essere rappresentati in formati diversi all'interno dell'interfaccia utente. Gli unici controlli garantiti nella visualizzazione controlli dell'albero Automazione interfaccia utente sono la griglia dei dati, l'intestazione, l'elemento di intestazione e i controlli elemento elenco.

## <a name="relevant-properties"></a>Proprietà rilevanti

Nella tabella seguente sono elencate le Automazione interfaccia utente il cui valore o definizione è particolarmente rilevante per il **tipo di controllo** Calendar. Per altre informazioni sulle Automazione interfaccia utente, vedere Recupero di proprietà [da Automazione interfaccia utente elementi](uiauto-propertiesforclients.md).



| Proprietà di automazione interfaccia utente                                                                                              | valore        | Note                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Vedere le note.   | Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata dell'Automazione interfaccia utente albero.                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vedere le note.   | Il rettangolo più esterno che contiene l'intero controllo.                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vedere le note.   | Supportata se è presente un rettangolo di delimitazione. Se non tutti i punti all'interno del rettangolo di delimitazione sono selezionabili e l'elemento esegue hit testing specializzati, esegue l'override e fornisce un punto selezionabile. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Calendario** | Questo valore è uguale per tutti i framework dell'interfaccia utente.                                                                                                                                                        |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | true         | Il controllo calendario è sempre incluso nella visualizzazione contenuto dell'Automazione interfaccia utente albero.                                                                                                               |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | true         | Il controllo calendario è sempre incluso nella visualizzazione controlli dell'Automazione interfaccia utente albero.                                                                                                               |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Vedere le note.   | Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.                                                                                                                            |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Vedere le note.   | Il valore di questa proprietà deve essere l'etichetta del controllo documento. In genere, viene usato il titolo del documento.                                                                                |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vedere le note.   | Stringa localizzata corrispondente al **tipo di controllo** Calendar. Il valore predefinito è "calendar" per en-US o english (Stati Uniti).                                                               |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Vedere le note.   | Il controllo calendario ottiene in genere il nome dalla data corrente.                                                                                                                                  |



 

## <a name="required-control-patterns"></a>Pattern di controllo obbligatori

Nella tabella seguente sono elencati i Automazione interfaccia utente di controllo necessari per essere supportati da tutti i controlli calendario. Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Pattern di controllo/proprietà del pattern                        | Supporto/valore | Note                                                                                                                                                                                                                                                                                                                          |
|---------------------------------------------------------|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider)           | Obbligatoria      | Il controllo calendario supporta sempre il pattern di controllo [Grid](uiauto-implementinggrid.md) perché i giorni all'interno di un mese sono elementi che possono essere esplorati in modo spaziale.                                                                                                                                                        |
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)       | Dipende da       | La maggior parte dei controlli Calendario supporta lo scorrimento della visualizzazione per pagina. Il [pattern di](uiauto-implementingscroll.md) controllo Scroll è consigliato per supportare lo spostamento tra pagine.                                                                                                                                                    |
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) | Dipende da       | La maggior parte dei controlli calendario conserva un giorno, un mese o un anno specifico come selezione del sottoelemento. Alcuni calendari sono selezionabili a più opzioni e altri sono selezionabili solo a selezione singola. Il controllo Calendario con sottoelementi selezionabili deve supportare il [pattern di controllo Selection.](uiauto-implementingselection.md)                         |
| [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider)         | Obbligatoria      | Poiché il controllo calendario ha sempre un'intestazione all'interno del sottoalbero per i giorni della settimana, il pattern di controllo [Table](uiauto-implementingtable.md) deve essere supportato.                                                                                                                                                     |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)         | No            | Il [pattern di](uiauto-implementingvalue.md) controllo Value non è necessario per i controlli calendario perché l'elemento non può impostare il valore direttamente nel controllo. Se al controllo è associata una data specifica, le informazioni devono essere fornite dal pattern [di controllo Selection.](uiauto-implementingselection.md) |



 

## <a name="required-events"></a>Eventi obbligatori

Nella tabella seguente sono elencati Automazione interfaccia utente eventi che i controlli calendario devono supportare. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automazione interfaccia utente eventi                                                                                                                                        | Note                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                           |                                                                                                                                                                                                              |
| [**Interfaccia \_ utente Evento di modifica della proprietà BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md)                      |                                                                                                                                                                                                              |
| [**Interfaccia \_ utente Evento di modifica della proprietà IsEnabledPropertyId.**](uiauto-automation-element-propids.md)                                      | Se il controllo supporta la [**proprietà IsEnabled,**](uiauto-automation-element-propids.md) deve supportare questo evento.                                                                                     |
| [**Interfaccia \_ utente Evento di modifica della proprietà IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)                                  | Se il controllo supporta la [**proprietà IsOffscreen,**](uiauto-automation-element-propids.md) deve supportare questo evento.                                                                                   |
| [**Layout \_ dell'interfaccia utenteInvalidatedEventId**](uiauto-event-ids.md)                                                                     |                                                                                                                                                                                                              |
| [**Interfaccia \_ utente Evento di modifica della proprietà MultipleViewCurrentViewPropertyId.**](uiauto-control-pattern-propids.md)             | Se il controllo supporta la [**proprietà CurrentView**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-get_currentview) del pattern di [controllo MultipleView,](uiauto-implementingmultipleview.md) deve supportare questo evento. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                       |                                                                                                                                                                                                              |
| [**Interfaccia \_ utente Evento di modifica della proprietà ScrollHorizontallyScrollablePropertyId.**](uiauto-control-pattern-propids.md)   | Se il controllo supporta il pattern [di controllo Scroll,](uiauto-implementingscroll.md) deve supportare questo evento.                                                                                             |
| [**Interfaccia \_ utente Evento di modifica della proprietà ScrollHorizontalScrollPercentPropertyId.**](uiauto-control-pattern-propids.md) | Se il controllo supporta il pattern [di controllo Scroll,](uiauto-implementingscroll.md) deve supportare questo evento.                                                                                             |
| [**Interfaccia \_ utente Evento di modifica della proprietà ScrollHorizontalViewSizePropertyId.**](uiauto-control-pattern-propids.md)           | Se il controllo supporta il pattern [di controllo Scroll,](uiauto-implementingscroll.md) deve supportare questo evento.                                                                                             |
| [**Interfaccia \_ utente Evento di modifica della proprietà ScrollVerticalScrollPercentPropertyId.**](uiauto-control-pattern-propids.md)     | Se il controllo supporta il pattern [di controllo Scroll,](uiauto-implementingscroll.md) deve supportare questo evento.                                                                                             |
| [**Interfaccia \_ utente Evento di modifica della proprietà ScrollVerticallyScrollablePropertyId.**](uiauto-control-pattern-propids.md)       | Se il controllo supporta il pattern [di controllo Scroll,](uiauto-implementingscroll.md) deve supportare questo evento.                                                                                             |
| [**Interfaccia \_ utente Evento di modifica della proprietà ScrollVerticalViewSizePropertyId.**](uiauto-control-pattern-propids.md)               | Se il controllo supporta il pattern [di controllo Scroll,](uiauto-implementingscroll.md) deve supportare questo evento.                                                                                             |
| [**UIA \_ Selection \_ InvalidatedEventId**](uiauto-event-ids.md)                                                            |                                                                                                                                                                                                              |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente](uiauto-controltypesoverview.md)
</dt> <dt>

[Cenni preliminari su automazione interfaccia utente](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




