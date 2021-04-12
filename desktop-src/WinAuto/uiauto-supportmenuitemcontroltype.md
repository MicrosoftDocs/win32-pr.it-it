---
title: Tipo di controllo MenuItem
description: In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo MenuItem.
ms.assetid: a6a04489-8e28-44ff-a3b0-ecf19c24daab
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo MenuItem
- Automazione interfaccia utente, tipo di controllo MenuItem
- Automazione interfaccia utente, struttura ad albero per il tipo di controllo MenuItem
- Automazione interfaccia utente, proprietà per il tipo di controllo MenuItem
- Automazione interfaccia utente, pattern di controllo per il tipo di controllo MenuItem
- Automazione interfaccia utente, eventi per il tipo di controllo MenuItem
- strutture ad albero, tipo di controllo MenuItem
- Proprietà, tipo di controllo MenuItem
- pattern di controllo, tipo di controllo MenuItem
- eventi, tipo di controllo MenuItem
- supporto per il tipo di controllo MenuItem
- Tipo di controllo MenuItem
- tipi di controllo, struttura ad albero per il tipo di controllo MenuItem
- tipi di controllo, pattern di controllo per il tipo di controllo MenuItem
- tipi di controllo, supporto per MenuItem
- tipi di controllo, MenuItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24033866f749974a41d39094b416e70f3c40f796
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329823"
---
# <a name="menuitem-control-type"></a>Tipo di controllo MenuItem

In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo **MenuItem** .

Un controllo menu consente l'organizzazione gerarchica degli elementi associati a comandi e gestori eventi. In una tipica applicazione Windows, una barra dei menu contiene diverse voci di menu (ad esempio **file**, **modifica** e **finestra**), mentre ogni voce di menu Visualizza un menu. Un menu contiene una raccolta di voci di menu (ad esempio **Nuovo**, **Apri** e **Chiudi**), che può essere espansa per visualizzare altre voci di menu che, se selezionate, consentono di eseguire un'azione specifica.

Nelle sezioni seguenti vengono definiti la struttura ad albero, le proprietà, i pattern di controllo e gli eventi di automazione interfaccia utente necessari per il tipo di controllo **MenuItem** . I requisiti di automazione interfaccia utente si applicano a tutti i controlli voce di menu in cui il Framework dell'interfaccia utente/piattaforma integra il supporto di automazione interfaccia utente per i tipi di controllo e i pattern

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Pattern di controllo obbligatori](#required-control-patterns)
-   [Eventi obbligatori](#required-events)
-   [Problemi preesistenti](#legacy-issues)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

Nella tabella seguente viene illustrata una tipica visualizzazione del controllo e del contenuto dell'albero di automazione interfaccia utente relativo ai controlli voce di menu e viene descritto il possibile contenuto di ogni visualizzazione. Per altre informazioni sull'albero di automazione interfaccia utente, vedere [Cenni preliminari sull'albero di automazione interfaccia utente](uiauto-treeoverview.md).



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
<li>Guida di MenuItem &quot;&quot;
<ul>
<li>Menu (sottomenu della voce di menu della guida)
<ul>
<li>Argomenti della Guida di MenuItem &quot;&quot;</li>
<li>MenuItem &quot; informazioni sul blocco note&quot;</li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li>Guida di MenuItem &quot;&quot;
<ul>
<li>Argomenti della Guida di MenuItem &quot;&quot;</li>
<li>MenuItem &quot; informazioni sul blocco note&quot;</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

La visualizzazione controlli del controllo voce di menu presenta la struttura ad albero di automazione interfaccia utente illustrata in precedenza. Si noti che la voce di menu per la **Guida** sulla barra dei menu è stata aggiunta per illustrare meglio la struttura.

Per la visualizzazione contenuto, il **menu** è assente dall'albero di automazione interfaccia utente perché non fornisce informazioni significative all'utente finale.

## <a name="relevant-properties"></a>Proprietà rilevanti

La tabella seguente elenca le proprietà di automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per il tipo di controllo **MenuItem** . Per altre informazioni sulle proprietà di automazione interfaccia utente, vedere [recupero di proprietà da elementi di automazione interfaccia utente](uiauto-propertiesforclients.md).



| Proprietà di automazione interfaccia utente                                                                                              | Valore        | Note                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_AUTOMATIONIDPROPERTYID UIA**](uiauto-automation-element-propids.md)                 | Vedere le note.   | Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata della struttura ad albero di automazione interfaccia utente. Allocare la proprietà **AutomationId** per una voce di menu se l'elemento è noto come coerente tra istanze diverse dell'interfaccia utente. Se la voce di menu viene popolata in modo dinamico e non stimabile, lasciare vuota la proprietà **AutomationId** . |
| [**\_BOUNDINGRECTANGLEPROPERTYID UIA**](uiauto-automation-element-propids.md)       | Vedere le note.   | Il rettangolo più esterno che contiene l'intero controllo.                                                                                                                                                                                                                                                                                                                 |
| [**\_CLICKABLEPOINTPROPERTYID UIA**](uiauto-automation-element-propids.md)             | Vedere le note.   | Supportata se è presente un rettangolo di delimitazione. Se non tutti i punti all'interno del rettangolo di delimitazione sono selezionabili e l'elemento esegue un hit testing specializzato, eseguire l'override e fornire un punto selezionabile.                                                                                                                                                                     |
| [**\_CONTROLTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md)                   | **MenuItem** |                                                                                                                                                                                                                                                                                                                                                                          |
| [**\_ISCONTENTELEMENTPROPERTYID UIA**](uiauto-automation-element-propids.md)         | true         | Il controllo voce di menu viene sempre incluso nella visualizzazione contenuto dell'albero di automazione interfaccia utente.                                                                                                                                                                                                                                                                                  |
| [**\_ISCONTROLELEMENTPROPERTYID UIA**](uiauto-automation-element-propids.md)         | true         | Il controllo voce di menu viene sempre incluso nella visualizzazione controlli dell'albero di automazione interfaccia utente.                                                                                                                                                                                                                                                                                  |
| [**\_ISKEYBOARDFOCUSABLEPROPERTYID UIA**](uiauto-automation-element-propids.md)   | Vedere le note.   | Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.                                                                                                                                                                                                                                                                                                |
| [**\_LOCALIZEDCONTROLTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md) | Vedere le note.   | Stringa localizzata corrispondente al tipo di controllo **MenuItem** . Il valore predefinito è "voce di menu" per en-US o inglese (Stati Uniti).                                                                                                                                                                                                                                  |
| [**\_NAMEPROPERTYID UIA**](uiauto-automation-element-propids.md)                                 | Vedere le note.   | Il nome del controllo voce di menu è il testo utilizzato per etichettarlo.                                                                                                                                                                                                                                                                                                          |



 

## <a name="required-control-patterns"></a>Pattern di controllo obbligatori

La tabella seguente elenca i pattern di controllo di automazione interfaccia utente che devono essere supportati dai controlli voce di menu. Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Pattern di controllo                                                   | Supporto | Note                                                                                                                                                |
|-------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Dipende da | Se il controllo può essere espanso o compresso, implementare [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider).                            |
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)                 | Dipende da | Se il controllo esegue una singola azione o comando, implementare [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider).                                     |
| [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)   | Dipende da | Se il controllo viene usato per effettuare una selezione da un elenco di opzioni tra le voci di menu, implementare [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider). |
| [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)                 | Dipende da | Se il controllo rappresenta un'opzione che può essere attivata o disattivata, implementare [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider).                       |



 

## <a name="required-events"></a>Eventi obbligatori

La tabella seguente elenca gli eventi di automazione interfaccia utente che sono necessari per supportare i controlli voce di menu. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



| Evento di automazione interfaccia utente                                                                                                                                                | Note                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**\_AUTOMATIONFOCUSCHANGEDEVENTID UIA**](uiauto-event-ids.md)                                                                   |                                                                                                                                  |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà BoundingRectanglePropertyId.                              |                                                                                                                                  |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ExpandCollapseExpandCollapseStatePropertyId. | Se il controllo supporta il pattern di controllo [ExpandCollapse](uiauto-implementingexpandcollapse.md) , deve supportare questo evento. |
| [**\_Richiama \_ InvokedEventId**](uiauto-event-ids.md)                                                                                  | Se il controllo supporta il pattern di controllo [Invoke](uiauto-implementinginvoke.md) , deve supportare questo evento.                 |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsEnabledPropertyId.                                              | Se il controllo supporta la proprietà [**IsEnabled**](uiauto-automation-element-propids.md) , deve supportare questo evento.         |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsOffscreenPropertyId.                                          | Se il controllo supporta la proprietà [**IsOffscreen**](uiauto-automation-element-propids.md) , deve supportare questo evento.       |
| [**\_ElementAddedToSelectionEventId SelectionItem di UIA \_**](uiauto-event-ids.md)                                    | Se il controllo supporta il pattern di controllo [SelectionItem](uiauto-implementingselectionitem.md) , deve supportare questo evento.   |
| [**\_ElementRemovedFromSelectionEventId SelectionItem di UIA \_**](uiauto-event-ids.md)                            | Se il controllo supporta il pattern di controllo [SelectionItem](uiauto-implementingselectionitem.md) , deve supportare questo evento.   |
| [**\_ElementSelectedEventId SelectionItem di UIA \_**](uiauto-event-ids.md)                                                    | Se il controllo supporta il pattern di controllo [SelectionItem](uiauto-implementingselectionitem.md) , deve supportare questo evento.   |
| [**\_STRUCTURECHANGEDEVENTID UIA**](uiauto-event-ids.md)                                                                               |                                                                                                                                  |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ToggleToggleStatePropertyId.                                 | Se il controllo supporta il pattern di controllo [interruttore](uiauto-implementingtoggle.md) , deve supportare questo evento.                 |



 

## <a name="legacy-issues"></a>Problemi preesistenti

Per le voci di menu di Microsoft Win32, il pattern di controllo di [attivazione/disattivazione](uiauto-implementingtoggle.md) è supportato solo quando viene selezionata una voce di menu ed è possibile determinare a livello di codice se è necessario il supporto del pattern di controllo di attivazione/disattivazione. Poiché una voce di menu Win32 non espone se può essere selezionata, il pattern di controllo Invoke è supportato quando la voce di menu non è selezionata. Il pattern di controllo Invoke è sempre supportato, anche per le voci di menu che sono necessarie solo per supportare il pattern di controllo di attivazione/disattivazione. In questo modo i client non vengono confusi quando una voce di menu che supporta il pattern di controllo [Invoke](uiauto-implementinginvoke.md) (quando la voce di menu è deselezionata) non supporta più tale modello quando viene selezionato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente](uiauto-controltypesoverview.md)
</dt> <dt>

[Cenni preliminari su automazione interfaccia utente](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




