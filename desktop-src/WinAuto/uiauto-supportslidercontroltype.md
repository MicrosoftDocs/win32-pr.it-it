---
title: Tipo di controllo Slider
description: In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo Slider.
ms.assetid: dc7bef7a-b68c-4184-a9e7-745bb41b592e
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo Slider
- Automazione interfaccia utente, tipo di controllo Slider
- Automazione interfaccia utente, struttura ad albero per il tipo di controllo Slider
- Automazione interfaccia utente, proprietà per il tipo di controllo Slider
- Automazione interfaccia utente, pattern di controllo per il tipo di controllo Slider
- Automazione interfaccia utente, eventi per il tipo di controllo Slider
- strutture ad albero, tipo di controllo Slider
- Proprietà, tipo di controllo Slider
- pattern di controllo, tipo di controllo Slider
- eventi, tipo di controllo Slider
- supporto per il tipo di controllo Slider
- Slider (tipo di controllo)
- tipi di controllo, struttura ad albero per il tipo di controllo Slider
- tipi di controllo, pattern di controllo per il tipo di controllo Slider
- tipi di controllo, supporto per il dispositivo di scorrimento
- tipi di controllo, dispositivo di scorrimento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5be8e82dfc8f011363086745368ed1693c45a6aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955599"
---
# <a name="slider-control-type"></a>Tipo di controllo Slider

In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo **Slider** .

Un controllo dispositivo di scorrimento è un controllo composito con pulsanti che consentono a un utente di impostare un intervallo numerico o effettuare una selezione da un set di elementi.

Nelle sezioni seguenti vengono definiti la struttura ad albero, le proprietà, i pattern di controllo e gli eventi di automazione interfaccia utente necessari per il tipo di controllo **Slider** . I requisiti di automazione interfaccia utente si applicano a tutti i controlli dispositivo di scorrimento in cui la piattaforma/Framework dell'interfaccia utente integra il supporto di automazione interfaccia utente per i tipi di controllo e

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Pattern di controllo obbligatori](#required-control-patterns)
-   [Eventi obbligatori](#required-events)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

Nella tabella seguente viene illustrata una tipica visualizzazione del controllo e del contenuto dell'albero di automazione interfaccia utente relativo ai controlli dispositivo di scorrimento e viene descritto il possibile contenuto di ogni visualizzazione. Per altre informazioni sull'albero di automazione interfaccia utente, vedere [Cenni preliminari sull'albero di automazione interfaccia utente](uiauto-treeoverview.md).



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
<li>Slider
<ul>
<li>Button (2 o 4)</li>
<li>Thumb (1)</li>
<li>Elemento elenco (0 o più)</li>
</ul></li>
</ul></td>
<td><ul>
<li>Slider
<ul>
<li>Elemento elenco (0 o più)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a>Proprietà rilevanti

La tabella seguente elenca le proprietà di automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per i controlli dispositivo di scorrimento. Per altre informazioni sulle proprietà di automazione interfaccia utente, vedere [recupero di proprietà da elementi di automazione interfaccia utente](uiauto-propertiesforclients.md).



| Proprietà di automazione interfaccia utente                                                                                              | Valore      | Note                                                                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_AUTOMATIONIDPROPERTYID UIA**](uiauto-automation-element-propids.md)                 | Vedere le note. | Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata della struttura ad albero di automazione interfaccia utente.                                                                                                                   |
| [**\_BOUNDINGRECTANGLEPROPERTYID UIA**](uiauto-automation-element-propids.md)       | Vedere le note. | Il rettangolo più esterno che contiene l'intero controllo.                                                                                                                                                                       |
| [**\_CLICKABLEPOINTPROPERTYID UIA**](uiauto-automation-element-propids.md)             | Vedere le note. | La maggior parte dei controlli dispositivo di scorrimento deve restituire l'errore [**UIA \_ E \_ NOCLICKABLEPOINT**](uiauto-error-codes.md) perché l'intero rettangolo di delimitazione del controllo dispositivo di scorrimento è occupato da controlli figlio. |
| [**\_CONTROLTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md)                   | **Dispositivo di scorrimento** | Questo valore è uguale per tutti i framework.                                                                                                                                                                                     |
| [**\_ISCONTENTELEMENTPROPERTYID UIA**](uiauto-automation-element-propids.md)         | true       | Il controllo dispositivo di scorrimento è sempre incluso nella visualizzazione contenuto dell'albero di automazione interfaccia utente.                                                                                                                                           |
| [**\_ISCONTROLELEMENTPROPERTYID UIA**](uiauto-automation-element-propids.md)         | true       | Il controllo Slider viene sempre incluso nella visualizzazione controlli dell'albero di automazione interfaccia utente.                                                                                                                                           |
| [**\_ISKEYBOARDFOCUSABLEPROPERTYID UIA**](uiauto-automation-element-propids.md)   | Vedere le note. | Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà. Gli elementi figlio (pulsanti e Thumb) di un controllo dispositivo di scorrimento non devono mai prendere lo stato attivo. Lo stato attivo deve rimanere sempre sul controllo dispositivo di scorrimento.       |
| [**\_LABELEDBYPROPERTYID UIA**](uiauto-automation-element-propids.md)                       | Vedere le note. | Se è presente un'etichetta di testo statico associata al controllo, questa proprietà deve esporre un riferimento a tale controllo. Se il controllo testo è un sottocomponente di un altro controllo, non avrà una proprietà **LabeledBy** impostata.   |
| [**\_LOCALIZEDCONTROLTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md) | Vedere le note. | Stringa localizzata corrispondente al tipo di controllo **Slider** . Il valore predefinito è "slider" per en-US o inglese (Stati Uniti).                                                                                             |
| [**\_NAMEPROPERTYID UIA**](uiauto-automation-element-propids.md)                                 | Vedere le note. | Il nome del controllo dispositivo di scorrimento viene in genere generato da un'etichetta di testo statico. Se non è presente un'etichetta di testo statico, lo sviluppatore dell'applicazione deve assegnare un valore di proprietà per il **nome** .                              |



 

## <a name="required-control-patterns"></a>Pattern di controllo obbligatori

La tabella seguente elenca i pattern di controllo di automazione interfaccia utente che devono essere supportati da tutti i controlli dispositivo di scorrimento. Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Pattern di controllo/proprietà del pattern                          | Supporto/valore | Note                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) | Dipende da       | Un dispositivo di scorrimento deve supportare il pattern di controllo [RangeValue](uiauto-implementingrangevalue.md) se il contenuto può essere impostato su un valore compreso in un intervallo numerico.                                                                                                                                                 |
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)   | Dipende da       | Un dispositivo di scorrimento deve supportare il pattern di controllo [Selection](uiauto-implementingselection.md) se il contenuto rappresenta un valore tra un set discreto di opzioni. Se il pattern di controllo Selection è supportato, la selezione corrispondente deve essere esposta come uno o più elementi di elenco figlio del dispositivo di scorrimento. |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)           | Dipende da       | Un dispositivo di scorrimento deve supportare il pattern di controllo [value](uiauto-implementingvalue.md) se il contenuto rappresenta un valore tra un set discreto di opzioni.                                                                                                                                                     |



 

## <a name="required-events"></a>Eventi obbligatori

La tabella seguente elenca gli eventi di automazione interfaccia utente che sono necessari per supportare i controlli dispositivo di scorrimento. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



| Evento di automazione interfaccia utente                                                                                                                   | Note                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**\_AUTOMATIONFOCUSCHANGEDEVENTID UIA**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà BoundingRectanglePropertyId. |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsEnabledPropertyId.                 | Se il controllo supporta la proprietà [**IsEnabled**](uiauto-automation-element-propids.md) , deve supportare questo evento.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsOffscreenPropertyId.             | Se il controllo supporta la proprietà [**IsOffscreen**](uiauto-automation-element-propids.md) , deve supportare questo evento. |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà RangeValueValuePropertyId.        | Se il controllo supporta il pattern di controllo [RangeValue](uiauto-implementingrangevalue.md) , deve supportare questo evento.   |
| [**\_InvalidatedEventId selezione \_ UIA**](uiauto-event-ids.md)                                       | Se il controllo supporta il pattern di controllo [Selection](uiauto-implementingselection.md) , deve supportare questo evento.     |
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

 

 




