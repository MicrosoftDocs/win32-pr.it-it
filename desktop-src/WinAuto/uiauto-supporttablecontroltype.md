---
title: Tipo di controllo Table
description: In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo Table.
ms.assetid: 508db2af-1ca3-4003-8e1f-6e225cf79b7a
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo Table
- Automazione interfaccia utente, tipo di controllo Table
- Automazione interfaccia utente, struttura ad albero per il tipo di controllo Table
- Automazione interfaccia utente, proprietà per il tipo di controllo Table
- Automazione interfaccia utente, pattern di controllo per il tipo di controllo Table
- Automazione interfaccia utente, eventi per il tipo di controllo Table
- strutture ad albero, tipo di controllo Table
- Proprietà, tipo di controllo Table
- pattern di controllo, tipo di controllo Table
- eventi, tipo di controllo Table
- supporto per il tipo di controllo Table
- Table (tipo di controllo)
- tipi di controllo, struttura ad albero per il tipo di controllo Table
- tipi di controllo, pattern di controllo per il tipo di controllo Table
- tipi di controllo, supporto per la tabella
- tipi di controllo, tabella
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb4ee709bd16156a62882aeee014b4744dab2214
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515925"
---
# <a name="table-control-type"></a>Tipo di controllo Table

In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo **Table** .

I controlli tabella contengono righe e colonne di testo e, facoltativamente, intestazioni di riga e intestazioni di colonna.

Nelle sezioni seguenti vengono definiti la struttura ad albero, le proprietà, i pattern di controllo e gli eventi di automazione interfaccia utente necessari per il tipo di controllo **Table** . I requisiti di automazione interfaccia utente si applicano a tutti i controlli tabella in cui la piattaforma/Framework dell'interfaccia utente integra il supporto di automazione interfaccia utente per tipi di controllo e pattern di controllo

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Pattern di controllo obbligatori](#required-control-patterns)
-   [Eventi obbligatori](#required-events)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

Nella tabella seguente viene illustrata una tipica visualizzazione del controllo e del contenuto dell'albero di automazione interfaccia utente relativo ai controlli tabella e viene descritto il possibile contenuto di ogni visualizzazione. Per altre informazioni sull'albero di automazione interfaccia utente, vedere [Cenni preliminari sull'albero di automazione interfaccia utente](uiauto-treeoverview.md).



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
<li>Tabella
<ul>
<li>Text (0 o 1)</li>
<li>Header (0 o più)</li>
<li>Vari controlli (0 o più)</li>
</ul></li>
</ul></td>
<td><ul>
<li>Tabella
<ul>
<li>Testo (1 o più)</li>
<li>Vari controlli (0 o più)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

Se un controllo tabella include intestazioni di riga o di colonna, queste devono essere esposte nella visualizzazione controlli dell'albero di automazione interfaccia utente. Non è necessario che la visualizzazione contenuto esponga queste informazioni perché è possibile accedervi usando [**IUIAutomationTablePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtablepattern).

## <a name="relevant-properties"></a>Proprietà rilevanti

La tabella seguente elenca le proprietà di automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per i controlli tabella. Per altre informazioni sulle proprietà di automazione interfaccia utente, vedere [recupero di proprietà da elementi di automazione interfaccia utente](uiauto-propertiesforclients.md).



| Proprietà di automazione interfaccia utente                                                                                              | Valore      | Note                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_AUTOMATIONIDPROPERTYID UIA**](uiauto-automation-element-propids.md)                 | Vedere le note. | Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata della struttura ad albero di automazione interfaccia utente.                                                                                                                      |
| [**\_BOUNDINGRECTANGLEPROPERTYID UIA**](uiauto-automation-element-propids.md)       | Vedere le note. | Il rettangolo più esterno che contiene l'intero controllo.                                                                                                                                                                          |
| [**\_CLICKABLEPOINTPROPERTYID UIA**](uiauto-automation-element-propids.md)             | Vedere le note. | Supportata se è presente un rettangolo di delimitazione. Se non tutti i punti all'interno del rettangolo di delimitazione sono selezionabili e l'elemento esegue un hit testing specializzato, eseguire l'override e fornire un punto selezionabile.                              |
| [**\_CONTROLTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md)                   | **Tabella**  |                                                                                                                                                                                                                                   |
| [**\_DESCRIBEDBYPROPERTYID UIA**](uiauto-automation-element-propids.md)                   | Vedere le note. | Se la tabella viene annotata mediante altri elementi dell'interfaccia utente, ad esempio un elemento di testo contenente la descrizione della tabella, la proprietà DescribedBy deve esporre un riferimento all'elemento di automazione del controllo testo.           |
| [**\_HELPTEXTPROPERTYID UIA**](uiauto-automation-element-propids.md)                         | Vedere le note. | Altre informazioni sullo scopo della tabella devono essere esposte tramite questa proprietà se non sono sufficientemente spiegate dalla proprietà [**\_ NamePropertyId di UIA**](uiauto-automation-element-propids.md) .      |
| [**\_ISCONTENTELEMENTPROPERTYID UIA**](uiauto-automation-element-propids.md)         | true       | Il controllo tabella deve essere sempre visualizzato nella visualizzazione contenuto dell'albero di automazione interfaccia utente.                                                                                                                                               |
| [**\_ISCONTROLELEMENTPROPERTYID UIA**](uiauto-automation-element-propids.md)         | true       | Il controllo tabella deve essere sempre visualizzato nella visualizzazione controlli dell'albero di automazione interfaccia utente.                                                                                                                                               |
| [**\_ISKEYBOARDFOCUSABLEPROPERTYID UIA**](uiauto-automation-element-propids.md)   | Vedere le note. | Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.                                                                                                                                                         |
| [**\_LABELEDBYPROPERTYID UIA**](uiauto-automation-element-propids.md)                       | Vedere le note. | Se è presente un'etichetta di testo statico, questa proprietà deve esporre un riferimento all'elemento di automazione del controllo.                                                                                                                |
| [**\_LOCALIZEDCONTROLTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md) | Vedere le note. | Stringa localizzata corrispondente al tipo di controllo **Table** . Il valore predefinito è "Table" per en-US o English (Stati Uniti).                                                                                                  |
| [**\_NAMEPROPERTYID UIA**](uiauto-automation-element-propids.md)                                 | Vedere le note. | Il controllo tabella in genere ottiene il valore per il nome da un'etichetta di testo statico. Se non è presente un'etichetta di testo statico, l'elemento deve assegnare una proprietà Name che deve essere sempre disponibile per spiegare lo scopo della tabella. |



 

## <a name="required-control-patterns"></a>Pattern di controllo obbligatori

La tabella seguente elenca i pattern di controllo di automazione interfaccia utente che devono essere supportati da tutti i controlli tabella. Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Pattern di controllo                                         | Supporto                     | Note                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider)           | Necessario                    | Poiché il controllo tabella contiene elementi presentati in una griglia, supporta sempre il pattern di controllo [Grid](uiauto-implementinggrid.md) .                                                                                                                                                    |
| [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)   | Obbligatorio con oggetti figlio | Gli oggetti interni di una tabella devono supportare sia il pattern di controllo [GridItem](uiauto-implementinggriditem.md) sia il pattern di controllo [TableItem](uiauto-implementingtableitem.md) . La tabella stessa non deve supportare il pattern di controllo GridItem o TableItem, a meno che la tabella non faccia parte di un'altra tabella.  |
| [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider)         | Necessario                    | Il controllo tabella può sempre avere intestazioni associate al contenuto.                                                                                                                                                                                                                       |
| [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) | Obbligatorio con oggetti figlio | Gli oggetti interni di una tabella devono supportare sia il pattern di controllo [GridItem](uiauto-implementinggriditem.md) sia il pattern di controllo [TableItem](uiauto-implementingtableitem.md) . La tabella stessa non deve supportare il pattern di controllo GridItem o TableItem, a meno che la tabella non faccia parte di un'altra tabella. |



 

## <a name="required-events"></a>Eventi obbligatori

La tabella seguente elenca gli eventi di automazione interfaccia utente necessari per supportare i controlli tabella. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



| Evento di automazione interfaccia utente                                                                                                                   | Note                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**\_AUTOMATIONFOCUSCHANGEDEVENTID UIA**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà BoundingRectanglePropertyId. |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsEnabledPropertyId.                 | Se il controllo supporta la proprietà [**IsEnabled**](uiauto-automation-element-propids.md) , deve supportare questo evento.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsOffscreenPropertyId.             | Se il controllo supporta la proprietà [**IsOffscreen**](uiauto-automation-element-propids.md) , deve supportare questo evento. |
| [**\_STRUCTURECHANGEDEVENTID UIA**](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente](uiauto-controltypesoverview.md)
</dt> <dt>

[Cenni preliminari su automazione interfaccia utente](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




