---
title: Tipo di controllo Separator
description: Questo argomento fornisce informazioni sul supporto di Microsoft Automazione interfaccia utente per il tipo di controllo Separator.
ms.assetid: 4987b05a-101e-48b1-aed2-bd7206146f70
keywords:
- Automazione interfaccia utente,supporto per il tipo di controllo Separator
- Automazione interfaccia utente,Tipo di controllo separatore
- Automazione interfaccia utente,struttura ad albero per il tipo di controllo Separator
- Automazione interfaccia utente,proprietà per il tipo di controllo Separator
- Automazione interfaccia utente,pattern di controllo per il tipo di controllo Separator
- Automazione interfaccia utente,events per il tipo di controllo Separator
- strutture ad albero, tipo di controllo Separator
- proprietà,Tipo di controllo separatore
- pattern di controllo,tipo di controllo separatore
- eventi,Tipo di controllo separatore
- supporto per il tipo di controllo Separator
- Separator (tipo di controllo)
- tipi di controllo, struttura ad albero per il tipo di controllo Separator
- tipi di controllo, pattern di controllo per il tipo di controllo Separator
- tipi di controllo, supporto per separatore
- tipi di controllo,separatore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0685f21565a6252febfadad115c8edf10990995c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477717"
---
# <a name="separator-control-type"></a>Tipo di controllo Separator

Questo argomento fornisce informazioni sul supporto di Microsoft Automazione interfaccia utente per il tipo di controllo **Separator.**

I controlli separatore vengono usati per dividere visivamente uno spazio in due aree. Ad esempio, un controllo separatore può essere una barra che definisce due riquadri in una finestra. Se il separatore può essere spostato, il controllo deve essere esposto come il tipo di controllo Thumb.

Le sezioni seguenti definiscono la struttura ad Automazione interfaccia utente, le proprietà, i pattern di controllo e gli eventi necessari per il tipo di controllo **Separator.** I Automazione interfaccia utente si applicano a tutti i controlli separatori in cui il framework o la piattaforma dell'interfaccia utente Automazione interfaccia utente supporto per i tipi di controllo e i pattern di controllo.

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Pattern di controllo obbligatori](#required-control-patterns)
-   [Eventi obbligatori](#required-events)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

La tabella seguente illustra un controllo tipico e una visualizzazione contenuto dell'albero Automazione interfaccia utente che riguarda i controlli separatori e descrive cosa può essere contenuto in ogni visualizzazione. Per altre informazioni sull'albero Automazione interfaccia utente, vedere Panoramica Automazione interfaccia utente [albero](uiauto-treeoverview.md).




| Visualizzazione controlli | Visualizzazione contenuto | 
|--------------|--------------|
| <ul><li>Separatore</li></ul> | <ul><li>Il <strong>tipo di</strong> controllo Separator non ha mai contenuto.</li></ul> | 




 

## <a name="relevant-properties"></a>Proprietà rilevanti

Nella tabella seguente sono elencate le Automazione interfaccia utente il cui valore o definizione è particolarmente rilevante per i controlli separatore. Per altre informazioni sulle Automazione interfaccia utente, vedere Recupero di proprietà [da Automazione interfaccia utente Elements](uiauto-propertiesforclients.md).



| Proprietà di automazione interfaccia utente                                                                                              | valore         | Note                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Vedere le note.    | Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata dell'Automazione interfaccia utente albero.                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vedere le note.    | Il rettangolo più esterno che contiene l'intero controllo.                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vedere le note.    | Supportata se è presente un rettangolo di delimitazione. Se non tutti i punti all'interno del rettangolo di delimitazione sono selezionabili e l'elemento esegue hit testing specializzati, esegue l'override e fornisce un punto selezionabile. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Separatore** |                                                                                                                                                                                                      |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | FALSE         | Il controllo separatore non è mai un contenuto.                                                                                                                                                              |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | true          | Il controllo separatore deve essere sempre un controllo.                                                                                                                                                      |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Vedere le note.    | Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.                                                                                                                            |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULL          | Il controllo separatore non dispone di un'etichetta statica.                                                                                                                                                  |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vedere le note.    | Stringa localizzata corrispondente al tipo di controllo **Separator.** Il valore predefinito è "Separator" per en-US o English (Stati Uniti).                                                             |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | ""            | Il controllo separatore non richiede una **proprietà** Name.                                                                                                                                          |



 

## <a name="required-control-patterns"></a>Pattern di controllo obbligatori

Il controllo separatore non deve supportare qualsiasi pattern di controllo. Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).

## <a name="required-events"></a>Eventi obbligatori

Nella tabella seguente sono elencati Automazione interfaccia utente che i controlli separatori devono supportare. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automazione interfaccia utente evento                                                                                                                   | Note                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**Interfaccia \_ utente Evento di modifica della proprietà BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md) |                                                                                                                            |
| [**Interfaccia \_ utente Evento di modifica della proprietà IsEnabledPropertyId.**](uiauto-automation-element-propids.md)                 | Se il controllo supporta la [**proprietà IsEnabled,**](uiauto-automation-element-propids.md) deve supportare questo evento.   |
| [**Interfaccia \_ utente Evento di modifica della proprietà IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)             | Se il controllo supporta la [**proprietà IsOffscreen,**](uiauto-automation-element-propids.md) deve supportare questo evento. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente](uiauto-controltypesoverview.md)
</dt> <dt>

[Cenni preliminari su automazione interfaccia utente](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




