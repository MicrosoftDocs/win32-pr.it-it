---
title: Tipo di controllo Tab
description: In questo argomento vengono fornite informazioni sul supporto Automazione interfaccia utente microsoft per il tipo di controllo Tab.
ms.assetid: 49e3f025-f49b-44b1-90ca-09f40dce8f2a
keywords:
- Automazione interfaccia utente,supporto per il tipo di controllo Tab
- Automazione interfaccia utente,Tipo di controllo Tab
- Automazione interfaccia utente,struttura ad albero per il tipo di controllo Tab
- Automazione interfaccia utente,proprietà per il tipo di controllo Tab
- Automazione interfaccia utente,pattern di controllo per il tipo di controllo Tab
- Automazione interfaccia utente,eventi per il tipo di controllo Tab
- strutture ad albero, tipo di controllo Tab
- proprietà, tipo di controllo Tab
- pattern di controllo, tipo di controllo Tab
- eventi, tipo di controllo Tab
- Supporto per il tipo di controllo Tab
- Tab (tipo di controllo)
- tipi di controllo, struttura ad albero per il tipo di controllo Tab
- tipi di controllo, pattern di controllo per il tipo di controllo Tab
- tipi di controllo, supporto per Tab
- tipi di controllo, tab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6a83263db87a68e258598ea46ca903af2ddb39c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482497"
---
# <a name="tab-control-type"></a>Tipo di controllo Tab

In questo argomento vengono fornite informazioni sul supporto Automazione interfaccia utente microsoft per il **tipo di controllo** Tab.

Un controllo Struttura a schede è simile ai separatori in un blocco per appunti o alle etichette in un archivio. L'uso del controllo Struttura a schede consente a un'applicazione di definire più pagine per la stessa area di una finestra o una finestra di dialogo.

Le sezioni seguenti definiscono la struttura ad Automazione interfaccia utente struttura ad albero, le proprietà, i pattern di controllo e gli eventi per il **tipo di controllo** Tab. I Automazione interfaccia utente si applicano a tutti i controlli struttura a schede in cui il framework o la piattaforma dell'interfaccia utente Automazione interfaccia utente il supporto per i tipi di controllo e i pattern di controllo.

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Pattern di controllo obbligatori](#required-control-patterns)
-   [Eventi obbligatori](#required-events)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

La tabella seguente illustra un controllo tipico e una visualizzazione contenuto dell'albero Automazione interfaccia utente relativo ai controlli struttura a schede e descrive gli elementi che possono essere contenuti in ogni visualizzazione. Per altre informazioni sull'albero Automazione interfaccia utente, vedere Automazione interfaccia utente [Tree Overview](uiauto-treeoverview.md).




| Visualizzazione controlli | Visualizzazione contenuto | 
|--------------|--------------|
| <ul><li>Scheda<ul><li>TabItem (1 o più)</li><li>ScrollBar (0 o 1)<ul><li>Button (0 o 2)</li></ul></li></ul></li></ul> | <ul><li>Scheda<ul><li>TabItem (1 o più)</li></ul></li></ul> | 




 

I controlli Struttura a schede Automazione interfaccia utente elementi figlio in base al [tipo di controllo TabItem.](uiauto-supporttabitemcontroltype.md) Quando gli elementi della scheda sono raggruppati( ad esempio, come nelle  applicazioni Microsoft Office), il tipo di controllo Scheda può ospitare anche i tipi di controllo Gruppi per gli elementi delle schede raggruppate, come illustrato nella struttura ad albero seguente. 




| Visualizzazione controlli | Visualizzazione contenuto | 
|--------------|--------------|
| <ul><li>Scheda<ul><li>TabItem (1 o più)</li><li>Group (0 o più)<ul><li>TabItem (0 o più)</li></ul></li><li>ScrollBar (0 o 1)<ul><li>Button (0 o 2)</li></ul></li></ul></li></ul> | <ul><li>Scheda<ul><li>TabItem (1 o più)</li><li>Group (0 o più)<ul><li>TabItem (0 o più)</li></ul></li></ul></li></ul> | 




 

## <a name="relevant-properties"></a>Proprietà rilevanti

La tabella seguente elenca le proprietà Automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per i controlli struttura a schede. Per altre informazioni sulle Automazione interfaccia utente, vedere [Recupero di proprietà da Automazione interfaccia utente elementi](uiauto-propertiesforclients.md).



| Proprietà di automazione interfaccia utente                                                                                              | valore      | Note                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Vedere le note. | Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata dell'Automazione interfaccia utente albero.                                                                                                                                                                                                                                                                  |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vedere le note. | Il rettangolo più esterno che contiene l'intero controllo.                                                                                                                                                                                                                                                                                                                      |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | No         | Il controllo Struttura a schede non dispone di punti selezionabili.                                                                                                                                                                                                                                                                                                                               |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **TAB**    |                                                                                                                                                                                                                                                                                                                                                                               |
| [**\_IsContentElementPropertyId dell'interfaccia utente**](uiauto-automation-element-propids.md)         | true       | Il controllo Struttura a schede è sempre incluso nella visualizzazione contenuto dell'Automazione interfaccia utente struttura ad albero.                                                                                                                                                                                                                                                                                             |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | true       | Il controllo Struttura a schede è sempre incluso nella visualizzazione controlli dell'Automazione interfaccia utente struttura ad albero.                                                                                                                                                                                                                                                                                             |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | true       | Il tipo di controllo Tab deve essere in grado di ricevere lo stato attivo. In genere, un client Automazione interfaccia utente chiama [**IUIAutomationElement::SetFocus**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-setfocus) su un controllo struttura a schede e uno dei relativi elementi inoltra lo stato attivo della tastiera al controllo Struttura a schede. È possibile che alcuni contenitori di schede assumano lo stato attivo senza che lo stato attivo venga impostato su uno dei relativi elementi. |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Vedere le note. | I controlli Struttura a schede in genere includono un'etichetta di testo statico che viene esposta tramite questa proprietà.                                                                                                                                                                                                                                                                                        |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vedere le note. | Stringa localizzata corrispondente al **tipo di controllo** Tab. Il valore predefinito è "tab" per en-US o english (Stati Uniti).                                                                                                                                                                                                                                                  |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Vedere le note. | Il controllo Struttura a schede raramente richiede **una proprietà** Name.                                                                                                                                                                                                                                                                                                                          |
| [**UIA \_ OrientationPropertyId**](uiauto-automation-element-propids.md)                   | Vedere le note. | Il controllo Struttura a schede deve sempre indicare se è posizionato orizzontalmente o verticalmente.                                                                                                                                                                                                                                                                                     |



 

## <a name="required-control-patterns"></a>Pattern di controllo obbligatori

Nella tabella seguente sono elencati i Automazione interfaccia utente che devono essere supportati da tutti i controlli struttura a schede. Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Pattern di controllo/proprietà del pattern                                             | Supporto/valore | Note                                                                                                                                                                  |
|------------------------------------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)                      | Obbligatoria      | Tutti i controlli Struttura a schede devono supportare il [pattern di](uiauto-implementingselection.md) controllo Selezione.                                                                       |
| [**IsSelectionRequired**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired) | true          | I controlli Struttura a schede richiedono sempre una selezione.                                                                                                                  |
| [**CanSelectMultiple**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple)     | FALSE         | I controlli Struttura a schede sono sempre contenitori a selezione singola.                                                                                                                   |
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)                            | Dipende da       | Il [pattern di](uiauto-implementingscroll.md) controllo Scroll deve essere supportato se il controllo Struttura a schede include widget che consentono lo scorrimento di un set di elementi della scheda. |



 

## <a name="required-events"></a>Eventi obbligatori

Nella tabella seguente sono elencati Automazione interfaccia utente eventi che i controlli Struttura a schede devono supportare. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automazione interfaccia utente evento                                                                                                                                        | Note                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                           |                                                                                                                            |
| [**Interfaccia \_ utente Evento di modifica della proprietà BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md)                      |                                                                                                                            |
| [**Interfaccia \_ utente Evento di modifica della proprietà IsEnabledPropertyId.**](uiauto-automation-element-propids.md)                                      | Se il controllo supporta la [**proprietà IsEnabled,**](uiauto-automation-element-propids.md) deve supportare questo evento.   |
| [**Interfaccia \_ utente Evento di modifica della proprietà IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)                                  | Se il controllo supporta la [**proprietà IsOffscreen,**](uiauto-automation-element-propids.md) deve supportare questo evento. |
| [**Interfaccia \_ utente Evento di modifica della proprietà ScrollHorizontallyScrollablePropertyId.**](uiauto-control-pattern-propids.md)   | Se il controllo supporta il pattern [di controllo Scroll,](uiauto-implementingscroll.md) deve supportare questo evento.           |
| [**Interfaccia \_ utente Evento di modifica della proprietà ScrollHorizontalScrollPercentPropertyId.**](uiauto-control-pattern-propids.md) | Se il controllo supporta il pattern [di controllo Scroll,](uiauto-implementingscroll.md) deve supportare questo evento.           |
| [**Interfaccia \_ utente Evento di modifica della proprietà ScrollHorizontalViewSizePropertyId.**](uiauto-control-pattern-propids.md)           | Se il controllo supporta il pattern [di controllo Scroll,](uiauto-implementingscroll.md) deve supportare questo evento.           |
| [**Interfaccia \_ utente Evento di modifica della proprietà ScrollVerticallyScrollablePropertyId.**](uiauto-control-pattern-propids.md)       | Se il controllo supporta il pattern [di controllo Scroll,](uiauto-implementingscroll.md) deve supportare questo evento.           |
| [**Interfaccia \_ utente Evento di modifica della proprietà ScrollVerticalScrollPercentPropertyId.**](uiauto-control-pattern-propids.md)     | Se il controllo supporta il pattern [di controllo Scroll,](uiauto-implementingscroll.md) deve supportare questo evento.           |
| [**Interfaccia \_ utente Evento di modifica della proprietà ScrollVerticalViewSizePropertyId.**](uiauto-control-pattern-propids.md)               | Se il controllo supporta il pattern [di controllo Scroll,](uiauto-implementingscroll.md) deve supportare questo evento.           |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                       |                                                                                                                            |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente](uiauto-controltypesoverview.md)
</dt> <dt>

[Cenni preliminari su automazione interfaccia utente](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




