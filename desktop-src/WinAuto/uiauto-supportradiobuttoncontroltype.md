---
title: Tipo di controllo RadioButton
description: In questo argomento vengono fornite informazioni sul supporto Automazione interfaccia utente Microsoft per il tipo di controllo RadioButton.
ms.assetid: 6fc4a6a3-f5c0-402b-b9e7-870dfaa3370d
keywords:
- Automazione interfaccia utente,supporto per il tipo di controllo RadioButton
- Automazione interfaccia utente,Tipo di controllo RadioButton
- Automazione interfaccia utente,struttura ad albero per il tipo di controllo RadioButton
- Automazione interfaccia utente,proprietà per il tipo di controllo RadioButton
- Automazione interfaccia utente,pattern di controllo per il tipo di controllo RadioButton
- Automazione interfaccia utente,eventi per il tipo di controllo RadioButton
- strutture ad albero, tipo di controllo RadioButton
- proprietà, tipo di controllo RadioButton
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
ms.openlocfilehash: 358a71f74b40d8465c910f8afe258183c8ea4d5c322fb70e6b6ea946ef7d44ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118825484"
---
# <a name="radiobutton-control-type"></a>Tipo di controllo RadioButton

In questo argomento vengono fornite informazioni sul supporto Automazione interfaccia utente Microsoft per il **tipo di controllo RadioButton.**

Un pulsante di opzione è composto da un pulsante circolare e testo definito dall'applicazione (etichetta), un'icona o una bitmap che indica una scelta che l'utente può effettuare selezionando il pulsante. Un'applicazione usa in genere i pulsanti di opzione in una casella di gruppo per consentire all'utente di effettuare la scelta da un set di opzioni correlate che si escludono a vicenda. Ad esempio, l'applicazione potrebbe visualizzare un gruppo di pulsanti di opzione da cui l'utente può selezionare una preferenza di formato per il testo selezionato nell'area client. L'utente può selezionare un formato allineato a sinistra, a destra oppure centrato selezionando il pulsante di opzione corrispondente. In genere, l'utente può selezionare una sola opzione alla volta da un set di pulsanti di opzione.

> [!Note]  
> Un'altra generalizzazione dei controlli per i pulsanti in cui è possibile selezionarne solo uno in un gruppo è il contenuto di un interruttore. Alcuni framework dell'interfaccia utente considerano un pulsante di opzione un interruttore specializzato.

 

Le sezioni seguenti definiscono la struttura ad Automazione interfaccia utente struttura ad albero, le proprietà, i pattern di controllo e gli eventi per il **tipo di controllo RadioButton.** I Automazione interfaccia utente si applicano a tutti i controlli pulsante in cui il framework o la piattaforma dell'interfaccia utente Automazione interfaccia utente il supporto per i tipi di controllo e i pattern di controllo.

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Pattern di controllo obbligatori](#required-control-patterns)
-   [Eventi obbligatori](#required-events)
-   [Osservazioni:](#remarks)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

La tabella seguente illustra un controllo tipico e una visualizzazione contenuto dell'albero Automazione interfaccia utente relativo ai controlli pulsante di opzione e descrive gli elementi che possono essere contenuti in ogni visualizzazione. Per altre informazioni sull'albero Automazione interfaccia utente, vedere panoramica Automazione interfaccia utente [albero.](uiauto-treeoverview.md)



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

La tabella seguente elenca le Automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per i controlli che implementano il tipo di controllo **RadioButton** , ad esempio i controlli pulsante. Per altre informazioni sulle Automazione interfaccia utente, vedere [Recupero di proprietà da Automazione interfaccia utente elementi](uiauto-propertiesforclients.md).



| Proprietà di automazione interfaccia utente                                                                                              | Valore           | Note                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Vedere le note.      | Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata dell'Automazione interfaccia utente albero.                                  |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vedere le note.      | Il rettangolo più esterno che contiene l'intero controllo.                                                                                      |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vedere le note.      | Il punto selezionabile deve essere un punto che, quando selezionato, seleziona il pulsante di opzione.                                                             |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **RadioButton** |                                                                                                                                               |
| [**IsContentElementPropertyId dell'interfaccia \_ utente**](uiauto-automation-element-propids.md)         | true            | Il controllo pulsante di opzione è sempre incluso nella visualizzazione contenuto dell'Automazione interfaccia utente albero.                                                    |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | true            | Il controllo pulsante di opzione è sempre incluso nella visualizzazione controlli dell'Automazione interfaccia utente albero.                                                    |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Vedere le note.      | Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.                                                                     |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULL            | I controlli pulsante di opzione sono auto-etichettati in base al relativo contenuto.                                                                                     |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vedere le note.      | Stringa localizzata corrispondente al **tipo di controllo RadioButton.** Il valore predefinito è "pulsante di opzione" per en-US o inglese (Stati Uniti). |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Vedere le note.      | Il nome del controllo pulsante di opzione è il testo visualizzato accanto al pulsante che mantiene lo stato di selezione.                      |



 

## <a name="required-control-patterns"></a>Pattern di controllo obbligatori

Nella tabella seguente sono elencati i Automazione interfaccia utente di controllo personalizzati che devono essere supportati da tutti i controlli pulsante di opzione. Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Pattern di controllo/proprietà del pattern                                               | Supporto/valore | Note                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)                | Necessario      | Tutti i controlli pulsante di opzione devono supportare il pattern [di controllo SelectionItem](uiauto-implementingselectionitem.md) per consentire la selezione di se stessi.                                                                                                                                                                                                                                                             |
| [**Selectioncontainer**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_selectioncontainer) | Vedere le note.    | La [**proprietà SelectionContainer**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_selectioncontainer) deve sempre essere completata in modo che un client Automazione interfaccia utente possa determinare quali altri pulsanti di opzione all'interno di un contesto specifico sono correlati tra loro. Per la versione Microsoft Win32 del pulsante di opzione, questa proprietà non è supportata perché non è possibile ottenere queste informazioni dal framework legacy. |
| [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)                              | Mai         | Dopo aver impostato questa proprietà, il pulsante di opzione non può scorrere tra i propri stati. Il [pattern di](uiauto-implementingtoggle.md) controllo Toggle non deve mai essere supportato in un pulsante di opzione.                                                                                                                                                                                                                                      |



 

## <a name="required-events"></a>Eventi obbligatori

La tabella seguente elenca gli eventi Automazione interfaccia utente che i controlli pulsante devono supportare. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automazione interfaccia utente evento                                                                                                                     | Note                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                        |                                                                                                                                |
| [**Interfaccia \_ utente Evento di modifica della proprietà BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md)   |                                                                                                                                |
| [**Interfaccia \_ utente Evento di modifica della proprietà IsEnabledPropertyId.**](uiauto-automation-element-propids.md)                   | Se il controllo supporta la [**proprietà IsEnabled,**](uiauto-automation-element-propids.md) deve supportare questo evento.       |
| [**Interfaccia \_ utente Evento di modifica della proprietà IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)               | Se il controllo supporta la [**proprietà IsOffscreen,**](uiauto-automation-element-propids.md) deve supportare questo evento.     |
| [**UIA \_ SelectionItem \_ ElementRemovedFromSelectionEventId**](uiauto-event-ids.md) | Se il controllo supporta il pattern [di controllo SelectionItem,](uiauto-implementingselectionitem.md) deve supportare questo evento. |
| [**UIA \_ SelectionItem \_ ElementSelectedEventId**](uiauto-event-ids.md)                         | Se il controllo supporta il pattern [di controllo SelectionItem,](uiauto-implementingselectionitem.md) deve supportare questo evento. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                    |                                                                                                                                |



 

## <a name="remarks"></a>Commenti

Un pulsante di opzione rappresenta una singola opzione selezionabile tra un gruppo di pulsanti di opzione peer. Idealmente, i pulsanti di opzione devono avere un elemento di raggruppamento che chiarisca i limiti dei pulsanti di opzione peer. Spesso, tuttavia, il limite è implicito nella struttura degli elementi dell'interfaccia utente. Ad esempio, un menu può contenere un set di pulsanti di opzione consecutivi anziché voci di menu o un set di pulsanti di opzione che si verificano dopo un'etichetta di gruppo, ma prima di un elemento utilizzabile come pulsante.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente](uiauto-controltypesoverview.md)
</dt> <dt>

[Cenni preliminari su automazione interfaccia utente](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




