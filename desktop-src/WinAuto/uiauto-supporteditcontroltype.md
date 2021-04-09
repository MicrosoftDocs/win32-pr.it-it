---
title: Modificare il tipo di controllo
description: In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo Edit.
ms.assetid: ec45ec5e-4faa-4635-8726-5bbe1f20b843
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo Edit
- Automazione interfaccia utente, modificare il tipo di controllo
- Automazione interfaccia utente, struttura ad albero per il tipo di controllo Edit
- Automazione interfaccia utente, proprietà per il tipo di controllo Edit
- Automazione interfaccia utente, pattern di controllo per il tipo di controllo Edit
- Automazione interfaccia utente, eventi per tipo di controllo di modifica
- strutture ad albero, modifica del tipo di controllo
- Proprietà, modificare il tipo di controllo
- pattern di controllo, modifica del tipo di controllo
- eventi, modificare il tipo di controllo
- supporto per il tipo di controllo Edit
- Edit (tipo di controllo)
- tipi di controllo, struttura ad albero per il tipo di controllo Edit
- tipi di controllo, pattern di controllo per il tipo di controllo Edit
- tipi di controllo, supporto per la modifica
- tipi di controllo, modifica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de7dffb572497df47d65def91dda22f3b8e59299
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856082"
---
# <a name="edit-control-type"></a>Modificare il tipo di controllo

In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo **Edit** .

I controlli di modifica consentono a un utente di visualizzare e modificare una semplice riga di testo senza il supporto del formato RTF.

Nelle sezioni seguenti vengono definiti la struttura ad albero, le proprietà, i pattern di controllo e gli eventi di automazione interfaccia utente necessari per il tipo di controllo Edit. I requisiti di automazione interfaccia utente si applicano a tutti i controlli di modifica in cui la piattaforma/Framework dell'interfaccia utente integra il supporto di automazione interfaccia utente per i tipi di controllo e pattern

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Pattern di controllo obbligatori](#required-control-patterns)
-   [Eventi obbligatori](#required-events)
-   [Osservazioni:](#remarks)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

Nella tabella seguente viene illustrata una tipica visualizzazione del controllo e del contenuto dell'albero di automazione interfaccia utente relativo ai controlli di modifica e viene descritto il possibile contenuto di ogni visualizzazione. Per altre informazioni sull'albero di automazione interfaccia utente, vedere [Cenni preliminari sull'albero di automazione interfaccia utente](uiauto-treeoverview.md).



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
<li>Modifica</li>
</ul></td>
<td><ul>
<li>Modifica</li>
</ul></td>
</tr>
</tbody>
</table>



 

I controlli che implementano il tipo di controllo **Edit** avranno sempre zero barre di scorrimento nella visualizzazione controlli dell'albero di automazione interfaccia utente, perché si tratta di un controllo a riga singola. In alcuni scenari di layout una singola riga di testo può essere interrotta da un ritorno a capo. Il tipo di controllo di **modifica** è destinato solo a piccole quantità di testo.

## <a name="relevant-properties"></a>Proprietà rilevanti

La tabella seguente elenca le proprietà di automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per i controlli di modifica. Per altre informazioni sulle proprietà di automazione interfaccia utente, vedere [recupero di proprietà da elementi di automazione interfaccia utente](uiauto-propertiesforclients.md).



| Proprietà di automazione interfaccia utente                                                                                              | Valore      | Note                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_AUTOMATIONIDPROPERTYID UIA**](uiauto-automation-element-propids.md)                 | Vedere le note. | Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata della struttura ad albero di automazione interfaccia utente.                                                                                                                                                                         |
| [**\_BOUNDINGRECTANGLEPROPERTYID UIA**](uiauto-automation-element-propids.md)       | Vedere le note. | Il rettangolo più esterno che contiene l'intero controllo.                                                                                                                                                                                                                             |
| [**\_CLICKABLEPOINTPROPERTYID UIA**](uiauto-automation-element-propids.md)             | Vedere le note. | Il controllo di modifica deve disporre di un punto selezionabile che rende disponibile lo stato attivo per l'input alla parte di modifica del controllo quando un utente fa clic su tale punto.                                                                                                                                           |
| [**\_CONTROLTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md)                   | **Modifica**   |                                                                                                                                                                                                                                                                                      |
| [**\_ISCONTENTELEMENTPROPERTYID UIA**](uiauto-automation-element-propids.md)         | **TRUE**   | Il controllo di modifica viene sempre incluso nella visualizzazione contenuto dell'albero di automazione interfaccia utente.                                                                                                                                                                                                   |
| [**\_ISCONTROLELEMENTPROPERTYID UIA**](uiauto-automation-element-propids.md)         | **TRUE**   | Il controllo di modifica viene sempre incluso nella visualizzazione controlli dell'albero di automazione interfaccia utente.                                                                                                                                                                                                   |
| [**\_ISKEYBOARDFOCUSABLEPROPERTYID UIA**](uiauto-automation-element-propids.md)   | Vedere le note. | Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.                                                                                                                                                                                                            |
| [**\_ISPASSWORDPROPERTYID UIA**](uiauto-automation-element-propids.md)                     | Vedere le note. | Deve essere impostato su **true** nei controlli di modifica che contengono password. Se un controllo di modifica include contenuto di tipo Password, questa proprietà può essere usata da una utilità per la lettura dello schermo per determinare se le sequenze di tasti devono essere lette mentre l'utente digita il testo.                                      |
| [**\_LABELEDBYPROPERTYID UIA**](uiauto-automation-element-propids.md)                       | Vedere le note. | Se è presente un'etichetta di testo statico associata al controllo, questa proprietà deve esporre un riferimento a tale controllo. Se il controllo testo è un sottocomponente di un altro controllo, non avrà una proprietà **LabeledBy** impostata.                                                         |
| [**\_LOCALIZEDCONTROLTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md) | Vedere le note. | Stringa localizzata corrispondente al tipo di controllo **Edit** . Il valore predefinito è "Edit" per en-US o inglese (Stati Uniti).                                                                                                                                                       |
| [**\_NAMEPROPERTYID UIA**](uiauto-automation-element-propids.md)                                 | Vedere le note. | Il nome del controllo di modifica viene in genere generato da un'etichetta di testo statico. Se non è presente un'etichetta di testo statico, lo sviluppatore dell'applicazione deve assegnare un valore di proprietà per il **nome** . La proprietà **Name** non deve mai contenere il contenuto testuale del controllo di modifica. |



 

## <a name="required-control-patterns"></a>Pattern di controllo obbligatori

La tabella seguente elenca i pattern di controllo di automazione interfaccia utente che devono essere supportati dai controlli di modifica. Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Pattern di controllo/proprietà del pattern                              | Supporto/valore | Note                                                                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider)     | Dipende da       | Tutti i controlli di modifica che accettano un intervallo numerico devono esporre il pattern di controllo [RangeValue](uiauto-implementingrangevalue.md) .                                                                                                                                                                                                                                                                                       |
| [**Minima**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_minimum)         | Vedere le note.    | Questa proprietà deve essere il valore più piccolo in cui è possibile impostare il contenuto del controllo di modifica.                                                                                                                                                                                                                                                                                                                     |
| [**Massimo**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_maximum)         | Vedere le note.    | Questa proprietà deve essere il valore più grande in cui è possibile impostare il contenuto del controllo di modifica.                                                                                                                                                                                                                                                                                                                      |
| [**SmallChange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_smallchange) | Vedere le note.    | Questa proprietà deve indicare il numero di cifre decimali che è possibile impostare per il valore. Se il controllo di modifica accetta solo numeri interi, il valore della proprietà **SmallChange** deve essere 1. Se il controllo di modifica accetta un intervallo compreso tra 1,0 e 2,0, il valore della proprietà **SmallChange** deve essere 0,1. Se il controllo di modifica accetta un intervallo compreso tra 1,00 e 2,00, il valore della proprietà **SmallChange** deve essere 0,001.                   |
| [**LargeChange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_largechange) | **NULL**      | Questa proprietà non deve essere esposta in un controllo di modifica.                                                                                                                                                                                                                                                                                                                                                      |
| [**Valore**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_value)             | Vedere le note.    | Questa proprietà indica il contenuto numerico del controllo di modifica. Quando un valore più preciso viene impostato da un client di automazione interfaccia utente all'interno degli intervalli specificati nelle proprietà [**Minimum**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_minimum) e [**Maximum**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_maximum) , la proprietà [**value**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_value) viene automaticamente arrotondata al valore accettato più vicino. |
| [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider)                 | Necessario      | Tutti i controlli di modifica devono supportare il pattern di controllo [Text](uiauto-implementingtextandtextrange.md) , perché le informazioni dettagliate devono sempre essere disponibili per i client di Assistive Technology.                                                                                                                                                                                                                     |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)               | Dipende da       | Tutti i controlli di modifica che accettano una stringa devono esporre il pattern di controllo [value](uiauto-implementingvalue.md) .                                                                                                                                                                                                                                                                                                        |
| [**IsReadOnly**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_isreadonly)        | Vedere le note.    | Questa proprietà deve essere impostata per indicare se il controllo può avere un valore impostato a livello di codice oppure può essere modificato dall'utente.                                                                                                                                                                                                                                                                                |
| [**Valore**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_value)                  | Vedere le note.    | Questa proprietà contiene il contenuto testuale del controllo di modifica. Se la [**proprietà \_ IsPasswordPropertyId di UIA**](uiauto-automation-element-propids.md) è impostata su **true**, l'esecuzione di una query sulla proprietà [**value**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_value) deve restituire un errore.                                                                                                                      |



 

## <a name="required-events"></a>Eventi obbligatori

La tabella seguente elenca gli eventi di automazione interfaccia utente che sono necessari per supportare i controlli di modifica. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



| Evento di automazione interfaccia utente                                                                                                                                        | Note                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**\_AUTOMATIONFOCUSCHANGEDEVENTID UIA**](uiauto-event-ids.md)                                                           |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà BoundingRectanglePropertyId.                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsEnabledPropertyId.                                      | Se il controllo supporta la proprietà [**IsEnabled**](uiauto-automation-element-propids.md) , deve supportare questo evento.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsOffscreenPropertyId.                                  | Se il controllo supporta la proprietà [**IsOffscreen**](uiauto-automation-element-propids.md) , deve supportare questo evento. |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà NamePropertyId.                                                |                                                                                                                            |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà RangeValueValuePropertyId.                             | Se il controllo supporta il pattern di controllo [RangeValue](uiauto-implementingrangevalue.md) , deve supportare questo evento.   |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ScrollHorizontallyScrollablePropertyId.   | Un controllo di modifica non supporta mai il pattern di controllo [Scroll](uiauto-implementingscroll.md) .                                |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ScrollHorizontalScrollPercentPropertyId. | Un controllo di modifica non supporta mai il pattern di controllo [Scroll](uiauto-implementingscroll.md) .                                |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ScrollHorizontalViewSizePropertyId.           | Un controllo di modifica non supporta mai il pattern di controllo [Scroll](uiauto-implementingscroll.md) .                                |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ScrollVerticallyScrollablePropertyId.       | Un controllo di modifica non supporta mai il pattern di controllo [Scroll](uiauto-implementingscroll.md) .                                |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ScrollVerticalScrollPercentPropertyId.     | Un controllo di modifica non supporta mai il pattern di controllo [Scroll](uiauto-implementingscroll.md) .                                |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ScrollVerticalViewSizePropertyId.               | Un controllo di modifica non supporta mai il pattern di controllo [Scroll](uiauto-implementingscroll.md) .                                |
| [**\_STRUCTURECHANGEDEVENTID UIA**](uiauto-event-ids.md)                                                                       |                                                                                                                            |
| [**\_TextChangedEventId testo \_ UIA**](uiauto-event-ids.md)                                                                      | Se il controllo supporta il pattern di controllo [Text](uiauto-implementingtextandtextrange.md) , deve supportare questo evento.   |
| [**\_TextSelectionChangedEventId testo \_ UIA**](uiauto-event-ids.md)                                                    | Se il controllo supporta il pattern di controllo [Text](uiauto-implementingtextandtextrange.md) , deve supportare questo evento.   |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ValueValuePropertyId.                                      | Se il controllo supporta il pattern di controllo [value](uiauto-implementingvalue.md) , deve supportare questo evento.             |



 

## <a name="remarks"></a>Commenti

Un controllo di modifica può essere utilizzato come campo di testo di sola lettura che non supporta la selezione o la modifica del testo. Questo controllo di modifica si comporta come un oggetto campo con un nome e un valore specifici.

Se un controllo di modifica contiene un testo segnaposto, ad esempio un banner cue, il testo deve essere utilizzato come proprietà **HelpText** , a meno che il testo non possa essere modificato dall'utente e quindi riutilizzato come testo segnaposto. La barra degli indirizzi di Windows Internet Explorer, ad esempio, contiene il testo "about: Tabs" quando viene aperta una nuova scheda. Questo non è **HelpText** perché è un indirizzo programmatico che può essere utilizzato o modificato dall'utente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente](uiauto-controltypesoverview.md)
</dt> <dt>

[Cenni preliminari su automazione interfaccia utente](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




