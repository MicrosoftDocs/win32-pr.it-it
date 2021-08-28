---
title: Tipo di controllo MenuItem
description: In questo argomento vengono fornite informazioni sul supporto Automazione interfaccia utente Microsoft per il tipo di controllo MenuItem.
ms.assetid: a6a04489-8e28-44ff-a3b0-ecf19c24daab
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo MenuItem
- Automazione interfaccia utente, tipo di controllo MenuItem
- Automazione interfaccia utente struttura ad albero per il tipo di controllo MenuItem
- Automazione interfaccia utente,proprietà per il tipo di controllo MenuItem
- Automazione interfaccia utente,pattern di controllo per il tipo di controllo MenuItem
- Automazione interfaccia utente,events per il tipo di controllo MenuItem
- strutture ad albero, tipo di controllo MenuItem
- proprietà, tipo di controllo MenuItem
- pattern di controllo, tipo di controllo MenuItem
- eventi, tipo di controllo MenuItem
- supporto per il tipo di controllo MenuItem
- Tipo di controllo MenuItem
- tipi di controllo, struttura ad albero per il tipo di controllo MenuItem
- tipi di controllo, pattern di controllo per il tipo di controllo MenuItem
- tipi di controllo, supporto per MenuItem
- tipi di controllo, MenuItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a48b94d7fc18cb9a8a6fe924fb73a250ab28708
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482513"
---
# <a name="menuitem-control-type"></a>Tipo di controllo MenuItem

Questo argomento fornisce informazioni sul supporto di Microsoft Automazione interfaccia utente per il **tipo di controllo MenuItem.**

Un controllo menu consente l'organizzazione gerarchica degli elementi associati a comandi e gestori eventi. In una tipica applicazione Windows, una barra dei menu contiene diverse voci di menu (ad esempio **File** **,** Modifica e **Finestra**) e ogni voce di menu visualizza un menu. Un menu contiene una raccolta di voci di menu (ad esempio **Nuovo**, **Apri** e **Chiudi**), che può essere espansa per visualizzare altre voci di menu che, se selezionate, consentono di eseguire un'azione specifica.

Le sezioni seguenti definiscono la struttura ad Automazione interfaccia utente struttura ad albero, le proprietà, i pattern di controllo e gli eventi per il **tipo di controllo MenuItem.** I Automazione interfaccia utente si applicano a tutti i controlli voce di menu in cui il framework o la piattaforma dell'interfaccia utente si integra Automazione interfaccia utente per i tipi di controllo e i pattern di controllo.

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Pattern di controllo obbligatori](#required-control-patterns)
-   [Eventi obbligatori](#required-events)
-   [Problemi preesistenti](#legacy-issues)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

La tabella seguente illustra un controllo tipico e una visualizzazione contenuto dell'albero Automazione interfaccia utente relativo ai controlli voce di menu e descrive cosa può essere contenuto in ogni visualizzazione. Per altre informazioni sull'albero Automazione interfaccia utente, vedere Automazione interfaccia utente [Tree Overview](uiauto-treeoverview.md).




| Visualizzazione controlli | Visualizzazione contenuto | 
|--------------|--------------|
| <ul><li>MenuItem "?"<ul><li>Menu (sottomenu della voce di menu ? )<ul><li>MenuItem "Guida in linea"</li><li>MenuItem "Informazioni su Blocco note"</li></ul></li></ul></li></ul> | <ul><li>MenuItem "?"<ul><li>MenuItem "Guida in linea"</li><li>MenuItem "Informazioni su Blocco note"</li></ul></li></ul> | 




 

La visualizzazione controlli del controllo voce di menu ha la Automazione interfaccia utente struttura ad albero illustrata in precedenza. Si noti che la voce di menu **Guida** sulla barra dei menu è stata aggiunta per illustrare meglio la struttura.

Per la visualizzazione contenuto, **Menu** non è presente nell'albero Automazione interfaccia utente perché non fornisce informazioni significative all'utente finale.

## <a name="relevant-properties"></a>Proprietà rilevanti

La tabella seguente elenca le Automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per il **tipo di controllo MenuItem.** Per altre informazioni sulle Automazione interfaccia utente, vedere [Recupero di proprietà da Automazione interfaccia utente elementi](uiauto-propertiesforclients.md).



| Proprietà di automazione interfaccia utente                                                                                              | valore        | Note                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Vedere le note.   | Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata dell'Automazione interfaccia utente albero. Allocare **la proprietà AutomationId** per una voce di menu se è noto che l'elemento è coerente tra istanze diverse dell'interfaccia utente. Se la voce di menu viene popolata in modo dinamico e non prevedibile, lasciare **vuota la proprietà AutomationId.** |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vedere le note.   | Il rettangolo più esterno che contiene l'intero controllo.                                                                                                                                                                                                                                                                                                                 |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vedere le note.   | Supportata se è presente un rettangolo di delimitazione. Se non tutti i punti all'interno del rettangolo di delimitazione sono selezionabili e l'elemento esegue hit testing specializzati, eseguire l'override e fornire un punto selezionabile.                                                                                                                                                                     |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **MenuItem** |                                                                                                                                                                                                                                                                                                                                                                          |
| [**\_IsContentElementPropertyId dell'interfaccia utente**](uiauto-automation-element-propids.md)         | true         | Il controllo voce di menu è sempre incluso nella visualizzazione contenuto dell'Automazione interfaccia utente albero.                                                                                                                                                                                                                                                                                  |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | true         | Il controllo voce di menu è sempre incluso nella visualizzazione controlli dell'Automazione interfaccia utente albero.                                                                                                                                                                                                                                                                                  |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Vedere le note.   | Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.                                                                                                                                                                                                                                                                                                |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vedere le note.   | Stringa localizzata corrispondente al **tipo di controllo MenuItem.** Il valore predefinito è "voce di menu" per en-US o inglese (Stati Uniti).                                                                                                                                                                                                                                  |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Vedere le note.   | Il nome del controllo voce di menu è il testo usato per etichettarlo.                                                                                                                                                                                                                                                                                                          |



 

## <a name="required-control-patterns"></a>Pattern di controllo obbligatori

Nella tabella seguente sono elencati i Automazione interfaccia utente che devono essere supportati dai controlli voce di menu. Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Pattern di controllo                                                   | Supporto | Note                                                                                                                                                |
|-------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Dipende da | Se il controllo può essere espanso o compresso, [**implementare IExpandCollapseProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider)                            |
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)                 | Dipende da | Se il controllo esegue una singola azione o comando, implementare [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider).                                     |
| [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)   | Dipende da | Se il controllo viene usato per selezionare da un elenco di opzioni tra le voci di menu, implementare [**ISelectionItemProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider) |
| [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)                 | Dipende da | Se il controllo rappresenta un'opzione che può essere attivata o disattivata, implementare [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider).                       |



 

## <a name="required-events"></a>Eventi obbligatori

Nella tabella seguente sono elencati Automazione interfaccia utente eventi che i controlli voce di menu devono supportare. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automazione interfaccia utente evento                                                                                                                                                | Note                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                                   |                                                                                                                                  |
| [**Interfaccia \_ utente Evento di modifica della proprietà BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md)                              |                                                                                                                                  |
| [**Interfaccia \_ utente Evento di modifica della proprietà ExpandCollapseExpandCollapseStatePropertyId.**](uiauto-control-pattern-propids.md) | Se il controllo supporta il [pattern di controllo ExpandCollapse,](uiauto-implementingexpandcollapse.md) deve supportare questo evento. |
| [**UIA \_ Invoke \_ InvokedEventId**](uiauto-event-ids.md)                                                                                  | Se il controllo supporta il [pattern di controllo Invoke,](uiauto-implementinginvoke.md) deve supportare questo evento.                 |
| [**Interfaccia \_ utente Evento di modifica della proprietà IsEnabledPropertyId.**](uiauto-automation-element-propids.md)                                              | Se il controllo supporta la [**proprietà IsEnabled,**](uiauto-automation-element-propids.md) deve supportare questo evento.         |
| [**Interfaccia \_ utente Evento di modifica della proprietà IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)                                          | Se il controllo supporta la [**proprietà IsOffscreen,**](uiauto-automation-element-propids.md) deve supportare questo evento.       |
| [**Elemento \_ UiA \_ SelectionItemAddedToSelectionEventId**](uiauto-event-ids.md)                                    | Se il controllo supporta il pattern [di controllo SelectionItem,](uiauto-implementingselectionitem.md) deve supportare questo evento.   |
| [**UIA \_ SelectionItem \_ ElementRemovedFromSelectionEventId**](uiauto-event-ids.md)                            | Se il controllo supporta il pattern [di controllo SelectionItem,](uiauto-implementingselectionitem.md) deve supportare questo evento.   |
| [**UIA \_ SelectionItem \_ ElementSelectedEventId**](uiauto-event-ids.md)                                                    | Se il controllo supporta il pattern [di controllo SelectionItem,](uiauto-implementingselectionitem.md) deve supportare questo evento.   |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                               |                                                                                                                                  |
| [**Interfaccia \_ utente Evento di modifica della proprietà ToggleToggleStatePropertyId.**](uiauto-control-pattern-propids.md)                                 | Se il controllo supporta il pattern di controllo [Toggle,](uiauto-implementingtoggle.md) deve supportare questo evento.                 |



 

## <a name="legacy-issues"></a>Problemi preesistenti

Per le voci di menu Microsoft Win32, il pattern di controllo [Toggle](uiauto-implementingtoggle.md) è supportato solo quando è selezionata una voce di menu ed è possibile determinare a livello di codice se è necessario il supporto per il pattern di controllo Toggle. Poiché una voce di menu Win32 non espone se può essere selezionata, il pattern di controllo Richiama è supportato quando la voce di menu non è selezionata. Il pattern di controllo Invoke è sempre supportato, anche per le voci di menu necessarie solo per supportare il pattern di controllo Toggle. In questo modo i client non si confondono quando una voce di menu che supporta il pattern di controllo [Invoke](uiauto-implementinginvoke.md) (quando la voce di menu è stata deselezionata) non supporta più tale modello quando viene selezionata.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente](uiauto-controltypesoverview.md)
</dt> <dt>

[Cenni preliminari su automazione interfaccia utente](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




