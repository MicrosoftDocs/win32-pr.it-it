---
title: Tipo di controllo Menu
description: Questo argomento fornisce informazioni sul supporto di Microsoft Automazione interfaccia utente per il tipo di controllo Menu.
ms.assetid: cdbb6db7-63d7-422e-952c-7b59779fefbe
keywords:
- Automazione interfaccia utente,supporto per il tipo di controllo Menu
- Automazione interfaccia utente,Tipo di controllo Menu
- Automazione interfaccia utente,struttura ad albero per il tipo di controllo Menu
- Automazione interfaccia utente,proprietà per il tipo di controllo Menu
- Automazione interfaccia utente,pattern di controllo per il tipo di controllo Menu
- Automazione interfaccia utente,eventi per il tipo di controllo Menu
- strutture ad albero, tipo di controllo Menu
- proprietà,Tipo di controllo Menu
- pattern di controllo,Tipo di controllo Menu
- eventi,Tipo di controllo Menu
- supporto per il tipo di controllo Menu
- Menu (tipo di controllo)
- tipi di controllo, struttura ad albero per il tipo di controllo Menu
- tipi di controllo,pattern di controllo per il tipo di controllo Menu
- tipi di controllo, supporto per Menu
- tipi di controllo,menu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d86d5aad29519bca4e9cfe03da4b6f0e9ccaeb9
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468078"
---
# <a name="menu-control-type"></a>Tipo di controllo Menu

Questo argomento fornisce informazioni sul supporto microsoft Automazione interfaccia utente per il **tipo di controllo Menu.**

Un controllo menu consente l'organizzazione gerarchica degli elementi associati a comandi e gestori eventi. In una tipica applicazione Microsoft Windows, una barra dei menu contiene diversi pulsanti di menu (ad esempio **File** **,** Modifica e **Finestra**) e ogni pulsante di menu visualizza un menu. Un menu contiene una raccolta di voci di menu (ad esempio **Nuovo**, **Apri** e **Chiudi**), che può essere espansa per visualizzare altre voci di menu che, se selezionate, consentono di eseguire un'azione specifica.

Le sezioni seguenti definiscono la struttura ad Automazione interfaccia utente, le proprietà, i pattern di controllo e gli eventi necessari per il tipo di controllo **Menu.** I Automazione interfaccia utente si applicano a tutti i controlli di menu in cui il framework o la piattaforma dell'interfaccia utente Automazione interfaccia utente supporto per i tipi di controllo e i pattern di controllo.

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Pattern di controllo obbligatori](#required-control-patterns)
-   [Eventi obbligatori](#required-events)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

La tabella seguente illustra un controllo tipico e una visualizzazione contenuto dell'albero Automazione interfaccia utente che riguarda i controlli menu e descrive cosa può essere contenuto in ogni visualizzazione. Per altre informazioni sull'albero Automazione interfaccia utente, vedere panoramica Automazione interfaccia utente [albero](uiauto-treeoverview.md).




| Visualizzazione controlli | Visualizzazione contenuto | 
|--------------|--------------|
| <ul><li>Menu<ul><li>MenuItem (1 o molti)</li></ul><ul><li>Altri controlli (0 o molti)</li></ul></li></ul> | <ul><li>Menu<ul><li>MenuItem (1 o molti)</li></ul><ul><li>Altri controlli (0 o molti)</li></ul></li></ul> | 




 

I controlli menu vengono sempre visualizzati nella visualizzazione controlli e nella visualizzazione contenuto dell'Automazione interfaccia utente albero. I controlli menu dovrebbero essere visualizzati sotto il controllo a cui fanno riferimento le relative informazioni. Automazione interfaccia utente client possono restare in ascolto di [**\_ UIA MenuOpenedEventId**](uiauto-event-ids.md) per assicurarsi di ottenere in modo coerente le informazioni trasmesse dai controlli menu. I controlli menu di scelta rapida rappresentano un caso speciale. Possono essere visualizzati come elementi figlio del desktop o di una finestra dell'applicazione di primo livello.

Un controllo menu può contenere altri controlli, ad esempio controlli di modifica e caselle combinate, all'interno della relativa struttura. Questi controlli aggiuntivi corrispondono agli "altri controlli" elencati nella tabella precedente nelle visualizzazioni controllo e contenuto.

## <a name="relevant-properties"></a>Proprietà rilevanti

Nella tabella seguente sono elencate le Automazione interfaccia utente il cui valore o definizione è particolarmente rilevante per il tipo di controllo **Menu.** Per altre informazioni sulle Automazione interfaccia utente, vedere Recupero di proprietà [da Automazione interfaccia utente elementi](uiauto-propertiesforclients.md).



| Proprietà di automazione interfaccia utente                                                                                      | valore      | Note                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)           | **Menu**   |                                                                                                                                                                         |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md) | true       | Il controllo menu è sempre incluso nella visualizzazione contenuto dell'Automazione interfaccia utente albero.                                                                                      |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md) | true       | Il controllo menu è sempre incluso nella visualizzazione controlli dell'Automazione interfaccia utente albero.                                                                                      |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)               | NULL       | Non è prevista alcuna etichetta con un controllo menu standard.                                                                                                                    |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                         | Vedere le note. | Il controllo menu non richiede l'impostazione di una proprietà **Name** oppure può avere lo stesso nome del controllo associato, ad esempio una voce di menu che ha aperto il sottomenu. |



 

## <a name="required-control-patterns"></a>Pattern di controllo obbligatori

Non sono presenti pattern di controllo obbligatori per il tipo di controllo Menu.

## <a name="required-events"></a>Eventi obbligatori

I controlli menu devono generare [**l'evento \_ UIA MenuOpenedEventId**](uiauto-event-ids.md) quando vengono visualizzati sullo schermo. **L'evento \_ UIA MenuOpenedEventId** includerà il testo del controllo. [**L'evento \_ UIA MenuClosedEventId**](uiauto-event-ids.md) deve essere generato quando un menu scompare dalla schermata.

Nella tabella seguente sono elencati Automazione interfaccia utente eventi che i controlli menu devono supportare. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automazione interfaccia utente evento                                                                                                                   | Note                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**Interfaccia \_ utente Evento di modifica della proprietà BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md) |                                                                                                                            |
| [**Interfaccia \_ utente Evento di modifica della proprietà IsEnabledPropertyId.**](uiauto-automation-element-propids.md)                 | Se il controllo supporta la [**proprietà IsEnabled,**](uiauto-automation-element-propids.md) deve supportare questo evento.   |
| [**Interfaccia \_ utente Evento di modifica della proprietà IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)             | Se il controllo supporta la [**proprietà IsOffscreen,**](uiauto-automation-element-propids.md) deve supportare questo evento. |
| [**UIA \_ MenuClosedEventId**](uiauto-event-ids.md)                                                              |                                                                                                                            |
| [**UIA \_ MenuOpenedEventId**](uiauto-event-ids.md)                                                              |                                                                                                                            |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente](uiauto-controltypesoverview.md)
</dt> <dt>

[Cenni preliminari su automazione interfaccia utente](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




