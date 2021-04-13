---
title: Tipo di controllo List
description: In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo elenco.
ms.assetid: e4cde080-32d1-4150-a6be-8bd750e972c9
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo List
- Automazione interfaccia utente, tipo di controllo elenco
- Automazione interfaccia utente, struttura ad albero per il tipo di controllo List
- Automazione interfaccia utente, proprietà per il tipo di controllo List
- Automazione interfaccia utente, pattern di controllo per il tipo di controllo List
- Automazione interfaccia utente, eventi per il tipo di controllo elenco
- strutture ad albero, tipo di controllo List
- Proprietà, tipo di controllo List
- pattern di controllo, tipo di controllo List
- eventi, tipo di controllo List
- supporto per il tipo di controllo List
- List (tipo di controllo)
- tipi di controllo, struttura ad albero per il tipo di controllo List
- tipi di controllo, pattern di controllo per il tipo di controllo List
- tipi di controllo, supporto per l'elenco
- tipi di controllo, elenco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8a493418750bff1932fe933340b3eb2cb05829e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395851"
---
# <a name="list-control-type"></a>Tipo di controllo List

In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo **elenco** .

Il tipo di controllo **List** fornisce un modo per organizzare un gruppo o gruppi di elementi flat e consente a un utente di selezionare uno o più di tali elementi. Il tipo di controllo **List** presenta una restrizione di tipo Loose sui tipi di elementi figlio che può contenere. I provider di automazione interfaccia utente sono quindi in grado di supportare un elemento noto per i contenitori di selezione.

Nelle sezioni seguenti vengono definiti la struttura ad albero, le proprietà, i pattern di controllo e gli eventi di automazione interfaccia utente necessari per il tipo di controllo **elenco** . I requisiti di automazione interfaccia utente si applicano a tutti i controlli elenco in cui la piattaforma/Framework dell'interfaccia utente integra il supporto di automazione interfaccia utente per tipi di controllo e pattern di controllo

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Pattern di controllo e proprietà obbligatori](#required-control-patterns-and-properties)
-   [Eventi obbligatori](#required-events)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

Nella tabella seguente viene illustrata una tipica visualizzazione del controllo e del contenuto dell'albero di automazione interfaccia utente relativo ai controlli elenco e viene descritto il possibile contenuto di ogni visualizzazione. Per altre informazioni sull'albero di automazione interfaccia utente, vedere [Cenni preliminari sull'albero di automazione interfaccia utente](uiauto-treeoverview.md).



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
<td>Contiene elementi che corrispondono ai controlli.</td>
<td>Rimuove le informazioni ridondanti dall'albero in modo che le tecnologie assistive funzionino con il set di informazioni più piccolo significativo per l'utente finale.</td>
</tr>
<tr class="even">
<td><ul>
<li>Elenco
<ul>
<li>DataItem (0 o più)</li>
<li>ListItem (0 o più)</li>
<li>Group (0 o più)</li>
<li>ScrollBar (0, 1 o 2)</li>
</ul></li>
</ul></td>
<td><ul>
<li>Elenco
<ul>
<li>DataItem (0 o più)</li>
<li>ListItem (0 o più)</li>
<li>Group (0 o più)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

La visualizzazione controlli per un controllo che implementa il tipo di controllo elenco (ad esempio un controllo elenco) contiene:

-   Zero o più elementi nel controllo elenco (gli elementi possono essere basati sui tipi di controllo [ListItem](uiauto-supportlistitemcontroltype.md) o [DataItem](uiauto-supportdataitemcontroltype.md) )
-   Zero o più controlli gruppo in un controllo elenco
-   Zero, uno o due controlli barra di scorrimento

La visualizzazione contenuto di un controllo che implementa il tipo di controllo elenco (ad esempio un controllo elenco) contiene:

-   Zero o più elementi nel controllo elenco (gli elementi possono essere basati sui tipi di controllo [ListItem](uiauto-supportlistitemcontroltype.md) o [DataItem](uiauto-supportdataitemcontroltype.md) )
-   Zero o più gruppi nel controllo elenco

Un controllo elenco non deve contenere elementi con una relazione gerarchica diversa dal raggruppamento. Se gli elementi hanno figli nell'albero di automazione interfaccia utente, il contenitore elenco deve essere basato sul tipo di controllo [Tree](uiauto-supporttreecontroltype.md) .

Gli elementi selezionabili nel controllo elenco saranno disponibili dai discendenti nell'albero di automazione interfaccia utente del controllo elenco. Tutti gli elementi nel controllo elenco devono appartenere allo stesso gruppo di selezione. Gli elementi selezionabili nell'elenco devono essere esposti come tipi di controllo [ListItem](uiauto-supportlistitemcontroltype.md) (anziché [DataItem](uiauto-supportdataitemcontroltype.md)).

## <a name="relevant-properties"></a>Proprietà rilevanti

La tabella seguente elenca le proprietà di automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per il tipo di controllo **elenco** . Per altre informazioni sulle proprietà di automazione interfaccia utente, vedere [recupero di proprietà da elementi di automazione interfaccia utente](uiauto-propertiesforclients.md).



| Proprietà di automazione interfaccia utente                                                                                              | Valore      | Note                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_AUTOMATIONIDPROPERTYID UIA**](uiauto-automation-element-propids.md)                 | Vedere le note. | Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata della struttura ad albero di automazione interfaccia utente.                                                                                                                                                                                                                                                                                                                                                         |
| [**\_BOUNDINGRECTANGLEPROPERTYID UIA**](uiauto-automation-element-propids.md)       | Vedere le note. | Il rettangolo più esterno che contiene l'intero controllo.                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**\_CLICKABLEPOINTPROPERTYID UIA**](uiauto-automation-element-propids.md)             | Vedere le note. | Se il controllo elenco ha un punto selezionabile, ovvero un punto su cui è possibile fare clic per fare in modo che l'elenco abbia lo stato attivo, tale punto deve essere esposto tramite questa proprietà. Se il valore della proprietà [**\_ IsOffscreenPropertyId di UIA**](uiauto-automation-element-propids.md) è **true**, il tentativo di recuperare questa proprietà comporta l'errore [**\_ \_ NOCLICKABLEPOINT di UIA E**](uiauto-error-codes.md) .                      |
| [**\_CONTROLTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md)                   | **Elenco**   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**\_HELPTEXTPROPERTYID UIA**](uiauto-automation-element-propids.md)                         | Vedere le note. | Il testo della Guida per i controlli elenco deve illustrare il motivo per cui viene chiesto all'utente di effettuare una selezione da un elenco di opzioni. Ad esempio, "La selezione di un elemento dall'elenco consente di impostare la risoluzione per il monitor".                                                                                                                                                                                                                                                |
| [**\_ISCONTENTELEMENTPROPERTYID UIA**](uiauto-automation-element-propids.md)         | **TRUE**   | Il controllo elenco è sempre incluso nella visualizzazione contenuto dell'albero di automazione interfaccia utente.                                                                                                                                                                                                                                                                                                                                                                                   |
| [**\_ISCONTROLELEMENTPROPERTYID UIA**](uiauto-automation-element-propids.md)         | **TRUE**   | Il controllo elenco è sempre incluso nella visualizzazione controlli dell'albero di automazione interfaccia utente.                                                                                                                                                                                                                                                                                                                                                                                   |
| [**\_ISKEYBOARDFOCUSABLEPROPERTYID UIA**](uiauto-automation-element-propids.md)   | Vedere le note. | Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.                                                                                                                                                                                                                                                                                                                                                                                            |
| [**\_LABELEDBYPROPERTYID UIA**](uiauto-automation-element-propids.md)                       | Vedere le note. | Se è presente un'etichetta di testo statico, questa proprietà deve esporre un riferimento a tale controllo.                                                                                                                                                                                                                                                                                                                                                                          |
| [**\_LOCALIZEDCONTROLTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md) | Vedere le note. | Stringa localizzata corrispondente al tipo di controllo **elenco** . Il valore predefinito è "list" per en-US o inglese (Stati Uniti).                                                                                                                                                                                                                                                                                                                                       |
| [**\_NAMEPROPERTYID UIA**](uiauto-automation-element-propids.md)                                 | Vedere le note. | Il valore della proprietà **Name** di un controllo elenco deve fornire la categoria di opzioni da cui l'utente deve effettuare la selezione. Questa proprietà deriva in genere il nome da un'etichetta di testo statico. Se non è presente un'etichetta di testo statico, lo sviluppatore dell'applicazione deve esporre un valore per la proprietà **Name** .<br/> L'unico caso in cui questa proprietà non è obbligatoria per i controlli elenco è quando si usa il controllo all'interno del sottoalbero di un altro controllo.<br/> |



 

## <a name="required-control-patterns-and-properties"></a>Pattern di controllo e proprietà obbligatori

La tabella seguente elenca i pattern di controllo di automazione interfaccia utente che devono essere supportati da tutti i controlli elenco. Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Pattern di controllo/proprietà del pattern                                             | Supporto/valore | Note                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider)                                | Dipende da       | Implementare il pattern di controllo [Grid](uiauto-implementinggrid.md) quando lo spostamento nella griglia deve essere disponibile in base all'elemento.                                                                                                                                                                                                                                           |
| [**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider)                | Dipende da       | Implementare il pattern di controllo [MultipleView](uiauto-implementingmultipleview.md) se il controllo può supportare più visualizzazioni degli elementi nel contenitore.                                                                                                                                                                                                                       |
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)                            | Dipende da       | Implementare il pattern di controllo [Scroll](uiauto-implementingscroll.md) se gli elementi nel contenitore sono scorrevoli.                                                                                                                                                                                                                                                                  |
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)                      | Dipende da       | Se un controllo supporta il tipo di controllo elenco che supporta la selezione, il controllo deve implementare il pattern di controllo [Selection](uiauto-implementingselection.md) quando viene mantenuto uno stato di selezione tra gli elementi contenuti nel controllo. Se gli elementi all'interno del controllo non sono selezionabili, è possibile usare il tipo di controllo [gruppo](uiauto-supportgroupcontroltype.md) . |
| [**CanSelectMultiple**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple)     | Dipende da       | I controlli elenco possono essere contenitori per una o più selezioni.                                                                                                                                                                                                                                                                                                                    |
| [**IsSelectionRequired**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired) | Dipende da       | Nei controlli elenco non è necessario che un elemento sia sempre selezionato.                                                                                                                                                                                                                                                                                                                    |
| [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider)                              | Mai         | Il pattern di controllo [Table](uiauto-implementingtable.md) non è mai supportato per il tipo di controllo **List** . Se il controllo deve supportare questo pattern di controllo, il controllo deve essere basato sul tipo di controllo [DataGrid](uiauto-supportdatagridcontroltype.md) .                                                                                                             |



 

## <a name="required-events"></a>Eventi obbligatori

La tabella seguente elenca gli eventi di automazione interfaccia utente necessari per supportare i controlli elenco. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



| Evento di automazione interfaccia utente                                                                                                                                        | Note                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**\_AUTOMATIONFOCUSCHANGEDEVENTID UIA**](uiauto-event-ids.md)                                                           |                                                                                                                              |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà BoundingRectanglePropertyId.                      |                                                                                                                              |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsEnabledPropertyId.                                      | Se il controllo supporta la proprietà [**IsEnabled**](uiauto-automation-element-propids.md) , deve supportare questo evento.     |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsOffscreenPropertyId.                                  | Se il controllo supporta la proprietà [**IsOffscreen**](uiauto-automation-element-propids.md) , deve supportare questo evento.   |
| [**\_LAYOUTINVALIDATEDEVENTID UIA**](uiauto-event-ids.md)                                                                     | Se il layout degli elementi figlio può essere modificato, il controllo deve supportare questo evento.                                            |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà MultipleViewCurrentViewPropertyId.             | Se il controllo supporta il pattern di controllo [MultipleView](uiauto-implementingmultipleview.md) , deve supportare questo evento. |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ScrollHorizontallyScrollablePropertyId.   | Se il controllo supporta il pattern di controllo [Scroll](uiauto-implementingscroll.md) , deve supportare questo evento.             |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ScrollHorizontalScrollPercentPropertyId. | Se il controllo supporta il pattern di controllo [Scroll](uiauto-implementingscroll.md) , deve supportare questo evento.             |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ScrollHorizontalViewSizePropertyId.           | Se il controllo supporta il pattern di controllo [Scroll](uiauto-implementingscroll.md) , deve supportare questo evento.             |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ScrollVerticalScrollPercentPropertyId.     | Se il controllo supporta il pattern di controllo [Scroll](uiauto-implementingscroll.md) , deve supportare questo evento.             |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ScrollVerticallyScrollablePropertyId.       | Se il controllo supporta il pattern di controllo [Scroll](uiauto-implementingscroll.md) , deve supportare questo evento.             |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ScrollVerticalViewSizePropertyId.               | Se il controllo supporta il pattern di controllo [Scroll](uiauto-implementingscroll.md) , deve supportare questo evento.             |
| [**\_InvalidatedEventId selezione \_ UIA**](uiauto-event-ids.md)                                                            | Se il controllo supporta il pattern di controllo [Selection](uiauto-implementingselection.md) , deve supportare questo evento.       |
| [**\_STRUCTURECHANGEDEVENTID UIA**](uiauto-event-ids.md)                                                                       |                                                                                                                              |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente](uiauto-controltypesoverview.md)
</dt> <dt>

[Cenni preliminari su automazione interfaccia utente](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 





