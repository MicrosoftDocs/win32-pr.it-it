---
title: Tipo di controllo HeaderItem
description: In questo argomento vengono fornite informazioni sul supporto Automazione interfaccia utente Microsoft per il tipo di controllo HeaderItem.
ms.assetid: c70420d6-d9f3-47c8-a09f-35ed170f815f
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo HeaderItem
- Automazione interfaccia utente,Tipo di controllo HeaderItem
- Automazione interfaccia utente,struttura ad albero per il tipo di controllo HeaderItem
- Automazione interfaccia utente,properties per il tipo di controllo HeaderItem
- Automazione interfaccia utente,pattern di controllo per il tipo di controllo HeaderItem
- Automazione interfaccia utente,events per il tipo di controllo HeaderItem
- strutture ad albero, tipo di controllo HeaderItem
- proprietà, tipo di controllo HeaderItem
- pattern di controllo, tipo di controllo HeaderItem
- eventi, tipo di controllo HeaderItem
- supporto per il tipo di controllo HeaderItem
- Tipo di controllo HeaderItem
- tipi di controllo, struttura ad albero per il tipo di controllo HeaderItem
- tipi di controllo, pattern di controllo per il tipo di controllo HeaderItem
- tipi di controllo, supporto per HeaderItem
- tipi di controllo, HeaderItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6bbcd6d86e7401c3fa98d162e3aa273613dfd3a32705da891fc89d1f4ea003f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098211"
---
# <a name="headeritem-control-type"></a>Tipo di controllo HeaderItem

In questo argomento vengono fornite informazioni sul supporto Automazione interfaccia utente Microsoft per il **tipo di controllo HeaderItem.**

Il **tipo di controllo HeaderItem** fornisce un'etichetta visiva per una riga o una colonna di informazioni.

Le sezioni seguenti definiscono la struttura Automazione interfaccia utente struttura ad albero, le proprietà, i pattern di controllo e gli eventi per il **tipo di controllo HeaderItem.** I Automazione interfaccia utente si applicano a tutti i controlli elemento intestazione in cui il framework o la piattaforma dell'interfaccia utente si integra Automazione interfaccia utente per i tipi di controllo e i pattern di controllo.

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Pattern di controllo obbligatori](#required-control-patterns)
-   [Eventi obbligatori](#required-events)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

La tabella seguente illustra un controllo tipico e una visualizzazione contenuto dell'albero Automazione interfaccia utente relativo ai controlli elemento intestazione e descrive cosa può essere contenuto in ogni visualizzazione. Per altre informazioni sull'albero Automazione interfaccia utente, vedere panoramica [Automazione interfaccia utente albero di .](uiauto-treeoverview.md)



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
<li>HeaderItem</li>
</ul></td>
<td>(Non applicabile)</td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a>Proprietà rilevanti

La tabella seguente elenca le Automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per il **tipo di controllo HeaderItem.** Per altre informazioni sulle Automazione interfaccia utente, vedere [Recupero di proprietà da Automazione interfaccia utente elementi](uiauto-propertiesforclients.md).



| Proprietà di automazione interfaccia utente                                                                                              | Valore          | Note                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Vedere le note.     | Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata dell'Automazione interfaccia utente albero.                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vedere le note.     | Il rettangolo più esterno che contiene l'intero controllo.                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vedere le note.     | Supportata se è presente un rettangolo di delimitazione. Se non tutti i punti all'interno del rettangolo di delimitazione sono selezionabili e l'elemento esegue hit testing specializzati, eseguire l'override e fornire un punto selezionabile. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **HeaderItem** | Questo valore è uguale per tutti i framework dell'interfaccia utente.                                                                                                                                                        |
| [**\_IsContentElementPropertyId dell'interfaccia utente**](uiauto-automation-element-propids.md)         | FALSE          | Il controllo elemento intestazione non è incluso nella visualizzazione contenuto dell'Automazione interfaccia utente struttura ad albero.                                                                                                               |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | true           | Il controllo elemento intestazione è sempre incluso nella visualizzazione controlli dell'Automazione interfaccia utente struttura ad albero.                                                                                                            |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Vedere le note.     | Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.                                                                                                                            |
| [**UIA \_ ItemStatusPropertyId**](uiauto-automation-element-propids.md)                     | Vedere le note      | Questa proprietà fornisce informazioni per i tipi di ordinamento per l'elemento dell'intestazione.                                                                                                                               |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULL           | I controlli elemento intestazione non hanno un'etichetta di testo statico.                                                                                                                                                |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vedere le note.     | Stringa localizzata corrispondente al **tipo di controllo HeaderItem.** Il valore predefinito è "header item" per en-US o English (Stati Uniti).                                                          |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Vedere le note.     | Il controllo elemento intestazione è sempre associato a un'etichetta automatica.                                                                                                                                                     |



 

## <a name="required-control-patterns"></a>Pattern di controllo obbligatori

Nella tabella seguente sono elencati i Automazione interfaccia utente che devono essere supportati da tutti i controlli elemento intestazione. Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Pattern di controllo                                         | Supporto | Note                                                                                                                             |
|---------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)       | Dipende da | Implementare il [pattern di](uiauto-implementinginvoke.md) controllo Invoke se è possibile fare clic sul controllo elemento intestazione per ordinare i dati. |
| [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) | Dipende da | Implementare [il pattern di](uiauto-implementingtransform.md) controllo Transform se il controllo elemento intestazione può essere ridimensionato.            |



 

## <a name="required-events"></a>Eventi obbligatori

La tabella seguente elenca gli eventi Automazione interfaccia utente che i controlli elemento intestazione devono supportare. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automazione interfaccia utente eventi                                                                                                                   | Note                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**Interfaccia \_ utente Evento di modifica della proprietà BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md) |                                                                                                                            |
| [**\_ \_ InvokedEventId dell'interfaccia utente**](uiauto-event-ids.md)                                                     | Se il controllo supporta il pattern [di controllo Invoke,](uiauto-implementinginvoke.md) deve supportare questo evento.           |
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

 

 




