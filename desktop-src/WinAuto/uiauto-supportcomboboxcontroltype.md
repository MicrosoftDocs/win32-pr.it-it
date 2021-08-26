---
title: Tipo di controllo ComboBox
description: In questo argomento vengono fornite informazioni sul supporto Automazione interfaccia utente Microsoft per il tipo di controllo ComboBox.
ms.assetid: e7c64dc1-e1e3-4f99-adde-d0d63eb6c4c9
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo ComboBox
- Automazione interfaccia utente,Tipo di controllo ComboBox
- Automazione interfaccia utente, struttura ad albero per il tipo di controllo ComboBox
- Automazione interfaccia utente,proprietà per il tipo di controllo ComboBox
- Automazione interfaccia utente,pattern di controllo per il tipo di controllo ComboBox
- Automazione interfaccia utente,eventi per il tipo di controllo ComboBox
- strutture ad albero, tipo di controllo ComboBox
- proprietà, tipo di controllo ComboBox
- pattern di controllo, tipo di controllo ComboBox
- eventi, tipo di controllo ComboBox
- supporto per il tipo di controllo ComboBox
- Tipo di controllo ComboBox
- tipi di controllo, struttura ad albero per il tipo di controllo ComboBox
- tipi di controllo, pattern di controllo per il tipo di controllo ComboBox
- tipi di controllo, supporto per ComboBox
- tipi di controllo, ComboBox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a9d9f38dab9877aee38773e5c900ee125d2ba6a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480107"
---
# <a name="combobox-control-type"></a>Tipo di controllo ComboBox

Questo argomento fornisce informazioni sul supporto di Microsoft Automazione interfaccia utente per il **tipo di controllo ComboBox.**

Una casella combinata è un casella di riepilogo combinata con un controllo statico o un controllo di modifica che visualizza l'elemento attualmente selezionato nel componente casella di riepilogo della casella combinata. Il componente casella di riepilogo del controllo viene visualizzato ogni volta o solo quando l'utente seleziona la freccia a discesa (un pulsante di comando) accanto al controllo. Se il campo di selezione è un controllo di modifica, l'utente può immettere informazioni non presenti nell'elenco. In caso contrario, l'utente può solo selezionare gli elementi nell'elenco.

Le sezioni seguenti definiscono la struttura Automazione interfaccia utente struttura ad albero, le proprietà, i pattern di controllo e gli eventi per il **tipo di controllo ComboBox.** I Automazione interfaccia utente si applicano a tutti i controlli casella combinata in cui il framework o la piattaforma dell'interfaccia utente si integra Automazione interfaccia utente per i tipi di controllo e i pattern di controllo.

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Pattern di controllo obbligatori](#required-control-patterns)
-   [Eventi obbligatori](#required-events)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

La tabella seguente illustra un controllo tipico e una visualizzazione contenuto dell'albero Automazione interfaccia utente relativo ai controlli casella combinata e descrive gli elementi che possono essere contenuti in ogni visualizzazione. Per altre informazioni sull'albero Automazione interfaccia utente, vedere Automazione interfaccia utente [Tree Overview](uiauto-treeoverview.md).




| Visualizzazione controlli | Visualizzazione contenuto | 
|--------------|--------------|
| <ul><li>ComboBox<ul><li>Edit (0 o 1)</li><li>Elenco (0 o 1)</li><li>List Item (elemento figlio di List; da 0 a molti)</li><li>Button (1)</li></ul></li></ul> | <ul><li>ComboBox<ul><li>List Item (da 0 a molti)</li></ul></li></ul> | 




 

Il controllo di modifica nella visualizzazione controlli della casella combinata è necessario solo se la casella combinata può essere  modificata per eseguire qualsiasi input, come nel caso della casella combinata nella finestra di dialogo Esegui.

## <a name="relevant-properties"></a>Proprietà rilevanti

La tabella seguente elenca le Automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per il **tipo di controllo ComboBox.** Per altre informazioni sulle Automazione interfaccia utente, vedere [Recupero di proprietà da Automazione interfaccia utente elementi](uiauto-propertiesforclients.md).



| Proprietà di automazione interfaccia utente                                                                                              | valore      | Note                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Vedere le note. | Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata dell'Automazione interfaccia utente albero.                                                                                                                                                                                                     |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vedere le note. | Il rettangolo più esterno che contiene l'intero controllo.                                                                                                                                                                                                                                                         |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vedere le note. | Supportata se è presente un rettangolo di delimitazione. Se non tutti i punti all'interno del rettangolo di delimitazione sono selezionabili e l'elemento esegue hit testing specializzati, eseguire l'override e fornire un punto selezionabile.                                                                                                             |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | ComboBox   |                                                                                                                                                                                                                                                                                                                  |
| [**UIA \_ HelpTextPropertyId**](uiauto-automation-element-propids.md)                         | Vedere le note. | Il testo della Guida per i controlli casella combinata deve spiegare perché all'utente viene chiesto di scegliere un'opzione dalla casella combinata. Il testo è simile a quello delle informazioni presentate in una descrizione comando. Ad esempio, "Selezionare un'opzione per impostare la risoluzione dello schermo".                                                |
| [**\_IsContentElementPropertyId dell'interfaccia utente**](uiauto-automation-element-propids.md)         | true       | I controlli casella combinata sono sempre inclusi nella visualizzazione contenuto dell'Automazione interfaccia utente albero.                                                                                                                                                                                                                            |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | true       | I controlli casella combinata sono sempre inclusi nella visualizzazione controlli dell'Automazione interfaccia utente albero.                                                                                                                                                                                                                            |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | true       | I controlli casella combinata possono ricevere lo stato attivo della tastiera. Tuttavia, quando un client Automazione interfaccia utente lo stato attivo su una casella combinata, qualsiasi elemento nel sottoalbero della casella combinata può ricevere lo stato attivo.                                                                                                                                          |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Vedere le note. | I controlli casella combinata in genere includono un'etichetta di testo statico a cui questa proprietà fa riferimento.                                                                                                                                                                                                                             |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vedere le note. | Stringa localizzata corrispondente al **tipo di controllo ComboBox.** Il valore predefinito è "casella combinata" per en-US o inglese (Stati Uniti).                                                                                                                                                                          |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Vedere le note. | Il nome del controllo casella combinata viene in genere generato da un'etichetta di testo statico. Se non è presente un'etichetta di testo statico, è necessario assegnare un valore per la **proprietà** Name. La **proprietà Name** non deve mai contenere il contenuto corrente della casella combinata o modificarla quando cambia il contenuto della casella combinata. |



 

## <a name="required-control-patterns"></a>Pattern di controllo obbligatori

Nella tabella seguente sono elencati i Automazione interfaccia utente di controllo personalizzati che devono essere supportati da tutti i controlli casella combinata. Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Pattern di controllo                                                   | Supporto  | Note                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Obbligatoria | Il [pattern di controllo ExpandCollapse](uiauto-implementingexpandcollapse.md) deve essere supportato perché un controllo casella combinata deve sempre contenere un pulsante a discesa.                                                                                                                                                                                |
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)           | Dipende da  | Visualizza la selezione corrente nella casella combinata. Il supporto per [il pattern di](uiauto-implementingselection.md) controllo Selection viene delegato alla casella di riepilogo sotto la casella combinata, ma potrebbe non essere sempre fattibile.                                                                                                                               |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)                   | Dipende da  | Se la casella combinata può assumere valori di testo arbitrari, il pattern [di](uiauto-implementingvalue.md) controllo Valore deve essere supportato. Questo modello consente di impostare il contenuto della stringa della casella combinata a livello di codice. Se il pattern di controllo Valore non è supportato, l'utente deve selezionare gli elementi dell'elenco all'interno del sottoalbero della casella combinata. |
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)                 | Mai    | Il [pattern di](uiauto-implementingscroll.md) controllo Scroll non è mai supportato direttamente in una casella combinata. È supportato se una casella di riepilogo contenuta in una casella combinata può scorrere e solo quando la casella di riepilogo è visibile sullo schermo.                                                                                                              |



 

## <a name="required-events"></a>Eventi obbligatori

Nella tabella seguente sono elencati Automazione interfaccia utente eventi che i controlli casella combinata devono supportare. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automazione interfaccia utente evento                                                                                                                                                | Note                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                                   |                                                                                                                            |
| [**Interfaccia \_ utente Evento di modifica della proprietà BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md)                              |                                                                                                                            |
| [**Interfaccia \_ utente Evento di modifica della proprietà IsEnabledPropertyId.**](uiauto-automation-element-propids.md)                                              | Se il controllo supporta la [**proprietà IsEnabled,**](uiauto-automation-element-propids.md) deve supportare questo evento.   |
| [**Interfaccia \_ utente Evento di modifica della proprietà IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)                                          | Se il controllo supporta la [**proprietà IsOffscreen,**](uiauto-automation-element-propids.md) deve supportare questo evento. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                               |                                                                                                                            |
| [**Interfaccia \_ utente Evento di modifica della proprietà ExpandCollapseExpandCollapseStatePropertyId.**](uiauto-control-pattern-propids.md) |                                                                                                                            |
| [**Interfaccia \_ utente Evento di modifica della proprietà ValueValuePropertyId.**](uiauto-control-pattern-propids.md)                                               | Se il controllo supporta il pattern [di controllo Value,](uiauto-implementingvalue.md) deve supportare questo evento.             |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente](uiauto-controltypesoverview.md)
</dt> <dt>

[Cenni preliminari su automazione interfaccia utente](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




