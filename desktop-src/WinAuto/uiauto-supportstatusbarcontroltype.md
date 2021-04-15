---
title: Tipo di controllo StatusBar
description: In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo StatusBar.
ms.assetid: a28df0a1-95a8-4941-a00d-1f5570589626
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo StatusBar
- Automazione interfaccia utente, tipo di controllo StatusBar
- Automazione interfaccia utente, struttura ad albero per il tipo di controllo StatusBar
- Automazione interfaccia utente, proprietà per il tipo di controllo StatusBar
- Automazione interfaccia utente, pattern di controllo per il tipo di controllo StatusBar
- Automazione interfaccia utente, eventi per il tipo di controllo StatusBar
- strutture ad albero, tipo di controllo StatusBar
- Proprietà, tipo di controllo StatusBar
- pattern di controllo, tipo di controllo StatusBar
- eventi, tipo di controllo StatusBar
- supporto per il tipo di controllo StatusBar
- StatusBar (tipo di controllo)
- tipi di controllo, struttura ad albero per il tipo di controllo StatusBar
- tipi di controllo, pattern di controllo per il tipo di controllo StatusBar
- tipi di controllo, supporto per StatusBar
- tipi di controllo, StatusBar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65ace64d34429a6d381dfdef2d99d82a3693fca2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331103"
---
# <a name="statusbar-control-type"></a>Tipo di controllo StatusBar

In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo **StatusBar** .

In un controllo barra di stato sono in genere presenti informazioni su un oggetto visualizzato in una finestra di un'applicazione, i componenti dell'oggetto o informazioni contestuali collegate alle operazioni di tale oggetto all'interno dell'applicazione.

Nelle sezioni seguenti vengono definiti la struttura ad albero, le proprietà, i pattern di controllo e gli eventi di automazione interfaccia utente necessari per il tipo di controllo **StatusBar** . I requisiti di automazione interfaccia utente si applicano a tutti i controlli barra di stato in cui la piattaforma/Framework dell'interfaccia utente integra il supporto di automazione interfaccia utente per tipi di controllo e pattern di controllo

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Pattern di controllo obbligatori](#required-control-patterns)
-   [Eventi obbligatori](#required-events)
-   [Osservazioni:](#remarks)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

Nella tabella seguente viene illustrata una tipica visualizzazione del controllo e del contenuto dell'albero di automazione interfaccia utente relativo ai controlli barra di stato e viene descritto il possibile contenuto di ogni visualizzazione. Per altre informazioni sull'albero di automazione interfaccia utente, vedere [Cenni preliminari sull'albero di automazione interfaccia utente](uiauto-treeoverview.md).



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
<li>StatusBar
<ul>
<li>Edit (0 o più)</li>
<li>ProgressBar (0 o più)</li>
<li>Image (0 o più)</li>
<li>Button (0 o più)</li>
</ul></li>
</ul></td>
<td><ul>
<li>StatusBar
<ul>
<li>Edit (0 o più)</li>
<li>ProgressBar (0 o più)</li>
<li>Image (0 o più)</li>
<li>Button (0 o più)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a>Proprietà rilevanti

La tabella seguente elenca le proprietà di automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per i controlli barra di stato. Per altre informazioni sulle proprietà di automazione interfaccia utente, vedere [recupero di proprietà da elementi di automazione interfaccia utente](uiauto-propertiesforclients.md).



| Proprietà di automazione interfaccia utente                                                                                              | Valore         | Note                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_AUTOMATIONIDPROPERTYID UIA**](uiauto-automation-element-propids.md)                 | Vedere le note.    | Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata della struttura ad albero di automazione interfaccia utente.                                                                                                        |
| [**\_BOUNDINGRECTANGLEPROPERTYID UIA**](uiauto-automation-element-propids.md)       | Vedere le note.    | Il rettangolo di delimitazione di una barra di stato deve includere tutti i controlli in esso contenuti.                                                                                                                      |
| [**\_CLICKABLEPOINTPROPERTYID UIA**](uiauto-automation-element-propids.md)             | Vedere le note.    | Supportata se è presente un rettangolo di delimitazione. Se sono presenti aree all'interno del rettangolo di delimitazione che non sono selezionabili e l'elemento esegue un hit testing specializzato, eseguire l'override di questo e fornire un punto selezionabile. |
| [**\_CONTROLTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md)                   | **StatusBar** |                                                                                                                                                                                                                     |
| [**\_ISCONTENTELEMENTPROPERTYID UIA**](uiauto-automation-element-propids.md)         | true          | Il controllo barra di stato viene sempre incluso nella visualizzazione contenuto dell'albero di automazione interfaccia utente.                                                                                                                            |
| [**\_ISCONTROLELEMENTPROPERTYID UIA**](uiauto-automation-element-propids.md)         | true          | Il controllo barra di stato viene sempre incluso nella visualizzazione controlli dell'albero di automazione interfaccia utente.                                                                                                                            |
| [**\_ISKEYBOARDFOCUSABLEPROPERTYID UIA**](uiauto-automation-element-propids.md)   | Dipende da       | Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.                                                                                                                                           |
| [**\_ISOFFSCREENPROPERTYID UIA**](uiauto-automation-element-propids.md)                   | Dipende da       | Se un controllo barra di stato non è attualmente visibile, restituirà TRUE per questa proprietà.                                                                                                                            |
| [**\_LABELEDBYPROPERTYID UIA**](uiauto-automation-element-propids.md)                       | NULL          | Il controllo barra di stato in genere non dispone di un'etichetta.                                                                                                                                                             |
| [**\_LOCALIZEDCONTROLTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md) | Vedere le note.    | Stringa localizzata corrispondente al tipo di controllo **StatusBar** . Il valore predefinito è "barra di stato" per en-US o inglese (Stati Uniti).                                                                           |
| [**\_NAMEPROPERTYID UIA**](uiauto-automation-element-propids.md)                                 | Vedere le note.    | Il controllo barra di stato non necessita di un nome a meno che non vengano usati più controlli all'interno di un'applicazione. In questo caso, distinguere ogni barra con nomi quali "stato Internet" o "stato applicazione".                    |
| [**\_ORIENTATIONPROPERTYID UIA**](uiauto-automation-element-propids.md)                   | Dipende da       | Valore che indica l'orientamento del controllo: orizzontale o verticale.                                                                                                                                               |



 

## <a name="required-control-patterns"></a>Pattern di controllo obbligatori

La tabella seguente elenca i pattern di controllo di automazione interfaccia utente che devono essere supportati per i controlli barra di stato. Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Pattern di controllo                               | Supporto  | Note                                                                                                                                                                        |
|-----------------------------------------------|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) | Facoltativo | I controlli barra di stato devono supportare il pattern di controllo [Grid](uiauto-implementinggrid.md) in modo che sia possibile monitorare e fare facilmente riferimento alle singole parti per ottenere informazioni. |



 

## <a name="required-events"></a>Eventi obbligatori

La tabella seguente elenca gli eventi di automazione interfaccia utente necessari per supportare i controlli barra di stato. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



| Evento di automazione interfaccia utente                                                                                                                   | Note                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [**\_AUTOMATIONFOCUSCHANGEDEVENTID UIA**](uiauto-event-ids.md)                                      |                                                                                   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà BoundingRectanglePropertyId. |                                                                                   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsEnabledPropertyId.                 | Se il controllo supporta la proprietà **IsEnabled** , deve supportare questo evento.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsOffscreenPropertyId.             | Se il controllo supporta la proprietà **IsOffscreen** , deve supportare questo evento. |
| [**\_STRUCTURECHANGEDEVENTID UIA**](uiauto-event-ids.md)                                                  |                                                                                   |



 

## <a name="remarks"></a>Commenti

Si consiglia di usare i controlli di modifica come elementi della griglia figlio in una barra di stato. Utilizzando i controlli di modifica è più semplice associare lo scopo del campo stato al relativo valore utilizzando il nome dell'elemento e la proprietà del valore. Poiché i controlli testo non devono supportare il pattern di controllo **value** , non devono essere usati come elementi Grid figlio.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente](uiauto-controltypesoverview.md)
</dt> <dt>

[Cenni preliminari su automazione interfaccia utente](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




