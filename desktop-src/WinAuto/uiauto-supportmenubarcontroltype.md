---
title: Tipo di controllo MenuBar
description: Questo argomento fornisce informazioni sul supporto microsoft Automazione interfaccia utente per il tipo di controllo MenuBar.
ms.assetid: e93a92ce-7c98-4e8f-8a6a-a365ccb705d6
keywords:
- Automazione interfaccia utente,supporto per il tipo di controllo MenuBar
- Automazione interfaccia utente,Tipo di controllo MenuBar
- Automazione interfaccia utente,struttura ad albero per il tipo di controllo MenuBar
- Automazione interfaccia utente,proprietà per il tipo di controllo MenuBar
- Automazione interfaccia utente,pattern di controllo per il tipo di controllo MenuBar
- Automazione interfaccia utente,eventi per il tipo di controllo MenuBar
- strutture ad albero, tipo di controllo MenuBar
- proprietà,Tipo di controllo MenuBar
- pattern di controllo, tipo di controllo MenuBar
- eventi, tipo di controllo MenuBar
- supporto per il tipo di controllo MenuBar
- Tipo di controllo MenuBar
- tipi di controllo, struttura ad albero per il tipo di controllo MenuBar
- tipi di controllo,pattern di controllo per il tipo di controllo MenuBar
- tipi di controllo, supporto per MenuBar
- tipi di controllo,MenuBar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 096dd2d48281c63a6006d679b8edacfc3607100574eb53325ae491ff1e011386
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119387801"
---
# <a name="menubar-control-type"></a>Tipo di controllo MenuBar

Questo argomento fornisce informazioni sul supporto di Microsoft Automazione interfaccia utente per il **tipo di controllo MenuBar.**

I controlli barra dei menu sono un esempio di controlli che implementano il **tipo di controllo MenuBar.** Le barre dei menu consentono agli utenti di attivare comandi e opzioni contenuti in un'applicazione.

Le sezioni seguenti definiscono la struttura ad Automazione interfaccia utente, le proprietà, i pattern di controllo e gli eventi necessari per il tipo di **controllo MenuBar.** I Automazione interfaccia utente si applicano a tutti i controlli barra dei menu in cui il framework o la piattaforma dell'interfaccia utente Automazione interfaccia utente supporto per i tipi di controllo e i pattern di controllo.

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Pattern di controllo obbligatori](#required-control-patterns)
-   [Eventi obbligatori](#required-events)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

La tabella seguente illustra un controllo tipico e una visualizzazione contenuto dell'albero Automazione interfaccia utente che riguarda i controlli barra dei menu e descrive cosa può essere contenuto in ogni visualizzazione. Per altre informazioni sull'albero Automazione interfaccia utente, vedere panoramica Automazione interfaccia utente [albero](uiauto-treeoverview.md).



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
<li>MenuBar
<ul>
<li>MenuItem (1 o più)</li>
<li>Altri controlli (0 o molti)</li>
</ul></li>
</ul></td>
<td><ul>
<li>Non applicabile
<ul>
<li>MenuItem (1 o più)</li>
<li>Altri controlli (0 o molti)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

Un controllo barra dei menu viene sempre visualizzato nella visualizzazione controlli, ma non nella visualizzazione contenuto perché in genere non trasmette informazioni significative all'utente finale(a meno che l'applicazione non contenga più di una barra dei menu).

Automazione interfaccia utente client possono restare in ascolto dell'evento [**\_ UIA MenuModeStartEventId**](uiauto-event-ids.md) per assicurarsi che siano informati in modo coerente quando l'interfaccia utente entra in modalità menu. Quando l'applicazione è in modalità menu, tutto l'input della tastiera può essere acquisito per la navigazione nei menu(ad esempio, la digitazione di 's' potrebbe richiamare il **menu** Salva invece di digitare il carattere nell'area client dell'applicazione). **L'evento UIA \_ MenuModeStartEventId** deve precedere il primo evento [**\_ UiA MenuOpenedEventId**](uiauto-event-ids.md) per garantire la coerenza logica. [**L'evento UIA \_ MenuModeEndEventId**](uiauto-event-ids.md) segue l'ultimo [**evento \_ UIA MenuClosedEventId.**](uiauto-event-ids.md) Facendo clic su una voce di menu è anche possibile attivare immediatamente l'evento **UIA \_ MenuModeStartEventId,** seguito da un evento **UIA \_ MenuOpenedEventId.**

Un controllo barra dei menu può contenere altri controlli, ad esempio controlli di modifica e caselle combinate, all'interno della relativa struttura. Questi controlli aggiuntivi corrispondono agli "altri controlli" elencati sopra nelle visualizzazioni controlli e contenuto.

## <a name="relevant-properties"></a>Proprietà rilevanti

Nella tabella seguente sono elencate le Automazione interfaccia utente il cui valore o definizione è particolarmente rilevante per il **tipo di controllo MenuBar.** Per altre informazioni sulle Automazione interfaccia utente, vedere Recupero di proprietà [da Automazione interfaccia utente elements](uiauto-propertiesforclients.md).



| Proprietà di automazione interfaccia utente                                                                                              | Valore       | Note                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AcceleratorKeyPropertyId**](uiauto-automation-element-propids.md)             | NULL        | Le barre dei menu in genere non dispongono di tasti di scelta rapida.                                                                                                                                                                                          |
| [**UIA \_ AccessKeyPropertyId**](uiauto-automation-element-propids.md)                       | "ALT"       | La pressione del tasto ALT dovrebbe in genere portare lo stato attivo sulla barra dei menu all'interno dell'applicazione.                                                                                                                                                  |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vedere le note.  | Il valore esposto da questa proprietà deve includere tutti i controlli contenuti.                                                                                                                                                 |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **MenuBar** |                                                                                                                                                                                                                                          |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | FALSE       | Il controllo barra dei menu non è incluso nella visualizzazione contenuto dell'Automazione interfaccia utente struttura ad albero.                                                                                                                                                      |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | true        | Il controllo barra dei menu è sempre incluso nella visualizzazione controlli dell'Automazione interfaccia utente albero.                                                                                                                                                   |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | true        | I controlli barra dei menu hanno lo stato attivabile perché i controlli che contengono possono prendere lo stato attivo.                                                                                                                                      |
| [**UIA \_ IsOffscreenPropertyId**](uiauto-automation-element-propids.md)                   | Vedere le note.  | Il valore di questa proprietà dipende dal fatto che il controllo sia visualizzabile o meno sullo schermo.                                                                                                                                                     |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULL        | I controlli barra dei menu in genere non hanno un'etichetta.                                                                                                                                                                                           |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vedere le note.  | Stringa localizzata corrispondente al **tipo di controllo MenuBar.** Il valore predefinito è "barra dei menu" per en-US o inglese (Stati Uniti).                                                                                                    |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Vedere le note.  | Il controllo barra dei menu non necessita di un nome a meno che un'applicazione non abbia più di una barra dei menu. Se in un'applicazione sono presenti più barre dei menu, usare questa proprietà per esporre nomi distinti, ad esempio "Formattazione" o "Struttura". |
| [**UIA \_ OrientationPropertyId**](uiauto-automation-element-propids.md)                   | Dipende da     | Questa proprietà espone l'orientamento orizzontale o verticale del controllo barra dei menu.                                                                                                                                                            |



 

## <a name="required-control-patterns"></a>Pattern di controllo obbligatori

Nella tabella seguente sono elencati i Automazione interfaccia utente di controllo necessari per essere supportati dai controlli barra dei menu. Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Pattern di controllo                                                   | Supporto | Note                                                                                                                                       |
|-------------------------------------------------------------------|---------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Dipende da | Se il controllo può essere espanso o compresso, deve implementare il [pattern di controllo ExpandCollapse.](uiauto-implementingexpandcollapse.md) |
| [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider)                     | Dipende da | Se il controllo può essere ancorato a parti diverse dello schermo, deve implementare il [pattern di controllo Dock.](uiauto-implementingdock.md)   |
| [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider)           | Dipende da | Se il controllo può essere ridimensionato, ruotato o spostato, deve implementare il [pattern di controllo Trasforma.](uiauto-implementingtransform.md)      |



 

## <a name="required-events"></a>Eventi obbligatori

Nella tabella seguente sono elencati Automazione interfaccia utente eventi che i controlli barra dei menu devono supportare. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automazione interfaccia utente evento                                                                                                                                                | Note                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                                   |                                                                                                                                  |
| [**Interfaccia \_ utente Evento di modifica della proprietà BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md)                              |                                                                                                                                  |
| [**Interfaccia \_ utente Evento di modifica della proprietà ExpandCollapseExpandCollapseStatePropertyId.**](uiauto-control-pattern-propids.md) | Se il controllo supporta il [pattern di controllo ExpandCollapse,](uiauto-implementingexpandcollapse.md) deve supportare questo evento. |
| [**Interfaccia \_ utente Evento di modifica della proprietà IsEnabledPropertyId.**](uiauto-automation-element-propids.md)                                              | Se il controllo supporta la [**proprietà IsEnabled,**](uiauto-automation-element-propids.md) deve supportare questo evento.         |
| [**Interfaccia \_ utente Evento di modifica della proprietà IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)                                          | Se il controllo supporta la [**proprietà IsOffscreen,**](uiauto-automation-element-propids.md) deve supportare questo evento.       |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                               |                                                                                                                                  |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente](uiauto-controltypesoverview.md)
</dt> <dt>

[Cenni preliminari su automazione interfaccia utente](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




