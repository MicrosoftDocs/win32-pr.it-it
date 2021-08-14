---
title: Tipo di controllo SplitButton
description: Questo argomento fornisce informazioni sul supporto di Microsoft Automazione interfaccia utente per il tipo di controllo SplitButton.
ms.assetid: ca4f8e45-7487-4a8b-9df5-edc2b0e56663
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo SplitButton
- Automazione interfaccia utente, tipo di controllo SplitButton
- Automazione interfaccia utente struttura ad albero per il tipo di controllo SplitButton
- Automazione interfaccia utente,proprietà per il tipo di controllo SplitButton
- Automazione interfaccia utente,pattern di controllo per il tipo di controllo SplitButton
- Automazione interfaccia utente,eventi per il tipo di controllo SplitButton
- strutture ad albero, tipo di controllo SplitButton
- proprietà, tipo di controllo SplitButton
- pattern di controllo, tipo di controllo SplitButton
- eventi, tipo di controllo SplitButton
- Supporto per il tipo di controllo SplitButton
- Tipo di controllo SplitButton
- tipi di controllo, struttura ad albero per il tipo di controllo SplitButton
- tipi di controllo, pattern di controllo per il tipo di controllo SplitButton
- tipi di controllo, supporto per SplitButton
- tipi di controllo, SplitButton
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb04f75a075fdd10b1cf31db01d09c6a9d9fd9a5d78c7c0499d9196a9ff8a956
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118825229"
---
# <a name="splitbutton-control-type"></a>Tipo di controllo SplitButton

Questo argomento fornisce informazioni sul supporto di Microsoft Automazione interfaccia utente per il **tipo di controllo SplitButton.**

Il controllo pulsante di menu suddiviso consente di eseguire un'azione su un controllo e di espandere il controllo per visualizzare un elenco di altre possibili azioni che è possibile eseguire.

Le sezioni seguenti definiscono la struttura ad Automazione interfaccia utente struttura ad albero, le proprietà, i pattern di controllo e gli eventi per il **tipo di controllo SplitButton.** I Automazione interfaccia utente si applicano a tutti i controlli pulsante di menu suddiviso in cui il framework o la piattaforma dell'interfaccia utente si integra Automazione interfaccia utente per i tipi di controllo e i pattern di controllo.

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Pattern di controllo obbligatori](#required-control-patterns)
-   [Eventi obbligatori](#required-events)
-   [Esempio di tipo di controllo SplitButton](#splitbutton-control-type-example)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

La tabella seguente illustra un controllo tipico e una visualizzazione contenuto dell'albero Automazione interfaccia utente relativo ai controlli pulsante di menu suddiviso e descrive gli elementi che possono essere contenuti in ogni visualizzazione. Per altre informazioni sull'albero Automazione interfaccia utente, vedere panoramica [Automazione interfaccia utente albero.](uiauto-treeoverview.md)



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
<li>Menu (0 o 1; viene visualizzato come elemento figlio di un pulsante secondario che supporta il modello ExpandCollapse)
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

La tabella seguente elenca le Automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per il **tipo di controllo SplitButton.** Per altre informazioni sulle Automazione interfaccia utente, vedere Recupero di [proprietà da Automazione interfaccia utente elementi](uiauto-propertiesforclients.md).



| Proprietà di automazione interfaccia utente                                                                                              | Valore           | Note                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Vedere le note.      | Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata dell'Automazione interfaccia utente albero.                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vedere le note.      | Il rettangolo più esterno che contiene l'intero controllo.                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vedere le note.      | Supportata se è presente un rettangolo di delimitazione. Se non tutti i punti all'interno del rettangolo di delimitazione sono selezionabili e l'elemento esegue hit testing specializzati, eseguire l'override e fornire un punto selezionabile. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **SplitButton** | Questo valore è uguale per tutti i framework dell'interfaccia utente.                                                                                                                                                        |
| [**UIA \_ HelpTextPropertyId**](uiauto-automation-element-propids.md)                         | Vedere le note.      | Il testo della Guida può indicare il risultato dell'attivazione del pulsante di menu combinato, che in genere è lo stesso tipo di informazioni visualizzate mediante una descrizione comando.                                                   |
| [**\_IsContentElementPropertyId dell'interfaccia utente**](uiauto-automation-element-propids.md)         | true            | Il controllo pulsante di menu combinato contiene informazioni per l'utente finale.                                                                                                                                      |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | true            | Il controllo pulsante di menu combinato è visibile all'utente finale.                                                                                                                                                 |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Vedere le note.      | Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.                                                                                                                            |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULL            | I controlli pulsante di menu combinato non hanno un'etichetta di testo statico.                                                                                                                                               |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vedere le note.      | Stringa localizzata corrispondente al **tipo di controllo SplitButton.** Il valore predefinito è "split button" per en-US o English (Stati Uniti).                                                        |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Vedere le note.      | Testo utilizzato per etichettare il pulsante di menu suddiviso. Ogni volta che un'immagine viene usata per etichettare un pulsante di menu suddiviso, è necessario fornire testo alternativo per la proprietà Name del pulsante di menu suddiviso.                              |



 

## <a name="required-control-patterns"></a>Pattern di controllo obbligatori

Nella tabella seguente sono elencati i Automazione interfaccia utente di controllo personalizzati che devono essere supportati da tutti i controlli pulsante di menu suddiviso. Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Pattern di controllo                                                   | Supporto  | Note                                                                                                                                                                                                                          |
|-------------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Necessario | Poiché i pulsanti di divisione hanno sempre la possibilità di espandere un elenco di opzioni, devono supportare il pattern di controllo [ExpandCollapse.](uiauto-implementingexpandcollapse.md)                                                      |
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)                 | Necessario | Poiché i pulsanti di divisione hanno sempre un'azione predefinita associata al metodo [**IInvokeProvider::Invoke,**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iinvokeprovider-invoke) devono supportare il pattern di controllo [Invoke.](uiauto-implementinginvoke.md) |



 

## <a name="required-events"></a>Eventi obbligatori

La tabella seguente elenca gli eventi Automazione interfaccia utente che i controlli pulsante di menu suddiviso devono supportare. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automazione interfaccia utente evento                                                                                                                                                | Note                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                                   |                                                                                                                            |
| [**Interfaccia \_ utente Evento di modifica della proprietà BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md)                              |                                                                                                                            |
| [**Interfaccia \_ utente Evento di modifica della proprietà ExpandCollapseExpandCollapseStatePropertyId.**](uiauto-control-pattern-propids.md) |                                                                                                                            |
| [**UIA \_ Invoke \_ InvokedEventId**](uiauto-event-ids.md)                                                                                  |                                                                                                                            |
| [**Interfaccia \_ utente Evento di modifica della proprietà IsEnabledPropertyId.**](uiauto-automation-element-propids.md)                                              | Se il controllo supporta la [**proprietà IsEnabled,**](uiauto-automation-element-propids.md) deve supportare questo evento.   |
| [**Interfaccia \_ utente Evento di modifica della proprietà IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)                                          | Se il controllo supporta la [**proprietà IsOffscreen,**](uiauto-automation-element-propids.md) deve supportare questo evento. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                               |                                                                                                                            |



 

## <a name="splitbutton-control-type-example"></a>Esempio di tipo di controllo SplitButton

L'immagine seguente illustra un controllo che implementa il **tipo di controllo SplitButton.**

![Screenshot che mostra l'esempio di un controllo splitbutton](images/splitbuttonxmpl.jpg)



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Automazione interfaccia utente struttura ad albero- Visualizzazione controlli</th>
<th>Automazione interfaccia utente struttura ad albero- Visualizzazione contenuto</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li>Nome splitbutton &quot; &quot; (Invoke, ExpandCollapse)
<ul>
<li>Opzione &quot; Pulsante Altro &quot; (Richiama)
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
<li>Nome splitbutton &quot; &quot; (Invoke, ExpandCollapse)
<ul>
<li>Opzione &quot; Pulsante Altro &quot; (Richiama)
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

 

 




