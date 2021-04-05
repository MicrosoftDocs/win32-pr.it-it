---
title: Tipo di controllo SplitButton
description: In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo SplitButton.
ms.assetid: ca4f8e45-7487-4a8b-9df5-edc2b0e56663
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo SplitButton
- Automazione interfaccia utente, tipo di controllo SplitButton
- Automazione interfaccia utente, struttura ad albero per il tipo di controllo SplitButton
- Automazione interfaccia utente, proprietà per il tipo di controllo SplitButton
- Automazione interfaccia utente, pattern di controllo per il tipo di controllo SplitButton
- Automazione interfaccia utente, eventi per il tipo di controllo SplitButton
- strutture ad albero, tipo di controllo SplitButton
- Proprietà, tipo di controllo SplitButton
- pattern di controllo, tipo di controllo SplitButton
- eventi, tipo di controllo SplitButton
- supporto per il tipo di controllo SplitButton
- Tipo di controllo SplitButton
- tipi di controllo, struttura ad albero per il tipo di controllo SplitButton
- tipi di controllo, pattern di controllo per il tipo di controllo SplitButton
- tipi di controllo, supporto per SplitButton
- tipi di controllo, SplitButton
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c56cd6b22838dfa92ba25ce05e74d228f4173ac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712697"
---
# <a name="splitbutton-control-type"></a>Tipo di controllo SplitButton

In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo **SplitButton** .

Il controllo pulsante di divisione consente di eseguire un'azione su un controllo ed espandere il controllo per visualizzare un elenco di altre possibili azioni che è possibile eseguire.

Nelle sezioni seguenti vengono definiti la struttura ad albero, le proprietà, i pattern di controllo e gli eventi di automazione interfaccia utente necessari per il tipo di controllo **SplitButton** . I requisiti di automazione interfaccia utente si applicano a tutti i controlli pulsante di divisione in cui il Framework dell'interfaccia utente/piattaforma integra il supporto di automazione interfaccia utente per i tipi di controllo e i pattern

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Pattern di controllo obbligatori](#required-control-patterns)
-   [Eventi obbligatori](#required-events)
-   [Esempio di tipo di controllo SplitButton](#splitbutton-control-type-example)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

Nella tabella seguente viene illustrata una tipica visualizzazione del controllo e del contenuto dell'albero di automazione interfaccia utente relativo ai controlli pulsante di suddivisione e viene descritto il possibile contenuto di ogni visualizzazione. Per altre informazioni sull'albero di automazione interfaccia utente, vedere [Cenni preliminari sull'albero di automazione interfaccia utente](uiauto-treeoverview.md).



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
<li>SplitButton
<ul>
<li>Image (0 o 1)</li>
<li>Text (0 o 1)</li>
<li>Button (1 o 2)
<ul>
<li>Menu (0 o 1; viene visualizzato come elemento figlio di un pulsante secondario che supporta il pattern ExpandCollapse)
<ul>
<li>MenuItem (da 1 a molti)</li>
</ul></li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li>SplitButton
<ul>
<li>Button (1 o 2)
<ul>
<li>MenuItem (da 1 a molti)</li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a>Proprietà rilevanti

La tabella seguente elenca le proprietà di automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per il tipo di controllo **SplitButton** . Per altre informazioni sulle proprietà di automazione interfaccia utente, vedere [recupero di proprietà da elementi di automazione interfaccia utente](uiauto-propertiesforclients.md).



| Proprietà di automazione interfaccia utente                                                                                              | Valore           | Note                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_AUTOMATIONIDPROPERTYID UIA**](uiauto-automation-element-propids.md)                 | Vedere le note.      | Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata della struttura ad albero di automazione interfaccia utente.                                                                                         |
| [**\_BOUNDINGRECTANGLEPROPERTYID UIA**](uiauto-automation-element-propids.md)       | Vedere le note.      | Il rettangolo più esterno che contiene l'intero controllo.                                                                                                                                             |
| [**\_CLICKABLEPOINTPROPERTYID UIA**](uiauto-automation-element-propids.md)             | Vedere le note.      | Supportata se è presente un rettangolo di delimitazione. Se non tutti i punti all'interno del rettangolo di delimitazione sono selezionabili e l'elemento esegue un hit testing specializzato, eseguire l'override e fornire un punto selezionabile. |
| [**\_CONTROLTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md)                   | **SplitButton** | Questo valore è uguale per tutti i framework dell'interfaccia utente.                                                                                                                                                        |
| [**\_HELPTEXTPROPERTYID UIA**](uiauto-automation-element-propids.md)                         | Vedere le note.      | Il testo della Guida può indicare il risultato dell'attivazione del pulsante di menu combinato, che in genere è lo stesso tipo di informazioni visualizzate mediante una descrizione comando.                                                   |
| [**\_ISCONTENTELEMENTPROPERTYID UIA**](uiauto-automation-element-propids.md)         | true            | Il controllo pulsante di menu combinato contiene informazioni per l'utente finale.                                                                                                                                      |
| [**\_ISCONTROLELEMENTPROPERTYID UIA**](uiauto-automation-element-propids.md)         | true            | Il controllo pulsante di menu combinato è visibile all'utente finale.                                                                                                                                                 |
| [**\_ISKEYBOARDFOCUSABLEPROPERTYID UIA**](uiauto-automation-element-propids.md)   | Vedere le note.      | Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.                                                                                                                            |
| [**\_LABELEDBYPROPERTYID UIA**](uiauto-automation-element-propids.md)                       | NULL            | I controlli pulsante di menu combinato non hanno un'etichetta di testo statico.                                                                                                                                               |
| [**\_LOCALIZEDCONTROLTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md) | Vedere le note.      | Stringa localizzata corrispondente al tipo di controllo **SplitButton** . Il valore predefinito è "Split Button" per en-US o English (Stati Uniti).                                                        |
| [**\_NAMEPROPERTYID UIA**](uiauto-automation-element-propids.md)                                 | Vedere le note.      | Testo utilizzato per assegnare un'etichetta al pulsante di suddivisione. Ogni volta che viene usata un'immagine per etichettare un pulsante di suddivisione, è necessario specificare il testo alternativo per la proprietà nome pulsante di divisione.                              |



 

## <a name="required-control-patterns"></a>Pattern di controllo obbligatori

La tabella seguente elenca i pattern di controllo di automazione interfaccia utente che devono essere supportati da tutti i controlli pulsante di comando combinato. Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Pattern di controllo                                                   | Supporto  | Note                                                                                                                                                                                                                          |
|-------------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Necessario | Poiché i pulsanti Split hanno sempre la possibilità di espandere un elenco di opzioni, devono supportare il pattern di controllo [ExpandCollapse](uiauto-implementingexpandcollapse.md) .                                                      |
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)                 | Necessario | Poiché i pulsanti Split hanno sempre un'azione predefinita associata al metodo [**IInvokeProvider:: Invoke**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iinvokeprovider-invoke) , devono supportare il pattern di controllo [Invoke](uiauto-implementinginvoke.md) . |



 

## <a name="required-events"></a>Eventi obbligatori

La tabella seguente elenca gli eventi di automazione interfaccia utente che sono necessari per supportare i controlli pulsante di suddivisione. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



| Evento di automazione interfaccia utente                                                                                                                                                | Note                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**\_AUTOMATIONFOCUSCHANGEDEVENTID UIA**](uiauto-event-ids.md)                                                                   |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà BoundingRectanglePropertyId.                              |                                                                                                                            |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ExpandCollapseExpandCollapseStatePropertyId. |                                                                                                                            |
| [**\_Richiama \_ InvokedEventId**](uiauto-event-ids.md)                                                                                  |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsEnabledPropertyId.                                              | Se il controllo supporta la proprietà [**IsEnabled**](uiauto-automation-element-propids.md) , deve supportare questo evento.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsOffscreenPropertyId.                                          | Se il controllo supporta la proprietà [**IsOffscreen**](uiauto-automation-element-propids.md) , deve supportare questo evento. |
| [**\_STRUCTURECHANGEDEVENTID UIA**](uiauto-event-ids.md)                                                                               |                                                                                                                            |



 

## <a name="splitbutton-control-type-example"></a>Esempio di tipo di controllo SplitButton

Nell'immagine seguente viene illustrato un controllo che implementa il tipo di controllo **SplitButton** .

![screenshot che mostra l'esempio di un controllo SplitButton](images/splitbuttonxmpl.jpg)



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Albero di automazione interfaccia utente-visualizzazione controlli</th>
<th>Albero di automazione interfaccia utente-visualizzazione contenuto</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li>&quot;Nome SplitButton &quot; (Invoke, ExpandCollapse)
<ul>
<li>&quot;Opzione altro pulsante &quot; (richiama)
<ul>
<li>Menu
<ul>
<li>MenuItem</li>
<li>...</li>
</ul></li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li>&quot;Nome SplitButton &quot; (Invoke, ExpandCollapse)
<ul>
<li>&quot;Opzione altro pulsante &quot; (richiama)
<ul>
<li>Menu
<ul>
<li>MenuItem</li>
<li>...</li>
</ul></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente](uiauto-controltypesoverview.md)
</dt> <dt>

[Cenni preliminari su automazione interfaccia utente](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




