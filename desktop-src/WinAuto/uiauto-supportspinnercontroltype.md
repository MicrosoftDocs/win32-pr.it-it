---
title: Tipo di controllo casella di selezione
description: In questo argomento vengono fornite informazioni sul supporto Automazione interfaccia utente Microsoft per il tipo di controllo Spinner.
ms.assetid: 28673ad5-645d-4314-96c4-81a951226256
keywords:
- Automazione interfaccia utente,supporto per il tipo di controllo Spinner
- Automazione interfaccia utente,Tipo di controllo Casella di selezione
- Automazione interfaccia utente,struttura ad albero per il tipo di controllo Spinner
- Automazione interfaccia utente,proprietà per il tipo di controllo Spinner
- Automazione interfaccia utente,pattern di controllo per il tipo di controllo Spinner
- Automazione interfaccia utente,eventi per il tipo di controllo Spinner
- strutture ad albero, tipo di controllo Spinner
- proprietà, tipo di controllo Casella di selezione
- pattern di controllo, tipo di controllo Spinner
- eventi, tipo di controllo Spinner
- supporto per il tipo di controllo Spinner
- Spinner (tipo di controllo)
- tipi di controllo, struttura ad albero per tipo di controllo Spinner
- tipi di controllo, pattern di controllo per il tipo di controllo Spinner
- tipi di controllo, supporto per Spinner
- tipi di controllo, spinner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1472fe400c189b6e5a1e894e1097395e8521e757
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478537"
---
# <a name="spinner-control-type"></a>Tipo di controllo casella di selezione

In questo argomento vengono fornite informazioni sul supporto Automazione interfaccia utente microsoft per il **tipo di controllo Spinner.**

I controlli casella di selezione vengono usati per effettuare selezioni da un dominio di elementi o un intervallo di numeri.

Le sezioni seguenti definiscono la struttura ad Automazione interfaccia utente struttura ad albero, le proprietà, i pattern di controllo e gli eventi per il **tipo di controllo Spinner.** I Automazione interfaccia utente di controllo si applicano a tutti i controlli casella di selezione in cui il framework o la piattaforma dell'interfaccia utente si integra Automazione interfaccia utente per i tipi di controllo e i pattern di controllo.

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Pattern di controllo obbligatori](#required-control-patterns)
-   [Eventi obbligatori](#required-events)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

La tabella seguente illustra un controllo tipico e una visualizzazione contenuto dell'albero di Automazione interfaccia utente che riguardano i controlli casella di selezione quando supportano i pattern di controllo **RangeValue** e **Selection** e descrive cosa può essere contenuto in ogni visualizzazione. Per altre informazioni sull'albero Automazione interfaccia utente, vedere Automazione interfaccia utente [Tree Overview](uiauto-treeoverview.md).

**Pattern di controllo RangeValue**




| Visualizzazione controlli | Visualizzazione contenuto | 
|--------------|--------------|
| <ul><li>Spinner<ul><li>Edit (0 o 1)</li><li>Button (2)</li></ul></li></ul> | <ul><li>Spinner</li></ul> | 




 

**Selection (pattern di controllo)**




| Visualizzazione controlli | Visualizzazione contenuto | 
|--------------|--------------|
| <ul><li>Spinner<ul><li>Edit (0 o 1)</li><li>Button (2)</li><li>List Item (0 o più)</li></ul></li></ul> | <ul><li>Spinner<ul><li>ListItem (0 o più)</li></ul></li></ul> | 




 

Per assicurarsi che i due pulsanti nel sottoalbero della visualizzazione controlli possano essere distinti dagli strumenti di test automatizzati, assegnare il valore **ScrollAmount \_ SmallIncrement** o [**ScrollAmount \_ SmallDecrement**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-scrollamount) alla proprietà **AutomationId** in base alle esigenze. Per alcune implementazioni, il controllo di modifica associato può essere un peer del controllo casella di selezione.

## <a name="relevant-properties"></a>Proprietà rilevanti

La tabella seguente elenca le proprietà Automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per i controlli casella di selezione. Per altre informazioni sulle Automazione interfaccia utente, vedere [Recupero di proprietà da Automazione interfaccia utente elementi](uiauto-propertiesforclients.md).



| Proprietà di automazione interfaccia utente                                                                                              | valore       | Note                                                                                                                                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Vedere le note.  | Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata dell'Automazione interfaccia utente albero.                                                                                                                                                                                                               |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vedere le note.  | Il rettangolo più esterno che contiene l'intero controllo.                                                                                                                                                                                                                                                                   |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vedere le note.  | Il punto selezionabile del controllo casella di selezione fornisce lo stato attivo alla parte modificabile del controllo.                                                                                                                                                                                                                                      |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Spinner** | Questo valore è uguale per tutti i framework.                                                                                                                                                                                                                                                                                 |
| [**\_IsContentElementPropertyId dell'interfaccia utente**](uiauto-automation-element-propids.md)         | true        | Il controllo casella di selezione deve essere sempre di tipo contenuto.                                                                                                                                                                                                                                                                                |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | true        | Il controllo casella di selezione deve essere sempre un controllo .                                                                                                                                                                                                                                                                              |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Vedere le note.  | Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà. Un controllo casella di selezione raramente assume lo stato attivo, ma quando lo fa, lo stato attivo deve rimanere sul controllo casella di selezione stesso, non sui pulsanti figlio. L'utente deve essere in grado di eseguire tutte le azioni di scorrimento usando i tasti FRECCIA SU e FRECCIA GIÙ. |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Vedere le note.  | I controlli casella di selezione hanno un'etichetta di testo statico.                                                                                                                                                                                                                                                                                 |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vedere le note.  | Stringa localizzata corrispondente al **tipo di controllo Spinner.** Il valore predefinito è "spinner" per en-US o english (Stati Uniti).                                                                                                                                                                                       |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Vedere le note.  | Il controllo casella di selezione in genere ricava il proprio nome da un'etichetta di testo statico.                                                                                                                                                                                                                                                      |



 

## <a name="required-control-patterns"></a>Pattern di controllo obbligatori

Nella tabella seguente sono elencati i Automazione interfaccia utente di controllo personalizzati che devono essere supportati da tutti i controlli casella di selezione. Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Pattern di controllo/proprietà del pattern                                         | Supporto/valore | Note                                                                                                                                     |
|--------------------------------------------------------------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider)                | Dipende da       | I controlli casella di selezione che si estendono su un intervallo numerico possono supportare il [pattern di controllo RangeValue.](uiauto-implementingrangevalue.md)               |
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)                  | Dipende da       | I controlli casella di selezione che hanno un elenco di elementi da selezionare devono supportare il [pattern di controllo](uiauto-implementingselection.md) Selezione. |
| [**CanSelectMultiple**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple) | FALSE         | I controlli casella di selezione sono sempre contenitori a selezione singola.                                                                                  |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)                          | Dipende da       | I controlli casella di selezione che si estendono su un set di opzioni o numeri descrete possono supportare il [pattern di controllo](uiauto-implementingvalue.md) Valore.    |



 

## <a name="required-events"></a>Eventi obbligatori

Nella tabella seguente sono elencati Automazione interfaccia utente che i controlli casella di selezione sono necessari per supportare. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automazione interfaccia utente evento                                                                                                                   | Note                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**Interfaccia \_ utente Evento di modifica della proprietà BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md) |                                                                                                                            |
| [**Interfaccia \_ utente Evento di modifica della proprietà IsEnabledPropertyId.**](uiauto-automation-element-propids.md)                 | Se il controllo supporta la [**proprietà IsEnabled,**](uiauto-automation-element-propids.md) deve supportare questo evento.   |
| [**Interfaccia \_ utente Evento di modifica della proprietà IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)             | Se il controllo supporta la [**proprietà IsOffscreen,**](uiauto-automation-element-propids.md) deve supportare questo evento. |
| [**Interfaccia \_ utente Evento di modifica della proprietà RangeValueValuePropertyId.**](uiauto-control-pattern-propids.md)        | Se il controllo supporta il pattern [di controllo RangeValue,](uiauto-implementingrangevalue.md) deve supportare questo evento.   |
| [**Interfaccia \_ utente Evento \_ di modifica della proprietà InvalidatedEventId**](uiauto-event-ids.md) di selezione.               | Se il controllo supporta il pattern [di controllo Selection,](uiauto-implementingselection.md) deve supportare questo evento.     |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |
| [**Interfaccia \_ utente Evento di modifica della proprietà ValueValuePropertyId.**](uiauto-control-pattern-propids.md)                  | Se il controllo supporta il pattern [di controllo Value,](uiauto-implementingvalue.md) deve supportare questo evento.             |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente](uiauto-controltypesoverview.md)
</dt> <dt>

[Cenni preliminari su automazione interfaccia utente](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




