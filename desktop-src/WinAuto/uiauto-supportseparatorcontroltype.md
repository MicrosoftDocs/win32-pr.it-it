---
title: Tipo di controllo Separator
description: In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo Separator.
ms.assetid: 4987b05a-101e-48b1-aed2-bd7206146f70
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo Separator
- Automazione interfaccia utente, tipo di controllo Separator
- Automazione interfaccia utente, struttura ad albero per il tipo di controllo Separator
- Automazione interfaccia utente, proprietà per il tipo di controllo Separator
- Automazione interfaccia utente, pattern di controllo per il tipo di controllo Separator
- Automazione interfaccia utente, eventi per il tipo di controllo Separator
- strutture ad albero, tipo di controllo Separator
- Proprietà, tipo di controllo Separator
- pattern di controllo, tipo di controllo Separator
- eventi, tipo di controllo Separator
- supporto per il tipo di controllo Separator
- Separator (tipo di controllo)
- tipi di controllo, struttura ad albero per il tipo di controllo Separator
- tipi di controllo, pattern di controllo per il tipo di controllo Separator
- tipi di controllo, supporto per il separatore
- tipi di controllo, separatore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92cdf6c15dbe461e78877c6b93f0ff4b52f67fc8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515931"
---
# <a name="separator-control-type"></a>Tipo di controllo Separator

In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo **separator** .

I controlli separatore vengono usati per dividere visivamente uno spazio in due aree. Ad esempio, un controllo separatore può essere una barra che definisce due riquadri in una finestra. Se il separatore può essere spostato, il controllo deve essere esposto come il tipo di controllo Thumb.

Nelle sezioni seguenti vengono definiti la struttura ad albero, le proprietà, i pattern di controllo e gli eventi di automazione interfaccia utente necessari per il tipo di controllo **separator** . I requisiti di automazione interfaccia utente si applicano a tutti i controlli separatore in cui la piattaforma/Framework dell'interfaccia utente integra il supporto di automazione interfaccia utente per i tipi di controllo e pattern

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Pattern di controllo obbligatori](#required-control-patterns)
-   [Eventi obbligatori](#required-events)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

Nella tabella seguente viene illustrata una tipica visualizzazione del controllo e del contenuto dell'albero di automazione interfaccia utente relativo ai controlli separatore e viene descritto il possibile contenuto di ogni visualizzazione. Per altre informazioni sull'albero di automazione interfaccia utente, vedere [Cenni preliminari sull'albero di automazione interfaccia utente](uiauto-treeoverview.md).



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
<li>Separatore</li>
</ul></td>
<td><ul>
<li>Il tipo di controllo <strong>separator</strong> non dispone mai di contenuto.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a>Proprietà rilevanti

La tabella seguente elenca le proprietà di automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per i controlli separatore. Per altre informazioni sulle proprietà di automazione interfaccia utente, vedere [recupero di proprietà da elementi di automazione interfaccia utente](uiauto-propertiesforclients.md).



| Proprietà di automazione interfaccia utente                                                                                              | Valore         | Note                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_AUTOMATIONIDPROPERTYID UIA**](uiauto-automation-element-propids.md)                 | Vedere le note.    | Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata della struttura ad albero di automazione interfaccia utente.                                                                                         |
| [**\_BOUNDINGRECTANGLEPROPERTYID UIA**](uiauto-automation-element-propids.md)       | Vedere le note.    | Il rettangolo più esterno che contiene l'intero controllo.                                                                                                                                             |
| [**\_CLICKABLEPOINTPROPERTYID UIA**](uiauto-automation-element-propids.md)             | Vedere le note.    | Supportata se è presente un rettangolo di delimitazione. Se non tutti i punti all'interno del rettangolo di delimitazione sono selezionabili e l'elemento esegue un hit testing specializzato, eseguire l'override e fornire un punto selezionabile. |
| [**\_CONTROLTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md)                   | **Separatore** |                                                                                                                                                                                                      |
| [**\_ISCONTENTELEMENTPROPERTYID UIA**](uiauto-automation-element-propids.md)         | FALSE         | Il controllo separatore non è mai un contenuto.                                                                                                                                                              |
| [**\_ISCONTROLELEMENTPROPERTYID UIA**](uiauto-automation-element-propids.md)         | true          | Il controllo separatore deve essere sempre un controllo.                                                                                                                                                      |
| [**\_ISKEYBOARDFOCUSABLEPROPERTYID UIA**](uiauto-automation-element-propids.md)   | Vedere le note.    | Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.                                                                                                                            |
| [**\_LABELEDBYPROPERTYID UIA**](uiauto-automation-element-propids.md)                       | NULL          | Il controllo separatore non dispone di un'etichetta statica.                                                                                                                                                  |
| [**\_LOCALIZEDCONTROLTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md) | Vedere le note.    | Stringa localizzata corrispondente al tipo di controllo **separator** . Il valore predefinito è "Separator" per en-US o inglese (Stati Uniti).                                                             |
| [**\_NAMEPROPERTYID UIA**](uiauto-automation-element-propids.md)                                 | ""            | Il controllo separatore non richiede una proprietà **Name** .                                                                                                                                          |



 

## <a name="required-control-patterns"></a>Pattern di controllo obbligatori

Il controllo separatore non deve supportare qualsiasi pattern di controllo. Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).

## <a name="required-events"></a>Eventi obbligatori

La tabella seguente elenca gli eventi di automazione interfaccia utente necessari per supportare i controlli separatore. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



| Evento di automazione interfaccia utente                                                                                                                   | Note                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**\_AUTOMATIONFOCUSCHANGEDEVENTID UIA**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà BoundingRectanglePropertyId. |                                                                                                                            |
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

 

 




