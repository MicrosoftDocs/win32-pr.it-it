---
title: Tipo di controllo Albero
description: Questo argomento fornisce informazioni sul supporto microsoft Automazione interfaccia utente per il tipo di controllo Albero.
ms.assetid: 0fa8f308-7815-4561-a1ce-c5f5582861da
keywords:
- Automazione interfaccia utente,supporto per il tipo di controllo Tree
- Automazione interfaccia utente,Tipo di controllo Albero
- Automazione interfaccia utente,struttura ad albero per il tipo di controllo Tree
- Automazione interfaccia utente,proprietà per il tipo di controllo Tree
- Automazione interfaccia utente,pattern di controllo per il tipo di controllo Tree
- Automazione interfaccia utente,events per il tipo di controllo Tree
- strutture ad albero, tipo di controllo Tree
- proprietà,tipo di controllo Tree
- pattern di controllo, tipo di controllo Tree
- eventi, tipo di controllo Tree
- supporto per il tipo di controllo Tree
- Tree (tipo di controllo)
- tipi di controllo, struttura ad albero per il tipo di controllo Tree
- tipi di controllo, pattern di controllo per il tipo di controllo Tree
- tipi di controllo, supporto per Tree
- tipi di controllo,albero
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea7ac6330428c2e79fca1e9a51d4ca0f7c63e8a7
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472847"
---
# <a name="tree-control-type"></a>Tipo di controllo Albero

Questo argomento fornisce informazioni sul supporto di Microsoft Automazione interfaccia utente per il **tipo di controllo Albero.**

Il **tipo di** controllo Albero viene usato per i contenitori il cui contenuto è rilevante come gerarchia di nodi, come nel modo in cui file e cartelle vengono visualizzati nel riquadro sinistro di Windows Explorer. Ciascun nodo può potenzialmente contenere altri nodi, denominati nodi figlio. I nodi padre, ovvero i nodi contenenti nodi figlio, possono essere visualizzati in formato espanso o compresso. Il Windows di visualizzazione albero ( identificato da [**WC \_ TREEVIEW**](/windows/desktop/Controls/common-control-window-classes)) è un esempio di un controllo appartenente al tipo di controllo **Tree.**

Le sezioni seguenti definiscono la struttura ad Automazione interfaccia utente, le proprietà, i pattern di controllo e gli eventi necessari per il **tipo di controllo Tree.** I Automazione interfaccia utente requisiti si applicano a tutti i controlli degli elementi della struttura ad albero in cui il framework o la piattaforma dell'interfaccia utente integra Automazione interfaccia utente per i tipi di controllo e i pattern di controllo.

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Pattern di controllo obbligatori](#required-control-patterns)
-   [Eventi obbligatori](#required-events)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

La tabella seguente illustra un controllo tipico e una visualizzazione contenuto dell'albero Automazione interfaccia utente che riguarda i controlli struttura ad albero e descrive cosa può essere contenuto in ogni visualizzazione. Per altre informazioni sull'albero Automazione interfaccia utente, vedere panoramica Automazione interfaccia utente [albero](uiauto-treeoverview.md).




| Visualizzazione controlli | Visualizzazione contenuto | 
|--------------|--------------|
| <ul><li>Albero<ul><li>DataItem (0 o più)</li><li>TreeItem (0 o più)<ul><li>TreeItem (0 o più)<ul><li>...</li></ul></li></ul></li><li>ScrollBar (0, 1, 2)</li></ul></li></ul> | <ul><li>Albero<ul><li>DataItem (0 o più)</li><li>TreeItem (0 o più)<ul><li>TreeItem (0 o più)<ul><li>...</li></ul></li></ul></li></ul></li></ul> | 




 

La visualizzazione di controllo dell'Automazione interfaccia utente struttura ad albero è costituita da:

-   Zero di molti elementi all'interno del contenitore (gli elementi possono essere basati sui tipi di controllo [TreeItem](uiauto-supporttreeitemcontroltype.md) o [DataItem).](uiauto-supportdataitemcontroltype.md)
-   Zero, uno o due controlli barra di scorrimento

La visualizzazione contenuto dell'albero Automazione interfaccia utente è costituita da zero o molti elementi all'interno del contenitore (gli elementi possono essere basati sui tipi di controllo [TreeItem](uiauto-supporttreeitemcontroltype.md) o [DataItem).](uiauto-supportdataitemcontroltype.md)

## <a name="relevant-properties"></a>Proprietà rilevanti

Nella tabella seguente sono elencate le Automazione interfaccia utente il cui valore o definizione è particolarmente rilevante per il **tipo di controllo Tree.** Per altre informazioni sulle Automazione interfaccia utente, vedere Recupero di proprietà [da Automazione interfaccia utente elementi](uiauto-propertiesforclients.md).



| Proprietà di automazione interfaccia utente                                                                                              | valore      | Note                                                                                                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Vedere le note. | Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata dell'Automazione interfaccia utente albero.                                                                                                                                                                               |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vedere le note. | Il rettangolo più esterno che contiene l'intero controllo.                                                                                                                                                                                                                                   |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vedere le note. | I controlli struttura ad albero hanno un punto selezionabile che fa sì che l'albero o uno degli elementi nel contenitore della struttura ad albero riceva lo stato attivo. Un controllo struttura ad albero può avere un punto selezionabile solo se è possibile fare clic su una posizione nell'albero senza causare la selezione di un elemento o la ricezione dello stato attivo. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Albero**   | Questo valore è uguale per tutti i framework dell'interfaccia utente.                                                                                                                                                                                                                                              |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | true       | Il controllo struttura ad albero è sempre incluso nella visualizzazione contenuto dell'Automazione interfaccia utente albero.                                                                                                                                                                                                         |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | true       | Il controllo struttura ad albero è sempre incluso nella visualizzazione controlli dell'Automazione interfaccia utente albero.                                                                                                                                                                                                         |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Vedere le note. | Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.                                                                                                                                                                                                                  |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Vedere le note. | Se al controllo struttura ad albero è associata un'etichetta, questa proprietà restituisce un puntatore [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) per tale etichetta. In caso contrario, la proprietà restituisce un riferimento Null.                                                                          |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vedere le note. | Stringa localizzata corrispondente al **tipo di controllo** Albero. Il valore predefinito è "tree" per en-US o english (Stati Uniti).                                                                                                                                                             |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Vedere le note. | Il valore della proprietà name di un controllo struttura in genere deriva dal testo dell'etichetta del controllo. Se non è presente alcuna etichetta di testo, è necessario specificare un valore per questa proprietà.                                                                                                                        |



 

## <a name="required-control-patterns"></a>Pattern di controllo obbligatori

Nella tabella seguente sono elencati i Automazione interfaccia utente di controllo che devono essere supportati da tutti i controlli struttura ad albero. Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Pattern di controllo/proprietà del pattern                                             | Supporto/valore | Note                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)                            | Dipende da       | Implementare [il pattern di](uiauto-implementingscroll.md) controllo Scroll se è possibile scorrere gli elementi nel contenitore della struttura ad albero.                                                                                                                 |
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)                      | Dipende da       | I controlli struttura ad albero che contengono un set di elementi selezionabili devono implementare il [pattern di controllo Selection.](uiauto-implementingselection.md) Non deve essere implementato se la selezione di un elemento non fornisce informazioni significative all'utente. |
| [**CanSelectMultiple**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple)     | Vedere le note.    | Implementare questa proprietà se il controllo struttura supporta la selezione multipla (la maggior parte dei controlli struttura non supporta la selezione multipla).                                                                                                       |
| [**IsSelectionRequired**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired) | Vedere le note.    | Il valore di questa proprietà viene esposta quando il controllo richiede la selezione di un elemento.                                                                                                                                               |



 

## <a name="required-events"></a>Eventi obbligatori

Nella tabella seguente sono elencati Automazione interfaccia utente eventi che tutti i controlli struttura ad albero devono supportare. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automazione interfaccia utente evento                                                                                                                                        | Note                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                           |                                                                                                                            |
| [**Interfaccia \_ utente Evento di modifica della proprietà BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md)                      |                                                                                                                            |
| [**Interfaccia \_ utente Evento di modifica della proprietà IsEnabledPropertyId.**](uiauto-automation-element-propids.md)                                      | Se il controllo supporta la [**proprietà IsEnabled,**](uiauto-automation-element-propids.md) deve supportare questo evento.   |
| [**Interfaccia \_ utente Evento di modifica della proprietà IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)                                  | Se il controllo supporta la [**proprietà IsOffscreen,**](uiauto-automation-element-propids.md) deve supportare questo evento. |
| [**Interfaccia \_ utente Evento di modifica della proprietà ScrollHorizontallyScrollablePropertyId.**](uiauto-control-pattern-propids.md)   | Se il controllo supporta il pattern [di controllo Scroll,](uiauto-implementingscroll.md) deve supportare questo evento.           |
| [**Interfaccia \_ utente Evento di modifica della proprietà ScrollHorizontalScrollPercentPropertyId.**](uiauto-control-pattern-propids.md) | Se il controllo supporta il pattern [di controllo Scroll,](uiauto-implementingscroll.md) deve supportare questo evento.           |
| [**Interfaccia \_ utente Evento di modifica della proprietà ScrollHorizontalViewSizePropertyId.**](uiauto-control-pattern-propids.md)           | Se il controllo supporta il pattern [di controllo Scroll,](uiauto-implementingscroll.md) deve supportare questo evento.           |
| [**Interfaccia \_ utente Evento di modifica della proprietà ScrollVerticalScrollPercentPropertyId.**](uiauto-control-pattern-propids.md)     | Se il controllo supporta il pattern [di controllo Scroll,](uiauto-implementingscroll.md) deve supportare questo evento.           |
| [**Interfaccia \_ utente Evento di modifica della proprietà ScrollVerticallyScrollablePropertyId.**](uiauto-control-pattern-propids.md)       | Se il controllo supporta il pattern [di controllo Scroll,](uiauto-implementingscroll.md) deve supportare questo evento.           |
| [**Interfaccia \_ utente Evento di modifica della proprietà ScrollVerticalViewSizePropertyId.**](uiauto-control-pattern-propids.md)               | Se il controllo supporta il pattern [di controllo Scroll,](uiauto-implementingscroll.md) deve supportare questo evento.           |
| [**UIA \_ Selection \_ InvalidatedEventId**](uiauto-event-ids.md)                                                            | Se il controllo supporta il pattern [di controllo Selection,](uiauto-implementingselection.md) deve supportare questo evento.     |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                       |                                                                                                                            |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente](uiauto-controltypesoverview.md)
</dt> <dt>

[Cenni preliminari su automazione interfaccia utente](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 
