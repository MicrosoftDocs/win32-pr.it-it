---
title: Tipo di controllo ToolTip
description: In questo argomento vengono fornite informazioni sul supporto di Microsoft Automazione interfaccia utente per il tipo di controllo ToolTip. I controlli descrizione comando sono finestre popup contenenti testo.
ms.assetid: 810f85a9-4d3b-4ceb-bd2c-bf70e8712ae2
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo ToolTip
- Automazione interfaccia utente,Tipo di controllo ToolTip
- Automazione interfaccia utente,struttura ad albero per il tipo di controllo ToolTip
- Automazione interfaccia utente,proprietà per il tipo di controllo ToolTip
- Automazione interfaccia utente,pattern di controllo per il tipo di controllo ToolTip
- Automazione interfaccia utente,eventi per il tipo di controllo ToolTip
- strutture ad albero, tipo di controllo ToolTip
- proprietà, tipo di controllo ToolTip
- pattern di controllo, tipo di controllo ToolTip
- eventi, tipo di controllo ToolTip
- supporto per il tipo di controllo ToolTip
- ToolTip (tipo di controllo)
- tipi di controllo, struttura ad albero per il tipo di controllo ToolTip
- tipi di controllo, pattern di controllo per il tipo di controllo ToolTip
- tipi di controllo, supporto per tooltip
- tipi di controllo, descrizione comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a627114afcdeeb9b6e156572476462fa7ecde75a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472857"
---
# <a name="tooltip-control-type"></a>Tipo di controllo ToolTip

Questo argomento fornisce informazioni sul supporto di Microsoft Automazione interfaccia utente per il **tipo di controllo ToolTip.** I controlli descrizione comando sono finestre popup contenenti testo.

Le sezioni seguenti definiscono la struttura ad Automazione interfaccia utente struttura ad albero, le proprietà, i pattern di controllo e gli eventi per il **tipo di controllo ToolTip.** I Automazione interfaccia utente si applicano a tutti i controlli descrizione comando in cui il framework o la piattaforma dell'interfaccia utente si integra Automazione interfaccia utente per i tipi di controllo e i pattern di controllo.

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Pattern di controllo obbligatori](#required-control-patterns)
-   [Eventi obbligatori](#required-events)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

La tabella seguente illustra un controllo tipico e una visualizzazione contenuto dell'albero Automazione interfaccia utente relativo ai controlli descrizione comando e descrive cosa può essere contenuto in ogni visualizzazione. Per altre informazioni sull'albero Automazione interfaccia utente, vedere panoramica [Automazione interfaccia utente albero.](uiauto-treeoverview.md)




| Visualizzazione controlli | Visualizzazione contenuto | 
|--------------|--------------|
| <ul><li>ToolTip<ul><li>Text (0 o più)</li><li>Image (0 o più)</li></ul></li></ul> | <ul><li>ToolTip</li></ul> | 




 

I controlli descrizione comando vengono visualizzati solo nella visualizzazione contenuto dell'albero Automazione interfaccia utente se possono ricevere lo stato attivo della tastiera. In caso contrario, tutte le informazioni della descrizione comando sono disponibili dalla proprietà [**IUIAutomationElement::CurrentHelpText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currenthelptext) (o [**CachedHelpText)**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedhelptext)dell'elemento a cui fa riferimento la descrizione comando.

Le descrizioni comando devono essere visualizzate sotto il controllo a cui fanno riferimento le relative informazioni. I client devono restare in ascolto del [**\_ toolTipOpenedEventId**](uiauto-event-ids.md) dell'interfaccia utente per assicurarsi di ottenere in modo coerente le informazioni contenute nelle descrizioni comando.

## <a name="relevant-properties"></a>Proprietà rilevanti

Nella tabella seguente sono elencate le Automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per il **tipo di controllo ToolTip.** Per altre informazioni sulle Automazione interfaccia utente, vedere [Recupero di proprietà da Automazione interfaccia utente elementi](uiauto-propertiesforclients.md).



| Proprietà di automazione interfaccia utente                                                                                              | valore       | Note                                                                                                                                                                                                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Vedere le note.  | Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata dell'Automazione interfaccia utente albero.                                                                                                                                                                                                                                                   |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vedere le note.  | Il rettangolo più esterno che contiene l'intero controllo.                                                                                                                                                                                                                                                                                                       |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vedere le note.  | Il punto selezionabile deve essere la parte della descrizione comando che chiude il controllo. Alcune descrizioni comando non hanno questa possibilità e non avranno un punto selezionabile.                                                                                                                                                                                                  |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **ToolTip** |                                                                                                                                                                                                                                                                                                                                                                |
| [**\_IsContentElementPropertyId dell'interfaccia utente**](uiauto-automation-element-propids.md)         | Dipende da     | Se il controllo descrizione comando può ricevere lo stato attivo della tastiera, deve essere visualizzato nella visualizzazione contenuto dell'albero di . Se è solo testo, è disponibile come proprietà [**IUIAutomationElement::CurrentHelpText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currenthelptext) (o [**CachedHelpText)**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedhelptext)dal controllo che lo ha generato. |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | Vero        | Il controllo descrizione comando è sempre incluso nella visualizzazione controlli dell'Automazione interfaccia utente albero.                                                                                                                                                                                                                                                                          |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Vedere le note.  | Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.                                                                                                                                                                                                                                                                                      |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULL        | I controlli descrizione comando sono sempre auto-etichettati in base al relativo contenuto.                                                                                                                                                                                                                                                                                                    |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vedere le note.  | Stringa localizzata corrispondente al tipo di controllo ToolTip. Il valore predefinito è "tooltip" per en-US o English (Stati Uniti).                                                                                                                                                                                                                               |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Vedere le note.  | Il nome del controllo descrizione comando è il testo visualizzato all'interno della descrizione comando.                                                                                                                                                                                                                                                                              |



 

## <a name="required-control-patterns"></a>Pattern di controllo obbligatori

Nella tabella seguente sono elencati i Automazione interfaccia utente che devono essere supportati dai controlli descrizione comando. Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Pattern di controllo                                   | Supporto | Note                                                                                                                                                                                                                                                                             |
|---------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider)     | Dipende da | Per una migliore accessibilità, un controllo descrizione comando può supportare il pattern di controllo [Text,](uiauto-implementingtextandtextrange.md) anche se non è obbligatorio. Il pattern di controllo Text è utile quando il testo ha stili di formattazione e attributi, ad esempio colore, grassetto e corsivo. |
| [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider) | Dipende da | Le descrizioni comando che possono essere chiuse facendo clic su un elemento dell'interfaccia utente devono supportare il pattern di controllo [Window](uiauto-implementingwindow.md) in modo che possano essere chiuse automaticamente.                                                                                                                 |



 

## <a name="required-events"></a>Eventi obbligatori

I controlli descrizione comando devono [**generare l'evento \_ UIA ToolTipOpenedEventId**](uiauto-event-ids.md) quando vengono visualizzati sullo schermo. L'evento includerà un riferimento all'Automazione interfaccia utente elemento della descrizione comando stessa.

La tabella seguente elenca gli eventi Automazione interfaccia utente che i controlli descrizione comando devono supportare. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automazione interfaccia utente eventi                                                                                                                            | Note                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                               |                                                                                                                            |
| [**Interfaccia \_ utente Evento di modifica della proprietà BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md)          |                                                                                                                            |
| [**Interfaccia \_ utente Evento di modifica della proprietà IsEnabledPropertyId.**](uiauto-automation-element-propids.md)                          | Se il controllo supporta la [**proprietà IsEnabled,**](uiauto-automation-element-propids.md) deve supportare questo evento.   |
| [**Interfaccia \_ utente Evento di modifica della proprietà IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)                      | Se il controllo supporta la [**proprietà IsOffscreen,**](uiauto-automation-element-propids.md) deve supportare questo evento. |
| [**Interfaccia \_ utente Evento di modifica**](uiauto-automation-element-propids.md) della proprietà NamePropertyId.                                    |                                                                                                                            |
| [**\_ \_ TextChangedEventId dell'interfaccia utente**](uiauto-event-ids.md)                                                          | Se il controllo supporta il pattern [di controllo Text,](uiauto-implementingtextandtextrange.md) deve supportare questo evento.   |
| [**UIA \_ ToolTipClosedEventId**](uiauto-event-ids.md)                                                                 |                                                                                                                            |
| [**UIA \_ ToolTipOpenedEventId**](uiauto-event-ids.md)                                                                 |                                                                                                                            |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                           |                                                                                                                            |
| [**UIA \_ Window \_ WindowClosedEventId**](uiauto-event-ids.md)                                                    | Se il controllo supporta il pattern [di controllo Window,](uiauto-implementingwindow.md) deve supportare questo evento.           |
| [**UIA \_ Window \_ WindowOpenedEventId**](uiauto-event-ids.md)                                                    | Se il controllo supporta il pattern [di controllo Window,](uiauto-implementingwindow.md) deve supportare questo evento.           |
| [**Interfaccia \_ utente Evento di modifica della proprietà WindowWindowVisualStatePropertyId.**](uiauto-control-pattern-propids.md) | Se il controllo supporta il pattern [di controllo Window,](uiauto-implementingwindow.md) deve supportare questo evento.           |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente](uiauto-controltypesoverview.md)
</dt> <dt>

[Cenni preliminari su automazione interfaccia utente](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




