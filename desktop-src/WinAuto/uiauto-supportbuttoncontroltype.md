---
title: Tipo di controllo Pulsante
description: Questo argomento fornisce informazioni sul supporto microsoft Automazione interfaccia utente per il tipo di controllo Button.
ms.assetid: a2942067-461c-4281-80cf-385e3c08c874
keywords:
- Automazione interfaccia utente,supporto per il tipo di controllo Button
- Automazione interfaccia utente,Tipo di controllo Button
- Automazione interfaccia utente,struttura ad albero per il tipo di controllo Button
- Automazione interfaccia utente,proprietà per il tipo di controllo Button
- Automazione interfaccia utente,pattern di controllo per il tipo di controllo Button
- Automazione interfaccia utente,eventi per il tipo di controllo Button
- strutture ad albero, tipo di controllo Button
- proprietà,Tipo di controllo Button
- pattern di controllo,tipo di controllo Button
- eventi, tipo di controllo Button
- supporto per il tipo di controllo Button
- Button (tipo di controllo)
- tipi di controllo, struttura ad albero per il tipo di controllo Button
- tipi di controllo, pattern di controllo per il tipo di controllo Button
- tipi di controllo, supporto per Button
- tipi di controllo,Pulsante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c080018e0fcaf8cd196204f80c61041d03fc1589
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478037"
---
# <a name="button-control-type"></a>Tipo di controllo Pulsante

Questo argomento fornisce informazioni sul supporto microsoft Automazione interfaccia utente per il **tipo di controllo** Button.

Un pulsante è un oggetto che un utente usa per eseguire un'azione, ad esempio i pulsanti OK e Annulla in una finestra di dialogo. Il controllo Button è un controllo semplice da esporre perché esegue il mapping a un unico comando che l'utente desidera completare.

Le sezioni seguenti definiscono la struttura ad Automazione interfaccia utente, le proprietà, i pattern di controllo e gli eventi necessari per il **tipo di controllo** Button. I Automazione interfaccia utente si applicano a tutti i controlli pulsante in cui il framework o la piattaforma dell'interfaccia utente Automazione interfaccia utente supporto per i tipi di controllo e i pattern di controllo.

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Pattern di controllo obbligatori](#required-control-patterns)
-   [Eventi obbligatori](#required-events)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

La tabella seguente illustra un controllo tipico e una visualizzazione contenuto dell'albero Automazione interfaccia utente che riguarda i controlli pulsante e descrive cosa può essere contenuto in ogni visualizzazione. Per altre informazioni sull'albero Automazione interfaccia utente, vedere Panoramica Automazione interfaccia utente [albero](uiauto-treeoverview.md).




| Visualizzazione controlli | Visualizzazione contenuto | 
|--------------|--------------|
| <ul><li>Button<ul><li>Image (0 o più)</li><li>Text (0 o più)</li></ul></li></ul> | <ul><li>Button</li></ul> | 




 

## <a name="relevant-properties"></a>Proprietà rilevanti

Nella tabella seguente sono elencate Automazione interfaccia utente proprietà il cui valore o definizione è particolarmente rilevante per i controlli che implementano il tipo di controllo **Button** ,ad esempio i controlli pulsante. Per altre informazioni sulle Automazione interfaccia utente, vedere Recupero di proprietà [da Automazione interfaccia utente elementi](uiauto-propertiesforclients.md).



| Proprietà di automazione interfaccia utente                                                                                              | valore      | Note                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AcceleratorKeyPropertyId**](uiauto-automation-element-propids.md)             | Vedere le note. | Un controllo pulsante supporta in genere un tasto di scelta rapida per consentire all'utente finale di eseguire rapidamente l'azione rappresentata dal pulsante dalla tastiera.                                             |
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Vedere le note. | Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata dell'Automazione interfaccia utente albero.                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vedere le note. | Il rettangolo più esterno che contiene l'intero controllo.                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vedere le note. | Supportata se è presente un rettangolo di delimitazione. Se non tutti i punti all'interno del rettangolo di delimitazione sono selezionabili e l'elemento esegue hit testing specializzati, esegue l'override e fornisce un punto selezionabile. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Button** |                                                                                                                                                                                                      |
| [**UIA \_ HelpTextPropertyId**](uiauto-automation-element-propids.md)                         | Vedere le note. | Il testo della Guida deve indicare quale sarà il risultato finale dell'attivazione del pulsante. Si tratta in genere dello stesso tipo di informazioni presentate tramite una descrizione comando.                                      |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | true       | Il controllo pulsante deve essere sempre contenuto.                                                                                                                                                           |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | true       | Il controllo pulsante deve essere sempre un controllo .                                                                                                                                                         |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Vedere le note. | Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.                                                                                                                            |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Null       | Ai controlli Button viene automaticamente applicata un'etichetta in base al relativo contenuto.                                                                                                                                                  |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vedere le note. | Stringa localizzata corrispondente al **tipo di controllo** Button. Il valore predefinito è "button" per en-US o english (Stati Uniti).                                                                   |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Vedere le note. | Il nome del controllo pulsante è il testo usato per etichettarlo. Ogni volta che un'immagine viene usata per etichettare un pulsante, è necessario specificare testo alternativo per la proprietà **Name del** pulsante.                        |



 

## <a name="required-control-patterns"></a>Pattern di controllo obbligatori

Nella tabella seguente sono elencati i Automazione interfaccia utente di controllo necessari per essere supportati da tutti i controlli pulsante. Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Pattern di controllo/proprietà del pattern                                  | Supporto/valore | Note                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Vedere le note.    | Quando un pulsante è ospitato come figlio di un pulsante di divisione, il pulsante figlio può supportare il pattern di controllo [ExpandCollapse](uiauto-implementingexpandcollapse.md) anziché il pattern di controllo [Invoke](uiauto-implementinginvoke.md) o [Toggle.](uiauto-implementingtoggle.md) Il pattern di controllo ExpandCollapse può essere usato per aprire o chiudere un menu o un'altra sotto struttura associata all'elemento pulsante. |
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)                 | Vedere le note.    | Tutti i pulsanti devono supportare [il pattern di](uiauto-implementinginvoke.md) controllo Invoke o [Toggle,](uiauto-implementingtoggle.md) ma non entrambi. Il pattern di controllo Invoke deve essere supportato quando il pulsante esegue un comando su richiesta dell'utente. Questo comando esegue il mapping a una singola operazione, ad esempio Taglia, Copia, Incolla o Elimina.                                                              |
| [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)                 | Vedere le note.    | Tutti i pulsanti devono supportare il pattern di controllo [Invoke](uiauto-implementinginvoke.md) o [Toggle,](uiauto-implementingtoggle.md) ma non entrambi. Il pattern di controllo Toggle deve essere supportato se il pulsante può scorrere una serie di un massimo di tre stati. In genere viene interpretato come opzione di attivazione/disattivazione per funzionalità specifiche.                                                                        |



 

## <a name="required-events"></a>Eventi obbligatori

La tabella seguente elenca gli eventi Automazione interfaccia utente che i controlli pulsante devono supportare. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automazione interfaccia utente eventi                                                                                                                   | Note                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**Interfaccia \_ utente Evento di modifica della proprietà BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md) |                                                                                                                            |
| [**\_ \_ InvokedEventId dell'interfaccia utente**](uiauto-event-ids.md)                                                     | Se il controllo supporta il pattern [di controllo Invoke,](uiauto-implementinginvoke.md) deve supportare questo evento.           |
| [**Interfaccia \_ utente Evento di modifica della proprietà IsEnabledPropertyId.**](uiauto-automation-element-propids.md)                 | Se il controllo supporta la [**proprietà IsEnabled,**](uiauto-automation-element-propids.md) deve supportare questo evento.   |
| [**Interfaccia \_ utente Evento di modifica della proprietà IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)             | Se il controllo supporta la [**proprietà IsOffscreen,**](uiauto-automation-element-propids.md) deve supportare questo evento. |
| [**Interfaccia \_ utente Evento di modifica**](uiauto-automation-element-propids.md) della proprietà NamePropertyId.                           |                                                                                                                            |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |
| [**Interfaccia \_ utente Evento di modifica della proprietà ToggleToggleStatePropertyId.**](uiauto-control-pattern-propids.md)    | Se il controllo supporta il pattern [di controllo Toggle,](uiauto-implementingtoggle.md) deve supportare questo evento.           |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente](uiauto-controltypesoverview.md)
</dt> <dt>

[Cenni preliminari su automazione interfaccia utente](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




