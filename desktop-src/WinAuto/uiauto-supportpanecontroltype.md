---
title: Tipo di controllo Riquadro
description: Questo argomento fornisce informazioni sul supporto di Microsoft Automazione interfaccia utente per il tipo di controllo Riquadro.
ms.assetid: 2a5d69dc-6880-4610-b481-4371637472ed
keywords:
- Automazione interfaccia utente,supporto per il tipo di controllo Pane
- Automazione interfaccia utente,Tipo di controllo Riquadro
- Automazione interfaccia utente,struttura ad albero per il tipo di controllo Pane
- Automazione interfaccia utente,proprietà per il tipo di controllo Pane
- Automazione interfaccia utente,pattern di controllo per il tipo di controllo Pane
- Automazione interfaccia utente,eventi per il tipo di controllo Pane
- strutture ad albero, tipo di controllo Pane
- proprietà,Tipo di controllo Riquadro
- pattern di controllo,tipo di controllo Riquadro
- eventi,Tipo di controllo Riquadro
- supporto per il tipo di controllo Pane
- Pane (tipo di controllo)
- tipi di controllo, struttura ad albero per il tipo di controllo Pane
- tipi di controllo,pattern di controllo per il tipo di controllo Riquadro
- tipi di controllo, supporto per Pane
- tipi di controllo,Riquadro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b335496d8d40d20ccc68f6bc2b048c87ff608dd
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474257"
---
# <a name="pane-control-type"></a>Tipo di controllo Riquadro

Questo argomento fornisce informazioni sul supporto di Microsoft Automazione interfaccia utente per il **tipo di controllo** Riquadro.

Il **tipo di** controllo Riquadro è per aree potenzialmente scorrevoli con contenuto diverso. Viene usato per rappresentare un oggetto all'interno di una cornice o di una finestra del documento. Gli utenti possono spostarsi tra i controlli riquadro e all'interno del contenuto del riquadro corrente. I controlli riquadro rappresentano un livello di raggruppamento inferiore rispetto alle finestre o ai documenti, ma sopra i singoli controlli. L'utente si sposta tra i riquadri premendo TAB, F6 o CTRL+TAB, a seconda del contesto.

Le sezioni seguenti definiscono la struttura ad Automazione interfaccia utente, le proprietà, i pattern di controllo e gli eventi necessari per il **tipo di controllo Pane.** I Automazione interfaccia utente si applicano a tutti i controlli riquadro in cui il framework o la piattaforma dell'interfaccia utente Automazione interfaccia utente supporto per i tipi di controllo e i pattern di controllo.

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Pattern di controllo obbligatori](#required-control-patterns)
-   [Eventi obbligatori](#required-events)
-   [Esempio di tipo di controllo Pane](#pane-control-type-example)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

La tabella seguente illustra un controllo tipico e una visualizzazione contenuto dell'albero Automazione interfaccia utente che riguarda i controlli riquadro e descrive cosa può essere contenuto in ogni visualizzazione. Per altre informazioni sull'albero Automazione interfaccia utente, vedere Panoramica Automazione interfaccia utente [albero](uiauto-treeoverview.md).




| Visualizzazione controlli | Visualizzazione contenuto | 
|--------------|--------------|
| <ul><li>Riquadro</li></ul> | <ul><li>Riquadro</li></ul> | 




 

Un controllo riquadro viene sempre visualizzato nelle visualizzazioni controllo e contenuto. Non esporre un oggetto di layout come riquadro nel controllo o nella visualizzazione contenuto se l'oggetto viene usato solo per la presentazione visiva.

## <a name="relevant-properties"></a>Proprietà rilevanti

Nella tabella seguente sono elencate le Automazione interfaccia utente il cui valore o definizione è particolarmente rilevante per i controlli riquadro. Per altre informazioni sulle Automazione interfaccia utente, vedere Recupero di proprietà [da Automazione interfaccia utente Elements](uiauto-propertiesforclients.md).



| Proprietà di automazione interfaccia utente                                                                                              | valore      | Note                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AccessKeyPropertyId**](uiauto-automation-element-propids.md)                       | Vedere le note. | Se una combinazione di tasti specifica fornisce lo stato attivo al riquadro, tali informazioni devono essere esposte tramite questa proprietà.                                                                                                                                                                                                      |
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Vedere le note. | Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata dell'Automazione interfaccia utente albero.                                                                                                                                                                                                          |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vedere le note. | Il rettangolo più esterno che contiene l'intero controllo.                                                                                                                                                                                                                                                              |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vedere le note. | Questa proprietà espone un punto selezionabile del controllo riquadro che fa sì che il riquadro assuma lo stato attivo quando viene selezionato.                                                                                                                                                                                                |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Riquadro**   |                                                                                                                                                                                                                                                                                                                       |
| [**UIA \_ HelpTextPropertyId**](uiauto-automation-element-propids.md)                         | Vedere le note. | Il testo della Guida per i controlli riquadro deve spiegare lo scopo del frame e il modo in cui è correlato ad altri frame. Una descrizione è necessaria se lo scopo e la relazione dei frame non sono chiari dal valore della proprietà [**UIA \_ NamePropertyId.**](uiauto-automation-element-propids.md) |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | true       | Il controllo riquadro è sempre incluso nella visualizzazione contenuto dell'Automazione interfaccia utente albero.                                                                                                                                                                                                                                    |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | true       | Il controllo riquadro è sempre incluso nella visualizzazione controlli dell'Automazione interfaccia utente albero.                                                                                                                                                                                                                                    |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Vedere le note. | Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.                                                                                                                                                                                                                                             |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Vedere le note. | I controlli riquadro in genere non hanno un'etichetta statica. Se è presente un'etichetta di testo statico, l'etichetta deve essere esposta tramite questa proprietà.                                                                                                                                                                                      |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vedere le note. | Stringa localizzata corrispondente al **tipo di controllo** Pane. Il valore predefinito è "pane" per en-US o english (Stati Uniti).                                                                                                                                                                                        |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Vedere le note. | Il valore di questa proprietà deve essere sempre un titolo chiaro, conciso e significativo.                                                                                                                                                                                                                                     |



 

## <a name="required-control-patterns"></a>Pattern di controllo obbligatori

Nella tabella seguente sono elencati i Automazione interfaccia utente di controllo necessari per essere supportati dai controlli riquadro. Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Pattern di controllo                                         | Supporto | Note                                                                                                                                                                                         |
|---------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider)           | Dipende da | Implementare [il pattern di](uiauto-implementingdock.md) controllo Dock se il controllo riquadro può essere ancorato.                                                                                          |
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)       | Dipende da | Implementare [il pattern di](uiauto-implementingscroll.md) controllo Scroll se è possibile scorrere il controllo riquadro.                                                                                    |
| [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) | Dipende da | Implementare [il](uiauto-implementingtransform.md) pattern di controllo Transform se il controllo riquadro può essere spostato, ridimensionato o ruotato sullo schermo.                                              |
| [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider)       | Mai   | Se l'elemento deve implementare il pattern di controllo [Window,](uiauto-implementingwindow.md) il controllo deve essere basato sul [tipo di controllo Window.](uiauto-supportwindowcontroltype.md) |



 

## <a name="required-events"></a>Eventi obbligatori

La tabella seguente elenca gli eventi Automazione interfaccia utente che i controlli riquadro devono supportare. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automazione interfaccia utente eventi                                                                                                                                        | Note                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AsyncContentLoadedEventId**](uiauto-event-ids.md)                                                                   |                                                                                                                            |
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                           |                                                                                                                            |
| [**Interfaccia \_ utente Evento di modifica della proprietà BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md)                      |                                                                                                                            |
| [**Interfaccia \_ utente Evento di modifica della proprietà IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)                                  | Se il controllo supporta la [**proprietà IsOffscreen,**](uiauto-automation-element-propids.md) deve supportare questo evento. |
| [**Interfaccia \_ utente Evento di modifica della proprietà ScrollHorizontallyScrollablePropertyId.**](uiauto-control-pattern-propids.md)   | Se il controllo supporta il pattern [di controllo Scroll,](uiauto-implementingscroll.md) deve supportare questo evento.           |
| [**Interfaccia \_ utente Evento di modifica della proprietà ScrollHorizontalScrollPercentPropertyId.**](uiauto-control-pattern-propids.md) | Se il controllo supporta il pattern [di controllo Scroll,](uiauto-implementingscroll.md) deve supportare questo evento.           |
| [**Interfaccia \_ utente Evento di modifica della proprietà ScrollHorizontalViewSizePropertyId.**](uiauto-control-pattern-propids.md)           | Se il controllo supporta il pattern [di controllo Scroll,](uiauto-implementingscroll.md) deve supportare questo evento.           |
| [**Interfaccia \_ utente Evento di modifica della proprietà ScrollVerticallyScrollablePropertyId.**](uiauto-control-pattern-propids.md)       | Se il controllo supporta il pattern [di controllo Scroll,](uiauto-implementingscroll.md) deve supportare questo evento.           |
| [**Interfaccia \_ utente Evento di modifica della proprietà ScrollVerticalScrollPercentPropertyId.**](uiauto-control-pattern-propids.md)     | Se il controllo supporta il pattern [di controllo Scroll,](uiauto-implementingscroll.md) deve supportare questo evento.           |
| [**Interfaccia \_ utente Evento di modifica della proprietà ScrollVerticalViewSizePropertyId.**](uiauto-control-pattern-propids.md)               | Se il controllo supporta il pattern [di controllo Scroll,](uiauto-implementingscroll.md) deve supportare questo evento.           |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                       |                                                                                                                            |



 

## <a name="pane-control-type-example"></a>Esempio di tipo di controllo Pane

L'immagine seguente illustra un controllo che implementa il tipo di controllo **Pane.**

![Screenshot che mostra l'esempio di un controllo riquadro](images/panexmpl.jpg)




| Automazione interfaccia utente struttura ad albero- Visualizzazione controlli | Automazione interfaccia utente struttura ad albero- Visualizzazione contenuto | 
|-----------------------------------|-----------------------------------|
| <ul><li>Riquadro<ul><li>Tree (pattern Scroll)<ul><li>TreeItem</li><li>...</li></ul></li></ul></li><li>Riquadro<ul><li>Modifica (pattern di scorrimento)</li></ul></li></ul> | <ul><li>Riquadro<ul><li>Tree (pattern Scroll)<ul><li>TreeItem</li><li>...</li></ul></li><li>Riquadro<ul><li>Modifica (pattern di scorrimento)</li></ul></li></ul></li></ul> | 




 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente](uiauto-controltypesoverview.md)
</dt> <dt>

[Cenni preliminari su automazione interfaccia utente](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




