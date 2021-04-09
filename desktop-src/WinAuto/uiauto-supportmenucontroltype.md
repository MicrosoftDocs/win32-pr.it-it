---
title: Tipo di controllo menu
description: In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo menu.
ms.assetid: cdbb6db7-63d7-422e-952c-7b59779fefbe
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo menu
- Automazione interfaccia utente, tipo di controllo menu
- Automazione interfaccia utente, struttura ad albero per il tipo di controllo menu
- Automazione interfaccia utente, proprietà per il tipo di controllo menu
- Automazione interfaccia utente, pattern di controllo per il tipo di controllo menu
- Automazione interfaccia utente, eventi per il tipo di controllo menu
- strutture ad albero, tipo di controllo menu
- Proprietà, tipo di controllo menu
- pattern di controllo, tipo di controllo menu
- eventi, tipo di controllo menu
- supporto per il tipo di controllo menu
- Menu (tipo di controllo)
- tipi di controllo, struttura ad albero per il tipo di controllo menu
- tipi di controllo, pattern di controllo per il tipo di controllo menu
- tipi di controllo, supporto per menu
- tipi di controllo, menu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edee9f30f4d4cea123a2c7f5ff4dac235782faea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044606"
---
# <a name="menu-control-type"></a>Tipo di controllo menu

In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo **menu** .

Un controllo menu consente l'organizzazione gerarchica degli elementi associati a comandi e gestori eventi. In una tipica applicazione di Microsoft Windows, una barra dei menu contiene diversi pulsanti di menu (ad esempio **file**, **modifica** e **finestra**), mentre ogni pulsante di menu Visualizza un menu. Un menu contiene una raccolta di voci di menu (ad esempio **Nuovo**, **Apri** e **Chiudi**), che può essere espansa per visualizzare altre voci di menu che, se selezionate, consentono di eseguire un'azione specifica.

Nelle sezioni seguenti vengono definiti la struttura ad albero, le proprietà, i pattern di controllo e gli eventi di automazione interfaccia utente necessari per il tipo di controllo **menu** . I requisiti di automazione interfaccia utente si applicano a tutti i controlli menu in cui la piattaforma/Framework dell'interfaccia utente integra il supporto di automazione interfaccia utente per i tipi di controllo e i pattern

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Pattern di controllo obbligatori](#required-control-patterns)
-   [Eventi obbligatori](#required-events)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

Nella tabella seguente viene illustrata una tipica visualizzazione del controllo e del contenuto dell'albero di automazione interfaccia utente relativo ai controlli menu e viene descritto il possibile contenuto di ogni visualizzazione. Per altre informazioni sull'albero di automazione interfaccia utente, vedere [Cenni preliminari sull'albero di automazione interfaccia utente](uiauto-treeoverview.md).



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
<li>Menu
<ul>
<li>MenuItem (1 o molti)</li>
</ul>
<ul>
<li>Altri controlli (0 o molti)</li>
</ul></li>
</ul></td>
<td><ul>
<li>Menu
<ul>
<li>MenuItem (1 o molti)</li>
</ul>
<ul>
<li>Altri controlli (0 o molti)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

I controlli menu vengono sempre visualizzati nella visualizzazione controlli e nella visualizzazione contenuto dell'albero di automazione interfaccia utente. I controlli menu devono essere visualizzati sotto il controllo a cui si riferiscono le relative informazioni. I client di automazione interfaccia utente possono restare in ascolto dei [**\_ MenuOpenedEventId**](uiauto-event-ids.md) dell'interfaccia utente per assicurarsi che ottengano costantemente informazioni trasmesse dai controlli menu. I controlli menu di scelta rapida rappresentano un caso speciale. Possono apparire come elementi figlio del desktop o di una finestra dell'applicazione di primo livello.

Un controllo menu può contenere altri controlli, ad esempio controlli di modifica e caselle combinate, all'interno della relativa struttura. Questi controlli aggiuntivi corrispondono agli "altri controlli" elencati nella tabella precedente nelle visualizzazioni controlli e contenuto.

## <a name="relevant-properties"></a>Proprietà rilevanti

La tabella seguente elenca le proprietà di automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per il tipo di controllo **menu** . Per altre informazioni sulle proprietà di automazione interfaccia utente, vedere [recupero di proprietà da elementi di automazione interfaccia utente](uiauto-propertiesforclients.md).



| Proprietà di automazione interfaccia utente                                                                                      | Valore      | Note                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_CONTROLTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md)           | **Menu**   |                                                                                                                                                                         |
| [**\_ISCONTENTELEMENTPROPERTYID UIA**](uiauto-automation-element-propids.md) | true       | Il controllo menu viene sempre incluso nella visualizzazione contenuto dell'albero di automazione interfaccia utente.                                                                                      |
| [**\_ISCONTROLELEMENTPROPERTYID UIA**](uiauto-automation-element-propids.md) | true       | Il controllo menu viene sempre incluso nella visualizzazione controlli dell'albero di automazione interfaccia utente.                                                                                      |
| [**\_LABELEDBYPROPERTYID UIA**](uiauto-automation-element-propids.md)               | NULL       | Non è prevista alcuna etichetta con un controllo menu standard.                                                                                                                    |
| [**\_NAMEPROPERTYID UIA**](uiauto-automation-element-propids.md)                         | Vedere le note. | Il controllo menu non richiede l'impostazione di una proprietà **Name** o potrebbe avere lo stesso nome del controllo associato, ad esempio una voce di menu che ha aperto il sottomenu. |



 

## <a name="required-control-patterns"></a>Pattern di controllo obbligatori

Non sono presenti pattern di controllo obbligatori per il tipo di controllo Menu.

## <a name="required-events"></a>Eventi obbligatori

I controlli menu devono generare l'evento [**\_ MenuOpenedEventId di UIA**](uiauto-event-ids.md) quando vengono visualizzati sullo schermo. L' **evento \_ MenuOpenedEventId di UIA** includerà il testo del controllo. L' [**evento \_ MenuClosedEventId di UIA**](uiauto-event-ids.md) deve essere generato quando un menu scompare dallo schermo.

La tabella seguente elenca gli eventi di automazione interfaccia utente che sono necessari per supportare i controlli menu. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



| Evento di automazione interfaccia utente                                                                                                                   | Note                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**\_AUTOMATIONFOCUSCHANGEDEVENTID UIA**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà BoundingRectanglePropertyId. |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsEnabledPropertyId.                 | Se il controllo supporta la proprietà [**IsEnabled**](uiauto-automation-element-propids.md) , deve supportare questo evento.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsOffscreenPropertyId.             | Se il controllo supporta la proprietà [**IsOffscreen**](uiauto-automation-element-propids.md) , deve supportare questo evento. |
| [**\_MENUCLOSEDEVENTID UIA**](uiauto-event-ids.md)                                                              |                                                                                                                            |
| [**\_MENUOPENEDEVENTID UIA**](uiauto-event-ids.md)                                                              |                                                                                                                            |
| [**\_STRUCTURECHANGEDEVENTID UIA**](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente](uiauto-controltypesoverview.md)
</dt> <dt>

[Cenni preliminari su automazione interfaccia utente](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




