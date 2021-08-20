---
title: Tipo di controllo Gruppo
description: In questo argomento vengono fornite informazioni sul supporto Automazione interfaccia utente Microsoft per il tipo di controllo Group.
ms.assetid: f8363c2f-dbff-43a3-831f-d30151829ef9
keywords:
- Automazione interfaccia utente,supporto per il tipo di controllo Gruppo
- Automazione interfaccia utente,Tipo di controllo Gruppo
- Automazione interfaccia utente,struttura ad albero per il tipo di controllo Gruppo
- Automazione interfaccia utente,proprietà per il tipo di controllo Gruppo
- Automazione interfaccia utente,pattern di controllo per tipo di controllo Gruppo
- Automazione interfaccia utente,eventi per tipo di controllo Gruppo
- strutture ad albero, tipo di controllo Group
- proprietà, tipo di controllo Gruppo
- pattern di controllo, tipo di controllo Group
- eventi, tipo di controllo Gruppo
- supporto per il tipo di controllo Group
- Group (tipo di controllo)
- tipi di controllo, struttura ad albero per tipo di controllo Gruppo
- tipi di controllo, pattern di controllo per il tipo di controllo Group
- tipi di controllo, supporto per Group
- tipi di controllo, gruppo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe0cee05f7132a35c8dd3f998ae9af5a89ac2a71
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477747"
---
# <a name="group-control-type"></a>Tipo di controllo Gruppo

In questo argomento vengono fornite informazioni sul supporto Automazione interfaccia utente Microsoft per il **tipo di controllo** Group.

Un controllo gruppo rappresenta un nodo all'interno di una gerarchia. Il **tipo di** controllo Group crea una separazione nell'albero Automazione interfaccia utente in modo che gli elementi raggruppati contemporaneamente presentino una divisione logica all'interno dell Automazione interfaccia utente albero.

Nelle sezioni seguenti vengono definiti gli eventi Automazione interfaccia utente struttura ad albero, le proprietà, i pattern di controllo e gli eventi per il **tipo di controllo** Group. I Automazione interfaccia utente di controllo si applicano a tutti i controlli di gruppo in cui il framework o la piattaforma dell'interfaccia utente Automazione interfaccia utente il supporto per i tipi di controllo e i pattern di controllo.

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Pattern di controllo obbligatori](#required-control-patterns)
-   [Eventi obbligatori](#required-events)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

La tabella seguente illustra un controllo tipico e una visualizzazione contenuto dell'albero Automazione interfaccia utente relativo ai controlli di gruppo e descrive gli elementi che possono essere contenuti in ogni visualizzazione. Per altre informazioni sull'albero Automazione interfaccia utente, vedere Automazione interfaccia utente [Tree Overview](uiauto-treeoverview.md).




| Visualizzazione controlli | Visualizzazione contenuto | 
|--------------|--------------|
| <ul><li>Group<ul><li>0 o molti controlli</li></ul></li></ul> | <ul><li>Group<ul><li>0 o molti controlli</li></ul></li></ul> | 




 

I controlli gruppo includono Automazione interfaccia utente per i tipi di controllo presenti sotto di essi nel sottoalbero, inclusi i tipi di controllo [ListItem](uiauto-supportlistitemcontroltype.md), [TreeItem](uiauto-supporttreeitemcontroltype.md)e [DataItem.](uiauto-supportdataitemcontroltype.md) Poiché un controllo gruppo è un contenitore generico, è possibile che qualsiasi tipo di controllo si trova sotto il controllo gruppo nell'albero di .

## <a name="relevant-properties"></a>Proprietà rilevanti

La tabella seguente elenca le Automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per i controlli gruppo. Per altre informazioni sulle Automazione interfaccia utente, vedere [Recupero di proprietà da Automazione interfaccia utente elementi](uiauto-propertiesforclients.md).



| Proprietà di automazione interfaccia utente                                                                                              | valore      | Note                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Vedere le note. | Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata dell'Automazione interfaccia utente albero.                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vedere le note. | Il rettangolo più esterno che contiene l'intero controllo.                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vedere le note. | Supportata se è presente un rettangolo di delimitazione. Se non tutti i punti all'interno del rettangolo di delimitazione sono selezionabili e l'elemento esegue hit testing specializzati, eseguire l'override e fornire un punto selezionabile. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Gruppo**  |                                                                                                                                                                                                      |
| [**\_IsContentElementPropertyId dell'interfaccia utente**](uiauto-automation-element-propids.md)         | **TRUE**   | Il controllo gruppo è sempre incluso nella visualizzazione contenuto dell'Automazione interfaccia utente albero.                                                                                                                  |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | **TRUE**   | Il controllo gruppo è sempre incluso nella visualizzazione controlli dell'Automazione interfaccia utente albero.                                                                                                                  |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Vedere le note. | Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.                                                                                                                            |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Vedere le note. | I controlli gruppo sono in genere associati a un'etichetta automatica. In questi casi, restituisce **NULL.** Se il gruppo ha un'etichetta di testo statico, restituire l'etichetta come valore della **proprietà LabeledBy.**                      |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vedere le note. | Stringa localizzata corrispondente al **tipo di** controllo Group. Il valore predefinito è "group" per en-US o English (Stati Uniti).                                                                     |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Vedere le note. | Il controllo gruppo in genere ricava il proprio nome dal testo dell'etichetta applicata al controllo.                                                                                                                     |



 

## <a name="required-control-patterns"></a>Pattern di controllo obbligatori

Nella tabella seguente sono elencati i Automazione interfaccia utente di controllo personalizzati che devono essere supportati per il **tipo di controllo** Group. Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Pattern di controllo                                                   | Supporto | Note                                                                                                                                                 |
|-------------------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Dipende da | I controlli di gruppo che possono essere usati per visualizzare o nascondere informazioni devono supportare il pattern di [controllo ExpandCollapse.](uiauto-implementingexpandcollapse.md) |



 

## <a name="required-events"></a>Eventi obbligatori

Nella tabella seguente sono elencati gli Automazione interfaccia utente che i controlli di gruppo devono supportare. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automazione interfaccia utente eventi                                                                                                                                                | Note                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                                   |                                                                                                                                                  |
| [**Interfaccia \_ utente Evento di modifica della proprietà BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md)                              |                                                                                                                                                  |
| [**Interfaccia \_ utente Evento di modifica della proprietà ExpandCollapseExpandCollapseStatePropertyId.**](uiauto-control-pattern-propids.md) | Se il controllo supporta il pattern [di controllo ExpandCollapse,](uiauto-implementingexpandcollapse.md) deve supportare questo evento. |
| [**Interfaccia \_ utente Evento di modifica della proprietà IsEnabledPropertyId.**](uiauto-automation-element-propids.md)                                              | Se il controllo supporta la [**proprietà IsEnabled,**](uiauto-automation-element-propids.md) deve supportare questo evento.                         |
| [**Interfaccia \_ utente Evento di modifica della proprietà IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)                                          | Se il controllo supporta la [**proprietà IsOffscreen,**](uiauto-automation-element-propids.md) deve supportare questo evento.                       |
| [**Interfaccia \_ utente Evento di modifica della proprietà ToggleToggleStatePropertyId.**](uiauto-control-pattern-propids.md)                                 | Se il controllo supporta il pattern [di controllo Toggle,](uiauto-implementingtoggle.md) deve supportare questo evento.                                 |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                               |                                                                                                                                                  |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente](uiauto-controltypesoverview.md)
</dt> <dt>

[Cenni preliminari su automazione interfaccia utente](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




