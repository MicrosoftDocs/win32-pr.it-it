---
title: Tipo di controllo ListItem
description: Questo argomento fornisce informazioni sul supporto di Microsoft Automazione interfaccia utente per il tipo di controllo ListItem.
ms.assetid: 8cb579ab-92c9-4311-aad7-5363f4cf2eaf
keywords:
- Automazione interfaccia utente,supporto per il tipo di controllo ListItem
- Automazione interfaccia utente,Tipo di controllo ListItem
- Automazione interfaccia utente,struttura ad albero per il tipo di controllo ListItem
- Automazione interfaccia utente,proprietà per il tipo di controllo ListItem
- Automazione interfaccia utente,pattern di controllo per il tipo di controllo ListItem
- Automazione interfaccia utente,events per il tipo di controllo ListItem
- strutture ad albero, tipo di controllo ListItem
- proprietà,Tipo di controllo ListItem
- pattern di controllo,tipo di controllo ListItem
- eventi, tipo di controllo ListItem
- supporto per il tipo di controllo ListItem
- Tipo di controllo ListItem
- tipi di controllo, struttura ad albero per il tipo di controllo ListItem
- tipi di controllo,pattern di controllo per il tipo di controllo ListItem
- tipi di controllo, supporto per ListItem
- tipi di controllo,ListItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cf7275212d44b795f354cb895c2d64727e375ea
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122483197"
---
# <a name="listitem-control-type"></a>Tipo di controllo ListItem

Questo argomento fornisce informazioni sul supporto microsoft Automazione interfaccia utente per il **tipo di controllo ListItem.**

I controlli elemento elenco sono un esempio di controlli che implementano il **tipo di controllo ListItem.**

Le sezioni seguenti definiscono la struttura ad Automazione interfaccia utente, le proprietà, i pattern di controllo e gli eventi necessari per il **tipo di controllo ListItem.** I Automazione interfaccia utente requisiti si applicano a tutti i controlli elemento elenco in cui il framework o la piattaforma dell'interfaccia utente Automazione interfaccia utente supporto per i tipi di controllo e i pattern di controllo.

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Pattern di controllo obbligatori](#required-control-patterns)
-   [Eventi obbligatori](#required-events)
-   [Osservazioni:](#remarks)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

La tabella seguente illustra un controllo tipico e una visualizzazione contenuto dell'albero Automazione interfaccia utente che riguarda i controlli elemento elenco e descrive cosa può essere contenuto in ogni visualizzazione. Per altre informazioni sull'albero Automazione interfaccia utente, vedere Panoramica Automazione interfaccia utente [albero](uiauto-treeoverview.md).




| Visualizzazione controlli | Visualizzazione contenuto | 
|--------------|--------------|
| <ul><li>ListItem<ul><li>Image (0 o più)</li><li>Text (0 o più)</li><li>Edit (0 o più)</li></ul></li></ul> | <ul><li>ListItem</li></ul> | 




 

Gli elementi figlio di un controllo elemento elenco all'interno della visualizzazione contenuto dell Automazione interfaccia utente albero devono sempre mostrare zero elementi figlio. Se la struttura del controllo è tale che altri elementi sono contenuti sotto l'elemento dell'elenco, deve seguire i requisiti per il supporto Automazione interfaccia utente per il [tipo di controllo TreeItem.](uiauto-supporttreeitemcontroltype.md)

## <a name="relevant-properties"></a>Proprietà rilevanti

Nella tabella seguente sono elencate le Automazione interfaccia utente il cui valore o definizione è particolarmente rilevante per il **tipo di controllo ListItem.** Per altre informazioni sulle Automazione interfaccia utente, vedere Recupero di proprietà [da Automazione interfaccia utente elementi](uiauto-propertiesforclients.md).



| Proprietà di automazione interfaccia utente                                                                                              | valore        | Note                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Vedere le note.   | Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata dell'Automazione interfaccia utente albero. Allocare la **proprietà AutomationId** per un elemento dell'elenco se l'elemento è noto per essere coerente tra istanze diverse dell'interfaccia utente. Se l'elemento dell'elenco viene popolato in modo dinamico e non prevedibile, lasciare vuota la **proprietà AutomationId.**                                                          |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vedere le note.   | Il valore di questa proprietà include l'area dei contenuti immagine e testo dell'elemento dell'elenco.                                                                                                                                                                                                                                                                                                                              |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Dipende da      | Se il controllo elenco ha un punto selezionabile (un punto su cui è possibile fare clic per fare in modo che l'elenco prenda lo stato attivo), tale punto deve essere esposto tramite questa proprietà. Se il controllo elenco è completamente coperto da elementi di elenco discendenti, restituirà l'errore [**UIA \_ E \_ NOCLICKABLEPOINT**](uiauto-error-codes.md) per indicare che il client deve richiedere un elemento all'interno del controllo elenco per un punto selezionabile. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **ListItem** | Questo valore è uguale per tutti i framework dell'interfaccia utente.                                                                                                                                                                                                                                                                                                                                                                                     |
| [**UIA \_ HelpTextPropertyId**](uiauto-automation-element-propids.md)                         | Vedere le note.   | Il testo della Guida per gli elenchi deve spiegare il motivo per cui all'utente viene chiesto di effettuare una selezione da un elenco di opzioni, che è in genere lo stesso tipo di informazioni visualizzate tramite una descrizione comando. Ad esempio, "Selezionare un elemento per impostare la risoluzione dello schermo per il monitoraggio".                                                                                                                                                    |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | **TRUE**     | Il controllo elenco è sempre incluso nella visualizzazione contenuto dell'Automazione interfaccia utente albero.                                                                                                                                                                                                                                                                                                                                                |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | **TRUE**     | Il controllo elenco è sempre incluso nella visualizzazione controlli dell'Automazione interfaccia utente albero.                                                                                                                                                                                                                                                                                                                                                |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Vedere le note.   | Se il contenitore può accettare l'input da tastiera, questo valore della proprietà deve essere **TRUE.**                                                                                                                                                                                                                                                                                                                                           |
| [**UIA \_ IsOffscreenPropertyId**](uiauto-automation-element-propids.md)                   | Dipende da      | Questa proprietà deve restituire un valore per indicare se l'elemento dell'elenco è attualmente in visualizzazione all'interno del contenitore padre che implementa il [pattern di controllo Scroll.](uiauto-implementingscroll.md)                                                                                                                                                                                                                                  |
| [**UIA \_ ItemStatusPropertyId**](uiauto-automation-element-propids.md)                     | Dipende da      | Se il controllo contiene lo stato che viene aggiornato dinamicamente, questa proprietà deve essere supportata in modo che un assistive technology possa ricevere aggiornamenti quando lo stato dell'elemento cambia.                                                                                                                                                                                                                                     |
| [**UIA \_ ItemTypePropertyId**](uiauto-automation-element-propids.md)                         | Dipende da      | Questa proprietà deve essere esposta per i controlli elemento elenco che rappresentano un oggetto sottostante. In genere, questi controlli elemento elenco includono un'icona associato al controllo che gli utenti associano all'oggetto sottostante.                                                                                                                                                                                                   |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Vedere le note.   | Se è presente un'etichetta di testo statico, questa proprietà deve esporre un riferimento a tale controllo.                                                                                                                                                                                                                                                                                                                                       |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vedere le note.   | Stringa localizzata corrispondente al **tipo di controllo ListItem.** Il valore predefinito è "list item" per en-US o English (Stati Uniti).                                                                                                                                                                                                                                                                                           |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Vedere le note.   | Il valore della proprietà name di un controllo elemento elenco deriva dall'etichetta di testo dell'elemento.                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="required-control-patterns"></a>Pattern di controllo obbligatori

Nella tabella seguente sono elencati i Automazione interfaccia utente di controllo necessari per essere supportati da tutti i controlli elemento elenco. Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Pattern di controllo                                                   | Supporto | Note                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Dipende da | Se l'elemento può essere modificato per visualizzare o nascondere informazioni, è necessario implementato il pattern di controllo [ExpandCollapse.](uiauto-implementingexpandcollapse.md)                                                                                                                                                                                                                        |
| [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)             | Dipende da | Se lo spostamento spaziale da elemento a elemento è supportato all'interno del contenitore elenco e il contenitore è organizzato in righe e colonne, è necessario implementato il pattern di [controllo GridItem.](uiauto-implementinggriditem.md)                                                                                                                                                                  |
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)                 | Dipende da | Se l'elemento dispone di un comando che può [](uiauto-implementinginvoke.md) essere eseguito su di esso, separato dalla selezione, è necessario che sia implementato il pattern di controllo Invoke. In genere si tratta di un'azione associata all'esecuzione del doppio clic sul controllo elemento elenco. Ad esempio, l'avvio di un documento Windows Explorer o la riproduzione di un file musicale in Microsoft Windows Media Player.        |
| [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider)         | Dipende da | Se l'elemento dell'elenco è contenuto in un contenitore scorrevole, è necessario implementato il pattern di [controllo ScrollItem.](uiauto-implementingscrollitem.md)                                                                                                                                                                                                                       |
| [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)   | Dipende da | Un controllo elemento elenco che supporta la selezione deve implementare il [pattern di controllo SelectionItem.](uiauto-implementingselectionitem.md) Ciò consente ai controlli elemento elenco di indicare quando sono selezionati.                                                                                                                                                                             |
| [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)                 | Dipende da | Se l'elemento dell'elenco è controllabile e l'azione non esegue una modifica dello stato di selezione, è necessario che sia implementato il pattern di controllo [Toggle.](uiauto-implementingtoggle.md)                                                                                                                                                                                                            |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)                   | Dipende da | Se l'elemento può essere modificato, [deve](uiauto-implementingvalue.md) essere implementato il pattern di controllo Value. Le modifiche al controllo elemento elenco causeranno modifiche ai valori delle proprietà [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md) e [**UIA \_ ValueValuePropertyId.**](uiauto-control-pattern-propids.md) |



 

## <a name="required-events"></a>Eventi obbligatori

Nella tabella seguente sono elencati Automazione interfaccia utente eventi che i controlli elemento elenco devono supportare. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automazione interfaccia utente evento                                                                                                                                                | Note                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                                   |                                                                                                                                  |
| [**Interfaccia \_ utente Evento di modifica della proprietà BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md)                              |                                                                                                                                  |
| [**Interfaccia \_ utente Evento di modifica della proprietà ExpandCollapseExpandCollapseStatePropertyId.**](uiauto-control-pattern-propids.md) | Se il controllo supporta il [pattern di controllo ExpandCollapse,](uiauto-implementingexpandcollapse.md) deve supportare questo evento. |
| [**UIA \_ Invoke \_ InvokedEventId**](uiauto-event-ids.md)                                                                                  | Se il controllo supporta il [pattern di controllo Invoke,](uiauto-implementinginvoke.md) deve supportare questo evento.                 |
| [**Interfaccia \_ utente Evento di modifica della proprietà IsEnabledPropertyId.**](uiauto-automation-element-propids.md)                                              | Se il controllo supporta la [**proprietà IsEnabled,**](uiauto-automation-element-propids.md) deve supportare questo evento.         |
| [**Interfaccia \_ utente Evento di modifica della proprietà IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)                                          | Se il controllo supporta la [**proprietà IsOffscreen,**](uiauto-automation-element-propids.md) deve supportare questo evento.       |
| [**Interfaccia \_ utente Evento di modifica della proprietà ItemStatusPropertyId.**](uiauto-automation-element-propids.md)                                            | Se il controllo supporta la [**proprietà ItemStatus,**](uiauto-automation-element-propids.md) è necessario supportare questo evento.        |
| [**Interfaccia \_ utente Evento di modifica**](uiauto-automation-element-propids.md) della proprietà NamePropertyId.                                                        |                                                                                                                                  |
| [**Elemento \_ UiA \_ SelectionItemAddedToSelectionEventId**](uiauto-event-ids.md)                                    | Se il controllo supporta il pattern [di controllo SelectionItem,](uiauto-implementingselectionitem.md) deve supportare questo evento.   |
| [**UIA \_ SelectionItem \_ ElementRemovedFromSelectionEventId**](uiauto-event-ids.md)                            | Se il controllo supporta il pattern [di controllo SelectionItem,](uiauto-implementingselectionitem.md) deve supportare questo evento.   |
| [**UIA \_ SelectionItem \_ ElementSelectedEventId**](uiauto-event-ids.md)                                                    | Se il controllo supporta il pattern [di controllo SelectionItem,](uiauto-implementingselectionitem.md) deve supportare questo evento.   |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                               |                                                                                                                                  |
| [**Interfaccia \_ utente Evento di modifica della proprietà ToggleToggleStatePropertyId.**](uiauto-control-pattern-propids.md)                                 | Se il controllo supporta il pattern di controllo [Toggle,](uiauto-implementingtoggle.md) deve supportare questo evento.                 |
| [**Interfaccia \_ utente Evento di modifica della proprietà ValueValuePropertyId.**](uiauto-control-pattern-propids.md)                                               | Se il controllo supporta il pattern [di controllo Value,](uiauto-implementingvalue.md) deve supportare questo evento.                   |



 

## <a name="remarks"></a>Commenti

Se un contenitore ospita elementi dell'elenco, il mezzo principale di spostamento deve passare agli elementi dell'elenco. L'inserimento dello stato attivo sui sottoelementi tramite la navigazione nell'elenco può generare confusione per gli utenti e gli strumenti di accessibilità. Se il contenitore ospita un elenco verticale di elementi, la pressione dei tasti FRECCIA SU e FRECCIA GIÙ deve spostarsi tra gli elementi, ma premendo i tasti FRECCIA DESTRA e FRECCIA SINISTRA è possibile passare ai sottoelementi dell'elemento attivo, ad esempio colonne elenco o sottoelementi dell'interfaccia utente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente](uiauto-controltypesoverview.md)
</dt> <dt>

[Cenni preliminari su automazione interfaccia utente](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




