---
title: Tipo di controllo ProgressBar
description: In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo ProgressBar.
ms.assetid: 2ea0c1f1-1a0a-4360-bdcb-8edc13cc3c31
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo ProgressBar
- Automazione interfaccia utente, tipo di controllo ProgressBar
- Automazione interfaccia utente, struttura ad albero per il tipo di controllo ProgressBar
- Automazione interfaccia utente, proprietà per il tipo di controllo ProgressBar
- Automazione interfaccia utente, pattern di controllo per il tipo di controllo ProgressBar
- Automazione interfaccia utente, eventi per il tipo di controllo ProgressBar
- strutture ad albero, tipo di controllo ProgressBar
- Proprietà, tipo di controllo ProgressBar
- pattern di controllo, tipo di controllo ProgressBar
- eventi, tipo di controllo ProgressBar
- supporto per il tipo di controllo ProgressBar
- ProgressBar (tipo di controllo)
- tipi di controllo, struttura ad albero per il tipo di controllo ProgressBar
- tipi di controllo, pattern di controllo per il tipo di controllo ProgressBar
- tipi di controllo, supporto per ProgressBar
- tipi di controllo, ProgressBar
ms.topic: article
ms.date: 12/04/2019
ms.openlocfilehash: 98be22a4a3d3b99e113d3c0d1402f2c45ee25550
ms.sourcegitcommit: 6f7576b297d54c0b8f9c79e02c912b83041aa4fb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/06/2019
ms.locfileid: "104117265"
---
# <a name="progressbar-control-type"></a>Tipo di controllo ProgressBar

In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo **ProgressBar** .

I controlli indicatore di stato indicano lo stato di avanzamento di un'operazione di lunga durata. Il controllo è costituito da un rettangolo che viene riempito gradualmente con il colore di sistema durante l'esecuzione dell'operazione.

Nelle sezioni seguenti vengono definiti la struttura ad albero, le proprietà, i pattern di controllo e gli eventi di automazione interfaccia utente necessari per il tipo di controllo **ProgressBar** . I requisiti di automazione interfaccia utente si applicano a tutti i controlli indicatore di stato in cui la piattaforma/Framework dell'interfaccia utente integra il supporto di automazione interfaccia utente per i tipi di controllo e i pattern

In questo argomento sono contenute le sezioni seguenti.

- [Struttura ad albero tipica](#typical-tree-structure)
- [Proprietà rilevanti](#relevant-properties)
- [Pattern di controllo obbligatori](#required-control-patterns)
- [Eventi obbligatori](#required-events)
- [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

Nella tabella seguente viene illustrata una tipica visualizzazione del controllo e del contenuto dell'albero di automazione interfaccia utente relativo ai controlli indicatore di stato e viene descritto il possibile contenuto di ogni visualizzazione. Per altre informazioni sull'albero di automazione interfaccia utente, vedere [Cenni preliminari sull'albero di automazione interfaccia utente](uiauto-treeoverview.md).

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
<li>ProgressBar</li>
</ul></td>
<td><ul>
<li>ProgressBar</li>
</ul></td>
</tr>
</tbody>
</table>

I controlli indicatore di stato non hanno elementi figlio nel controllo o nella visualizzazione contenuto dell'albero di automazione interfaccia utente.

## <a name="relevant-properties"></a>Proprietà rilevanti

La tabella seguente elenca le proprietà di automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per gli indicatori di stato. Per altre informazioni sulle proprietà di automazione interfaccia utente, vedere [recupero di proprietà da elementi di automazione interfaccia utente](uiauto-propertiesforclients.md).

| Proprietà di automazione interfaccia utente                                                                                              | Valore           | Note                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_AUTOMATIONIDPROPERTYID UIA**](uiauto-automation-element-propids.md)                 | Vedere le note.      | Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata della struttura ad albero di automazione interfaccia utente.                                                                                         |
| [**\_BOUNDINGRECTANGLEPROPERTYID UIA**](uiauto-automation-element-propids.md)       | Vedere le note.      | Il rettangolo più esterno che contiene l'intero controllo.                                                                                                                                             |
| [**\_CLICKABLEPOINTPROPERTYID UIA**](uiauto-automation-element-propids.md)             | Vedere le note.      | Supportata se è presente un rettangolo di delimitazione. Se non tutti i punti all'interno del rettangolo di delimitazione sono selezionabili e l'elemento esegue un hit testing specializzato, eseguire l'override e fornire un punto selezionabile. |
| [**\_CONTROLTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md)                   | **ProgressBar** |                                                                                                                                                                                                      |
| [**\_ISCONTENTELEMENTPROPERTYID UIA**](uiauto-automation-element-propids.md)         | **TRUE**        | Il controllo indicatore di stato viene sempre incluso nella visualizzazione contenuto dell'albero di automazione interfaccia utente.                                                                                                           |
| [**\_ISCONTROLELEMENTPROPERTYID UIA**](uiauto-automation-element-propids.md)         | **TRUE**        | Il controllo indicatore di stato viene sempre incluso nella visualizzazione controlli dell'albero di automazione interfaccia utente.                                                                                                           |
| [**\_ISKEYBOARDFOCUSABLEPROPERTYID UIA**](uiauto-automation-element-propids.md)   | Vedere le note.      | Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.                                                                                                                            |
| [**\_LABELEDBYPROPERTYID UIA**](uiauto-automation-element-propids.md)                       | Vedere le note.      | Se è presente un'etichetta di testo statico, questa proprietà deve esporre un riferimento a tale controllo.                                                                                                              |
| [**\_LOCALIZEDCONTROLTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md) | Vedere le note.      | Stringa localizzata corrispondente al tipo di controllo **ProgressBar** . Il valore predefinito è "indicatore di stato" per en-US o inglese (Stati Uniti).                                                        |
| [**\_NAMEPROPERTYID UIA**](uiauto-automation-element-propids.md)                                 | Vedere le note.      | Il controllo indicatore di stato in genere ricava il proprio nome da un'etichetta di testo statico. Se non è presente alcuna etichetta di testo statico, lo sviluppatore dell'applicazione deve esporre un valore per la proprietà Name.                  |



 

## <a name="required-control-patterns"></a>Pattern di controllo obbligatori

La tabella seguente elenca i pattern di controllo di automazione interfaccia utente che devono essere supportati dai controlli indicatore di stato. Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Pattern di controllo/proprietà del pattern                              | Supporto/valore | Note                                                                                                                                      |
|---------------------------------------------------------------|---------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider)     | Dipende da       | I controlli indicatore di stato che accettano un intervallo numerico devono implementare il pattern di controllo [RangeValue](uiauto-implementingrangevalue.md) .        |
| [**Minima**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_minimum)         | Dipende da           | Il valore di questa proprietà è il valore minimo su cui è possibile impostare il controllo. Questo valore deve essere minore di [**Maximum**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_maximum).                                                      |
| [**Massimo**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_maximum)         | Dipende da         | Il valore di questa proprietà è il valore massimo su cui è possibile impostare il controllo. Questo valore deve essere maggiore del valore [**minimo**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_minimum).                                                        |
| [**SmallChange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_smallchange) | **NaN**       | Questa proprietà non è necessaria perché i controlli indicatore di stato sono di sola lettura.                                                                 |
| [**LargeChange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_largechange) | **NaN**       | Questa proprietà non è necessaria perché i controlli indicatore di stato sono di sola lettura.                                                                 |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)               | Dipende da       | I controlli indicatore di stato che forniscono un'indicazione testuale dello stato di avanzamento devono implementare il pattern di controllo [value](uiauto-implementingvalue.md) . |
| [**IsReadOnly**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_isreadonly)        | **TRUE**      | Il valore di questa proprietà è sempre **true**.                                                                                            |
| [**Valore**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_value)                  | Vedere le note.    | Questa proprietà espone lo stato di avanzamento in formato testuale di un controllo indicatore di stato.                                                                          |



 

## <a name="required-events"></a>Eventi obbligatori

La tabella seguente elenca gli eventi di automazione interfaccia utente che sono necessari per supportare le barre di stato. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



| Evento di automazione interfaccia utente                                                                                                                   | Note                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**\_AUTOMATIONFOCUSCHANGEDEVENTID UIA**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà BoundingRectanglePropertyId. |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsEnabledPropertyId.                 | Se il controllo supporta la proprietà [**IsEnabled**](uiauto-automation-element-propids.md) , deve supportare questo evento.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsOffscreenPropertyId.             | Se il controllo supporta la proprietà [**IsOffscreen**](uiauto-automation-element-propids.md) , deve supportare questo evento. |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà NamePropertyId.                           |                                                                                                                            |
| [**\_STRUCTURECHANGEDEVENTID UIA**](uiauto-event-ids.md)                                                  |                                                                                                                            |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà RangeValueValuePropertyId.        | Se il controllo supporta il pattern di controllo [RangeValue](uiauto-implementingrangevalue.md) , deve supportare questo evento.   |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ValueValuePropertyId.                  | Se il controllo supporta il pattern di controllo [value](uiauto-implementingvalue.md) , deve supportare questo evento.             |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente](uiauto-controltypesoverview.md)
</dt> <dt>

[Cenni preliminari su automazione interfaccia utente](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




