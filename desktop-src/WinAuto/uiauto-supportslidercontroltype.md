---
title: Tipo di controllo Slider
description: Questo argomento fornisce informazioni sul supporto di Microsoft Automazione interfaccia utente per il tipo di controllo Slider.
ms.assetid: dc7bef7a-b68c-4184-a9e7-745bb41b592e
keywords:
- Automazione interfaccia utente,supporto per il tipo di controllo Slider
- Automazione interfaccia utente,Tipo di controllo Slider
- Automazione interfaccia utente,struttura ad albero per il tipo di controllo Slider
- Automazione interfaccia utente,proprietà per il tipo di controllo Slider
- Automazione interfaccia utente,pattern di controllo per il tipo di controllo Slider
- Automazione interfaccia utente,eventi per il tipo di controllo Slider
- strutture ad albero, tipo di controllo Slider
- proprietà, tipo di controllo Slider
- pattern di controllo, tipo di controllo Slider
- eventi, tipo di controllo Slider
- supporto per il tipo di controllo Slider
- Slider (tipo di controllo)
- tipi di controllo, struttura ad albero per il tipo di controllo Slider
- tipi di controllo, pattern di controllo per il tipo di controllo Slider
- tipi di controllo, supporto per Slider
- tipi di controllo, Dispositivo di scorrimento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 354217323ba4c3c59e416f7b9c36661d8ffe8a77
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472877"
---
# <a name="slider-control-type"></a>Tipo di controllo Slider

Questo argomento fornisce informazioni sul supporto di Microsoft Automazione interfaccia utente per il tipo **di controllo Slider.**

Un controllo dispositivo di scorrimento è un controllo composito con pulsanti che consentono a un utente di impostare un intervallo numerico o di selezionarlo da un set di elementi.

Le sezioni seguenti definiscono la struttura ad Automazione interfaccia utente struttura ad albero, le proprietà, i pattern di controllo e gli eventi necessari per il tipo **di controllo Slider.** I Automazione interfaccia utente si applicano a tutti i controlli dispositivo di scorrimento in cui il framework o la piattaforma dell'interfaccia utente Automazione interfaccia utente il supporto per i tipi di controllo e i pattern di controllo.

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Pattern di controllo obbligatori](#required-control-patterns)
-   [Eventi obbligatori](#required-events)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

La tabella seguente illustra un controllo tipico e una visualizzazione contenuto dell'albero Automazione interfaccia utente relativo ai controlli dispositivo di scorrimento e descrive gli elementi che possono essere contenuti in ogni visualizzazione. Per altre informazioni sull'albero Automazione interfaccia utente, vedere panoramica [Automazione interfaccia utente albero.](uiauto-treeoverview.md)




| Visualizzazione controlli | Visualizzazione contenuto | 
|--------------|--------------|
| <ul><li>Slider<ul><li>Button (2 o 4)</li><li>Thumb (1)</li><li>List Item (0 o più)</li></ul></li></ul> | <ul><li>Slider<ul><li>List Item (0 o più)</li></ul></li></ul> | 




 

## <a name="relevant-properties"></a>Proprietà rilevanti

La tabella seguente elenca le proprietà Automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per i controlli dispositivo di scorrimento. Per altre informazioni sulle Automazione interfaccia utente, vedere [Recupero di proprietà da Automazione interfaccia utente elementi](uiauto-propertiesforclients.md).



| Proprietà di automazione interfaccia utente                                                                                              | valore      | Note                                                                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Vedere le note. | Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata dell'Automazione interfaccia utente albero.                                                                                                                   |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vedere le note. | Il rettangolo più esterno che contiene l'intero controllo.                                                                                                                                                                       |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vedere le note. | La maggior parte dei controlli dispositivo di scorrimento deve restituire l'errore [**UIA \_ E \_ NOCLICKABLEPOINT**](uiauto-error-codes.md) perché l'intero rettangolo di delimitazione del controllo dispositivo di scorrimento è occupato dai controlli figlio. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Dispositivo di scorrimento** | Questo valore è uguale per tutti i framework.                                                                                                                                                                                     |
| [**\_IsContentElementPropertyId dell'interfaccia utente**](uiauto-automation-element-propids.md)         | true       | Il controllo dispositivo di scorrimento è sempre incluso nella visualizzazione contenuto dell'Automazione interfaccia utente struttura ad albero.                                                                                                                                           |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | true       | Il controllo dispositivo di scorrimento è sempre incluso nella visualizzazione controlli dell'Automazione interfaccia utente albero.                                                                                                                                           |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Vedere le note. | Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà. Gli elementi figlio (pulsanti e cursore) di un controllo dispositivo di scorrimento non devono mai spostare lo stato attivo. Lo stato attivo deve rimanere sempre sul dispositivo di scorrimento stesso.       |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Vedere le note. | Se al controllo è associata un'etichetta di testo statico, questa proprietà deve esporre un riferimento a tale controllo. Se il controllo testo è un sottocomponente di un altro controllo, non avrà una **proprietà LabeledBy** impostata.   |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vedere le note. | Stringa localizzata corrispondente al tipo **di controllo Slider.** Il valore predefinito è "slider" per en-US o english (Stati Uniti).                                                                                             |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Vedere le note. | Il nome del dispositivo di scorrimento viene in genere generato da un'etichetta di testo statico. Se non è presente un'etichetta di testo statico, il valore della proprietà **Name** deve essere assegnato dallo sviluppatore dell'applicazione.                              |



 

## <a name="required-control-patterns"></a>Pattern di controllo obbligatori

Nella tabella seguente sono elencati i Automazione interfaccia utente che devono essere supportati da tutti i controlli dispositivo di scorrimento. Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Pattern di controllo/proprietà del pattern                          | Supporto/valore | Note                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) | Dipende da       | Un dispositivo di scorrimento deve supportare il pattern di controllo [RangeValue](uiauto-implementingrangevalue.md) se il contenuto può essere impostato su un valore all'interno di un intervallo numerico.                                                                                                                                                 |
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)   | Dipende da       | Un dispositivo di scorrimento deve [supportare](uiauto-implementingselection.md) il pattern di controllo Selection se il contenuto rappresenta un valore tra un set discreto di opzioni. Se il pattern di controllo Selection è supportato, la selezione corrispondente deve essere esposta come uno o più elementi di elenco figlio del dispositivo di scorrimento. |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)           | Dipende da       | Un dispositivo di scorrimento deve [supportare](uiauto-implementingvalue.md) il pattern di controllo Value se il contenuto rappresenta un valore tra un set discreto di opzioni.                                                                                                                                                     |



 

## <a name="required-events"></a>Eventi obbligatori

La tabella seguente elenca gli eventi Automazione interfaccia utente che i controlli dispositivo di scorrimento devono supportare. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automazione interfaccia utente eventi                                                                                                                   | Note                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**Interfaccia \_ utente Evento di modifica della proprietà BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md) |                                                                                                                            |
| [**Interfaccia \_ utente Evento di modifica della proprietà IsEnabledPropertyId.**](uiauto-automation-element-propids.md)                 | Se il controllo supporta la [**proprietà IsEnabled,**](uiauto-automation-element-propids.md) deve supportare questo evento.   |
| [**Interfaccia \_ utente Evento di modifica della proprietà IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)             | Se il controllo supporta la [**proprietà IsOffscreen,**](uiauto-automation-element-propids.md) deve supportare questo evento. |
| [**Interfaccia \_ utente Evento di modifica della proprietà RangeValueValuePropertyId.**](uiauto-control-pattern-propids.md)        | Se il controllo supporta il pattern [di controllo RangeValue,](uiauto-implementingrangevalue.md) deve supportare questo evento.   |
| [**UIA \_ Selection \_ InvalidatedEventId**](uiauto-event-ids.md)                                       | Se il controllo supporta il pattern [di controllo Selection,](uiauto-implementingselection.md) deve supportare questo evento.     |
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

 

 




