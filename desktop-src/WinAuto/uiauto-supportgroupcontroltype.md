---
title: Tipo di controllo gruppo
description: In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo Group.
ms.assetid: f8363c2f-dbff-43a3-831f-d30151829ef9
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo Group
- Automazione interfaccia utente, tipo di controllo gruppo
- Automazione interfaccia utente, struttura ad albero per il tipo di controllo Group
- Automazione interfaccia utente, proprietà per il tipo di controllo Group
- Automazione interfaccia utente, pattern di controllo per il tipo di controllo Group
- Automazione interfaccia utente, eventi per il tipo di controllo Group
- strutture ad albero, tipo di controllo Group
- Proprietà, tipo di controllo gruppo
- pattern di controllo, tipo di controllo Group
- eventi, tipo di controllo gruppo
- supporto per il tipo di controllo Group
- Group (tipo di controllo)
- tipi di controllo, struttura ad albero per il tipo di controllo Group
- tipi di controllo, pattern di controllo per il tipo di controllo Group
- tipi di controllo, supporto per il gruppo
- tipi di controllo, gruppo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44b630d0ef736d937e4f024c8131adc4c843b6e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395858"
---
# <a name="group-control-type"></a>Tipo di controllo gruppo

In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo **Group** .

Un controllo gruppo rappresenta un nodo all'interno di una gerarchia. Il tipo di controllo **Group** crea una separazione nell'albero di automazione interfaccia utente in modo che gli elementi raggruppati abbiano una divisione logica all'interno dell'albero di automazione interfaccia utente.

Nelle sezioni seguenti vengono definiti la struttura ad albero, le proprietà, i pattern di controllo e gli eventi di automazione interfaccia utente necessari per il tipo di controllo **Group** . I requisiti di automazione interfaccia utente si applicano a tutti i controlli gruppo in cui la piattaforma/Framework dell'interfaccia utente integra il supporto di automazione interfaccia utente per tipi di controllo e pattern di controllo

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Pattern di controllo obbligatori](#required-control-patterns)
-   [Eventi obbligatori](#required-events)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

Nella tabella seguente viene illustrata una tipica visualizzazione del controllo e del contenuto dell'albero di automazione interfaccia utente relativo ai controlli gruppo e viene descritto il possibile contenuto di ogni visualizzazione. Per altre informazioni sull'albero di automazione interfaccia utente, vedere [Cenni preliminari sull'albero di automazione interfaccia utente](uiauto-treeoverview.md).



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
<li>Group
<ul>
<li>0 o molti controlli</li>
</ul></li>
</ul></td>
<td><ul>
<li>Group
<ul>
<li>0 o molti controlli</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

I controlli gruppo includono in genere il supporto di automazione interfaccia utente per i tipi di controllo trovati sotto di essi nel sottoalbero, inclusi i tipi di controllo [ListItem](uiauto-supportlistitemcontroltype.md), [TreeItem](uiauto-supporttreeitemcontroltype.md)e [DataItem](uiauto-supportdataitemcontroltype.md) . Poiché un controllo gruppo è un contenitore generico, è possibile che qualsiasi tipo di controllo si trovi sotto il controllo gruppo nell'albero.

## <a name="relevant-properties"></a>Proprietà rilevanti

La tabella seguente elenca le proprietà di automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per i controlli gruppo. Per altre informazioni sulle proprietà di automazione interfaccia utente, vedere [recupero di proprietà da elementi di automazione interfaccia utente](uiauto-propertiesforclients.md).



| Proprietà di automazione interfaccia utente                                                                                              | Valore      | Note                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_AUTOMATIONIDPROPERTYID UIA**](uiauto-automation-element-propids.md)                 | Vedere le note. | Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata della struttura ad albero di automazione interfaccia utente.                                                                                         |
| [**\_BOUNDINGRECTANGLEPROPERTYID UIA**](uiauto-automation-element-propids.md)       | Vedere le note. | Il rettangolo più esterno che contiene l'intero controllo.                                                                                                                                             |
| [**\_CLICKABLEPOINTPROPERTYID UIA**](uiauto-automation-element-propids.md)             | Vedere le note. | Supportata se è presente un rettangolo di delimitazione. Se non tutti i punti all'interno del rettangolo di delimitazione sono selezionabili e l'elemento esegue un hit testing specializzato, eseguire l'override e fornire un punto selezionabile. |
| [**\_CONTROLTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md)                   | **Gruppo**  |                                                                                                                                                                                                      |
| [**\_ISCONTENTELEMENTPROPERTYID UIA**](uiauto-automation-element-propids.md)         | **TRUE**   | Il controllo gruppo viene sempre incluso nella visualizzazione contenuto dell'albero di automazione interfaccia utente.                                                                                                                  |
| [**\_ISCONTROLELEMENTPROPERTYID UIA**](uiauto-automation-element-propids.md)         | **TRUE**   | Il controllo gruppo viene sempre incluso nella visualizzazione controlli dell'albero di automazione interfaccia utente.                                                                                                                  |
| [**\_ISKEYBOARDFOCUSABLEPROPERTYID UIA**](uiauto-automation-element-propids.md)   | Vedere le note. | Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.                                                                                                                            |
| [**\_LABELEDBYPROPERTYID UIA**](uiauto-automation-element-propids.md)                       | Vedere le note. | I controlli gruppo sono in genere associati a un'etichetta automatica. In questi casi, restituisce **null**. Se il gruppo ha un'etichetta di testo statico, restituire l'etichetta come valore della proprietà **LabeledBy** .                      |
| [**\_LOCALIZEDCONTROLTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md) | Vedere le note. | Stringa localizzata corrispondente al tipo di controllo **Group** . Il valore predefinito è "Group" per en-US o inglese (Stati Uniti).                                                                     |
| [**\_NAMEPROPERTYID UIA**](uiauto-automation-element-propids.md)                                 | Vedere le note. | Il controllo gruppo in genere ricava il proprio nome dal testo dell'etichetta applicata al controllo.                                                                                                                     |



 

## <a name="required-control-patterns"></a>Pattern di controllo obbligatori

La tabella seguente elenca i pattern di controllo di automazione interfaccia utente che devono essere supportati per il tipo di controllo **gruppo** . Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Pattern di controllo                                                   | Supporto | Note                                                                                                                                                 |
|-------------------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Dipende da | I controlli gruppo che possono essere usati per mostrare o nascondere le informazioni devono supportare il pattern di controllo [ExpandCollapse](uiauto-implementingexpandcollapse.md) . |



 

## <a name="required-events"></a>Eventi obbligatori

La tabella seguente elenca gli eventi di automazione interfaccia utente necessari per supportare i controlli di gruppo. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



| Evento di automazione interfaccia utente                                                                                                                                                | Note                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_AUTOMATIONFOCUSCHANGEDEVENTID UIA**](uiauto-event-ids.md)                                                                   |                                                                                                                                                  |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà BoundingRectanglePropertyId.                              |                                                                                                                                                  |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ExpandCollapseExpandCollapseStatePropertyId. | Se il controllo supporta il pattern di controllo pattern di controllo [ExpandCollapse](uiauto-implementingexpandcollapse.md) , deve supportare questo evento. |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsEnabledPropertyId.                                              | Se il controllo supporta la proprietà [**IsEnabled**](uiauto-automation-element-propids.md) , deve supportare questo evento.                         |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsOffscreenPropertyId.                                          | Se il controllo supporta la proprietà [**IsOffscreen**](uiauto-automation-element-propids.md) , deve supportare questo evento.                       |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ToggleToggleStatePropertyId.                                 | Se il controllo supporta il pattern di controllo [interruttore](uiauto-implementingtoggle.md) , deve supportare questo evento.                                 |
| [**\_STRUCTURECHANGEDEVENTID UIA**](uiauto-event-ids.md)                                                                               |                                                                                                                                                  |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente](uiauto-controltypesoverview.md)
</dt> <dt>

[Cenni preliminari su automazione interfaccia utente](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




