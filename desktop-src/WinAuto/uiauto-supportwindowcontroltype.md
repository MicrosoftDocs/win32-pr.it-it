---
title: Tipo di controllo Window
description: In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo Window.
ms.assetid: 521fb514-e083-48b3-b4a0-52c530154740
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo Window
- Automazione interfaccia utente, tipo di controllo Window
- Automazione interfaccia utente, struttura ad albero per il tipo di controllo Window
- Automazione interfaccia utente, proprietà per il tipo di controllo Window
- Automazione interfaccia utente, pattern di controllo per il tipo di controllo Window
- Automazione interfaccia utente, eventi per il tipo di controllo Window
- strutture ad albero, tipo di controllo Window
- Proprietà, tipo di controllo Window
- pattern di controllo, tipo di controllo Window
- eventi, tipo di controllo Window
- supporto per il tipo di controllo Window
- Window (tipo di controllo)
- tipi di controllo, struttura ad albero per il tipo di controllo Window
- tipi di controllo, pattern di controllo per il tipo di controllo Window
- tipi di controllo, supporto per la finestra
- tipi di controllo, finestra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 422742381cd501d295e4cb7e354ca07e10c13360
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331551"
---
# <a name="window-control-type"></a>Tipo di controllo Window

In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo **Window** .

Il controllo finestra è costituito dalla cornice della finestra, che contiene oggetti figlio, ad esempio barra del titolo, oggetti client e altri oggetti.

Nelle sezioni seguenti vengono definiti la struttura ad albero, le proprietà, i pattern di controllo e gli eventi di automazione interfaccia utente necessari per il tipo di controllo **Window** . I requisiti di automazione interfaccia utente si applicano a tutti i controlli finestra in cui la piattaforma/Framework dell'interfaccia utente integra il supporto di automazione interfaccia utente per tipi di controllo e pattern di controllo

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Pattern di controllo obbligatori](#required-control-patterns)
-   [Eventi obbligatori](#required-events)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

Nella tabella seguente viene illustrata una tipica visualizzazione del controllo e del contenuto dell'albero di automazione interfaccia utente relativo ai controlli finestra e viene descritto il possibile contenuto di ogni visualizzazione. Per altre informazioni sull'albero di automazione interfaccia utente, vedere [Cenni preliminari sull'albero di automazione interfaccia utente](uiauto-treeoverview.md).



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
<li>Finestra</li>
</ul></td>
<td><ul>
<li>Finestra</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a>Proprietà rilevanti

La tabella seguente elenca le proprietà di automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per i controlli finestra. Per altre informazioni sulle proprietà di automazione interfaccia utente, vedere [recupero di proprietà da elementi di automazione interfaccia utente](uiauto-propertiesforclients.md).



| Proprietà di automazione interfaccia utente                                                                                              | Valore      | Note                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_AUTOMATIONIDPROPERTYID UIA**](uiauto-automation-element-propids.md)                 | Vedere le note. | Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata della struttura ad albero di automazione interfaccia utente.                                            |
| [**\_BOUNDINGRECTANGLEPROPERTYID UIA**](uiauto-automation-element-propids.md)       | Vedere le note. | Il rettangolo più esterno che contiene l'intero controllo.                                                                                                |
| [**\_CLICKABLEPOINTPROPERTYID UIA**](uiauto-automation-element-propids.md)             | Vedere le note. | Il controllo finestra deve avere un punto selezionabile che fa sì che la finestra venga selezionata o deselezionata.                                                 |
| [**\_CONTROLTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md)                   | **Window** | Questo valore è uguale per tutti i framework dell'interfaccia utente.                                                                                                           |
| [**\_ISCONTENTELEMENTPROPERTYID UIA**](uiauto-automation-element-propids.md)         | true       | Il controllo finestra è sempre incluso nella visualizzazione contenuto dell'albero di automazione interfaccia utente.                                                                    |
| [**\_ISCONTROLELEMENTPROPERTYID UIA**](uiauto-automation-element-propids.md)         | true       | Il controllo finestra viene sempre incluso nella visualizzazione controlli dell'albero di automazione interfaccia utente.                                                                    |
| [**\_ISKEYBOARDFOCUSABLEPROPERTYID UIA**](uiauto-automation-element-propids.md)   | Vedere le note. | Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.                                                                               |
| [**\_LABELEDBYPROPERTYID UIA**](uiauto-automation-element-propids.md)                       | NULL       | I controlli finestra non hanno un'etichetta di finestra statica.                                                                                                      |
| [**\_LOCALIZEDCONTROLTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md) | Vedere le note. | Stringa localizzata corrispondente al tipo di controllo **Window** . Il valore predefinito è "window" per en-US o inglese (Stati Uniti).                      |
| [**\_NAMEPROPERTYID UIA**](uiauto-automation-element-propids.md)                                 | Vedere le note. | Il controllo finestra contiene sempre un elemento della finestra primaria che si riferisce a quello che l'utente associa come identificatore più semantico per l'elemento. |



 

## <a name="required-control-patterns"></a>Pattern di controllo obbligatori

La tabella seguente elenca i pattern di controllo di automazione interfaccia utente che devono essere supportati dai controlli finestra. Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Pattern di controllo/proprietà del pattern                        | Supporto/valore | Note                                                                                                                                                                        |
|---------------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider)           | Condizionale   | Il pattern di controllo [Dock](uiauto-implementingdock.md) deve essere supportato se la finestra può essere ancorata.                                                                       |
| [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) | Necessario      | Il pattern di controllo [Transform](uiauto-implementingtransform.md) consente lo spostamento, il ridimensionamento o la rotazione della finestra sullo schermo. (Non si applica alle app di Windows Store). |
| [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider)       | Necessario      | Il pattern di controllo [Window](uiauto-implementingwindow.md) Abilita operazioni specifiche per la finestra.                                                                      |



 

## <a name="required-events"></a>Eventi obbligatori

La tabella seguente elenca gli eventi di automazione interfaccia utente necessari per supportare i controlli **finestra** . Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



| Evento di automazione interfaccia utente                                                                                                                                        | Note                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ASYNCCONTENTLOADEDEVENTID UIA**](uiauto-event-ids.md)                                                                   |                                                                                                                                                                                                                           |
| [**\_AUTOMATIONFOCUSCHANGEDEVENTID UIA**](uiauto-event-ids.md)                                                           |                                                                                                                                                                                                                           |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà BoundingRectanglePropertyId.                      |                                                                                                                                                                                                                           |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsEnabledPropertyId.                                      | Se il controllo supporta la proprietà [**IsEnabled**](uiauto-automation-element-propids.md) , deve supportare questo evento.                                                                                                  |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsOffscreenPropertyId.                                  | Se il controllo supporta la proprietà [**IsOffscreen**](uiauto-automation-element-propids.md) , deve supportare questo evento.                                                                                                |
| [**\_LAYOUTINVALIDATEDEVENTID UIA**](uiauto-event-ids.md)                                                                     |                                                                                                                                                                                                                           |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà NamePropertyId.                                                |                                                                                                                                                                                                                           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ScrollHorizontallyScrollablePropertyId.   | Se il controllo supporta il pattern di controllo [Scroll](uiauto-implementingscroll.md) , deve supportare questo evento.                                                                                                          |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ScrollHorizontalScrollPercentPropertyId. | Se il controllo supporta il pattern di controllo [Scroll](uiauto-implementingscroll.md) , deve supportare questo evento.                                                                                                          |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ScrollHorizontalViewSizePropertyId.           | Se il controllo supporta il pattern di controllo [Scroll](uiauto-implementingscroll.md) , deve supportare questo evento.                                                                                                          |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ScrollVerticallyScrollablePropertyId.       | Se il controllo supporta il pattern di controllo [Scroll](uiauto-implementingscroll.md) , deve supportare questo evento.                                                                                                          |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ScrollVerticalScrollPercentPropertyId.     | Se il controllo supporta il pattern di controllo [Scroll](uiauto-implementingscroll.md) , deve supportare questo evento.                                                                                                          |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ScrollVerticalViewSizePropertyId.               | Se il controllo supporta il pattern di controllo [Scroll](uiauto-implementingscroll.md) , deve supportare questo evento.                                                                                                          |
| [**\_STRUCTURECHANGEDEVENTID UIA**](uiauto-event-ids.md)                                                                       |                                                                                                                                                                                                                           |
| [**\_WindowClosedEventId finestra \_ UIA**](uiauto-event-ids.md)                                                                |                                                                                                                                                                                                                           |
| [**\_WindowOpenedEventId finestra \_ UIA**](uiauto-event-ids.md)                                                                |                                                                                                                                                                                                                           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà WindowWindowVisualStatePropertyId.             | Se il controllo supporta la proprietà [**WindowVisualState**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationwindowpattern-get_cachedwindowvisualstate) del pattern di controllo [Window](uiauto-implementingwindow.md) , questo evento deve essere supportato. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente](uiauto-controltypesoverview.md)
</dt> <dt>

[Cenni preliminari su automazione interfaccia utente](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




