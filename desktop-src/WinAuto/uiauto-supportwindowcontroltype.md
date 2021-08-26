---
title: Tipo di controllo Finestra
description: In questo argomento vengono fornite informazioni sul supporto Automazione interfaccia utente microsoft per il tipo di controllo Window.
ms.assetid: 521fb514-e083-48b3-b4a0-52c530154740
keywords:
- Automazione interfaccia utente,supporto per il tipo di controllo Window
- Automazione interfaccia utente,Tipo di controllo Finestra
- Automazione interfaccia utente,struttura ad albero per il tipo di controllo Window
- Automazione interfaccia utente,proprietà per il tipo di controllo Window
- Automazione interfaccia utente,pattern di controllo per il tipo di controllo Window
- Automazione interfaccia utente,eventi per il tipo di controllo Window
- strutture ad albero, tipo di controllo Window
- proprietà, tipo di controllo Window
- pattern di controllo, tipo di controllo Window
- eventi, tipo di controllo Window
- supporto per il tipo di controllo Window
- Window (tipo di controllo)
- tipi di controllo, struttura ad albero per il tipo di controllo Finestra
- tipi di controllo, pattern di controllo per il tipo di controllo Finestra
- tipi di controllo, supporto per Window
- tipi di controllo, finestra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59486f12545c0dbe6b38e20e29f6df5397cbca21
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466418"
---
# <a name="window-control-type"></a>Tipo di controllo Finestra

In questo argomento vengono fornite informazioni sul supporto Automazione interfaccia utente Microsoft per il **tipo di controllo** Window.

Il controllo finestra è costituito dalla cornice della finestra, che contiene oggetti figlio, ad esempio barra del titolo, oggetti client e altri oggetti.

Le sezioni seguenti definiscono la struttura ad Automazione interfaccia utente struttura ad albero, le proprietà, i pattern di controllo e gli eventi per il **tipo di controllo** Window. I Automazione interfaccia utente si applicano a tutti i controlli finestra in cui il framework/piattaforma dell'interfaccia utente si integra Automazione interfaccia utente per i tipi di controllo e i pattern di controllo.

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Pattern di controllo obbligatori](#required-control-patterns)
-   [Eventi obbligatori](#required-events)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

La tabella seguente illustra un controllo tipico e una visualizzazione contenuto dell'albero Automazione interfaccia utente relativo ai controlli finestra e descrive gli elementi che possono essere contenuti in ogni visualizzazione. Per altre informazioni sull'albero Automazione interfaccia utente, vedere Automazione interfaccia utente [Tree Overview](uiauto-treeoverview.md).




| Visualizzazione controlli | Visualizzazione contenuto | 
|--------------|--------------|
| <ul><li>Finestra</li></ul> | <ul><li>Finestra</li></ul> | 




 

## <a name="relevant-properties"></a>Proprietà rilevanti

La tabella seguente elenca le proprietà Automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per i controlli finestra. Per altre informazioni sulle Automazione interfaccia utente, vedere [Recupero di proprietà da Automazione interfaccia utente elementi](uiauto-propertiesforclients.md).



| Proprietà di automazione interfaccia utente                                                                                              | valore      | Note                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Vedere le note. | Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata dell'Automazione interfaccia utente albero.                                            |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vedere le note. | Il rettangolo più esterno che contiene l'intero controllo.                                                                                                |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vedere le note. | Il controllo finestra deve avere un punto selezionabile che fa sì che la finestra diventi selezionata o deselezionata.                                                 |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Window** | Questo valore è uguale per tutti i framework dell'interfaccia utente.                                                                                                           |
| [**\_IsContentElementPropertyId dell'interfaccia utente**](uiauto-automation-element-propids.md)         | true       | Il controllo finestra è sempre incluso nella visualizzazione contenuto dell'Automazione interfaccia utente struttura ad albero.                                                                    |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | true       | Il controllo finestra è sempre incluso nella visualizzazione controlli dell'Automazione interfaccia utente struttura ad albero.                                                                    |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Vedere le note. | Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.                                                                               |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULL       | I controlli finestra non hanno un'etichetta di finestra statica.                                                                                                      |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vedere le note. | Stringa localizzata corrispondente al **tipo di controllo** Window. Il valore predefinito è "window" per en-US o english (Stati Uniti).                      |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Vedere le note. | Il controllo finestra contiene sempre un elemento finestra primario correlato a ciò che l'utente associerebbe come identificatore più semantico per l'elemento. |



 

## <a name="required-control-patterns"></a>Pattern di controllo obbligatori

Nella tabella seguente sono elencati i Automazione interfaccia utente che devono essere supportati dai controlli finestra. Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Pattern di controllo/proprietà del pattern                        | Supporto/valore | Note                                                                                                                                                                        |
|---------------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider)           | Condizionale   | Il pattern di controllo [Dock](uiauto-implementingdock.md) deve essere supportato se la finestra può essere ancorata.                                                                       |
| [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) | Obbligatoria      | Il [pattern](uiauto-implementingtransform.md) di controllo Transform consente di spostare, ridimensionare o ruotare la finestra sullo schermo. Non si applica alle app Windows Store. |
| [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider)       | Obbligatoria      | Il [pattern di](uiauto-implementingwindow.md) controllo Window abilita operazioni specifiche per la finestra.                                                                      |



 

## <a name="required-events"></a>Eventi obbligatori

La tabella seguente elenca gli Automazione interfaccia utente che **i controlli Window** devono supportare. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automazione interfaccia utente eventi                                                                                                                                        | Note                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AsyncContentLoadedEventId**](uiauto-event-ids.md)                                                                   |                                                                                                                                                                                                                           |
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                           |                                                                                                                                                                                                                           |
| [**Interfaccia \_ utente Evento di modifica della proprietà BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md)                      |                                                                                                                                                                                                                           |
| [**Interfaccia \_ utente Evento di modifica della proprietà IsEnabledPropertyId.**](uiauto-automation-element-propids.md)                                      | Se il controllo supporta la [**proprietà IsEnabled,**](uiauto-automation-element-propids.md) deve supportare questo evento.                                                                                                  |
| [**Interfaccia \_ utente Evento di modifica della proprietà IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)                                  | Se il controllo supporta la [**proprietà IsOffscreen,**](uiauto-automation-element-propids.md) deve supportare questo evento.                                                                                                |
| [**Layout \_ dell'interfaccia utenteInvalidatedEventId**](uiauto-event-ids.md)                                                                     |                                                                                                                                                                                                                           |
| [**Interfaccia \_ utente Evento di modifica**](uiauto-automation-element-propids.md) della proprietà NamePropertyId.                                                |                                                                                                                                                                                                                           |
| [**Interfaccia \_ utente Evento di modifica della proprietà ScrollHorizontallyScrollablePropertyId.**](uiauto-control-pattern-propids.md)   | Se il controllo supporta il pattern [di controllo Scroll,](uiauto-implementingscroll.md) deve supportare questo evento.                                                                                                          |
| [**Interfaccia \_ utente Evento di modifica della proprietà ScrollHorizontalScrollPercentPropertyId.**](uiauto-control-pattern-propids.md) | Se il controllo supporta il pattern [di controllo Scroll,](uiauto-implementingscroll.md) deve supportare questo evento.                                                                                                          |
| [**Interfaccia \_ utente Evento di modifica della proprietà ScrollHorizontalViewSizePropertyId.**](uiauto-control-pattern-propids.md)           | Se il controllo supporta il pattern [di controllo Scroll,](uiauto-implementingscroll.md) deve supportare questo evento.                                                                                                          |
| [**Interfaccia \_ utente Evento di modifica della proprietà ScrollVerticallyScrollablePropertyId.**](uiauto-control-pattern-propids.md)       | Se il controllo supporta il pattern [di controllo Scroll,](uiauto-implementingscroll.md) deve supportare questo evento.                                                                                                          |
| [**Interfaccia \_ utente Evento di modifica della proprietà ScrollVerticalScrollPercentPropertyId.**](uiauto-control-pattern-propids.md)     | Se il controllo supporta il pattern [di controllo Scroll,](uiauto-implementingscroll.md) deve supportare questo evento.                                                                                                          |
| [**Interfaccia \_ utente Evento di modifica della proprietà ScrollVerticalViewSizePropertyId.**](uiauto-control-pattern-propids.md)               | Se il controllo supporta il pattern [di controllo Scroll,](uiauto-implementingscroll.md) deve supportare questo evento.                                                                                                          |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                       |                                                                                                                                                                                                                           |
| [**UIA \_ Window \_ WindowClosedEventId**](uiauto-event-ids.md)                                                                |                                                                                                                                                                                                                           |
| [**UIA \_ Window \_ WindowOpenedEventId**](uiauto-event-ids.md)                                                                |                                                                                                                                                                                                                           |
| [**Interfaccia \_ utente Evento di modifica della proprietà WindowWindowVisualStatePropertyId.**](uiauto-control-pattern-propids.md)             | Se il controllo supporta la [**proprietà WindowVisualState**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationwindowpattern-get_cachedwindowvisualstate) del pattern [di controllo Window,](uiauto-implementingwindow.md) questo evento deve essere supportato. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente](uiauto-controltypesoverview.md)
</dt> <dt>

[Cenni preliminari su automazione interfaccia utente](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




