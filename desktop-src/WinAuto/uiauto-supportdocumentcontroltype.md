---
title: Tipo di controllo documento
description: Questo argomento fornisce informazioni sul supporto di Microsoft Automazione interfaccia utente per il tipo di controllo Documento.
ms.assetid: 62565f16-f0d6-42ff-bc36-897a2618c867
keywords:
- Automazione interfaccia utente,supporto per il tipo di controllo Documento
- Automazione interfaccia utente,Tipo di controllo documento
- Automazione interfaccia utente,struttura ad albero per tipo di controllo Documento
- Automazione interfaccia utente,proprietà per tipo di controllo Documento
- Automazione interfaccia utente,pattern di controllo per tipo di controllo Documento
- Automazione interfaccia utente,eventi per il tipo di controllo Documento
- strutture ad albero, tipo di controllo Documento
- proprietà,Tipo di controllo documento
- pattern di controllo,Tipo di controllo documento
- eventi,Tipo di controllo documento
- supporto per il tipo di controllo Documento
- Document (tipo di controllo)
- tipi di controllo,struttura ad albero per tipo di controllo Documento
- tipi di controllo,pattern di controllo per il tipo di controllo Documento
- tipi di controllo, supporto per Document
- tipi di controllo,documento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cb068e5b2d69c3b7ac180b65436888ca550b1db
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467798"
---
# <a name="document-control-type"></a>Tipo di controllo documento

Questo argomento fornisce informazioni sul supporto di Microsoft Automazione interfaccia utente per il **tipo di controllo** Documento.

I controlli Document consentono a un utente di visualizzare e modificare più pagine di testo. A differenza dei controlli di modifica che supportano solo una semplice riga di testo non formattato, i controlli documento possono ospitare testo con stile e formattazione rtf

Le sezioni seguenti definiscono la struttura ad Automazione interfaccia utente struttura ad albero, le proprietà, i pattern di controllo e gli eventi necessari per il **tipo di controllo** Document. I Automazione interfaccia utente si applicano a tutti i controlli documento in cui il framework o la piattaforma dell'interfaccia utente si integra Automazione interfaccia utente per i tipi di controllo e i pattern di controllo.

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Pattern di controllo obbligatori](#required-control-patterns)
-   [Eventi obbligatori](#required-events)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

La tabella seguente illustra un controllo tipico e una visualizzazione contenuto dell'albero Automazione interfaccia utente che riguarda i controlli documento e descrive cosa può essere contenuto in ogni visualizzazione. Per altre informazioni sull'albero Automazione interfaccia utente, vedere Panoramica Automazione interfaccia utente [albero](uiauto-treeoverview.md).




| Visualizzazione controlli | Visualizzazione contenuto | 
|--------------|--------------|
| <ul><li>Documento<ul><li>Varia</li></ul></li></ul> | <ul><li>Documento<ul><li>Varia</li></ul></li></ul> | 




 

## <a name="relevant-properties"></a>Proprietà rilevanti

Nella tabella seguente sono elencate le Automazione interfaccia utente il cui valore o definizione è particolarmente rilevante per i controlli documento. Per altre informazioni sulle Automazione interfaccia utente, vedere Recupero di proprietà [da Automazione interfaccia utente Elements](uiauto-propertiesforclients.md).



| Proprietà di automazione interfaccia utente                                                                                              | valore        | Note                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Vedere le note.   | Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata dell'Automazione interfaccia utente albero.                                      |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vedere le note.   | Il rettangolo più esterno che contiene l'intero controllo.                                                                                          |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vedere le note.   | Il documento ha un punto selezionabile che farà passare lo stato attivo sul documento o su uno degli elementi nel documento contenitore.                   |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Documento** |                                                                                                                                                   |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | true         | Il controllo documento è sempre incluso nella visualizzazione contenuto dell'Automazione interfaccia utente struttura ad albero.                                                            |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | true         | Il controllo documento è sempre incluso nella visualizzazione controlli dell'Automazione interfaccia utente struttura ad albero.                                                            |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Vedere le note.   | Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.                                                                         |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Vedere le note.   | Il valore di questa proprietà deve essere l'etichetta del controllo documento. In genere, viene usato il titolo del documento.                             |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vedere le note.   | Stringa localizzata corrispondente al **tipo di controllo** Documento. Il valore predefinito è "document" per en-US o english (Stati Uniti).            |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Vedere le note.   | Il controllo documento ottiene in genere il nome dal nome file da cui viene caricato. Viene spesso visualizzato nel titolo di una finestra o di un frame contenitore. |



 

## <a name="required-control-patterns"></a>Pattern di controllo obbligatori

Nella tabella seguente sono elencati i Automazione interfaccia utente di controllo necessari per essere supportati dai controlli documento. Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Pattern di controllo/proprietà del pattern                  | Supporto/valore | Note                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider) | Dipende da       | Il controllo documento può estendersi oltre il riquadro di visualizzazione. Il controllo deve supportare il [pattern di controllo Scroll](uiauto-implementingscroll.md) se il contenuto è scorrevole.                                                                                                                              |
| [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider)     | Obbligatoria      | Tutti i controlli documento devono supportare il [pattern di controllo](uiauto-implementingtextandtextrange.md) Text.                                                                                                                                                                                                                |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)   | Dipende da       | Sebbene Automazione interfaccia utente client possano [**usare IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) per ottenere informazioni di testo su un documento, è necessario il pattern di controllo [Value](uiauto-implementingvalue.md) per impostare il valore interno. L'immissione di testo semplice è possibile solo tramite il pattern di controllo Value. |



 

## <a name="required-events"></a>Eventi obbligatori

Nella tabella seguente sono elencati gli Automazione interfaccia utente che i controlli documento devono supportare. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automazione interfaccia utente evento                                                                                                                                        | Note                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                           |                                                                                                                            |
| [**Interfaccia \_ utente Evento di modifica della proprietà BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md)                      |                                                                                                                            |
| [**Interfaccia \_ utente Evento di modifica della proprietà IsEnabledPropertyId.**](uiauto-automation-element-propids.md)                                      | Se il controllo supporta la [**proprietà IsEnabled,**](uiauto-automation-element-propids.md) deve supportare questo evento.   |
| [**Interfaccia \_ utente Evento di modifica della proprietà IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)                                  | Se il controllo supporta la [**proprietà IsOffscreen,**](uiauto-automation-element-propids.md) deve supportare questo evento. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                       |                                                                                                                            |
| [**Interfaccia \_ utente Evento di modifica della proprietà ScrollHorizontallyScrollablePropertyId.**](uiauto-control-pattern-propids.md)   | Se il controllo supporta il pattern [di controllo Scroll,](uiauto-implementingscroll.md) deve supportare questo evento.           |
| [**Interfaccia \_ utente Evento di modifica della proprietà ScrollHorizontalScrollPercentPropertyId.**](uiauto-control-pattern-propids.md) | Se il controllo supporta il pattern [di controllo Scroll,](uiauto-implementingscroll.md) deve supportare questo evento.           |
| [**Interfaccia \_ utente Evento di modifica della proprietà ScrollHorizontalViewSizePropertyId.**](uiauto-control-pattern-propids.md)           | Se il controllo supporta il pattern [di controllo Scroll,](uiauto-implementingscroll.md) deve supportare questo evento.           |
| [**Interfaccia \_ utente Evento di modifica della proprietà ScrollVerticallyScrollablePropertyId.**](uiauto-control-pattern-propids.md)       | Se il controllo supporta il pattern [di controllo Scroll,](uiauto-implementingscroll.md) deve supportare questo evento.           |
| [**Interfaccia \_ utente Evento di modifica della proprietà ScrollVerticalScrollPercentPropertyId.**](uiauto-control-pattern-propids.md)     | Se il controllo supporta il pattern [di controllo Scroll,](uiauto-implementingscroll.md) deve supportare questo evento.           |
| [**Interfaccia \_ utente Evento di modifica della proprietà ScrollVerticalViewSizePropertyId.**](uiauto-control-pattern-propids.md)               | Se il controllo supporta il pattern [di controllo Scroll,](uiauto-implementingscroll.md) deve supportare questo evento.           |
| [**UIA \_ Selection \_ InvalidatedEventId**](uiauto-event-ids.md)                                                            | Se il controllo supporta il pattern [di controllo Selection,](uiauto-implementingselection.md) deve supportare questo evento.     |
| [**UIA \_ Text \_ TextSelectionChangedEventId**](uiauto-event-ids.md)                                                    |                                                                                                                            |
| [**UIA \_ Text \_ TextChangedEventId**](uiauto-event-ids.md)                                                                      |                                                                                                                            |
| [**Interfaccia \_ utente Evento di modifica della proprietà ValueValuePropertyId.**](uiauto-control-pattern-propids.md)                                       | Se il controllo supporta il pattern [di controllo Value,](uiauto-implementingvalue.md) deve supportare questo evento.             |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente](uiauto-controltypesoverview.md)
</dt> <dt>

[Cenni preliminari su automazione interfaccia utente](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




