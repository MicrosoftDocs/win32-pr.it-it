---
title: Tipo di controllo barra dei menu
description: In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo barra dei menu.
ms.assetid: e93a92ce-7c98-4e8f-8a6a-a365ccb705d6
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo barra dei menu
- Automazione interfaccia utente, tipo di controllo barra dei menu
- Automazione interfaccia utente, struttura ad albero per il tipo di controllo barra dei menu
- Automazione interfaccia utente, proprietà per il tipo di controllo barra dei menu
- Automazione interfaccia utente, pattern di controllo per il tipo di controllo barra dei menu
- Automazione interfaccia utente, eventi per il tipo di controllo barra dei menu
- strutture ad albero, tipo di controllo barra dei menu
- Proprietà, tipo di controllo barra dei menu
- pattern di controllo, tipo di controllo barra dei menu
- eventi, tipo di controllo barra dei menu
- supporto per il tipo di controllo barra dei menu
- Tipo di controllo barra dei menu
- tipi di controllo, struttura ad albero per il tipo di controllo barra dei menu
- tipi di controllo, pattern di controllo per il tipo di controllo barra dei menu
- tipi di controllo, supporto per la barra dei menu
- tipi di controllo, barra dei menu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b94bb60c13b5999bc8020eb70b84f6c932a2fb94
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298151"
---
# <a name="menubar-control-type"></a>Tipo di controllo barra dei menu

In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo **barra dei menu** .

I controlli barra dei menu sono un esempio di controlli che implementano il tipo di controllo **barra** dei menu. Le barre dei menu consentono agli utenti di attivare comandi e opzioni contenuti in un'applicazione.

Nelle sezioni seguenti vengono definiti la struttura ad albero, le proprietà, i pattern di controllo e gli eventi di automazione interfaccia utente necessari per il tipo di controllo **barra dei menu** . I requisiti di automazione interfaccia utente si applicano a tutti i controlli barra dei menu in cui il Framework dell'interfaccia utente/piattaforma integra il supporto di automazione interfaccia utente per i tipi di controllo e i pattern

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Pattern di controllo obbligatori](#required-control-patterns)
-   [Eventi obbligatori](#required-events)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

La tabella seguente illustra una tipica visualizzazione del controllo e del contenuto dell'albero di automazione interfaccia utente relativo ai controlli barra dei menu e descrive il possibile contenuto di ogni visualizzazione. Per altre informazioni sull'albero di automazione interfaccia utente, vedere [Cenni preliminari sull'albero di automazione interfaccia utente](uiauto-treeoverview.md).



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
<li>MenuBar
<ul>
<li>MenuItem (1 o più)</li>
<li>Altri controlli (0 o molti)</li>
</ul></li>
</ul></td>
<td><ul>
<li>Non applicabile
<ul>
<li>MenuItem (1 o più)</li>
<li>Altri controlli (0 o molti)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

Un controllo barra dei menu viene sempre visualizzato nella visualizzazione controlli, ma non nella visualizzazione contenuto, perché in genere non fornisce informazioni significative all'utente finale (a meno che l'applicazione non contenga più di una barra dei menu).

I client di automazione interfaccia utente possono restare in ascolto dell'evento [**\_ MenuModeStartEventId di UIA**](uiauto-event-ids.md) per assicurarsi che vengano informati costantemente quando l'interfaccia utente entra in modalità menu. Quando l'applicazione è in modalità menu, è possibile acquisire tutti gli input da tastiera per la navigazione dei menu. ad esempio, la digitazione di ' potrebbe richiamare il menu **Salva** anziché digitare il carattere nell'area client dell'applicazione. L' **evento \_ MenuModeStartEventId di UIA** deve precedere il primo evento [**\_ MenuOpenedEventId di UIA**](uiauto-event-ids.md) per garantire la coerenza logica. L' [**evento \_ MenuModeEndEventId di UIA**](uiauto-event-ids.md) segue l'ultimo evento [**\_ MenuClosedEventId di UIA**](uiauto-event-ids.md) . Se si fa clic su una voce di menu, è possibile attivare immediatamente l'evento **\_ MenuModeStartEventId di UIA** , seguito da un evento **\_ MenuOpenedEventId di UIA** .

Un controllo barra dei menu può contenere altri controlli, ad esempio controlli di modifica e caselle combinate, all'interno della relativa struttura. Questi controlli aggiuntivi corrispondono agli "altri controlli" elencati sopra nelle visualizzazioni controlli e contenuto.

## <a name="relevant-properties"></a>Proprietà rilevanti

La tabella seguente elenca le proprietà di automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per il tipo di controllo **barra dei menu** . Per altre informazioni sulle proprietà di automazione interfaccia utente, vedere [recupero di proprietà da elementi di automazione interfaccia utente](uiauto-propertiesforclients.md).



| Proprietà di automazione interfaccia utente                                                                                              | Valore       | Note                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ACCELERATORKEYPROPERTYID UIA**](uiauto-automation-element-propids.md)             | NULL        | Le barre dei menu in genere non dispongono di tasti di scelta rapida.                                                                                                                                                                                          |
| [**\_ACCESSKEYPROPERTYID UIA**](uiauto-automation-element-propids.md)                       | "ALT"       | La pressione del tasto ALT dovrebbe in genere spostare lo stato attivo sulla barra dei menu all'interno dell'applicazione.                                                                                                                                                  |
| [**\_BOUNDINGRECTANGLEPROPERTYID UIA**](uiauto-automation-element-propids.md)       | Vedere le note.  | Il valore esposto da questa proprietà deve includere tutti i controlli contenuti.                                                                                                                                                 |
| [**\_CONTROLTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md)                   | **MenuBar** |                                                                                                                                                                                                                                          |
| [**\_ISCONTENTELEMENTPROPERTYID UIA**](uiauto-automation-element-propids.md)         | FALSE       | Il controllo barra dei menu non è incluso nella visualizzazione contenuto dell'albero di automazione interfaccia utente.                                                                                                                                                      |
| [**\_ISCONTROLELEMENTPROPERTYID UIA**](uiauto-automation-element-propids.md)         | true        | Il controllo barra dei menu viene sempre incluso nella visualizzazione controlli dell'albero di automazione interfaccia utente.                                                                                                                                                   |
| [**\_ISKEYBOARDFOCUSABLEPROPERTYID UIA**](uiauto-automation-element-propids.md)   | true        | I controlli barra dei menu hanno lo stato attivabile perché i controlli che contengono possono prendere lo stato attivo.                                                                                                                                      |
| [**\_ISOFFSCREENPROPERTYID UIA**](uiauto-automation-element-propids.md)                   | Vedere le note.  | Il valore di questa proprietà dipende dal fatto che il controllo sia visualizzabile o meno sullo schermo.                                                                                                                                                     |
| [**\_LABELEDBYPROPERTYID UIA**](uiauto-automation-element-propids.md)                       | NULL        | I controlli barra dei menu in genere non hanno un'etichetta.                                                                                                                                                                                           |
| [**\_LOCALIZEDCONTROLTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md) | Vedere le note.  | Stringa localizzata corrispondente al tipo di controllo **barra dei menu** . Il valore predefinito è "barra dei menu" per en-US o inglese (Stati Uniti).                                                                                                    |
| [**\_NAMEPROPERTYID UIA**](uiauto-automation-element-propids.md)                                 | Vedere le note.  | Il controllo barra dei menu non necessita di un nome a meno che un'applicazione non abbia più di una barra dei menu. Se in un'applicazione è presente più di una barra dei menu, utilizzare questa proprietà per esporre i nomi distinti, ad esempio "formattazione" o "struttura". |
| [**\_ORIENTATIONPROPERTYID UIA**](uiauto-automation-element-propids.md)                   | Dipende da     | Questa proprietà espone l'orientamento orizzontale o verticale del controllo barra dei menu.                                                                                                                                                            |



 

## <a name="required-control-patterns"></a>Pattern di controllo obbligatori

La tabella seguente elenca i pattern di controllo di automazione interfaccia utente che devono essere supportati dai controlli barra dei menu. Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Pattern di controllo                                                   | Supporto | Note                                                                                                                                       |
|-------------------------------------------------------------------|---------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Dipende da | Se il controllo può essere espanso o compresso, deve implementare il pattern di controllo [ExpandCollapse](uiauto-implementingexpandcollapse.md) . |
| [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider)                     | Dipende da | Se il controllo può essere ancorato a parti diverse dello schermo, deve implementare il pattern di controllo [Dock](uiauto-implementingdock.md) .   |
| [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider)           | Dipende da | Se il controllo può essere ridimensionato, ruotato o spostato, deve implementare il pattern di controllo [Transform](uiauto-implementingtransform.md) .      |



 

## <a name="required-events"></a>Eventi obbligatori

La tabella seguente elenca gli eventi di automazione interfaccia utente che sono necessari per supportare i controlli barra dei menu. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



| Evento di automazione interfaccia utente                                                                                                                                                | Note                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**\_AUTOMATIONFOCUSCHANGEDEVENTID UIA**](uiauto-event-ids.md)                                                                   |                                                                                                                                  |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà BoundingRectanglePropertyId.                              |                                                                                                                                  |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ExpandCollapseExpandCollapseStatePropertyId. | Se il controllo supporta il pattern di controllo [ExpandCollapse](uiauto-implementingexpandcollapse.md) , deve supportare questo evento. |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsEnabledPropertyId.                                              | Se il controllo supporta la proprietà [**IsEnabled**](uiauto-automation-element-propids.md) , deve supportare questo evento.         |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsOffscreenPropertyId.                                          | Se il controllo supporta la proprietà [**IsOffscreen**](uiauto-automation-element-propids.md) , deve supportare questo evento.       |
| [**\_STRUCTURECHANGEDEVENTID UIA**](uiauto-event-ids.md)                                                                               |                                                                                                                                  |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente](uiauto-controltypesoverview.md)
</dt> <dt>

[Cenni preliminari su automazione interfaccia utente](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




