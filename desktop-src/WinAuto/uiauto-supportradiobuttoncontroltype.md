---
title: RadioButton (tipo di controllo)
description: In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo RadioButton.
ms.assetid: 6fc4a6a3-f5c0-402b-b9e7-870dfaa3370d
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo RadioButton
- Automazione interfaccia utente, tipo di controllo RadioButton
- Automazione interfaccia utente, struttura ad albero per il tipo di controllo RadioButton
- Automazione interfaccia utente, proprietà per il tipo di controllo RadioButton
- Automazione interfaccia utente, pattern di controllo per il tipo di controllo RadioButton
- Automazione interfaccia utente, eventi per il tipo di controllo RadioButton
- strutture ad albero, tipo di controllo RadioButton
- Proprietà, tipo di controllo RadioButton
- pattern di controllo, tipo di controllo RadioButton
- eventi, tipo di controllo RadioButton
- supporto per il tipo di controllo RadioButton
- RadioButton (tipo di controllo)
- tipi di controllo, struttura ad albero per il tipo di controllo RadioButton
- tipi di controllo, pattern di controllo per il tipo di controllo RadioButton
- tipi di controllo, supporto per RadioButton
- tipi di controllo, RadioButton
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4702a2227a5164ff694378c82fa3b7cde33f9823
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712703"
---
# <a name="radiobutton-control-type"></a>RadioButton (tipo di controllo)

In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo **RadioButton** .

Un pulsante di opzione è composto da un pulsante circolare e testo definito dall'applicazione (etichetta), un'icona o una bitmap che indica una scelta che l'utente può effettuare selezionando il pulsante. Un'applicazione usa in genere i pulsanti di opzione in una casella di gruppo per consentire all'utente di effettuare la scelta da un set di opzioni correlate che si escludono a vicenda. Ad esempio, l'applicazione potrebbe visualizzare un gruppo di pulsanti di opzione da cui l'utente può selezionare una preferenza di formato per il testo selezionato nell'area client. L'utente può selezionare un formato allineato a sinistra, a destra oppure centrato selezionando il pulsante di opzione corrispondente. In genere, l'utente può selezionare una sola opzione alla volta da un set di pulsanti di opzione.

> [!Note]  
> Un'altra generalizzazione del controllo per i pulsanti in cui è possibile selezionare solo un gruppo è il contenuto di un interruttore. Alcuni framework dell'interfaccia utente considerano un pulsante di opzione come interruttore specializzato.

 

Nelle sezioni seguenti vengono definiti la struttura ad albero, le proprietà, i pattern di controllo e gli eventi di automazione interfaccia utente necessari per il tipo di controllo **RadioButton** . I requisiti di automazione interfaccia utente si applicano a tutti i controlli Button in cui la piattaforma/Framework dell'interfaccia utente integra il supporto di automazione interfaccia utente per i tipi di controllo e i pattern

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Pattern di controllo obbligatori](#required-control-patterns)
-   [Eventi obbligatori](#required-events)
-   [Osservazioni:](#remarks)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

Nella tabella seguente viene illustrata una tipica visualizzazione del controllo e del contenuto dell'albero di automazione interfaccia utente relativo ai controlli pulsante di opzione e viene descritto il possibile contenuto di ogni visualizzazione. Per altre informazioni sull'albero di automazione interfaccia utente, vedere [Cenni preliminari sull'albero di automazione interfaccia utente](uiauto-treeoverview.md).



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
<li>RadioButton</li>
</ul></td>
<td><ul>
<li>RadioButton</li>
</ul></td>
</tr>
</tbody>
</table>



 

Non sono presenti elementi figli nella visualizzazione controlli o nella visualizzazione contenuto.

## <a name="relevant-properties"></a>Proprietà rilevanti

La tabella seguente elenca le proprietà di automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per i controlli che implementano il tipo di controllo **RadioButton** , ad esempio i controlli Button. Per altre informazioni sulle proprietà di automazione interfaccia utente, vedere [recupero di proprietà da elementi di automazione interfaccia utente](uiauto-propertiesforclients.md).



| Proprietà di automazione interfaccia utente                                                                                              | Valore           | Note                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_AUTOMATIONIDPROPERTYID UIA**](uiauto-automation-element-propids.md)                 | Vedere le note.      | Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata della struttura ad albero di automazione interfaccia utente.                                  |
| [**\_BOUNDINGRECTANGLEPROPERTYID UIA**](uiauto-automation-element-propids.md)       | Vedere le note.      | Il rettangolo più esterno che contiene l'intero controllo.                                                                                      |
| [**\_CLICKABLEPOINTPROPERTYID UIA**](uiauto-automation-element-propids.md)             | Vedere le note.      | Il punto selezionabile deve essere un punto che, quando selezionato, seleziona il pulsante di opzione.                                                             |
| [**\_CONTROLTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md)                   | **RadioButton** |                                                                                                                                               |
| [**\_ISCONTENTELEMENTPROPERTYID UIA**](uiauto-automation-element-propids.md)         | true            | Il controllo pulsante di opzione viene sempre incluso nella visualizzazione contenuto dell'albero di automazione interfaccia utente.                                                    |
| [**\_ISCONTROLELEMENTPROPERTYID UIA**](uiauto-automation-element-propids.md)         | true            | Il controllo pulsante di opzione viene sempre incluso nella visualizzazione controlli dell'albero di automazione interfaccia utente.                                                    |
| [**\_ISKEYBOARDFOCUSABLEPROPERTYID UIA**](uiauto-automation-element-propids.md)   | Vedere le note.      | Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.                                                                     |
| [**\_LABELEDBYPROPERTYID UIA**](uiauto-automation-element-propids.md)                       | NULL            | I controlli pulsante di opzione hanno un'etichetta automatica in base al relativo contenuto.                                                                                     |
| [**\_LOCALIZEDCONTROLTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md) | Vedere le note.      | Stringa localizzata corrispondente al tipo di controllo **RadioButton** . Il valore predefinito è "pulsante di opzione" per en-US o inglese (Stati Uniti). |
| [**\_NAMEPROPERTYID UIA**](uiauto-automation-element-propids.md)                                 | Vedere le note.      | Il nome del controllo pulsante di opzione è il testo visualizzato accanto al pulsante che mantiene lo stato di selezione.                      |



 

## <a name="required-control-patterns"></a>Pattern di controllo obbligatori

La tabella seguente elenca i pattern di controllo di automazione interfaccia utente che devono essere supportati da tutti i controlli pulsante di opzione. Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Pattern di controllo/proprietà del pattern                                               | Supporto/valore | Note                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)                | Necessario      | Tutti i controlli pulsante di opzione devono supportare il pattern di controllo [SelectionItem](uiauto-implementingselectionitem.md) per abilitarne la selezione.                                                                                                                                                                                                                                                             |
| [**SelectionContainer**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_selectioncontainer) | Vedere le note.    | La proprietà [**SelectionContainer**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_selectioncontainer) deve sempre essere completata in modo che un client di automazione interfaccia utente possa determinare quali altri pulsanti di opzione in un contesto specifico sono correlati tra loro. Per la versione Microsoft Win32 del pulsante di opzione, questa proprietà non è supportata perché non è possibile ottenere queste informazioni da tale framework legacy. |
| [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)                              | Mai         | Dopo aver impostato questa proprietà, il pulsante di opzione non può scorrere tra i propri stati. Il pattern di controllo di [attivazione/disattivazione](uiauto-implementingtoggle.md) non deve mai essere supportato su un pulsante di opzione.                                                                                                                                                                                                                                      |



 

## <a name="required-events"></a>Eventi obbligatori

La tabella seguente elenca gli eventi di automazione interfaccia utente necessari per supportare i controlli Button. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



| Evento di automazione interfaccia utente                                                                                                                     | Note                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**\_AUTOMATIONFOCUSCHANGEDEVENTID UIA**](uiauto-event-ids.md)                                        |                                                                                                                                |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà BoundingRectanglePropertyId.   |                                                                                                                                |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsEnabledPropertyId.                   | Se il controllo supporta la proprietà [**IsEnabled**](uiauto-automation-element-propids.md) , deve supportare questo evento.       |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsOffscreenPropertyId.               | Se il controllo supporta la proprietà [**IsOffscreen**](uiauto-automation-element-propids.md) , deve supportare questo evento.     |
| [**\_ElementRemovedFromSelectionEventId SelectionItem di UIA \_**](uiauto-event-ids.md) | Se il controllo supporta il pattern di controllo [SelectionItem](uiauto-implementingselectionitem.md) , deve supportare questo evento. |
| [**\_ElementSelectedEventId SelectionItem di UIA \_**](uiauto-event-ids.md)                         | Se il controllo supporta il pattern di controllo [SelectionItem](uiauto-implementingselectionitem.md) , deve supportare questo evento. |
| [**\_STRUCTURECHANGEDEVENTID UIA**](uiauto-event-ids.md)                                                    |                                                                                                                                |



 

## <a name="remarks"></a>Commenti

Un pulsante di opzione rappresenta una singola opzione selezionabile tra un gruppo di pulsanti di opzione peer. Idealmente, i pulsanti di opzione devono avere un elemento Grouping che chiarisca i limiti dei pulsanti di opzione peer. Spesso, tuttavia, il limite è implicito nella struttura degli elementi dell'interfaccia utente. Un menu, ad esempio, può contenere un set di pulsanti di opzione consecutivi anziché voci di menu o un set di pulsanti di opzione che si verificano dopo un'etichetta di gruppo, ma prima di un elemento di cui è possibile eseguire l'azione, ad esempio un pulsante.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente](uiauto-controltypesoverview.md)
</dt> <dt>

[Cenni preliminari su automazione interfaccia utente](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




