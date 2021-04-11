---
title: Tipo di controllo Document
description: In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo Document.
ms.assetid: 62565f16-f0d6-42ff-bc36-897a2618c867
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo Document
- Automazione interfaccia utente, tipo di controllo Document
- Automazione interfaccia utente, struttura ad albero per il tipo di controllo Document
- Automazione interfaccia utente, proprietà per il tipo di controllo Document
- Automazione interfaccia utente, pattern di controllo per il tipo di controllo Document
- Automazione interfaccia utente, eventi per il tipo di controllo Document
- strutture ad albero, tipo di controllo Document
- Proprietà, tipo di controllo Document
- pattern di controllo, tipo di controllo Document
- eventi, tipo di controllo Document
- supporto per il tipo di controllo Document
- Document (tipo di controllo)
- tipi di controllo, struttura ad albero per il tipo di controllo Document
- tipi di controllo, pattern di controllo per il tipo di controllo Document
- tipi di controllo, supporto per documenti
- tipi di controllo, documento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46ca481df812e3321da7bb4bbb39bdcb5628fb98
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044608"
---
# <a name="document-control-type"></a>Tipo di controllo Document

In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo **Document** .

I controlli Document consentono a un utente di visualizzare e modificare più pagine di testo. A differenza dei controlli di modifica che supportano solo una semplice riga di testo non formattato, i controlli documento possono ospitare testo con stili e formattazione avanzati

Nelle sezioni seguenti vengono definiti la struttura ad albero, le proprietà, i pattern di controllo e gli eventi di automazione interfaccia utente necessari per il tipo di controllo **Document** . I requisiti di automazione interfaccia utente si applicano a tutti i controlli dei documenti in cui la piattaforma/Framework dell'interfaccia utente integra il supporto di automazione interfaccia utente per i tipi di controllo e pattern

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Pattern di controllo obbligatori](#required-control-patterns)
-   [Eventi obbligatori](#required-events)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

Nella tabella seguente viene illustrata una tipica visualizzazione del controllo e del contenuto dell'albero di automazione interfaccia utente relativo ai controlli documento e viene descritto il possibile contenuto di ogni visualizzazione. Per altre informazioni sull'albero di automazione interfaccia utente, vedere [Cenni preliminari sull'albero di automazione interfaccia utente](uiauto-treeoverview.md).



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
<li>Documento
<ul>
<li>Varia</li>
</ul></li>
</ul></td>
<td><ul>
<li>Documento
<ul>
<li>Varia</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a>Proprietà rilevanti

La tabella seguente elenca le proprietà di automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per i controlli documento. Per altre informazioni sulle proprietà di automazione interfaccia utente, vedere [recupero di proprietà da elementi di automazione interfaccia utente](uiauto-propertiesforclients.md).



| Proprietà di automazione interfaccia utente                                                                                              | Valore        | Note                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_AUTOMATIONIDPROPERTYID UIA**](uiauto-automation-element-propids.md)                 | Vedere le note.   | Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata della struttura ad albero di automazione interfaccia utente.                                      |
| [**\_BOUNDINGRECTANGLEPROPERTYID UIA**](uiauto-automation-element-propids.md)       | Vedere le note.   | Il rettangolo più esterno che contiene l'intero controllo.                                                                                          |
| [**\_CLICKABLEPOINTPROPERTYID UIA**](uiauto-automation-element-propids.md)             | Vedere le note.   | Il documento ha un punto selezionabile che farà passare lo stato attivo sul documento o su uno degli elementi nel documento contenitore.                   |
| [**\_CONTROLTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md)                   | **Documento** |                                                                                                                                                   |
| [**\_ISCONTENTELEMENTPROPERTYID UIA**](uiauto-automation-element-propids.md)         | true         | Il controllo documento viene sempre incluso nella visualizzazione contenuto dell'albero di automazione interfaccia utente.                                                            |
| [**\_ISCONTROLELEMENTPROPERTYID UIA**](uiauto-automation-element-propids.md)         | true         | Il controllo documento viene sempre incluso nella visualizzazione controlli dell'albero di automazione interfaccia utente.                                                            |
| [**\_ISKEYBOARDFOCUSABLEPROPERTYID UIA**](uiauto-automation-element-propids.md)   | Vedere le note.   | Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.                                                                         |
| [**\_LABELEDBYPROPERTYID UIA**](uiauto-automation-element-propids.md)                       | Vedere le note.   | Il valore di questa proprietà deve essere l'etichetta del controllo documento. In genere, viene usato il titolo del documento.                             |
| [**\_LOCALIZEDCONTROLTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md) | Vedere le note.   | Stringa localizzata corrispondente al tipo di controllo **Document** . Il valore predefinito è "Document" per en-US o inglese (Stati Uniti).            |
| [**\_NAMEPROPERTYID UIA**](uiauto-automation-element-propids.md)                                 | Vedere le note.   | Il controllo documento in genere ottiene il nome dal nome file da cui viene caricato. Viene spesso visualizzato nel titolo di una finestra o di un frame contenitore. |



 

## <a name="required-control-patterns"></a>Pattern di controllo obbligatori

La tabella seguente elenca i pattern di controllo di automazione interfaccia utente che devono essere supportati dai controlli documento. Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Pattern di controllo/proprietà del pattern                  | Supporto/valore | Note                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider) | Dipende da       | Il controllo documento può estendersi oltre il riquadro di visualizzazione. Il controllo deve supportare il pattern di controllo [Scroll](uiauto-implementingscroll.md) se il contenuto è scorrevole.                                                                                                                              |
| [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider)     | Necessario      | Tutti i controlli documento devono supportare il pattern di controllo [Text](uiauto-implementingtextandtextrange.md) .                                                                                                                                                                                                                |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)   | Dipende da       | Sebbene i client di automazione interfaccia utente possano usare [**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) per ottenere informazioni di testo su un documento, hanno bisogno del pattern di controllo [value](uiauto-implementingvalue.md) per impostare il valore interno. La voce di testo semplice è possibile solo tramite il pattern di controllo value. |



 

## <a name="required-events"></a>Eventi obbligatori

La tabella seguente elenca gli eventi di automazione interfaccia utente necessari per supportare i controlli documento. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



| Evento di automazione interfaccia utente                                                                                                                                        | Note                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**\_AUTOMATIONFOCUSCHANGEDEVENTID UIA**](uiauto-event-ids.md)                                                           |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà BoundingRectanglePropertyId.                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsEnabledPropertyId.                                      | Se il controllo supporta la proprietà [**IsEnabled**](uiauto-automation-element-propids.md) , deve supportare questo evento.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsOffscreenPropertyId.                                  | Se il controllo supporta la proprietà [**IsOffscreen**](uiauto-automation-element-propids.md) , deve supportare questo evento. |
| [**\_STRUCTURECHANGEDEVENTID UIA**](uiauto-event-ids.md)                                                                       |                                                                                                                            |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ScrollHorizontallyScrollablePropertyId.   | Se il controllo supporta il pattern di controllo [Scroll](uiauto-implementingscroll.md) , deve supportare questo evento.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ScrollHorizontalScrollPercentPropertyId. | Se il controllo supporta il pattern di controllo [Scroll](uiauto-implementingscroll.md) , deve supportare questo evento.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ScrollHorizontalViewSizePropertyId.           | Se il controllo supporta il pattern di controllo [Scroll](uiauto-implementingscroll.md) , deve supportare questo evento.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ScrollVerticallyScrollablePropertyId.       | Se il controllo supporta il pattern di controllo [Scroll](uiauto-implementingscroll.md) , deve supportare questo evento.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ScrollVerticalScrollPercentPropertyId.     | Se il controllo supporta il pattern di controllo [Scroll](uiauto-implementingscroll.md) , deve supportare questo evento.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ScrollVerticalViewSizePropertyId.               | Se il controllo supporta il pattern di controllo [Scroll](uiauto-implementingscroll.md) , deve supportare questo evento.           |
| [**\_InvalidatedEventId selezione \_ UIA**](uiauto-event-ids.md)                                                            | Se il controllo supporta il pattern di controllo [Selection](uiauto-implementingselection.md) , deve supportare questo evento.     |
| [**\_TextSelectionChangedEventId testo \_ UIA**](uiauto-event-ids.md)                                                    |                                                                                                                            |
| [**\_TextChangedEventId testo \_ UIA**](uiauto-event-ids.md)                                                                      |                                                                                                                            |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ValueValuePropertyId.                                       | Se il controllo supporta il pattern di controllo [value](uiauto-implementingvalue.md) , deve supportare questo evento.             |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente](uiauto-controltypesoverview.md)
</dt> <dt>

[Cenni preliminari su automazione interfaccia utente](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




