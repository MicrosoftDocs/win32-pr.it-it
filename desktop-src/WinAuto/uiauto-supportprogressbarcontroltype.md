---
title: Tipo di controllo ProgressBar
description: Questo argomento fornisce informazioni sul supporto di Microsoft Automazione interfaccia utente per il tipo di controllo ProgressBar.
ms.assetid: 2ea0c1f1-1a0a-4360-bdcb-8edc13cc3c31
keywords:
- Automazione interfaccia utente,supporto per il tipo di controllo ProgressBar
- Automazione interfaccia utente, tipo di controllo ProgressBar
- Automazione interfaccia utente, struttura ad albero per il tipo di controllo ProgressBar
- Automazione interfaccia utente,proprietà per il tipo di controllo ProgressBar
- Automazione interfaccia utente,pattern di controllo per il tipo di controllo ProgressBar
- Automazione interfaccia utente,eventi per il tipo di controllo ProgressBar
- strutture ad albero, tipo di controllo ProgressBar
- proprietà, tipo di controllo ProgressBar
- pattern di controllo, tipo di controllo ProgressBar
- eventi, tipo di controllo ProgressBar
- supporto per il tipo di controllo ProgressBar
- ProgressBar (tipo di controllo)
- tipi di controllo, struttura ad albero per il tipo di controllo ProgressBar
- tipi di controllo, pattern di controllo per il tipo di controllo ProgressBar
- tipi di controllo, supporto per ProgressBar
- tipi di controllo, ProgressBar
ms.topic: article
ms.date: 12/04/2019
ms.openlocfilehash: 5dc5dd22abcaca70ae9ce86717db6055642a21ce
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472299"
---
# <a name="progressbar-control-type"></a>Tipo di controllo ProgressBar

In questo argomento vengono fornite informazioni sul supporto Automazione interfaccia utente Microsoft per il **tipo di controllo ProgressBar.**

I controlli indicatore di stato indicano lo stato di avanzamento di un'operazione di lunga durata. Il controllo è costituito da un rettangolo che viene riempito gradualmente con il colore di sistema durante l'esecuzione dell'operazione.

Le sezioni seguenti definiscono la struttura ad Automazione interfaccia utente struttura ad albero, le proprietà, i pattern di controllo e gli eventi per il **tipo di controllo ProgressBar.** I Automazione interfaccia utente si applicano a tutti i controlli indicatore di stato in cui il framework o la piattaforma dell'interfaccia utente si integra Automazione interfaccia utente per i tipi di controllo e i pattern di controllo.

In questo argomento sono contenute le sezioni seguenti.

- [Struttura ad albero tipica](#typical-tree-structure)
- [Proprietà rilevanti](#relevant-properties)
- [Pattern di controllo obbligatori](#required-control-patterns)
- [Eventi obbligatori](#required-events)
- [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

La tabella seguente illustra un controllo tipico e una visualizzazione contenuto dell'albero Automazione interfaccia utente relativo ai controlli indicatore di stato e descrive gli elementi che possono essere contenuti in ogni visualizzazione. Per altre informazioni sull'albero Automazione interfaccia utente, vedere Automazione interfaccia utente [Tree Overview](uiauto-treeoverview.md).


| Visualizzazione controlli | Visualizzazione contenuto | 
|--------------|--------------|
| <ul><li>ProgressBar</li></ul> | <ul><li>ProgressBar</li></ul> | 


I controlli indicatore di stato non hanno elementi figlio nella visualizzazione controlli o contenuto dell'Automazione interfaccia utente albero.

## <a name="relevant-properties"></a>Proprietà rilevanti

Nella tabella seguente sono elencate le Automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per gli barre di stato. Per altre informazioni sulle Automazione interfaccia utente, vedere [Recupero di proprietà da Automazione interfaccia utente elementi](uiauto-propertiesforclients.md).

| Proprietà di automazione interfaccia utente                                                                                              | valore           | Note                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Vedere le note.      | Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata dell'Automazione interfaccia utente albero.                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vedere le note.      | Il rettangolo più esterno che contiene l'intero controllo.                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vedere le note.      | Supportata se è presente un rettangolo di delimitazione. Se non tutti i punti all'interno del rettangolo di delimitazione sono selezionabili e l'elemento esegue hit testing specializzati, eseguire l'override e fornire un punto selezionabile. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **ProgressBar** |                                                                                                                                                                                                      |
| [**\_IsContentElementPropertyId dell'interfaccia utente**](uiauto-automation-element-propids.md)         | **TRUE**        | Il controllo indicatore di stato è sempre incluso nella visualizzazione contenuto dell'Automazione interfaccia utente albero.                                                                                                           |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | **TRUE**        | Il controllo indicatore di stato è sempre incluso nella visualizzazione controlli dell'Automazione interfaccia utente albero.                                                                                                           |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Vedere le note.      | Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.                                                                                                                            |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Vedere le note.      | Se è presente un'etichetta di testo statico, questa proprietà deve esporre un riferimento a tale controllo.                                                                                                              |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vedere le note.      | Stringa localizzata corrispondente al **tipo di controllo ProgressBar.** Il valore predefinito è "progress bar" per en-US o English (Stati Uniti).                                                        |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Vedere le note.      | Il controllo indicatore di stato in genere ricava il proprio nome da un'etichetta di testo statico. Se non è presente alcuna etichetta di testo statico, lo sviluppatore dell'applicazione deve esporre un valore per la proprietà Name.                  |



 

## <a name="required-control-patterns"></a>Pattern di controllo obbligatori

Nella tabella seguente sono elencati i Automazione interfaccia utente che devono essere supportati dai controlli indicatore di stato. Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Pattern di controllo/proprietà del pattern                              | Supporto/valore | Note                                                                                                                                      |
|---------------------------------------------------------------|---------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider)     | Dipende da       | I controlli indicatore di stato che accettano un intervallo numerico devono implementare il [pattern di controllo RangeValue.](uiauto-implementingrangevalue.md)        |
| [**Minimo**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_minimum)         | Dipende da           | Il valore di questa proprietà è il valore minimo su cui è possibile impostare il controllo. Questo valore deve essere minore di [**Maximum.**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_maximum)                                                      |
| [**Massimo**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_maximum)         | Dipende da         | Il valore di questa proprietà è il valore massimo su cui è possibile impostare il controllo. Questo valore deve essere maggiore di [**Minimum.**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_minimum)                                                        |
| [**Smallchange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_smallchange) | **NaN**       | Questa proprietà non è necessaria perché i controlli indicatore di stato sono di sola lettura.                                                                 |
| [**Largechange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_largechange) | **NaN**       | Questa proprietà non è necessaria perché i controlli indicatore di stato sono di sola lettura.                                                                 |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)               | Dipende da       | I controlli indicatore di stato che forniscono un'indicazione testuale dello stato di avanzamento devono implementare il [pattern di controllo](uiauto-implementingvalue.md) Value. |
| [**IsReadOnly**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_isreadonly)        | **TRUE**      | Il valore di questa proprietà è sempre **TRUE.**                                                                                            |
| [**valore**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_value)                  | Vedere le note.    | Questa proprietà espone lo stato di avanzamento in formato testuale di un controllo indicatore di stato.                                                                          |



 

## <a name="required-events"></a>Eventi obbligatori

Nella tabella seguente sono elencati gli Automazione interfaccia utente che gli barre di stato devono supportare. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automazione interfaccia utente eventi                                                                                                                   | Note                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**Interfaccia \_ utente Evento di modifica della proprietà BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md) |                                                                                                                            |
| [**Interfaccia \_ utente Evento di modifica della proprietà IsEnabledPropertyId.**](uiauto-automation-element-propids.md)                 | Se il controllo supporta la [**proprietà IsEnabled,**](uiauto-automation-element-propids.md) deve supportare questo evento.   |
| [**Interfaccia \_ utente Evento di modifica della proprietà IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)             | Se il controllo supporta la [**proprietà IsOffscreen,**](uiauto-automation-element-propids.md) deve supportare questo evento. |
| [**Interfaccia \_ utente Evento di modifica**](uiauto-automation-element-propids.md) della proprietà NamePropertyId.                           |                                                                                                                            |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |
| [**Interfaccia \_ utente Evento di modifica della proprietà RangeValueValuePropertyId.**](uiauto-control-pattern-propids.md)        | Se il controllo supporta il pattern [di controllo RangeValue,](uiauto-implementingrangevalue.md) deve supportare questo evento.   |
| [**Interfaccia \_ utente Evento di modifica della proprietà ValueValuePropertyId.**](uiauto-control-pattern-propids.md)                  | Se il controllo supporta il pattern [di controllo Value,](uiauto-implementingvalue.md) deve supportare questo evento.             |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente](uiauto-controltypesoverview.md)
</dt> <dt>

[Cenni preliminari su automazione interfaccia utente](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




