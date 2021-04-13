---
title: Tipo di controllo ToolBar
description: In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo ToolBar. I controlli della barra degli strumenti consentono agli utenti finali di attivare i comandi e gli strumenti contenuti in un'applicazione.
ms.assetid: e2a72ce3-5263-43f8-be4d-715a78224b68
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo ToolBar
- Automazione interfaccia utente, tipo di controllo ToolBar
- Automazione interfaccia utente, struttura ad albero per il tipo di controllo ToolBar
- Automazione interfaccia utente, proprietà per il tipo di controllo ToolBar
- Automazione interfaccia utente, pattern di controllo per il tipo di controllo ToolBar
- Automazione interfaccia utente, eventi per il tipo di controllo ToolBar
- strutture ad albero, tipo di controllo ToolBar
- Proprietà, tipo di controllo ToolBar
- pattern di controllo, tipo di controllo ToolBar
- eventi, tipo di controllo ToolBar
- supporto per il tipo di controllo ToolBar
- ToolBar (tipo di controllo)
- tipi di controllo, struttura ad albero per il tipo di controllo ToolBar
- tipi di controllo, pattern di controllo per il tipo di controllo ToolBar
- tipi di controllo, supporto per la barra degli strumenti
- tipi di controllo, barra degli strumenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4327c187a86ace6f02b93082675c345eae4d4edf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396742"
---
# <a name="toolbar-control-type"></a>Tipo di controllo ToolBar

In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo **Toolbar** . I controlli della barra degli strumenti consentono agli utenti finali di attivare i comandi e gli strumenti contenuti in un'applicazione.

Nelle sezioni seguenti vengono definiti la struttura ad albero, le proprietà, i pattern di controllo e gli eventi di automazione interfaccia utente necessari per il tipo di controllo **Toolbar** . I requisiti di automazione interfaccia utente si applicano a tutti i controlli della barra degli strumenti in cui la piattaforma/Framework dell'interfaccia utente integra il supporto di automazione interfaccia utente per i tipi di controllo

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Pattern di controllo obbligatori](#required-control-patterns)
-   [Eventi obbligatori](#required-events)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

Nella tabella seguente viene illustrata una tipica visualizzazione del controllo e del contenuto dell'albero di automazione interfaccia utente relativo ai controlli della barra degli strumenti e viene descritto il possibile contenuto di ogni visualizzazione. Per altre informazioni sull'albero di automazione interfaccia utente, vedere [Cenni preliminari sull'albero di automazione interfaccia utente](uiauto-treeoverview.md).



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
<li>ToolBar
<ul>
<li>Vari controlli (0 o più)</li>
</ul></li>
</ul></td>
<td><ul>
<li>ToolBar
<ul>
<li>Vari controlli (0 o più)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

Un controllo barra degli strumenti può contenere qualsiasi tipo di controllo all'interno del relativo sottoalbero. In genere contengono pulsanti, caselle combinate e pulsanti di menu combinato.

## <a name="relevant-properties"></a>Proprietà rilevanti

La tabella seguente elenca le proprietà di automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per il tipo di controllo **Toolbar** . Per altre informazioni sulle proprietà di automazione interfaccia utente, vedere [recupero di proprietà da elementi di automazione interfaccia utente](uiauto-propertiesforclients.md).



| Proprietà di automazione interfaccia utente                                                                                              | Valore       | Note                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_AUTOMATIONIDPROPERTYID UIA**](uiauto-automation-element-propids.md)                 | Vedere le note.  | Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata della struttura ad albero di automazione interfaccia utente.                                                                                               |
| [**\_BOUNDINGRECTANGLEPROPERTYID UIA**](uiauto-automation-element-propids.md)       | Vedere le note.  | Il rettangolo più esterno che contiene l'intero controllo.                                                                                                                                                   |
| [**\_CLICKABLEPOINTPROPERTYID UIA**](uiauto-automation-element-propids.md)             | Vedere le note.  | Supportata se è presente un rettangolo di delimitazione. Se non tutti i punti all'interno del rettangolo di delimitazione sono selezionabili e l'elemento esegue un hit testing specializzato, eseguire l'override e fornire un punto selezionabile.       |
| [**\_CONTROLTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md)                   | **Barra degli strumenti** | Questo valore è uguale per tutti i framework dell'interfaccia utente.                                                                                                                                                              |
| [**\_ISCONTENTELEMENTPROPERTYID UIA**](uiauto-automation-element-propids.md)         | true        | Il controllo Toolbar viene sempre incluso nella visualizzazione contenuto dell'albero di automazione interfaccia utente.                                                                                                                      |
| [**\_ISCONTROLELEMENTPROPERTYID UIA**](uiauto-automation-element-propids.md)         | true        | Il controllo Toolbar viene sempre incluso nella visualizzazione controlli dell'albero di automazione interfaccia utente.                                                                                                                      |
| [**\_ISKEYBOARDFOCUSABLEPROPERTYID UIA**](uiauto-automation-element-propids.md)   | Vedere le note.  | Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.                                                                                                                                  |
| [**\_LABELEDBYPROPERTYID UIA**](uiauto-automation-element-propids.md)                       | NULL        | Un controllo Toolbar non dispone mai di un'etichetta.                                                                                                                                                                       |
| [**\_LOCALIZEDCONTROLTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md) | Vedere le note.  | Stringa localizzata corrispondente al tipo di controllo **Toolbar** . Il valore predefinito è "barra degli strumenti" per en-US o inglese (Stati Uniti).                                                                      |
| [**\_NAMEPROPERTYID UIA**](uiauto-automation-element-propids.md)                                 | Dipende da     | Il controllo Toolbar non necessita di un nome a meno che non venga usato più di un oggetto all'interno di un'applicazione. Se sono presenti più di uno, ognuno deve avere un nome distinto (ad esempio, "Formatting" o "delining"). |



 

## <a name="required-control-patterns"></a>Pattern di controllo obbligatori

La tabella seguente elenca i pattern di controllo di automazione interfaccia utente che devono essere supportati dai controlli della barra degli strumenti. Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Pattern di controllo                                                   | Supporto | Note                                                                                                                                                         |
|-------------------------------------------------------------------|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider)                     | Dipende da | Se la barra degli strumenti può essere ancorata a parti diverse dello schermo, deve supportare il pattern di controllo [Dock](uiauto-implementingdock.md) .                       |
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Dipende da | Se la barra degli strumenti può essere espansa e compressa per visualizzare più elementi, deve supportare il pattern di controllo [ExpandCollapse](uiauto-implementingexpandcollapse.md) . |
| [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider)           | Dipende da | Se la barra degli strumenti può essere ridimensionata, ruotata o spostata, deve supportare il pattern di controllo [Transform](uiauto-implementingtransform.md) .                          |



 

## <a name="required-events"></a>Eventi obbligatori

La tabella seguente elenca gli eventi di automazione interfaccia utente necessari per supportare i controlli della barra degli strumenti. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



| Evento di automazione interfaccia utente                                                                                                                                                | Note                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**\_AUTOMATIONFOCUSCHANGEDEVENTID UIA**](uiauto-event-ids.md)                                                                   |                                                                                                                                  |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà BoundingRectanglePropertyId.                              |                                                                                                                                  |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ExpandCollapseExpandCollapseStatePropertyId. | Se il controllo supporta il pattern di controllo [ExpandCollapse](uiauto-implementingexpandcollapse.md) , deve supportare questo evento. |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsEnabledPropertyId.                                              | Se il controllo supporta la proprietà [**IsEnabled**](uiauto-automation-element-propids.md) , deve supportare questo evento.         |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsOffscreenPropertyId.                                          | Se il controllo supporta la proprietà [**IsOffscreen**](uiauto-automation-element-propids.md) , deve supportare questo evento.       |
| [**\_STRUCTURECHANGEDEVENTID UIA**](uiauto-event-ids.md)                                                                               |                                                                                                                                  |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente](uiauto-controltypesoverview.md)
</dt> <dt>

[Cenni preliminari su automazione interfaccia utente](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




