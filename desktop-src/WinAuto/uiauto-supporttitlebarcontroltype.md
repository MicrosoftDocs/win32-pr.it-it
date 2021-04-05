---
title: Tipo di controllo barra di titolo
description: In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo barra del titolo. Un controllo barra del titolo rappresenta una barra del titolo o della didascalia in una finestra.
ms.assetid: dc707198-ceb6-4fbf-ace4-8fec88c92b98
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo barra di titolo
- Automazione interfaccia utente, tipo di controllo barra di titolo
- Automazione interfaccia utente, struttura ad albero per il tipo di controllo barra del titolo
- Automazione interfaccia utente, proprietà per il tipo di controllo barra di titolo
- Automazione interfaccia utente, pattern di controllo per il tipo di controllo barra del titolo
- Automazione interfaccia utente, eventi per il tipo di controllo barra di titolo
- strutture ad albero, tipo di controllo barra di titolo
- Proprietà, tipo di controllo barra di titolo
- pattern di controllo, tipo di controllo barra di titolo
- eventi, tipo di controllo barra di titolo
- supporto per il tipo di controllo barra di titolo
- Tipo di controllo barra di titolo
- tipi di controllo, struttura ad albero per il tipo di controllo barra del titolo
- tipi di controllo, pattern di controllo per il tipo di controllo barra del titolo
- tipi di controllo, supporto per la barra del titolo
- tipi di controllo, barra di titolo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f9471d08479345bf8c1df118f720bf273d4d89d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955798"
---
# <a name="titlebar-control-type"></a>Tipo di controllo barra di titolo

In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo **barra** del titolo. Un controllo barra del titolo rappresenta una barra del titolo o della didascalia in una finestra.

Nelle sezioni seguenti vengono definiti la struttura ad albero, le proprietà, i pattern di controllo e gli eventi di automazione interfaccia utente necessari per il tipo di controllo **barra** del titolo. I requisiti di automazione interfaccia utente si applicano a tutti i controlli barra del titolo in cui la piattaforma/Framework dell'interfaccia utente integra il supporto di automazione interfaccia utente per tipi di controllo e pattern di controllo

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Pattern di controllo obbligatori](#required-control-patterns)
-   [Eventi obbligatori](#required-events)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

Nella tabella seguente viene illustrata una tipica visualizzazione del controllo e del contenuto dell'albero di automazione interfaccia utente relativo ai controlli barra del titolo e viene descritto il possibile contenuto di ogni visualizzazione. Per altre informazioni sull'albero di automazione interfaccia utente, vedere [Cenni preliminari sull'albero di automazione interfaccia utente](uiauto-treeoverview.md).



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
<li>TitleBar
<ul>
<li>Menu (0 o 1)</li>
<li>Button (0 o più)</li>
</ul></li>
</ul></td>
<td>(Non applicabile; il controllo barra del titolo non include contenuto)</td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a>Proprietà rilevanti

La tabella seguente elenca le proprietà di automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per il tipo di controllo della **barra** del titolo. Per altre informazioni sulle proprietà di automazione interfaccia utente, vedere [recupero di proprietà da elementi di automazione interfaccia utente](uiauto-propertiesforclients.md).



| Proprietà di automazione interfaccia utente                                                                                              | Valore        | Note                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_AUTOMATIONIDPROPERTYID UIA**](uiauto-automation-element-propids.md)                 | Vedere le note.   | Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata della struttura ad albero di automazione interfaccia utente.                                                                                         |
| [**\_BOUNDINGRECTANGLEPROPERTYID UIA**](uiauto-automation-element-propids.md)       | Vedere le note.   | Il valore esposto da questa proprietà deve includere tutti i controlli contenuti.                                                                                                             |
| [**\_CLICKABLEPOINTPROPERTYID UIA**](uiauto-automation-element-propids.md)             | Vedere le note.   | Supportata se è presente un rettangolo di delimitazione. Se non tutti i punti all'interno del rettangolo di delimitazione sono selezionabili e l'elemento esegue un hit testing specializzato, eseguire l'override e fornire un punto selezionabile. |
| [**\_CONTROLTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md)                   | **TitleBar** | Questo valore è uguale per tutti i framework dell'interfaccia utente.                                                                                                                                                        |
| [**\_ISCONTENTELEMENTPROPERTYID UIA**](uiauto-automation-element-propids.md)         | FALSE        | Il controllo barra del titolo non viene mai incluso nella visualizzazione contenuto dell'albero di automazione interfaccia utente.                                                                                                               |
| [**\_ISCONTROLELEMENTPROPERTYID UIA**](uiauto-automation-element-propids.md)         | true         | Il controllo barra del titolo viene sempre incluso nella visualizzazione controlli dell'albero di automazione interfaccia utente.                                                                                                              |
| [**\_ISKEYBOARDFOCUSABLEPROPERTYID UIA**](uiauto-automation-element-propids.md)   | FALSE        | Un controllo barra del titolo non ha mai lo stato attivo della tastiera.                                                                                                                                                        |
| [**\_ISOFFSCREENPROPERTYID UIA**](uiauto-automation-element-propids.md)                   | Dipende da      | Un controllo barra del titolo restituisce un valore a seconda che sia visibile sullo schermo.                                                                                                                |
| [**\_LABELEDBYPROPERTYID UIA**](uiauto-automation-element-propids.md)                       | Vedere le note.   | Un controllo barra del titolo in genere non dispone di un'etichetta.                                                                                                                                                 |
| [**\_LOCALIZEDCONTROLTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md) | Vedere le note.   | Stringa localizzata corrispondente al tipo di controllo TitleBar. Il valore predefinito è "barra del titolo" per en-US o inglese (Stati Uniti).                                                                  |
| [**\_NAMEPROPERTYID UIA**](uiauto-automation-element-propids.md)                                 | ""           | Una barra del titolo non è contenuto; le informazioni testuali sono esposte dal nome della finestra padre.                                                                                                     |



 

## <a name="required-control-patterns"></a>Pattern di controllo obbligatori

Il tipo di controllo **barra** del titolo non è necessario per supportare alcun pattern di controllo. La relativa funzionalità viene esposta tramite il pattern di controllo [Window](uiauto-implementingwindow.md) sul tipo di controllo [Window](uiauto-supportwindowcontroltype.md) .

## <a name="required-events"></a>Eventi obbligatori

La tabella seguente elenca gli eventi di automazione interfaccia utente necessari per supportare i controlli della barra del titolo. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



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

 

 




