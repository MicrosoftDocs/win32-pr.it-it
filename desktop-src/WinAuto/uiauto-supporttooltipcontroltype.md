---
title: Tipo di controllo ToolTip
description: In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo ToolTip. I controlli ToolTip sono finestre popup contenenti testo.
ms.assetid: 810f85a9-4d3b-4ceb-bd2c-bf70e8712ae2
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo ToolTip
- Automazione interfaccia utente, tipo di controllo ToolTip
- Automazione interfaccia utente, struttura ad albero per il tipo di controllo ToolTip
- Automazione interfaccia utente, proprietà per il tipo di controllo ToolTip
- Automazione interfaccia utente, pattern di controllo per il tipo di controllo ToolTip
- Automazione interfaccia utente, eventi per il tipo di controllo ToolTip
- strutture ad albero, tipo di controllo ToolTip
- Proprietà, tipo di controllo ToolTip
- pattern di controllo, tipo di controllo ToolTip
- eventi, tipo di controllo ToolTip
- supporto per il tipo di controllo ToolTip
- ToolTip (tipo di controllo)
- tipi di controllo, struttura ad albero per il tipo di controllo ToolTip
- tipi di controllo, pattern di controllo per il tipo di controllo ToolTip
- tipi di controllo, supporto per la descrizione comando
- tipi di controllo, descrizione comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc3c9f227faf5dd9844f809dac43cf160371490d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710306"
---
# <a name="tooltip-control-type"></a>Tipo di controllo ToolTip

In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo **ToolTip** . I controlli ToolTip sono finestre popup contenenti testo.

Nelle sezioni seguenti vengono definiti la struttura ad albero, le proprietà, i pattern di controllo e gli eventi di automazione interfaccia utente necessari per il tipo di controllo **ToolTip** . I requisiti di automazione interfaccia utente si applicano a tutti i controlli ToolTip in cui la piattaforma/Framework dell'interfaccia utente integra il supporto di automazione interfaccia utente per i tipi di controllo e i pattern

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Pattern di controllo obbligatori](#required-control-patterns)
-   [Eventi obbligatori](#required-events)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

Nella tabella seguente viene illustrata una tipica visualizzazione del controllo e del contenuto dell'albero di automazione interfaccia utente relativo ai controlli ToolTip e viene descritto il possibile contenuto di ogni visualizzazione. Per altre informazioni sull'albero di automazione interfaccia utente, vedere [Cenni preliminari sull'albero di automazione interfaccia utente](uiauto-treeoverview.md).



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
<li>ToolTip
<ul>
<li>Text (0 o più)</li>
<li>Image (0 o più)</li>
</ul></li>
</ul></td>
<td><ul>
<li>ToolTip</li>
</ul></td>
</tr>
</tbody>
</table>



 

I controlli ToolTip vengono visualizzati solo nella visualizzazione contenuto dell'albero di automazione interfaccia utente se possono ricevere lo stato attivo. In caso contrario, tutte le informazioni della descrizione comando sono disponibili nella proprietà [**IUIAutomationElement:: CurrentHelpText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currenthelptext) (o [**CachedHelpText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedhelptext)) nell'elemento a cui fa riferimento la descrizione comando.

Le descrizioni comandi devono essere visualizzate sotto il controllo a cui si riferiscono le relative informazioni. I client devono restare in ascolto dei [**\_ ToolTipOpenedEventId**](uiauto-event-ids.md) di controllo dell'interfaccia utente per assicurarsi che ottengano costantemente le informazioni contenute nelle descrizioni comandi.

## <a name="relevant-properties"></a>Proprietà rilevanti

La tabella seguente elenca le proprietà di automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per il tipo di controllo **ToolTip** . Per altre informazioni sulle proprietà di automazione interfaccia utente, vedere [recupero di proprietà da elementi di automazione interfaccia utente](uiauto-propertiesforclients.md).



| Proprietà di automazione interfaccia utente                                                                                              | Valore       | Note                                                                                                                                                                                                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_AUTOMATIONIDPROPERTYID UIA**](uiauto-automation-element-propids.md)                 | Vedere le note.  | Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata della struttura ad albero di automazione interfaccia utente.                                                                                                                                                                                                                                                   |
| [**\_BOUNDINGRECTANGLEPROPERTYID UIA**](uiauto-automation-element-propids.md)       | Vedere le note.  | Il rettangolo più esterno che contiene l'intero controllo.                                                                                                                                                                                                                                                                                                       |
| [**\_CLICKABLEPOINTPROPERTYID UIA**](uiauto-automation-element-propids.md)             | Vedere le note.  | Il punto selezionabile deve essere la parte della descrizione comando che respinge il controllo. Alcune descrizioni comandi non dispongono di questa funzionalità e non avranno un punto selezionabile.                                                                                                                                                                                                  |
| [**\_CONTROLTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md)                   | **ToolTip** |                                                                                                                                                                                                                                                                                                                                                                |
| [**\_ISCONTENTELEMENTPROPERTYID UIA**](uiauto-automation-element-propids.md)         | Dipende da     | Se il controllo ToolTip può ricevere lo stato attivo, deve essere visualizzato nella visualizzazione contenuto della struttura ad albero. Se è solo testo, è disponibile come proprietà [**IUIAutomationElement:: CurrentHelpText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currenthelptext) (o [**CachedHelpText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedhelptext)) dal controllo che lo ha generato. |
| [**\_ISCONTROLELEMENTPROPERTYID UIA**](uiauto-automation-element-propids.md)         | Vero        | Il controllo ToolTip viene sempre incluso nella visualizzazione controlli dell'albero di automazione interfaccia utente.                                                                                                                                                                                                                                                                          |
| [**\_ISKEYBOARDFOCUSABLEPROPERTYID UIA**](uiauto-automation-element-propids.md)   | Vedere le note.  | Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.                                                                                                                                                                                                                                                                                      |
| [**\_LABELEDBYPROPERTYID UIA**](uiauto-automation-element-propids.md)                       | NULL        | I controlli ToolTip sono sempre etichettati con il relativo contenuto.                                                                                                                                                                                                                                                                                                    |
| [**\_LOCALIZEDCONTROLTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md) | Vedere le note.  | Stringa localizzata corrispondente al tipo di controllo ToolTip. Il valore predefinito è "ToolTip" per en-US o English (Stati Uniti).                                                                                                                                                                                                                               |
| [**\_NAMEPROPERTYID UIA**](uiauto-automation-element-propids.md)                                 | Vedere le note.  | Il nome del controllo ToolTip è il testo visualizzato all'interno della descrizione comando.                                                                                                                                                                                                                                                                              |



 

## <a name="required-control-patterns"></a>Pattern di controllo obbligatori

La tabella seguente elenca i pattern di controllo di automazione interfaccia utente che devono essere supportati dai controlli ToolTip. Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Pattern di controllo                                   | Supporto | Note                                                                                                                                                                                                                                                                             |
|---------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider)     | Dipende da | Per una migliore accessibilità, un controllo ToolTip può supportare il pattern di controllo [Text](uiauto-implementingtextandtextrange.md) , anche se non è obbligatorio. Il pattern di controllo Text è utile quando il testo ha stili di formattazione e attributi, ad esempio colore, grassetto e corsivo. |
| [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider) | Dipende da | Le descrizioni comandi che possono essere chiuse facendo clic su un elemento dell'interfaccia utente devono supportare il pattern di controllo [Window](uiauto-implementingwindow.md) , in modo che possano essere chiuse automaticamente.                                                                                                                 |



 

## <a name="required-events"></a>Eventi obbligatori

I controlli ToolTip devono generare l'evento [**\_ ToolTipOpenedEventId di UIA**](uiauto-event-ids.md) quando vengono visualizzati sullo schermo. L'evento includerà un riferimento all'elemento di automazione interfaccia utente della descrizione comando.

La tabella seguente elenca gli eventi di automazione interfaccia utente necessari per supportare i controlli ToolTip. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



| Evento di automazione interfaccia utente                                                                                                                            | Note                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**\_AUTOMATIONFOCUSCHANGEDEVENTID UIA**](uiauto-event-ids.md)                                               |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà BoundingRectanglePropertyId.          |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsEnabledPropertyId.                          | Se il controllo supporta la proprietà [**IsEnabled**](uiauto-automation-element-propids.md) , deve supportare questo evento.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsOffscreenPropertyId.                      | Se il controllo supporta la proprietà [**IsOffscreen**](uiauto-automation-element-propids.md) , deve supportare questo evento. |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà NamePropertyId.                                    |                                                                                                                            |
| [**\_TextChangedEventId testo \_ UIA**](uiauto-event-ids.md)                                                          | Se il controllo supporta il pattern di controllo [Text](uiauto-implementingtextandtextrange.md) , deve supportare questo evento.   |
| [**\_TOOLTIPCLOSEDEVENTID UIA**](uiauto-event-ids.md)                                                                 |                                                                                                                            |
| [**\_TOOLTIPOPENEDEVENTID UIA**](uiauto-event-ids.md)                                                                 |                                                                                                                            |
| [**\_STRUCTURECHANGEDEVENTID UIA**](uiauto-event-ids.md)                                                           |                                                                                                                            |
| [**\_WindowClosedEventId finestra \_ UIA**](uiauto-event-ids.md)                                                    | Se il controllo supporta il pattern di controllo [Window](uiauto-implementingwindow.md) , deve supportare questo evento.           |
| [**\_WindowOpenedEventId finestra \_ UIA**](uiauto-event-ids.md)                                                    | Se il controllo supporta il pattern di controllo [Window](uiauto-implementingwindow.md) , deve supportare questo evento.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà WindowWindowVisualStatePropertyId. | Se il controllo supporta il pattern di controllo [Window](uiauto-implementingwindow.md) , deve supportare questo evento.           |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente](uiauto-controltypesoverview.md)
</dt> <dt>

[Cenni preliminari su automazione interfaccia utente](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




