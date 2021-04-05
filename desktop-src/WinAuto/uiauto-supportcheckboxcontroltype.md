---
title: Tipo di controllo CheckBox
description: In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo CheckBox.
ms.assetid: 5a9061bc-2eac-4839-8f2c-32b9d58fe712
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo CheckBox
- Automazione interfaccia utente, tipo di controllo CheckBox
- Automazione interfaccia utente, struttura ad albero per il tipo di controllo CheckBox
- Automazione interfaccia utente, proprietà per il tipo di controllo CheckBox
- Automazione interfaccia utente, pattern di controllo per il tipo di controllo CheckBox
- Automazione interfaccia utente, eventi per il tipo di controllo CheckBox
- strutture ad albero, tipo di controllo CheckBox
- Proprietà, tipo di controllo CheckBox
- pattern di controllo, tipo di controllo CheckBox
- eventi, tipo di controllo CheckBox
- supporto per il tipo di controllo CheckBox
- CheckBox (tipo di controllo)
- tipi di controllo, struttura ad albero per il tipo di controllo CheckBox
- tipi di controllo, pattern di controllo per il tipo di controllo CheckBox
- tipi di controllo, supporto per CheckBox
- tipi di controllo, casella di controllo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8e5bac106c8ba3bbf58c7f5b06c087ceb7b3418
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856085"
---
# <a name="checkbox-control-type"></a>Tipo di controllo CheckBox

In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo **CheckBox** .

Una casella di controllo è un oggetto usato per indicare uno stato con cui gli utenti possono interagire per scorrere tale stato. Le caselle di controllo presentano all'utente un'opzione binaria (Yes/No), (On/Off) o terziaria (On, Off, Indeterminate).

Nelle sezioni seguenti vengono definiti la struttura ad albero, le proprietà, i pattern di controllo e gli eventi di automazione interfaccia utente necessari per il tipo di controllo **CheckBox** . I requisiti di automazione interfaccia utente si applicano a tutti i controlli casella di controllo in cui la piattaforma/Framework dell'interfaccia utente integra il supporto di automazione interfaccia utente per tipi di controllo e pattern di controllo

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Pattern di controllo obbligatori](#required-control-patterns)
-   [Eventi obbligatori](#required-events)
-   [DefaultAction](#defaultaction)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

Nella tabella seguente viene illustrata una tipica visualizzazione del controllo e del contenuto dell'albero di automazione interfaccia utente relativo ai controlli casella di controllo e viene descritto il possibile contenuto di ogni visualizzazione. Per altre informazioni sull'albero di automazione interfaccia utente, vedere [Cenni preliminari sull'albero di automazione interfaccia utente](uiauto-treeoverview.md).



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
<li>CheckBox</li>
</ul></td>
<td><ul>
<li>CheckBox</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a>Proprietà rilevanti

La tabella seguente elenca le proprietà di automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per il tipo di controllo **CheckBox** . Per altre informazioni sulle proprietà di automazione interfaccia utente, vedere [recupero di proprietà da elementi di automazione interfaccia utente](uiauto-propertiesforclients.md).



| Proprietà di automazione interfaccia utente                                                                                              | Valore        | Note                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_AUTOMATIONIDPROPERTYID UIA**](uiauto-automation-element-propids.md)                 | Vedere le note.   | Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata della struttura ad albero di automazione interfaccia utente.                                                                                                                                                                       |
| [**\_BOUNDINGRECTANGLEPROPERTYID UIA**](uiauto-automation-element-propids.md)       | Vedere le note.   | Il rettangolo più esterno che contiene l'intero controllo.                                                                                                                                                                                                                           |
| [**\_CLICKABLEPOINTPROPERTYID UIA**](uiauto-automation-element-propids.md)             | Vedere le note.   | Supportata se è presente un rettangolo di delimitazione. Se non tutti i punti all'interno del rettangolo di delimitazione sono selezionabili e l'elemento esegue un hit testing specializzato, eseguire l'override e fornire un punto selezionabile.                                                                               |
| [**\_CONTROLTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md)                   | **CheckBox** |                                                                                                                                                                                                                                                                                    |
| [**\_ISCONTENTELEMENTPROPERTYID UIA**](uiauto-automation-element-propids.md)         | true         | Il valore di questa proprietà deve essere sempre **true**. Questo significa che il controllo casella di controllo deve essere sempre incluso nella visualizzazione contenuto dell'albero di automazione interfaccia utente.                                                                                                                   |
| [**\_ISCONTROLELEMENTPROPERTYID UIA**](uiauto-automation-element-propids.md)         | true         | Il valore di questa proprietà deve essere sempre **true**. Questo significa che il controllo casella di controllo deve essere sempre incluso nella visualizzazione controlli dell'albero di automazione interfaccia utente.                                                                                                                   |
| [**\_ISKEYBOARDFOCUSABLEPROPERTYID UIA**](uiauto-automation-element-propids.md)   | Vedere le note.   | Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.                                                                                                                                                                                                          |
| [**\_LABELEDBYPROPERTYID UIA**](uiauto-automation-element-propids.md)                       | Null         | I controlli casella di controllo sono con etichetta automatica.                                                                                                                                                                                                                                              |
| [**\_LOCALIZEDCONTROLTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md) | Vedere le note.   | Stringa localizzata corrispondente al tipo di controllo **CheckBox** . Il valore predefinito è "casella di controllo" per en-US o inglese (Stati Uniti).                                                                                                                                            |
| [**\_NAMEPROPERTYID UIA**](uiauto-automation-element-propids.md)                                 | Vedere le note.   | Il valore della proprietà [**IUIAutomationElement:: currentname**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) (o [**CacheName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedname)) del controllo casella di controllo è il testo visualizzato accanto alla casella che mantiene lo stato dell'interruttore. |



 

## <a name="required-control-patterns"></a>Pattern di controllo obbligatori

La tabella seguente elenca i pattern di controllo di automazione interfaccia utente che devono essere supportati da tutti i controlli casella di controllo. Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Pattern di controllo/proprietà del pattern                  | Supporto/valore | Note                                                                                                                                                             |
|---------------------------------------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) | Necessario      | Le caselle di controllo supportano il pattern di controllo di [attivazione/disattivazione](uiauto-implementingtoggle.md) per consentire la visualizzazione della casella di controllo a livello di programmazione tramite gli Stati interni. |



 

## <a name="required-events"></a>Eventi obbligatori

La tabella seguente elenca gli eventi di automazione interfaccia utente che sono necessari per supportare i controlli casella di controllo. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



| Evento di automazione interfaccia utente                                                                                                                   | Note                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**\_AUTOMATIONFOCUSCHANGEDEVENTID UIA**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà BoundingRectanglePropertyId. |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsOffscreenPropertyId.             | Se il controllo supporta la proprietà [**IsOffscreen**](uiauto-automation-element-propids.md) , deve supportare questo evento. |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsEnabledPropertyId.                 | Se il controllo supporta la proprietà [**IsEnabled**](uiauto-automation-element-propids.md) , deve supportare questo evento.   |
| [**\_STRUCTURECHANGEDEVENTID UIA**](uiauto-event-ids.md)                                                  |                                                                                                                            |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ToggleToggleStatePropertyId.    |                                                                                                                            |



 

## <a name="defaultaction"></a>DefaultAction

L'azione predefinita della casella di controllo è fare sì che un pulsante di opzione assuma lo stato attivo e attivarne/disattivarne lo stato corrente. Come indicato in precedenza, le caselle di controllo presentano una decisione binaria (Yes/No o on/off) per l'utente o terziaria (on, off, Indeterminate). Se la casella di controllo è binaria, l'azione predefinita fa sì che lo stato "on" diventi "off" o che lo stato "off" diventi "on". In una casella di controllo terziario l'azione predefinita scorre gli Stati della casella di controllo nello stesso ordine in cui l'utente ha inviato i clic del mouse successivi al controllo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente](uiauto-controltypesoverview.md)
</dt> <dt>

[Cenni preliminari su automazione interfaccia utente](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




