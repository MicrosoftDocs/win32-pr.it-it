---
title: Tipo di controllo ComboBox
description: In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo ComboBox.
ms.assetid: e7c64dc1-e1e3-4f99-adde-d0d63eb6c4c9
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo ComboBox
- Automazione interfaccia utente, tipo di controllo ComboBox
- Automazione interfaccia utente, struttura ad albero per il tipo di controllo ComboBox
- Automazione interfaccia utente, proprietà per il tipo di controllo ComboBox
- Automazione interfaccia utente, pattern di controllo per il tipo di controllo ComboBox
- Automazione interfaccia utente, eventi per il tipo di controllo ComboBox
- strutture ad albero, tipo di controllo ComboBox
- Proprietà, tipo di controllo ComboBox
- pattern di controllo, tipo di controllo ComboBox
- eventi, tipo di controllo ComboBox
- supporto per il tipo di controllo ComboBox
- Tipo di controllo ComboBox
- tipi di controllo, struttura ad albero per il tipo di controllo ComboBox
- tipi di controllo, pattern di controllo per il tipo di controllo ComboBox
- tipi di controllo, supporto per ComboBox
- tipi di controllo, casella combinata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 410cca4887c04a00d6da53feb9fcf1242476a979
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710318"
---
# <a name="combobox-control-type"></a>Tipo di controllo ComboBox

In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo **ComboBox** .

Una casella combinata è un casella di riepilogo combinata con un controllo statico o un controllo di modifica che visualizza l'elemento attualmente selezionato nel componente casella di riepilogo della casella combinata. Il componente casella di riepilogo del controllo viene visualizzato ogni volta o solo quando l'utente seleziona la freccia a discesa (un pulsante di comando) accanto al controllo. Se il campo di selezione è un controllo di modifica, l'utente può immettere informazioni non presenti nell'elenco. In caso contrario, l'utente può solo selezionare gli elementi nell'elenco.

Nelle sezioni seguenti vengono definiti la struttura ad albero, le proprietà, i pattern di controllo e gli eventi di automazione interfaccia utente necessari per il tipo di controllo **ComboBox** . I requisiti di automazione interfaccia utente si applicano a tutti i controlli casella combinata in cui il Framework dell'interfaccia utente/piattaforma integra il supporto di automazione interfaccia utente per i tipi di controllo e pattern di controllo

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Pattern di controllo obbligatori](#required-control-patterns)
-   [Eventi obbligatori](#required-events)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

Nella tabella seguente viene illustrata una tipica visualizzazione del controllo e del contenuto dell'albero di automazione interfaccia utente relativo ai controlli casella combinata e viene descritto il possibile contenuto di ogni visualizzazione. Per altre informazioni sull'albero di automazione interfaccia utente, vedere [Cenni preliminari sull'albero di automazione interfaccia utente](uiauto-treeoverview.md).



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
<li>ComboBox
<ul>
<li>Edit (0 o 1)</li>
<li>List (0 o 1)</li>
<li>List Item (elemento figlio di List; da 0 a molti)</li>
<li>Button (1)</li>
</ul></li>
</ul></td>
<td><ul>
<li>ComboBox
<ul>
<li>List Item (da 0 a molti)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

Il controllo di modifica nella visualizzazione controlli della casella combinata è necessario solo se la casella combinata può essere modificata in modo da assumere qualsiasi input, come nel caso della casella combinata nella finestra di dialogo **Esegui** .

## <a name="relevant-properties"></a>Proprietà rilevanti

La tabella seguente elenca le proprietà di automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per il tipo di controllo **ComboBox** . Per altre informazioni sulle proprietà di automazione interfaccia utente, vedere [recupero di proprietà da elementi di automazione interfaccia utente](uiauto-propertiesforclients.md).



| Proprietà di automazione interfaccia utente                                                                                              | Valore      | Note                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_AUTOMATIONIDPROPERTYID UIA**](uiauto-automation-element-propids.md)                 | Vedere le note. | Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata della struttura ad albero di automazione interfaccia utente.                                                                                                                                                                                                     |
| [**\_BOUNDINGRECTANGLEPROPERTYID UIA**](uiauto-automation-element-propids.md)       | Vedere le note. | Il rettangolo più esterno che contiene l'intero controllo.                                                                                                                                                                                                                                                         |
| [**\_CLICKABLEPOINTPROPERTYID UIA**](uiauto-automation-element-propids.md)             | Vedere le note. | Supportata se è presente un rettangolo di delimitazione. Se non tutti i punti all'interno del rettangolo di delimitazione sono selezionabili e l'elemento esegue un hit testing specializzato, eseguire l'override e fornire un punto selezionabile.                                                                                                             |
| [**\_CONTROLTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md)                   | ComboBox   |                                                                                                                                                                                                                                                                                                                  |
| [**\_HELPTEXTPROPERTYID UIA**](uiauto-automation-element-propids.md)                         | Vedere le note. | Il testo della Guida per i controlli casella combinata deve spiegare il motivo per cui all'utente viene chiesto di scegliere un'opzione dalla casella combinata. Il testo è simile a quello delle informazioni presentate in una descrizione comando. Ad esempio, "Selezionare un'opzione per impostare la risoluzione dello schermo".                                                |
| [**\_ISCONTENTELEMENTPROPERTYID UIA**](uiauto-automation-element-propids.md)         | true       | I controlli casella combinata vengono sempre inclusi nella visualizzazione contenuto dell'albero di automazione interfaccia utente.                                                                                                                                                                                                                            |
| [**\_ISCONTROLELEMENTPROPERTYID UIA**](uiauto-automation-element-propids.md)         | true       | I controlli casella combinata vengono sempre inclusi nella visualizzazione controlli dell'albero di automazione interfaccia utente.                                                                                                                                                                                                                            |
| [**\_ISKEYBOARDFOCUSABLEPROPERTYID UIA**](uiauto-automation-element-propids.md)   | true       | I controlli casella combinata possono ricevere lo stato attivo della tastiera; Tuttavia, quando un client di automazione interfaccia utente imposta lo stato attivo su una casella combinata, tutti gli elementi nel sottoalbero della casella combinata possono ricevere lo stato attivo.                                                                                                                                          |
| [**\_LABELEDBYPROPERTYID UIA**](uiauto-automation-element-propids.md)                       | Vedere le note. | I controlli casella combinata in genere includono un'etichetta di testo statico a cui questa proprietà fa riferimento.                                                                                                                                                                                                                             |
| [**\_LOCALIZEDCONTROLTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md) | Vedere le note. | Stringa localizzata corrispondente al tipo di controllo **ComboBox** . Il valore predefinito è "casella combinata" per en-US o inglese (Stati Uniti).                                                                                                                                                                          |
| [**\_NAMEPROPERTYID UIA**](uiauto-automation-element-propids.md)                                 | Vedere le note. | Il nome del controllo casella combinata viene in genere generato da un'etichetta di testo statico. Se non è presente un'etichetta di testo statico, è necessario assegnare un valore per la proprietà **Name** . La proprietà **Name** non deve mai contenere il contenuto corrente della casella combinata o modificare quando il contenuto della casella combinata viene modificato. |



 

## <a name="required-control-patterns"></a>Pattern di controllo obbligatori

La tabella seguente elenca i pattern di controllo di automazione interfaccia utente che devono essere supportati da tutti i controlli casella combinata. Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Pattern di controllo                                                   | Supporto  | Note                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Necessario | Il pattern di controllo [ExpandCollapse](uiauto-implementingexpandcollapse.md) deve essere supportato perché un controllo casella combinata deve sempre contenere un pulsante a discesa.                                                                                                                                                                                |
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)           | Dipende da  | Visualizza la selezione corrente nella casella combinata. Il supporto per il pattern di controllo [Selection](uiauto-implementingselection.md) è delegato alla casella di riepilogo sotto la casella combinata, ma potrebbe non essere sempre fattibile.                                                                                                                               |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)                   | Dipende da  | Se la casella combinata può assumere valori di testo arbitrari, il pattern di controllo [value](uiauto-implementingvalue.md) deve essere supportato. Questo modello consente di impostare il contenuto della stringa della casella combinata a livello di codice. Se il pattern di controllo value non è supportato, l'utente deve selezionare una delle voci dell'elenco all'interno del sottoalbero della casella combinata. |
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)                 | Mai    | Il pattern di controllo [Scroll](uiauto-implementingscroll.md) non è mai supportato direttamente in una casella combinata. È supportato se è possibile scorrere una casella di riepilogo contenuta in una casella combinata e solo quando la casella di riepilogo è visibile sullo schermo.                                                                                                              |



 

## <a name="required-events"></a>Eventi obbligatori

La tabella seguente elenca gli eventi di automazione interfaccia utente necessari per supportare i controlli casella combinata. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



| Evento di automazione interfaccia utente                                                                                                                                                | Note                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**\_AUTOMATIONFOCUSCHANGEDEVENTID UIA**](uiauto-event-ids.md)                                                                   |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà BoundingRectanglePropertyId.                              |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsEnabledPropertyId.                                              | Se il controllo supporta la proprietà [**IsEnabled**](uiauto-automation-element-propids.md) , deve supportare questo evento.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsOffscreenPropertyId.                                          | Se il controllo supporta la proprietà [**IsOffscreen**](uiauto-automation-element-propids.md) , deve supportare questo evento. |
| [**\_STRUCTURECHANGEDEVENTID UIA**](uiauto-event-ids.md)                                                                               |                                                                                                                            |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ExpandCollapseExpandCollapseStatePropertyId. |                                                                                                                            |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ValueValuePropertyId.                                               | Se il controllo supporta il pattern di controllo [value](uiauto-implementingvalue.md) , deve supportare questo evento.             |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente](uiauto-controltypesoverview.md)
</dt> <dt>

[Cenni preliminari su automazione interfaccia utente](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




