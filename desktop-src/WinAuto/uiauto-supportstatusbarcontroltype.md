---
title: Tipo di controllo StatusBar
description: Questo argomento fornisce informazioni sul supporto di Microsoft Automazione interfaccia utente per il tipo di controllo StatusBar.
ms.assetid: a28df0a1-95a8-4941-a00d-1f5570589626
keywords:
- Automazione interfaccia utente,supporto per il tipo di controllo StatusBar
- Automazione interfaccia utente, tipo di controllo StatusBar
- Automazione interfaccia utente,struttura ad albero per il tipo di controllo StatusBar
- Automazione interfaccia utente,proprietà per il tipo di controllo StatusBar
- Automazione interfaccia utente,pattern di controllo per il tipo di controllo StatusBar
- Automazione interfaccia utente,eventi per il tipo di controllo StatusBar
- strutture ad albero, tipo di controllo StatusBar
- proprietà, tipo di controllo StatusBar
- pattern di controllo, tipo di controllo StatusBar
- eventi, tipo di controllo StatusBar
- supporto per il tipo di controllo StatusBar
- StatusBar (tipo di controllo)
- tipi di controllo, struttura ad albero per il tipo di controllo StatusBar
- tipi di controllo, pattern di controllo per il tipo di controllo StatusBar
- tipi di controllo, supporto per StatusBar
- tipi di controllo, StatusBar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 032c0122bc472a8b2deace8cc48d41926778a11b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473697"
---
# <a name="statusbar-control-type"></a>Tipo di controllo StatusBar

Questo argomento fornisce informazioni sul supporto di Microsoft Automazione interfaccia utente per il **tipo di controllo StatusBar.**

In un controllo barra di stato sono in genere presenti informazioni su un oggetto visualizzato in una finestra di un'applicazione, i componenti dell'oggetto o informazioni contestuali collegate alle operazioni di tale oggetto all'interno dell'applicazione.

Le sezioni seguenti definiscono la struttura ad Automazione interfaccia utente struttura ad albero, le proprietà, i pattern di controllo e gli eventi per il **tipo di controllo StatusBar.** I Automazione interfaccia utente di controllo si applicano a tutti i controlli barra di stato in cui il framework o la piattaforma dell'interfaccia utente si integra Automazione interfaccia utente per i tipi di controllo e i pattern di controllo.

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Pattern di controllo obbligatori](#required-control-patterns)
-   [Eventi obbligatori](#required-events)
-   [Osservazioni:](#remarks)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

La tabella seguente illustra un controllo tipico e una visualizzazione contenuto dell'albero Automazione interfaccia utente relativo ai controlli barra di stato e descrive gli elementi che possono essere contenuti in ogni visualizzazione. Per altre informazioni sull'albero Automazione interfaccia utente, vedere panoramica [Automazione interfaccia utente albero.](uiauto-treeoverview.md)




| Visualizzazione controlli | Visualizzazione contenuto | 
|--------------|--------------|
| <ul><li>StatusBar<ul><li>Edit (0 o più)</li><li>ProgressBar (0 o più)</li><li>Image (0 o più)</li><li>Button (0 o più)</li></ul></li></ul> | <ul><li>StatusBar<ul><li>Edit (0 o più)</li><li>ProgressBar (0 o più)</li><li>Image (0 o più)</li><li>Button (0 o più)</li></ul></li></ul> | 




 

## <a name="relevant-properties"></a>Proprietà rilevanti

La tabella seguente elenca le proprietà Automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per i controlli barra di stato. Per altre informazioni sulle Automazione interfaccia utente, vedere [Recupero di proprietà da Automazione interfaccia utente elementi](uiauto-propertiesforclients.md).



| Proprietà di automazione interfaccia utente                                                                                              | valore         | Note                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Vedere le note.    | Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata dell'Automazione interfaccia utente albero.                                                                                                        |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vedere le note.    | Il rettangolo di delimitazione di una barra di stato deve includere tutti i controlli in esso contenuti.                                                                                                                      |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vedere le note.    | Supportata se è presente un rettangolo di delimitazione. Se sono presenti aree all'interno del rettangolo di delimitazione che non sono selezionabili e l'elemento esegue un hit testing specializzato, eseguire l'override di questo oggetto e fornire un punto selezionabile. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **StatusBar** |                                                                                                                                                                                                                     |
| [**\_IsContentElementPropertyId dell'interfaccia utente**](uiauto-automation-element-propids.md)         | true          | Il controllo barra di stato è sempre incluso nella visualizzazione contenuto dell'Automazione interfaccia utente albero.                                                                                                                            |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | true          | Il controllo barra di stato è sempre incluso nella visualizzazione controlli dell'Automazione interfaccia utente albero.                                                                                                                            |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Dipende da       | Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.                                                                                                                                           |
| [**UIA \_ IsOffscreenPropertyId**](uiauto-automation-element-propids.md)                   | Dipende da       | Se un controllo barra di stato non è attualmente visibile, restituirà TRUE per questa proprietà.                                                                                                                            |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULL          | Il controllo barra di stato in genere non ha un'etichetta.                                                                                                                                                             |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vedere le note.    | Stringa localizzata corrispondente al **tipo di controllo StatusBar.** Il valore predefinito è "barra di stato" per en-US o inglese (Stati Uniti).                                                                           |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Vedere le note.    | Il controllo barra di stato non necessita di un nome a meno che non vengano usati più controlli all'interno di un'applicazione. In questo caso, distinguere ogni barra con nomi quali "Stato Internet" o "Stato applicazione".                    |
| [**UIA \_ OrientationPropertyId**](uiauto-automation-element-propids.md)                   | Dipende da       | Valore che indica l'orientamento del controllo: orizzontale o verticale.                                                                                                                                               |



 

## <a name="required-control-patterns"></a>Pattern di controllo obbligatori

Nella tabella seguente sono elencati i Automazione interfaccia utente che devono essere supportati per i controlli barra di stato. Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Pattern di controllo                               | Supporto  | Note                                                                                                                                                                        |
|-----------------------------------------------|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) | Facoltativo | I controlli barra di stato devono supportare il pattern di controllo [Grid](uiauto-implementinggrid.md) in modo che sia possibile monitorare le singole parti e farvi facilmente riferimento per ottenere informazioni. |



 

## <a name="required-events"></a>Eventi obbligatori

La tabella seguente elenca gli eventi Automazione interfaccia utente che i controlli barra di stato devono supportare. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automazione interfaccia utente eventi                                                                                                                   | Note                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                   |
| [**Interfaccia \_ utente Evento di modifica della proprietà BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md) |                                                                                   |
| [**Interfaccia \_ utente Evento di modifica della proprietà IsEnabledPropertyId.**](uiauto-automation-element-propids.md)                 | Se il controllo supporta la **proprietà IsEnabled,** deve supportare questo evento.   |
| [**Interfaccia \_ utente Evento di modifica della proprietà IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)             | Se il controllo supporta la **proprietà IsOffscreen,** deve supportare questo evento. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                   |



 

## <a name="remarks"></a>Commenti

È consigliabile usare i controlli di modifica come elementi figlio della griglia in una barra di stato. L'uso dei controlli di modifica rende più semplice associare lo scopo del campo di stato al relativo valore usando il nome dell'elemento e la proprietà value. Poiché i controlli di testo non devono supportare il pattern di controllo **Value,** non devono essere usati come elementi figlio della griglia.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente](uiauto-controltypesoverview.md)
</dt> <dt>

[Cenni preliminari su automazione interfaccia utente](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




