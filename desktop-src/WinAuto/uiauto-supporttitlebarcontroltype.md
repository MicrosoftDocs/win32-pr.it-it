---
title: Tipo di controllo TitleBar
description: Questo argomento fornisce informazioni sul supporto di Microsoft Automazione interfaccia utente per il tipo di controllo TitleBar. Un controllo barra del titolo rappresenta una barra del titolo o una barra del titolo in una finestra.
ms.assetid: dc707198-ceb6-4fbf-ace4-8fec88c92b98
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo TitleBar
- Automazione interfaccia utente, tipo di controllo TitleBar
- Automazione interfaccia utente struttura ad albero per il tipo di controllo TitleBar
- Automazione interfaccia utente,proprietà per il tipo di controllo TitleBar
- Automazione interfaccia utente,pattern di controllo per il tipo di controllo TitleBar
- Automazione interfaccia utente,eventi per il tipo di controllo TitleBar
- strutture ad albero, tipo di controllo TitleBar
- proprietà, tipo di controllo TitleBar
- pattern di controllo, tipo di controllo TitleBar
- eventi, tipo di controllo TitleBar
- supporto per il tipo di controllo TitleBar
- Tipo di controllo TitleBar
- tipi di controllo, struttura ad albero per il tipo di controllo TitleBar
- tipi di controllo, pattern di controllo per il tipo di controllo TitleBar
- tipi di controllo, supporto per TitleBar
- tipi di controllo, TitleBar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ee83d3fb61b58bf627a424ec9fbe2c230968c07e8ae000f5af39d1682c3ddca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119570421"
---
# <a name="titlebar-control-type"></a>Tipo di controllo TitleBar

Questo argomento fornisce informazioni sul supporto di Microsoft Automazione interfaccia utente per il **tipo di controllo TitleBar.** Un controllo barra del titolo rappresenta una barra del titolo o una barra del titolo in una finestra.

Le sezioni seguenti definiscono la struttura ad Automazione interfaccia utente struttura ad albero, le proprietà, i pattern di controllo e gli eventi per il **tipo di controllo TitleBar.** I Automazione interfaccia utente si applicano a tutti i controlli barra del titolo in cui il framework o la piattaforma dell'interfaccia utente si integra Automazione interfaccia utente per i tipi di controllo e i pattern di controllo.

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Pattern di controllo obbligatori](#required-control-patterns)
-   [Eventi obbligatori](#required-events)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

La tabella seguente illustra un controllo tipico e una visualizzazione contenuto dell'albero Automazione interfaccia utente relativo ai controlli barra del titolo e descrive gli elementi che possono essere contenuti in ogni visualizzazione. Per altre informazioni sull'albero Automazione interfaccia utente, vedere panoramica Automazione interfaccia utente [albero.](uiauto-treeoverview.md)



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
<li>TitleBar
<ul>
<li>Menu (0 o 1)</li>
<li>Button (0 o più)</li>
</ul></li>
</ul></td>
<td>(Non applicabile; il controllo barra del titolo non ha contenuto)</td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a>Proprietà rilevanti

La tabella seguente elenca le proprietà Automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per il **tipo di controllo TitleBar.** Per altre informazioni sulle Automazione interfaccia utente, vedere [Recupero di proprietà da Automazione interfaccia utente elementi](uiauto-propertiesforclients.md).



| Proprietà di automazione interfaccia utente                                                                                              | Valore        | Note                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Vedere le note.   | Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata dell'Automazione interfaccia utente albero.                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vedere le note.   | Il valore esposto da questa proprietà deve includere tutti i controlli contenuti.                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vedere le note.   | Supportata se è presente un rettangolo di delimitazione. Se non tutti i punti all'interno del rettangolo di delimitazione sono selezionabili e l'elemento esegue hit testing specializzati, eseguire l'override e fornire un punto selezionabile. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Titlebar** | Questo valore è uguale per tutti i framework dell'interfaccia utente.                                                                                                                                                        |
| [**IsContentElementPropertyId dell'interfaccia \_ utente**](uiauto-automation-element-propids.md)         | FALSE        | Il controllo barra del titolo non viene mai incluso nella visualizzazione contenuto dell'Automazione interfaccia utente struttura ad albero.                                                                                                               |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | true         | Il controllo barra del titolo è sempre incluso nella visualizzazione controlli dell'Automazione interfaccia utente albero.                                                                                                              |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | FALSE        | Un controllo barra del titolo non ha mai lo stato attivo della tastiera.                                                                                                                                                        |
| [**UIA \_ IsOffscreenPropertyId**](uiauto-automation-element-propids.md)                   | Dipende da      | Un controllo barra del titolo restituisce un valore a seconda che sia visibile sullo schermo.                                                                                                                |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Vedere le note.   | Un controllo barra del titolo in genere non ha un'etichetta.                                                                                                                                                 |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vedere le note.   | Stringa localizzata corrispondente al tipo di controllo TitleBar. Il valore predefinito è "title bar" per en-US o English (Stati Uniti).                                                                  |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | ""           | Una barra del titolo non è contenuto. Le informazioni testuali vengono esposte in base al nome della finestra padre.                                                                                                     |



 

## <a name="required-control-patterns"></a>Pattern di controllo obbligatori

Il **tipo di controllo TitleBar** non è necessario per supportare pattern di controllo. La relativa funzionalità viene esposta tramite il pattern di controllo [Window](uiauto-implementingwindow.md) nel [tipo di](uiauto-supportwindowcontroltype.md) controllo Window.

## <a name="required-events"></a>Eventi obbligatori

La tabella seguente elenca gli eventi Automazione interfaccia utente che i controlli barra del titolo devono supportare. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automazione interfaccia utente eventi                                                                                                                   | Note                                                                                                                      |
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

 

 




