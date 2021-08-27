---
title: Tipo di controllo ToolBar
description: In questo argomento vengono fornite informazioni sul supporto Automazione interfaccia utente microsoft per il tipo di controllo ToolBar. I controlli barra degli strumenti consentono agli utenti finali di attivare comandi e strumenti contenuti in un'applicazione.
ms.assetid: e2a72ce3-5263-43f8-be4d-715a78224b68
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo ToolBar
- Automazione interfaccia utente, tipo di controllo ToolBar
- Automazione interfaccia utente,struttura ad albero per il tipo di controllo ToolBar
- Automazione interfaccia utente,proprietà per il tipo di controllo ToolBar
- Automazione interfaccia utente,pattern di controllo per il tipo di controllo ToolBar
- Automazione interfaccia utente,eventi per il tipo di controllo ToolBar
- strutture ad albero, tipo di controllo ToolBar
- proprietà, tipo di controllo ToolBar
- pattern di controllo, tipo di controllo ToolBar
- eventi, tipo di controllo ToolBar
- supporto per il tipo di controllo ToolBar
- ToolBar (tipo di controllo)
- tipi di controllo, struttura ad albero per il tipo di controllo ToolBar
- tipi di controllo, pattern di controllo per il tipo di controllo ToolBar
- tipi di controllo, supporto per ToolBar
- tipi di controllo, ToolBar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1194c9aabaa684370b99d23d91c979ff3410305b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471157"
---
# <a name="toolbar-control-type"></a>Tipo di controllo ToolBar

Questo argomento fornisce informazioni sul supporto di Microsoft Automazione interfaccia utente per il **tipo di controllo ToolBar.** I controlli barra degli strumenti consentono agli utenti finali di attivare comandi e strumenti contenuti in un'applicazione.

Le sezioni seguenti definiscono la struttura ad Automazione interfaccia utente struttura ad albero, le proprietà, i pattern di controllo e gli eventi per il **tipo di controllo ToolBar.** I Automazione interfaccia utente si applicano a tutti i controlli barra degli strumenti in cui il framework o la piattaforma dell'interfaccia utente si integra Automazione interfaccia utente per i tipi di controllo e i pattern di controllo.

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Pattern di controllo obbligatori](#required-control-patterns)
-   [Eventi obbligatori](#required-events)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

La tabella seguente illustra un controllo tipico e una visualizzazione contenuto dell'albero Automazione interfaccia utente che riguarda i controlli barra degli strumenti e descrive cosa può essere contenuto in ogni visualizzazione. Per altre informazioni sull'albero Automazione interfaccia utente, vedere Automazione interfaccia utente [Tree Overview](uiauto-treeoverview.md).




| Visualizzazione controlli | Visualizzazione contenuto | 
|--------------|--------------|
| <ul><li>ToolBar<ul><li>Vari controlli (0 o più)</li></ul></li></ul> | <ul><li>ToolBar<ul><li>Vari controlli (0 o più)</li></ul></li></ul> | 




 

Un controllo barra degli strumenti può contenere qualsiasi tipo di controllo all'interno del relativo sottoalbero. In genere contengono pulsanti, caselle combinate e pulsanti di menu combinato.

## <a name="relevant-properties"></a>Proprietà rilevanti

La tabella seguente elenca le Automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per il **tipo di controllo ToolBar.** Per altre informazioni sulle Automazione interfaccia utente, vedere [Recupero di proprietà da Automazione interfaccia utente elementi](uiauto-propertiesforclients.md).



| Proprietà di automazione interfaccia utente                                                                                              | valore       | Note                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Vedere le note.  | Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata dell'Automazione interfaccia utente albero.                                                                                               |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vedere le note.  | Il rettangolo più esterno che contiene l'intero controllo.                                                                                                                                                   |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vedere le note.  | Supportata se è presente un rettangolo di delimitazione. Se non tutti i punti all'interno del rettangolo di delimitazione sono selezionabili e l'elemento esegue hit testing specializzati, eseguire l'override e fornire un punto selezionabile.       |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Barra degli strumenti** | Questo valore è uguale per tutti i framework dell'interfaccia utente.                                                                                                                                                              |
| [**\_IsContentElementPropertyId dell'interfaccia utente**](uiauto-automation-element-propids.md)         | true        | Il controllo barra degli strumenti è sempre incluso nella visualizzazione contenuto dell'Automazione interfaccia utente struttura ad albero.                                                                                                                      |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | true        | Il controllo barra degli strumenti è sempre incluso nella visualizzazione controlli dell'Automazione interfaccia utente albero.                                                                                                                      |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Vedere le note.  | Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.                                                                                                                                  |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULL        | Un controllo barra degli strumenti non ha mai un'etichetta.                                                                                                                                                                       |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vedere le note.  | Stringa localizzata corrispondente al **tipo di controllo ToolBar.** Il valore predefinito è "barra degli strumenti" per en-US o inglese (Stati Uniti).                                                                      |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Dipende da     | Il controllo barra degli strumenti non richiede un nome, a meno che non ne vengano usati più di uno all'interno di un'applicazione. Se ne sono presenti più di uno, ognuno deve avere un nome distintivo, ad esempio "Formattazione" o "Struttura". |



 

## <a name="required-control-patterns"></a>Pattern di controllo obbligatori

Nella tabella seguente sono elencati i Automazione interfaccia utente che devono essere supportati dai controlli barra degli strumenti. Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Pattern di controllo                                                   | Supporto | Note                                                                                                                                                         |
|-------------------------------------------------------------------|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider)                     | Dipende da | Se la barra degli strumenti può essere ancorata a parti diverse dello schermo, deve supportare il pattern [di controllo Dock.](uiauto-implementingdock.md)                       |
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Dipende da | Se la barra degli strumenti può essere espansa e compressa per visualizzare più elementi, deve supportare il pattern di controllo [ExpandCollapse.](uiauto-implementingexpandcollapse.md) |
| [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider)           | Dipende da | Se la barra degli strumenti può essere ridimensionata, ruotata o spostata, deve supportare il [pattern di controllo Transform.](uiauto-implementingtransform.md)                          |



 

## <a name="required-events"></a>Eventi obbligatori

La tabella seguente elenca gli eventi Automazione interfaccia utente che i controlli barra degli strumenti devono supportare. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automazione interfaccia utente eventi                                                                                                                                                | Note                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                                   |                                                                                                                                  |
| [**Interfaccia \_ utente Evento di modifica della proprietà BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md)                              |                                                                                                                                  |
| [**Interfaccia \_ utente Evento di modifica della proprietà ExpandCollapseExpandCollapseStatePropertyId.**](uiauto-control-pattern-propids.md) | Se il controllo supporta il pattern [di controllo ExpandCollapse,](uiauto-implementingexpandcollapse.md) deve supportare questo evento. |
| [**Interfaccia \_ utente Evento di modifica della proprietà IsEnabledPropertyId.**](uiauto-automation-element-propids.md)                                              | Se il controllo supporta la [**proprietà IsEnabled,**](uiauto-automation-element-propids.md) deve supportare questo evento.         |
| [**Interfaccia \_ utente Evento di modifica della proprietà IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)                                          | Se il controllo supporta la [**proprietà IsOffscreen,**](uiauto-automation-element-propids.md) deve supportare questo evento.       |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                               |                                                                                                                                  |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente](uiauto-controltypesoverview.md)
</dt> <dt>

[Cenni preliminari su automazione interfaccia utente](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




