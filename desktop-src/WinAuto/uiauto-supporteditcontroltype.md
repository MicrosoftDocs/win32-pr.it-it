---
title: Modifica tipo di controllo
description: In questo argomento vengono fornite informazioni sul supporto Automazione interfaccia utente Microsoft per il tipo di controllo Edit.
ms.assetid: ec45ec5e-4faa-4635-8726-5bbe1f20b843
keywords:
- Automazione interfaccia utente,supporto per il tipo di controllo Edit
- Automazione interfaccia utente,Modifica tipo di controllo
- Automazione interfaccia utente,struttura ad albero per il tipo di controllo Edit
- Automazione interfaccia utente,proprietà per il tipo di controllo Edit
- Automazione interfaccia utente,pattern di controllo per il tipo di controllo Edit
- Automazione interfaccia utente,eventi per il tipo di controllo Edit
- strutture ad albero, modifica del tipo di controllo
- proprietà,Modifica tipo di controllo
- pattern di controllo, modifica del tipo di controllo
- eventi,Modifica tipo di controllo
- supporto per il tipo di controllo Edit
- Edit (tipo di controllo)
- tipi di controllo, struttura ad albero per il tipo di controllo Edit
- tipi di controllo, pattern di controllo per il tipo di controllo Edit
- tipi di controllo, supporto per Edit
- tipi di controllo, modifica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5eea05d463f191483cb53f7cbfceef83058093f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476136"
---
# <a name="edit-control-type"></a>Modifica tipo di controllo

In questo argomento vengono fornite informazioni sul supporto Automazione interfaccia utente Microsoft per il **tipo di controllo** Edit.

I controlli di modifica consentono a un utente di visualizzare e modificare una semplice riga di testo senza il supporto del formato RTF.

Le sezioni seguenti definiscono la struttura ad Automazione interfaccia utente struttura ad albero, le proprietà, i pattern di controllo e gli eventi per il tipo di controllo di modifica. I Automazione interfaccia utente si applicano a tutti i controlli di modifica in cui il framework o la piattaforma dell'interfaccia utente si integra Automazione interfaccia utente per i tipi di controllo e i pattern di controllo.

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Pattern di controllo obbligatori](#required-control-patterns)
-   [Eventi obbligatori](#required-events)
-   [Osservazioni:](#remarks)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

La tabella seguente illustra un controllo tipico e una visualizzazione contenuto dell'albero Automazione interfaccia utente relativo ai controlli di modifica e descrive cosa può essere contenuto in ogni visualizzazione. Per altre informazioni sull'albero Automazione interfaccia utente, vedere Automazione interfaccia utente [Tree Overview](uiauto-treeoverview.md).




| Visualizzazione controlli | Visualizzazione contenuto | 
|--------------|--------------|
| <ul><li>Modifica</li></ul> | <ul><li>Modifica</li></ul> | 




 

I controlli che implementano il **tipo** di controllo Edit avranno sempre zero barre di scorrimento nella visualizzazione controlli dell'albero Automazione interfaccia utente perché si tratta di un controllo a riga singola. In alcuni scenari di layout una singola riga di testo può essere interrotta da un ritorno a capo. Il **tipo** di controllo Edit è destinato solo a piccole quantità di testo.

## <a name="relevant-properties"></a>Proprietà rilevanti

La tabella seguente elenca le Automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per i controlli di modifica. Per altre informazioni sulle Automazione interfaccia utente, vedere [Recupero di proprietà da Automazione interfaccia utente elementi](uiauto-propertiesforclients.md).



| Proprietà di automazione interfaccia utente                                                                                              | valore      | Note                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Vedere le note. | Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata dell'Automazione interfaccia utente albero.                                                                                                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vedere le note. | Il rettangolo più esterno che contiene l'intero controllo.                                                                                                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vedere le note. | Il controllo di modifica deve disporre di un punto selezionabile che rende disponibile lo stato attivo per l'input alla parte di modifica del controllo quando un utente fa clic su tale punto.                                                                                                                                           |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Modifica**   |                                                                                                                                                                                                                                                                                      |
| [**\_IsContentElementPropertyId dell'interfaccia utente**](uiauto-automation-element-propids.md)         | **TRUE**   | Il controllo di modifica è sempre incluso nella visualizzazione contenuto dell'Automazione interfaccia utente albero.                                                                                                                                                                                                   |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | **TRUE**   | Il controllo di modifica è sempre incluso nella visualizzazione controlli dell'Automazione interfaccia utente albero.                                                                                                                                                                                                   |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Vedere le note. | Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.                                                                                                                                                                                                            |
| [**UIA \_ IsPasswordPropertyId**](uiauto-automation-element-propids.md)                     | Vedere le note. | Deve essere impostato su **TRUE nei** controlli di modifica che contengono password. Se un controllo di modifica include contenuto di tipo Password, questa proprietà può essere usata da una utilità per la lettura dello schermo per determinare se le sequenze di tasti devono essere lette mentre l'utente digita il testo.                                      |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Vedere le note. | Se al controllo è associata un'etichetta di testo statico, questa proprietà deve esporre un riferimento a tale controllo. Se il controllo testo è un sottocomponente di un altro controllo, non avrà una **proprietà LabeledBy** impostata.                                                         |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vedere le note. | Stringa localizzata corrispondente al **tipo di** controllo Edit. Il valore predefinito è "edit" per en-US o english (Stati Uniti).                                                                                                                                                       |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Vedere le note. | Il nome del controllo di modifica viene in genere generato da un'etichetta di testo statico. Se non è presente un'etichetta di testo statico, il valore della proprietà **Name** deve essere assegnato dallo sviluppatore dell'applicazione. La **proprietà Name** non deve mai contenere il contenuto testuale del controllo di modifica. |



 

## <a name="required-control-patterns"></a>Pattern di controllo obbligatori

Nella tabella seguente sono elencati i Automazione interfaccia utente di controllo personalizzati che devono essere supportati dai controlli di modifica. Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Pattern di controllo/proprietà del pattern                              | Supporto/valore | Note                                                                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider)     | Dipende da       | Tutti i controlli di modifica che accettano un intervallo numerico devono esporre il [pattern di controllo RangeValue.](uiauto-implementingrangevalue.md)                                                                                                                                                                                                                                                                                       |
| [**Minimo**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_minimum)         | Vedere le note.    | Questa proprietà deve essere il valore più piccolo su cui è possibile impostare il contenuto del controllo di modifica.                                                                                                                                                                                                                                                                                                                     |
| [**Massimo**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_maximum)         | Vedere le note.    | Questa proprietà deve essere il valore più grande su cui è possibile impostare il contenuto del controllo di modifica.                                                                                                                                                                                                                                                                                                                      |
| [**Smallchange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_smallchange) | Vedere le note.    | Questa proprietà deve indicare il numero di cifre decimali che è possibile impostare per il valore. Se il controllo di modifica accetta solo numeri interi, il valore della proprietà **SmallChange** deve essere 1. Se il controllo di modifica accetta un intervallo compreso tra 1.0 e 2.0, il valore della proprietà **SmallChange** deve essere 0,1. Se il controllo di modifica accetta un intervallo compreso tra 1,00 e 2,00, il valore della proprietà **SmallChange** deve essere 0,001.                   |
| [**Largechange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_largechange) | **NULL**      | Questa proprietà non deve essere esposta in un controllo di modifica.                                                                                                                                                                                                                                                                                                                                                      |
| [**valore**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_value)             | Vedere le note.    | Questa proprietà indica il contenuto numerico del controllo di modifica. Quando un valore più preciso viene impostato da un client Automazione interfaccia utente all'interno degli intervalli specificati nelle proprietà [**Minimum**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_minimum) e [**Maximum,**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_maximum) la proprietà [**Value**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_value) viene arrotondata automaticamente al valore accettato più vicino. |
| [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider)                 | Obbligatoria      | Tutti i controlli di modifica devono supportare il pattern di controllo [Text](uiauto-implementingtextandtextrange.md) perché le informazioni dettagliate devono essere sempre disponibili assistive technology client.                                                                                                                                                                                                                     |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)               | Dipende da       | Tutti i controlli di modifica che accettano una stringa devono esporre il [pattern di controllo](uiauto-implementingvalue.md) Value.                                                                                                                                                                                                                                                                                                        |
| [**IsReadOnly**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_isreadonly)        | Vedere le note.    | Questa proprietà deve essere impostata per indicare se il controllo può avere un valore impostato a livello di codice o che può essere modificato dall'utente.                                                                                                                                                                                                                                                                                |
| [**valore**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_value)                  | Vedere le note.    | Questa proprietà contiene il contenuto testuale del controllo di modifica. Se la [**proprietà UIA \_ IsPasswordPropertyId**](uiauto-automation-element-propids.md) è impostata su **TRUE,** l'esecuzione di query sulla [**proprietà Value**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_value) deve restituire un errore.                                                                                                                      |



 

## <a name="required-events"></a>Eventi obbligatori

Nella tabella seguente sono elencati Automazione interfaccia utente eventi che i controlli di modifica devono supportare. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automazione interfaccia utente evento                                                                                                                                        | Note                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                           |                                                                                                                            |
| [**Interfaccia \_ utente Evento di modifica della proprietà BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md)                      |                                                                                                                            |
| [**Interfaccia \_ utente Evento di modifica della proprietà IsEnabledPropertyId.**](uiauto-automation-element-propids.md)                                      | Se il controllo supporta la [**proprietà IsEnabled,**](uiauto-automation-element-propids.md) deve supportare questo evento.   |
| [**Interfaccia \_ utente Evento di modifica della proprietà IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)                                  | Se il controllo supporta la [**proprietà IsOffscreen,**](uiauto-automation-element-propids.md) deve supportare questo evento. |
| [**Interfaccia \_ utente Evento di modifica**](uiauto-automation-element-propids.md) della proprietà NamePropertyId.                                                |                                                                                                                            |
| [**Interfaccia \_ utente Evento di modifica della proprietà RangeValueValuePropertyId.**](uiauto-control-pattern-propids.md)                             | Se il controllo supporta il pattern [di controllo RangeValue,](uiauto-implementingrangevalue.md) deve supportare questo evento.   |
| [**Interfaccia \_ utente Evento di modifica della proprietà ScrollHorizontallyScrollablePropertyId.**](uiauto-control-pattern-propids.md)   | Un controllo di modifica non supporta mai il pattern [di controllo Scroll.](uiauto-implementingscroll.md)                                |
| [**Interfaccia \_ utente Evento di modifica della proprietà ScrollHorizontalScrollPercentPropertyId.**](uiauto-control-pattern-propids.md) | Un controllo di modifica non supporta mai il pattern [di controllo Scroll.](uiauto-implementingscroll.md)                                |
| [**Interfaccia \_ utente Evento di modifica della proprietà ScrollHorizontalViewSizePropertyId.**](uiauto-control-pattern-propids.md)           | Un controllo di modifica non supporta mai il pattern [di controllo Scroll.](uiauto-implementingscroll.md)                                |
| [**Interfaccia \_ utente Evento di modifica della proprietà ScrollVerticallyScrollablePropertyId.**](uiauto-control-pattern-propids.md)       | Un controllo di modifica non supporta mai il pattern [di controllo Scroll.](uiauto-implementingscroll.md)                                |
| [**Interfaccia \_ utente Evento di modifica della proprietà ScrollVerticalScrollPercentPropertyId.**](uiauto-control-pattern-propids.md)     | Un controllo di modifica non supporta mai il pattern [di controllo Scroll.](uiauto-implementingscroll.md)                                |
| [**Interfaccia \_ utente Evento di modifica della proprietà ScrollVerticalViewSizePropertyId.**](uiauto-control-pattern-propids.md)               | Un controllo di modifica non supporta mai il pattern [di controllo Scroll.](uiauto-implementingscroll.md)                                |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                       |                                                                                                                            |
| [**UIA \_ Text \_ TextChangedEventId**](uiauto-event-ids.md)                                                                      | Se il controllo supporta il pattern [di controllo Text,](uiauto-implementingtextandtextrange.md) deve supportare questo evento.   |
| [**UIA \_ Text \_ TextSelectionChangedEventId**](uiauto-event-ids.md)                                                    | Se il controllo supporta il pattern [di controllo Text,](uiauto-implementingtextandtextrange.md) deve supportare questo evento.   |
| [**Interfaccia \_ utente Evento di modifica**](uiauto-control-pattern-propids.md) della proprietà ValueValuePropertyId .                                      | Se il controllo supporta il pattern [di controllo Value,](uiauto-implementingvalue.md) deve supportare questo evento.             |



 

## <a name="remarks"></a>Commenti

Un controllo di modifica può essere usato come campo di testo di sola lettura che non supporta la selezione o la modifica del testo. Tale controllo di modifica si comporta come un oggetto campo con un nome e un valore specifici.

Se un controllo di modifica contiene testo segnaposto(ad esempio, un banner di segnale), il testo deve essere usato come proprietà **HelpText** a meno che il testo non possa essere modificato dall'utente e quindi riutilizzato come testo segnaposto. Ad esempio, la Windows Internet Explorer degli indirizzi contiene il testo "about:Tabs" quando viene aperta una nuova scheda. Questo non è **HelpText** perché è un indirizzo a livello di codice che può essere usato o modificato dall'utente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente](uiauto-controltypesoverview.md)
</dt> <dt>

[Cenni preliminari su automazione interfaccia utente](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




