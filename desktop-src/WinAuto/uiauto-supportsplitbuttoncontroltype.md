---
title: Tipo di controllo SplitButton
description: Questo argomento fornisce informazioni sul supporto microsoft Automazione interfaccia utente per il tipo di controllo SplitButton.
ms.assetid: ca4f8e45-7487-4a8b-9df5-edc2b0e56663
keywords:
- Automazione interfaccia utente,supporto per il tipo di controllo SplitButton
- Automazione interfaccia utente,Tipo di controllo SplitButton
- Automazione interfaccia utente,struttura ad albero per il tipo di controllo SplitButton
- Automazione interfaccia utente,proprietà per il tipo di controllo SplitButton
- Automazione interfaccia utente,pattern di controllo per il tipo di controllo SplitButton
- Automazione interfaccia utente,eventi per il tipo di controllo SplitButton
- strutture ad albero, tipo di controllo SplitButton
- proprietà,tipo di controllo SplitButton
- pattern di controllo, tipo di controllo SplitButton
- eventi, tipo di controllo SplitButton
- supporto per il tipo di controllo SplitButton
- Tipo di controllo SplitButton
- tipi di controllo, struttura ad albero per il tipo di controllo SplitButton
- tipi di controllo, pattern di controllo per il tipo di controllo SplitButton
- tipi di controllo, supporto per SplitButton
- tipi di controllo,SplitButton
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30e420d369ee09dfd2d92b5e5d79cf94c7013566
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470098"
---
# <a name="splitbutton-control-type"></a>Tipo di controllo SplitButton

Questo argomento fornisce informazioni sul supporto di Microsoft Automazione interfaccia utente per il **tipo di controllo SplitButton.**

Il controllo pulsante di divisione consente di eseguire un'azione su un controllo e di espandere il controllo per visualizzare un elenco di altre possibili azioni che possono essere eseguite.

Le sezioni seguenti definiscono la struttura ad Automazione interfaccia utente, le proprietà, i pattern di controllo e gli eventi necessari per il **tipo di controllo SplitButton.** I Automazione interfaccia utente si applicano a tutti i controlli pulsante di divisione in cui il framework o la piattaforma dell'interfaccia utente integra Automazione interfaccia utente per i tipi di controllo e i pattern di controllo.

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Pattern di controllo obbligatori](#required-control-patterns)
-   [Eventi obbligatori](#required-events)
-   [Esempio di tipo di controllo SplitButton](#splitbutton-control-type-example)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

La tabella seguente illustra un controllo tipico e una visualizzazione contenuto dell'albero Automazione interfaccia utente che riguarda i controlli pulsante di divisione e descrive cosa può essere contenuto in ogni visualizzazione. Per altre informazioni sull'albero Automazione interfaccia utente, vedere panoramica Automazione interfaccia utente [albero](uiauto-treeoverview.md).




| Visualizzazione controlli | Visualizzazione contenuto | 
|--------------|--------------|
| <ul><li>SplitButton<ul><li>Image (0 o 1)</li><li>Text (0 o 1)</li><li>Button (1 o 2)<ul><li>Menu (0 o 1; viene visualizzato come elemento figlio di un pulsante secondario che supporta il modello ExpandCollapse)<ul><li>MenuItem (da 1 a molti)</li></ul></li></ul></li></ul></li></ul> | <ul><li>SplitButton<ul><li>Button (1 o 2)<ul><li>MenuItem (da 1 a molti)</li></ul></li></ul></li></ul> | 




 

## <a name="relevant-properties"></a>Proprietà rilevanti

Nella tabella seguente sono elencate Automazione interfaccia utente proprietà il cui valore o definizione è particolarmente rilevante per il tipo di controllo **SplitButton.** Per altre informazioni sulle Automazione interfaccia utente, vedere Recupero di proprietà [da Automazione interfaccia utente elementi](uiauto-propertiesforclients.md).



| Proprietà di automazione interfaccia utente                                                                                              | valore           | Note                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Vedere le note.      | Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata dell'Automazione interfaccia utente albero.                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vedere le note.      | Il rettangolo più esterno che contiene l'intero controllo.                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vedere le note.      | Supportata se è presente un rettangolo di delimitazione. Se non tutti i punti all'interno del rettangolo di delimitazione sono selezionabili e l'elemento esegue hit testing specializzati, esegue l'override e fornisce un punto selezionabile. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **SplitButton** | Questo valore è uguale per tutti i framework dell'interfaccia utente.                                                                                                                                                        |
| [**UIA \_ HelpTextPropertyId**](uiauto-automation-element-propids.md)                         | Vedere le note.      | Il testo della Guida può indicare il risultato dell'attivazione del pulsante di menu combinato, che in genere è lo stesso tipo di informazioni visualizzate mediante una descrizione comando.                                                   |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | true            | Il controllo pulsante di menu combinato contiene informazioni per l'utente finale.                                                                                                                                      |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | true            | Il controllo pulsante di menu combinato è visibile all'utente finale.                                                                                                                                                 |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Vedere le note.      | Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.                                                                                                                            |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULL            | I controlli pulsante di menu combinato non hanno un'etichetta di testo statico.                                                                                                                                               |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vedere le note.      | Stringa localizzata corrispondente al **tipo di controllo SplitButton.** Il valore predefinito è "pulsante di divisione" per en-US o inglese (Stati Uniti).                                                        |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Vedere le note.      | Testo utilizzato per etichettare il pulsante di divisione. Ogni volta che un'immagine viene usata per etichettare un pulsante di divisione, è necessario specificare testo alternativo per la proprietà Nome pulsante di divisione.                              |



 

## <a name="required-control-patterns"></a>Pattern di controllo obbligatori

Nella tabella seguente sono elencati i Automazione interfaccia utente di controllo necessari per essere supportati da tutti i controlli pulsante di divisione. Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Pattern di controllo                                                   | Supporto  | Note                                                                                                                                                                                                                          |
|-------------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Obbligatoria | Poiché i pulsanti di divisione hanno sempre la possibilità di espandere un elenco di opzioni, devono supportare il pattern di [controllo ExpandCollapse.](uiauto-implementingexpandcollapse.md)                                                      |
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)                 | Obbligatoria | Poiché i pulsanti di divisione hanno sempre un'azione predefinita associata al metodo [**IInvokeProvider::Invoke,**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iinvokeprovider-invoke) devono supportare il pattern di controllo [Invoke.](uiauto-implementinginvoke.md) |



 

## <a name="required-events"></a>Eventi obbligatori

Nella tabella seguente sono elencati Automazione interfaccia utente eventi che i controlli pulsante di divisione devono supportare. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automazione interfaccia utente eventi                                                                                                                                                | Note                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                                   |                                                                                                                            |
| [**Interfaccia \_ utente Evento di modifica della proprietà BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md)                              |                                                                                                                            |
| [**Interfaccia \_ utente Evento di modifica della proprietà ExpandCollapseExpandCollapseStatePropertyId.**](uiauto-control-pattern-propids.md) |                                                                                                                            |
| [**\_ \_ InvokedEventId dell'interfaccia utente**](uiauto-event-ids.md)                                                                                  |                                                                                                                            |
| [**Interfaccia \_ utente Evento di modifica della proprietà IsEnabledPropertyId.**](uiauto-automation-element-propids.md)                                              | Se il controllo supporta la [**proprietà IsEnabled,**](uiauto-automation-element-propids.md) deve supportare questo evento.   |
| [**Interfaccia \_ utente Evento di modifica della proprietà IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)                                          | Se il controllo supporta la [**proprietà IsOffscreen,**](uiauto-automation-element-propids.md) deve supportare questo evento. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                               |                                                                                                                            |



 

## <a name="splitbutton-control-type-example"></a>Esempio di tipo di controllo SplitButton

L'immagine seguente illustra un controllo che implementa il **tipo di controllo SplitButton.**

![Screenshot che mostra un esempio di controllo splitbutton](images/splitbuttonxmpl.jpg)




| Automazione interfaccia utente struttura ad albero- Visualizzazione controlli | Automazione interfaccia utente struttura ad albero- Visualizzazione contenuto | 
|-----------------------------------|-----------------------------------|
| <ul><li>SplitButton "Nome" (Invoke, ExpandCollapse)<ul><li>Pulsante "Opzione Altro" (Richiama)<ul><li>Menu<ul><li>MenuItem</li><li>...</li></ul></li></ul></li></ul></li></ul> | <ul><li>SplitButton "Nome" (Invoke, ExpandCollapse)<ul><li>Pulsante "Opzione Altro" (Richiama)<ul><li>Menu<ul><li>MenuItem</li><li>...</li></ul></li></ul></li></ul></li></ul> | 




 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente](uiauto-controltypesoverview.md)
</dt> <dt>

[Cenni preliminari su automazione interfaccia utente](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




