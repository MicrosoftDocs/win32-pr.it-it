---
title: Tipo di controllo Spinner
description: In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo Spinner.
ms.assetid: 28673ad5-645d-4314-96c4-81a951226256
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo Spinner
- Automazione interfaccia utente, tipo di controllo Spinner
- Automazione interfaccia utente, struttura ad albero per il tipo di controllo Spinner
- Automazione interfaccia utente, proprietà per il tipo di controllo Spinner
- Automazione interfaccia utente, pattern di controllo per il tipo di controllo Spinner
- Automazione interfaccia utente, eventi per il tipo di controllo Spinner
- strutture ad albero, tipo di controllo Spinner
- Proprietà, tipo di controllo Spinner
- pattern di controllo, tipo di controllo Spinner
- eventi, tipo di controllo Spinner
- supporto per il tipo di controllo Spinner
- Spinner (tipo di controllo)
- tipi di controllo, struttura ad albero per il tipo di controllo Spinner
- tipi di controllo, pattern di controllo per il tipo di controllo Spinner
- tipi di controllo, supporto per Spinner
- tipi di controllo, casella di selezione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9681160bf82c9a541412bb6dde8958c603fcfe22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712700"
---
# <a name="spinner-control-type"></a>Tipo di controllo Spinner

In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo **Spinner** .

I controlli casella di selezione vengono usati per effettuare selezioni da un dominio di elementi o un intervallo di numeri.

Nelle sezioni seguenti vengono definiti la struttura ad albero, le proprietà, i pattern di controllo e gli eventi di automazione interfaccia utente necessari per il tipo di controllo **Spinner** . I requisiti di automazione interfaccia utente si applicano a tutti i controlli casella di selezione in cui la piattaforma/Framework dell'interfaccia utente integra il supporto di automazione interfaccia utente per i tipi di controllo e

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Pattern di controllo obbligatori](#required-control-patterns)
-   [Eventi obbligatori](#required-events)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

La tabella seguente illustra una tipica visualizzazione del controllo e del contenuto dell'albero di automazione interfaccia utente che riguarda i controlli casella di selezione quando supportano i pattern di controllo **RangeValue** e **Selection** e descrive il possibile contenuto di ogni visualizzazione. Per altre informazioni sull'albero di automazione interfaccia utente, vedere [Cenni preliminari sull'albero di automazione interfaccia utente](uiauto-treeoverview.md).

**Pattern di controllo RangeValue**



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
<li>Spinner
<ul>
<li>Edit (0 o 1)</li>
<li>Button (2)</li>
</ul></li>
</ul></td>
<td><ul>
<li>Spinner</li>
</ul></td>
</tr>
</tbody>
</table>



 

**Selection (pattern di controllo)**



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
<li>Spinner
<ul>
<li>Edit (0 o 1)</li>
<li>Button (2)</li>
<li>Elemento elenco (0 o più)</li>
</ul></li>
</ul></td>
<td><ul>
<li>Spinner
<ul>
<li>ListItem (0 o più)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

Per assicurarsi che i due pulsanti nel sottoalbero della visualizzazione controlli possano essere distinti dagli strumenti di test automatici, assegnare il valore **ScrollAmount \_ SmallIncrement** o [**ScrollAmount \_ SmallDecrement**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-scrollamount) alla proprietà **AutomationId** nel modo appropriato. Per alcune implementazioni il controllo di modifica associato può essere un peer del controllo casella di selezione.

## <a name="relevant-properties"></a>Proprietà rilevanti

La tabella seguente elenca le proprietà di automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per i controlli casella di selezione. Per altre informazioni sulle proprietà di automazione interfaccia utente, vedere [recupero di proprietà da elementi di automazione interfaccia utente](uiauto-propertiesforclients.md).



| Proprietà di automazione interfaccia utente                                                                                              | Valore       | Note                                                                                                                                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_AUTOMATIONIDPROPERTYID UIA**](uiauto-automation-element-propids.md)                 | Vedere le note.  | Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata della struttura ad albero di automazione interfaccia utente.                                                                                                                                                                                                               |
| [**\_BOUNDINGRECTANGLEPROPERTYID UIA**](uiauto-automation-element-propids.md)       | Vedere le note.  | Il rettangolo più esterno che contiene l'intero controllo.                                                                                                                                                                                                                                                                   |
| [**\_CLICKABLEPOINTPROPERTYID UIA**](uiauto-automation-element-propids.md)             | Vedere le note.  | Il punto selezionabile del controllo casella di selezione fornisce lo stato attivo alla parte modificabile del controllo.                                                                                                                                                                                                                                      |
| [**\_CONTROLTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md)                   | **Spinner** | Questo valore è uguale per tutti i framework.                                                                                                                                                                                                                                                                                 |
| [**\_ISCONTENTELEMENTPROPERTYID UIA**](uiauto-automation-element-propids.md)         | true        | Il controllo casella di selezione deve essere sempre di tipo contenuto.                                                                                                                                                                                                                                                                                |
| [**\_ISCONTROLELEMENTPROPERTYID UIA**](uiauto-automation-element-propids.md)         | true        | Il controllo casella di selezione deve essere sempre un controllo.                                                                                                                                                                                                                                                                              |
| [**\_ISKEYBOARDFOCUSABLEPROPERTYID UIA**](uiauto-automation-element-propids.md)   | Vedere le note.  | Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà. Un controllo casella di selezione assume raramente lo stato attivo, ma, in questo caso, lo stato attivo deve rimanere sul controllo casella di selezione, non sui pulsanti figlio. L'utente deve essere in grado di eseguire tutte le azioni di scorrimento usando i tasti freccia su e freccia giù. |
| [**\_LABELEDBYPROPERTYID UIA**](uiauto-automation-element-propids.md)                       | Vedere le note.  | I controlli casella di selezione hanno un'etichetta di testo statico.                                                                                                                                                                                                                                                                                 |
| [**\_LOCALIZEDCONTROLTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md) | Vedere le note.  | Stringa localizzata corrispondente al tipo di controllo **Spinner** . Il valore predefinito è "Spinner" per en-US o inglese (Stati Uniti).                                                                                                                                                                                       |
| [**\_NAMEPROPERTYID UIA**](uiauto-automation-element-propids.md)                                 | Vedere le note.  | Il controllo casella di selezione in genere ricava il proprio nome da un'etichetta di testo statico.                                                                                                                                                                                                                                                      |



 

## <a name="required-control-patterns"></a>Pattern di controllo obbligatori

La tabella seguente elenca i pattern di controllo di automazione interfaccia utente che devono essere supportati da tutti i controlli casella di selezione. Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Pattern di controllo/proprietà del pattern                                         | Supporto/valore | Note                                                                                                                                     |
|--------------------------------------------------------------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider)                | Dipende da       | I controlli casella di selezione che si estendono su un intervallo numerico possono supportare il pattern di controllo [RangeValue](uiauto-implementingrangevalue.md) .               |
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)                  | Dipende da       | I controlli casella di selezione che dispongono di un elenco di elementi da selezionare devono supportare il pattern di controllo [Selection](uiauto-implementingselection.md) . |
| [**CanSelectMultiple**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple) | FALSE         | I controlli casella di selezione sono sempre contenitori a selezione singola.                                                                                  |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)                          | Dipende da       | I controlli casella di selezione che si estendono su un set descrete di opzioni o numeri possono supportare il pattern di controllo [value](uiauto-implementingvalue.md) .    |



 

## <a name="required-events"></a>Eventi obbligatori

La tabella seguente elenca gli eventi di automazione interfaccia utente necessari per supportare i controlli casella di selezione. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



| Evento di automazione interfaccia utente                                                                                                                   | Note                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**\_AUTOMATIONFOCUSCHANGEDEVENTID UIA**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà BoundingRectanglePropertyId. |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsEnabledPropertyId.                 | Se il controllo supporta la proprietà [**IsEnabled**](uiauto-automation-element-propids.md) , deve supportare questo evento.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsOffscreenPropertyId.             | Se il controllo supporta la proprietà [**IsOffscreen**](uiauto-automation-element-propids.md) , deve supportare questo evento. |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà RangeValueValuePropertyId.        | Se il controllo supporta il pattern di controllo [RangeValue](uiauto-implementingrangevalue.md) , deve supportare questo evento.   |
| [**UIA \_ Evento \_**](uiauto-event-ids.md) di modifica della proprietà InvalidatedEventId di selezione.               | Se il controllo supporta il pattern di controllo [Selection](uiauto-implementingselection.md) , deve supportare questo evento.     |
| [**\_STRUCTURECHANGEDEVENTID UIA**](uiauto-event-ids.md)                                                  |                                                                                                                            |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ValueValuePropertyId.                  | Se il controllo supporta il pattern di controllo [value](uiauto-implementingvalue.md) , deve supportare questo evento.             |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente](uiauto-controltypesoverview.md)
</dt> <dt>

[Cenni preliminari su automazione interfaccia utente](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




