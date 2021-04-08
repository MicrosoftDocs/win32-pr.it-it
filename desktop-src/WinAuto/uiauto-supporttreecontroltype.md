---
title: Tipo di controllo Tree
description: In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo Tree.
ms.assetid: 0fa8f308-7815-4561-a1ce-c5f5582861da
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo Tree
- Automazione interfaccia utente, tipo di controllo Tree
- Automazione interfaccia utente, struttura ad albero per il tipo di controllo Tree
- Automazione interfaccia utente, proprietà per il tipo di controllo Tree
- Automazione interfaccia utente, pattern di controllo per il tipo di controllo Tree
- Automazione interfaccia utente, eventi per il tipo di controllo Tree
- strutture ad albero, tipo di controllo Tree
- Proprietà, tipo di controllo Tree
- pattern di controllo, tipo di controllo Tree
- eventi, tipo di controllo Tree
- supporto per il tipo di controllo Tree
- Tree (tipo di controllo)
- tipi di controllo, struttura ad albero per il tipo di controllo Tree
- tipi di controllo, pattern di controllo per il tipo di controllo Tree
- tipi di controllo, supporto per l'albero
- tipi di controllo, struttura ad albero
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4679af32f974cd1611cbd31c71e66db62631391
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047182"
---
# <a name="tree-control-type"></a>Tipo di controllo Tree

In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo **Tree** .

Il tipo di controllo **Tree** viene usato per i contenitori il cui contenuto ha una rilevanza come gerarchia di nodi, come nel caso della modalità di visualizzazione di file e cartelle nel riquadro sinistro di Esplora risorse. Ciascun nodo può potenzialmente contenere altri nodi, denominati nodi figlio. I nodi padre, ovvero i nodi contenenti nodi figlio, possono essere visualizzati in formato espanso o compresso. Il controllo di visualizzazione ad albero di Windows (identificato da [**WC \_ TreeView**](/windows/desktop/Controls/common-control-window-classes)) è un esempio di un controllo che appartiene al tipo di controllo **Tree** .

Nelle sezioni seguenti vengono definiti la struttura ad albero, le proprietà, i pattern di controllo e gli eventi di automazione interfaccia utente necessari per il tipo di controllo **Tree** . I requisiti di automazione interfaccia utente si applicano a tutti i controlli elemento della struttura ad albero in cui la piattaforma/Framework dell'interfaccia utente integra il supporto di automazione interfaccia utente per i tipi di controllo e

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Pattern di controllo obbligatori](#required-control-patterns)
-   [Eventi obbligatori](#required-events)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

Nella tabella seguente viene illustrata una tipica visualizzazione del controllo e del contenuto dell'albero di automazione interfaccia utente che riguarda i controlli struttura ad albero e viene descritto il possibile contenuto di ogni visualizzazione. Per altre informazioni sull'albero di automazione interfaccia utente, vedere [Cenni preliminari sull'albero di automazione interfaccia utente](uiauto-treeoverview.md).



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
<li>Albero
<ul>
<li>DataItem (0 o più)</li>
<li>TreeItem (0 o più)
<ul>
<li>TreeItem (0 o più)
<ul>
<li>...</li>
</ul></li>
</ul></li>
<li>ScrollBar (0, 1, 2)</li>
</ul></li>
</ul></td>
<td><ul>
<li>Albero
<ul>
<li>DataItem (0 o più)</li>
<li>TreeItem (0 o più)
<ul>
<li>TreeItem (0 o più)
<ul>
<li>...</li>
</ul></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

La visualizzazione controlli dell'albero di automazione interfaccia utente è costituita da:

-   Zero di molti elementi all'interno del contenitore (gli elementi possono essere basati sui tipi di controllo [TreeItem](uiauto-supporttreeitemcontroltype.md) o [DataItem](uiauto-supportdataitemcontroltype.md) ).
-   Zero, uno o due controlli barra di scorrimento

La visualizzazione contenuto dell'albero di automazione interfaccia utente è costituita da zero o molti elementi all'interno del contenitore (gli elementi possono essere basati sui tipi di controllo [TreeItem](uiauto-supporttreeitemcontroltype.md) o [DataItem](uiauto-supportdataitemcontroltype.md) ).

## <a name="relevant-properties"></a>Proprietà rilevanti

La tabella seguente elenca le proprietà di automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per il tipo di controllo **Tree** . Per altre informazioni sulle proprietà di automazione interfaccia utente, vedere [recupero di proprietà da elementi di automazione interfaccia utente](uiauto-propertiesforclients.md).



| Proprietà di automazione interfaccia utente                                                                                              | Valore      | Note                                                                                                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_AUTOMATIONIDPROPERTYID UIA**](uiauto-automation-element-propids.md)                 | Vedere le note. | Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata della struttura ad albero di automazione interfaccia utente.                                                                                                                                                                               |
| [**\_BOUNDINGRECTANGLEPROPERTYID UIA**](uiauto-automation-element-propids.md)       | Vedere le note. | Il rettangolo più esterno che contiene l'intero controllo.                                                                                                                                                                                                                                   |
| [**\_CLICKABLEPOINTPROPERTYID UIA**](uiauto-automation-element-propids.md)             | Vedere le note. | I controlli Tree dispongono di un punto selezionabile che determina la ricezione dello stato attivo nell'albero o in uno degli elementi nel contenitore della struttura. Un controllo albero può avere un punto selezionabile solo se è possibile fare clic su una posizione nell'albero senza causare la selezione di un elemento o ricevere lo stato attivo. |
| [**\_CONTROLTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md)                   | **Albero**   | Questo valore è uguale per tutti i framework dell'interfaccia utente.                                                                                                                                                                                                                                              |
| [**\_ISCONTENTELEMENTPROPERTYID UIA**](uiauto-automation-element-propids.md)         | true       | Il controllo albero viene sempre incluso nella visualizzazione contenuto dell'albero di automazione interfaccia utente.                                                                                                                                                                                                         |
| [**\_ISCONTROLELEMENTPROPERTYID UIA**](uiauto-automation-element-propids.md)         | true       | Il controllo albero viene sempre incluso nella visualizzazione controlli dell'albero di automazione interfaccia utente.                                                                                                                                                                                                         |
| [**\_ISKEYBOARDFOCUSABLEPROPERTYID UIA**](uiauto-automation-element-propids.md)   | Vedere le note. | Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.                                                                                                                                                                                                                  |
| [**\_LABELEDBYPROPERTYID UIA**](uiauto-automation-element-propids.md)                       | Vedere le note. | Se al controllo struttura ad albero è associata un'etichetta, questa proprietà restituisce un puntatore [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) per l'etichetta. In caso contrario, la proprietà restituisce un riferimento null.                                                                          |
| [**\_LOCALIZEDCONTROLTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md) | Vedere le note. | Stringa localizzata corrispondente al tipo di controllo **Tree** . Il valore predefinito è "Tree" per en-US o inglese (Stati Uniti).                                                                                                                                                             |
| [**\_NAMEPROPERTYID UIA**](uiauto-automation-element-propids.md)                                 | Vedere le note. | Il valore della proprietà name di un controllo struttura in genere deriva dal testo dell'etichetta del controllo. Se non è presente alcuna etichetta di testo, è necessario specificare un valore per questa proprietà.                                                                                                                        |



 

## <a name="required-control-patterns"></a>Pattern di controllo obbligatori

La tabella seguente elenca i pattern di controllo di automazione interfaccia utente che devono essere supportati da tutti i controlli struttura ad albero. Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Pattern di controllo/proprietà del pattern                                             | Supporto/valore | Note                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)                            | Dipende da       | Implementare il pattern di controllo [Scroll](uiauto-implementingscroll.md) se è possibile scorrere gli elementi nel contenitore della struttura ad albero.                                                                                                                 |
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)                      | Dipende da       | I controlli struttura ad albero contenenti un set di elementi selezionabili devono implementare il pattern di controllo [Selection](uiauto-implementingselection.md) . Non deve essere implementato se la selezione di un elemento non trasmette informazioni significative all'utente. |
| [**CanSelectMultiple**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple)     | Vedere le note.    | Implementare questa proprietà se il controllo struttura supporta la selezione multipla (la maggior parte dei controlli struttura non supporta la selezione multipla).                                                                                                       |
| [**IsSelectionRequired**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired) | Vedere le note.    | Il valore di questa proprietà viene esposta quando il controllo richiede la selezione di un elemento.                                                                                                                                               |



 

## <a name="required-events"></a>Eventi obbligatori

La tabella seguente elenca gli eventi di automazione interfaccia utente che devono essere supportati da tutti i controlli struttura ad albero. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



| Evento di automazione interfaccia utente                                                                                                                                        | Note                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**\_AUTOMATIONFOCUSCHANGEDEVENTID UIA**](uiauto-event-ids.md)                                                           |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà BoundingRectanglePropertyId.                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsEnabledPropertyId.                                      | Se il controllo supporta la proprietà [**IsEnabled**](uiauto-automation-element-propids.md) , deve supportare questo evento.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsOffscreenPropertyId.                                  | Se il controllo supporta la proprietà [**IsOffscreen**](uiauto-automation-element-propids.md) , deve supportare questo evento. |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ScrollHorizontallyScrollablePropertyId.   | Se il controllo supporta il pattern di controllo [Scroll](uiauto-implementingscroll.md) , deve supportare questo evento.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ScrollHorizontalScrollPercentPropertyId. | Se il controllo supporta il pattern di controllo [Scroll](uiauto-implementingscroll.md) , deve supportare questo evento.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ScrollHorizontalViewSizePropertyId.           | Se il controllo supporta il pattern di controllo [Scroll](uiauto-implementingscroll.md) , deve supportare questo evento.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ScrollVerticalScrollPercentPropertyId.     | Se il controllo supporta il pattern di controllo [Scroll](uiauto-implementingscroll.md) , deve supportare questo evento.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ScrollVerticallyScrollablePropertyId.       | Se il controllo supporta il pattern di controllo [Scroll](uiauto-implementingscroll.md) , deve supportare questo evento.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ScrollVerticalViewSizePropertyId.               | Se il controllo supporta il pattern di controllo [Scroll](uiauto-implementingscroll.md) , deve supportare questo evento.           |
| [**\_InvalidatedEventId selezione \_ UIA**](uiauto-event-ids.md)                                                            | Se il controllo supporta il pattern di controllo [Selection](uiauto-implementingselection.md) , deve supportare questo evento.     |
| [**\_STRUCTURECHANGEDEVENTID UIA**](uiauto-event-ids.md)                                                                       |                                                                                                                            |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente](uiauto-controltypesoverview.md)
</dt> <dt>

[Cenni preliminari su automazione interfaccia utente](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 