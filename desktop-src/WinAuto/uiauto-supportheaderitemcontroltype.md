---
title: Tipo di controllo HeaderItem
description: In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo HeaderItem.
ms.assetid: c70420d6-d9f3-47c8-a09f-35ed170f815f
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo HeaderItem
- Automazione interfaccia utente, tipo di controllo HeaderItem
- Automazione interfaccia utente, struttura ad albero per il tipo di controllo HeaderItem
- Automazione interfaccia utente, proprietà per il tipo di controllo HeaderItem
- Automazione interfaccia utente, pattern di controllo per il tipo di controllo HeaderItem
- Automazione interfaccia utente, eventi per il tipo di controllo HeaderItem
- strutture ad albero, tipo di controllo HeaderItem
- Proprietà, tipo di controllo HeaderItem
- pattern di controllo, tipo di controllo HeaderItem
- eventi, tipo di controllo HeaderItem
- supporto per il tipo di controllo HeaderItem
- Tipo di controllo HeaderItem
- tipi di controllo, struttura ad albero per il tipo di controllo HeaderItem
- tipi di controllo, pattern di controllo per il tipo di controllo HeaderItem
- tipi di controllo, supporto per HeaderItem
- tipi di controllo, HeaderItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bab61f92a6ab4db221810f9f083279ade4bf353
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298153"
---
# <a name="headeritem-control-type"></a>Tipo di controllo HeaderItem

In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo **HeaderItem** .

Il tipo di controllo **HeaderItem** fornisce un'etichetta visiva per una riga o una colonna di informazioni.

Nelle sezioni seguenti vengono definiti la struttura ad albero, le proprietà, i pattern di controllo e gli eventi di automazione interfaccia utente necessari per il tipo di controllo **HeaderItem** . I requisiti di automazione interfaccia utente si applicano a tutti i controlli elemento intestazione in cui la piattaforma/Framework dell'interfaccia utente integra il supporto di automazione interfaccia utente per i tipi di controllo e pattern di controllo

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Pattern di controllo obbligatori](#required-control-patterns)
-   [Eventi obbligatori](#required-events)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

Nella tabella seguente viene illustrata una tipica visualizzazione del controllo e del contenuto della struttura ad albero di automazione interfaccia utente relativa ai controlli elemento intestazione e viene descritto il possibile contenuto di ogni visualizzazione. Per altre informazioni sull'albero di automazione interfaccia utente, vedere [Cenni preliminari sull'albero di automazione interfaccia utente](uiauto-treeoverview.md).



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
<li>HeaderItem</li>
</ul></td>
<td>(Non applicabile)</td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a>Proprietà rilevanti

La tabella seguente elenca le proprietà di automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per il tipo di controllo **HeaderItem** . Per altre informazioni sulle proprietà di automazione interfaccia utente, vedere [recupero di proprietà da elementi di automazione interfaccia utente](uiauto-propertiesforclients.md).



| Proprietà di automazione interfaccia utente                                                                                              | Valore          | Note                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_AUTOMATIONIDPROPERTYID UIA**](uiauto-automation-element-propids.md)                 | Vedere le note.     | Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata della struttura ad albero di automazione interfaccia utente.                                                                                         |
| [**\_BOUNDINGRECTANGLEPROPERTYID UIA**](uiauto-automation-element-propids.md)       | Vedere le note.     | Il rettangolo più esterno che contiene l'intero controllo.                                                                                                                                             |
| [**\_CLICKABLEPOINTPROPERTYID UIA**](uiauto-automation-element-propids.md)             | Vedere le note.     | Supportata se è presente un rettangolo di delimitazione. Se non tutti i punti all'interno del rettangolo di delimitazione sono selezionabili e l'elemento esegue un hit testing specializzato, eseguire l'override e fornire un punto selezionabile. |
| [**\_CONTROLTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md)                   | **HeaderItem** | Questo valore è uguale per tutti i framework dell'interfaccia utente.                                                                                                                                                        |
| [**\_ISCONTENTELEMENTPROPERTYID UIA**](uiauto-automation-element-propids.md)         | FALSE          | Il controllo elemento intestazione non è incluso nella visualizzazione contenuto dell'albero di automazione interfaccia utente.                                                                                                               |
| [**\_ISCONTROLELEMENTPROPERTYID UIA**](uiauto-automation-element-propids.md)         | true           | Il controllo elemento intestazione viene sempre incluso nella visualizzazione controlli dell'albero di automazione interfaccia utente.                                                                                                            |
| [**\_ISKEYBOARDFOCUSABLEPROPERTYID UIA**](uiauto-automation-element-propids.md)   | Vedere le note.     | Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.                                                                                                                            |
| [**\_ITEMSTATUSPROPERTYID UIA**](uiauto-automation-element-propids.md)                     | Vedere le note      | Questa proprietà fornisce informazioni per i tipi di ordinamento per l'elemento dell'intestazione.                                                                                                                               |
| [**\_LABELEDBYPROPERTYID UIA**](uiauto-automation-element-propids.md)                       | NULL           | I controlli elemento intestazione non hanno un'etichetta di testo statico.                                                                                                                                                |
| [**\_LOCALIZEDCONTROLTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md) | Vedere le note.     | Stringa localizzata corrispondente al tipo di controllo **HeaderItem** . Il valore predefinito è "elemento intestazione" per en-US o inglese (Stati Uniti).                                                          |
| [**\_NAMEPROPERTYID UIA**](uiauto-automation-element-propids.md)                                 | Vedere le note.     | Il controllo elemento intestazione è sempre associato a un'etichetta automatica.                                                                                                                                                     |



 

## <a name="required-control-patterns"></a>Pattern di controllo obbligatori

La tabella seguente elenca i pattern di controllo di automazione interfaccia utente che devono essere supportati da tutti i controlli elemento intestazione. Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Pattern di controllo                                         | Supporto | Note                                                                                                                             |
|---------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)       | Dipende da | Implementare il pattern di controllo [Invoke](uiauto-implementinginvoke.md) se è possibile fare clic sul controllo elemento intestazione per ordinare i dati. |
| [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) | Dipende da | Implementare il pattern di controllo [Transform](uiauto-implementingtransform.md) se il controllo elemento intestazione può essere ridimensionato.            |



 

## <a name="required-events"></a>Eventi obbligatori

La tabella seguente elenca gli eventi di automazione interfaccia utente necessari per supportare i controlli elemento intestazione. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



| Evento di automazione interfaccia utente                                                                                                                   | Note                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**\_AUTOMATIONFOCUSCHANGEDEVENTID UIA**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà BoundingRectanglePropertyId. |                                                                                                                            |
| [**\_Richiama \_ InvokedEventId**](uiauto-event-ids.md)                                                     | Se il controllo supporta il pattern di controllo [Invoke](uiauto-implementinginvoke.md) , deve supportare questo evento.           |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsEnabledPropertyId.                 | Se il controllo supporta la proprietà [**IsEnabled**](uiauto-automation-element-propids.md) , deve supportare questo evento.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsOffscreenPropertyId.             | Se il controllo supporta la proprietà [**IsOffscreen**](uiauto-automation-element-propids.md) , deve supportare questo evento. |
| [**\_STRUCTURECHANGEDEVENTID UIA**](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente](uiauto-controltypesoverview.md)
</dt> <dt>

[Cenni preliminari su automazione interfaccia utente](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




