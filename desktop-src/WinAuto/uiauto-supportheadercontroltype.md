---
title: Tipo di controllo Header
description: Questo argomento fornisce informazioni sul supporto microsoft Automazione interfaccia utente per il tipo di controllo Header.
ms.assetid: 032fc3a1-f939-40db-abbb-532afe309ba3
keywords:
- Automazione interfaccia utente,supporto per il tipo di controllo Header
- Automazione interfaccia utente,Tipo di controllo Header
- Automazione interfaccia utente,struttura ad albero per il tipo di controllo Header
- Automazione interfaccia utente,proprietà per il tipo di controllo Header
- Automazione interfaccia utente,pattern di controllo per il tipo di controllo Header
- Automazione interfaccia utente,events per il tipo di controllo Header
- strutture ad albero, tipo di controllo Header
- proprietà,tipo di controllo Header
- pattern di controllo,tipo di controllo Header
- eventi, tipo di controllo Header
- supporto per il tipo di controllo Header
- Header (tipo di controllo)
- tipi di controllo, struttura ad albero per il tipo di controllo Header
- tipi di controllo, pattern di controllo per il tipo di controllo Header
- tipi di controllo, supporto per Header
- tipi di controllo,intestazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 472a0d7185fa3c2b2dc1dc7593afd106008890bb
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482512"
---
# <a name="header-control-type"></a>Tipo di controllo Header

Questo argomento fornisce informazioni sul supporto microsoft Automazione interfaccia utente per il **tipo di controllo** Header.

Il controllo intestazione fornisce un contenitore visivo per le etichette di righe o colonne di informazioni.

Le sezioni seguenti definiscono la struttura ad Automazione interfaccia utente, le proprietà, i pattern di controllo e gli eventi necessari per il **tipo di controllo Header.** I Automazione interfaccia utente si applicano a tutti i controlli intestazione in cui il framework o la piattaforma dell'interfaccia utente Automazione interfaccia utente supporto per i tipi di controllo e i pattern di controllo.

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Pattern di controllo obbligatori](#required-control-patterns)
-   [Eventi obbligatori](#required-events)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

La tabella seguente illustra un controllo tipico e una visualizzazione contenuto dell'albero Automazione interfaccia utente che riguarda i controlli intestazione e descrive cosa può essere contenuto in ogni visualizzazione. Per altre informazioni sull'albero Automazione interfaccia utente, vedere Panoramica Automazione interfaccia utente [albero](uiauto-treeoverview.md).




| Visualizzazione controlli | Visualizzazione contenuto | 
|--------------|--------------|
| <ul><li>Intestazione<ul><li>HeaderItem (1 o più)</li></ul></li></ul> | (Non applicabile) | 




 

I controlli intestazione hanno sempre uno o più elementi figlio nella visualizzazione controlli dell'Automazione interfaccia utente albero.

I controlli intestazione hanno zero elementi figlio nella visualizzazione contenuto dell'Automazione interfaccia utente struttura ad albero.

## <a name="relevant-properties"></a>Proprietà rilevanti

La tabella seguente elenca le proprietà Automazione interfaccia utente il cui valore o definizione è particolarmente rilevante per i controlli intestazione. Per altre informazioni sulle Automazione interfaccia utente, vedere Recupero di proprietà [da Automazione interfaccia utente elementi](uiauto-propertiesforclients.md).



| Proprietà di automazione interfaccia utente                                                                                              | valore                                                            | Note                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Vedere le note.                                                       | Il valore di questa proprietà deve essere univoco in tutti i controlli di un'applicazione.                                                                                                                     |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vedere le note.                                                       | Il rettangolo più esterno che contiene l'intero controllo.                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vedere le note.                                                       | Supportata se è presente un rettangolo di delimitazione. Se non tutti i punti all'interno del rettangolo di delimitazione sono selezionabili e l'elemento esegue hit testing specializzati, esegue l'override e fornisce un punto selezionabile. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Intestazione**                                                       |                                                                                                                                                                                                      |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | FALSE                                                            | Il controllo intestazione non è incluso nella visualizzazione contenuto dell'Automazione interfaccia utente albero.                                                                                                                    |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | true                                                             | Il controllo intestazione è sempre incluso nella visualizzazione controlli dell'Automazione interfaccia utente albero.                                                                                                                 |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Vedere le note.                                                       | Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.                                                                                                                            |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULL                                                             | I controlli intestazione in genere non hanno un'etichetta statica.                                                                                                                                                          |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vedere le note.                                                       | Il valore predefinito è "header" per en-US o english (Stati Uniti).                                                                                                                                  |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Vedere le note.                                                       | Il controllo intestazione richiede un nome se è presente più di un'intestazione di riga o più di un'intestazione di colonna. Identifica le informazioni all'interno dell'intestazione.                                              |
| [**UIA \_ OrientationPropertyId**](uiauto-automation-element-propids.md)                   | **OrientationType \_ Orizzontale** o **OrientamentoTipo \_ verticale** | Il valore di questa proprietà espone la posizione del controllo intestazione, sia che si tratta di un'intestazione di riga (**OrientationType \_ Horizontal**) o di un'intestazione di colonna (**OrientationType \_ Vertical**).                 |



 

## <a name="required-control-patterns"></a>Pattern di controllo obbligatori

Nella tabella seguente sono elencati i Automazione interfaccia utente di controllo necessari per essere supportati per i controlli intestazione. Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Pattern di controllo                                         | Supporto | Note                                                                                                             |
|---------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------|
| [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) | Dipende da | Implementare [il pattern di](uiauto-implementingtransform.md) controllo Transform se il controllo intestazione può essere ridimensionato. |



 

## <a name="required-events"></a>Eventi obbligatori

Nella tabella seguente sono elencati Automazione interfaccia utente eventi che i controlli intestazione devono supportare. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



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

 

 




