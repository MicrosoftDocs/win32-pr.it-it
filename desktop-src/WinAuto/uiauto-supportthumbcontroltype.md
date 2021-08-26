---
title: Tipo di controllo Thumb
description: Questo argomento fornisce informazioni sul supporto microsoft Automazione interfaccia utente per il tipo di controllo Thumb.
ms.assetid: 3b1d6802-cfd4-4b07-80a0-2950ca7f4e96
keywords:
- Automazione interfaccia utente,supporto per il tipo di controllo Thumb
- Automazione interfaccia utente,Tipo di controllo Thumb
- Automazione interfaccia utente, struttura ad albero per il tipo di controllo Thumb
- Automazione interfaccia utente,proprietà per il tipo di controllo Thumb
- Automazione interfaccia utente,pattern di controllo per il tipo di controllo Thumb
- Automazione interfaccia utente,eventi per il tipo di controllo Thumb
- strutture ad albero, tipo di controllo Thumb
- proprietà,Tipo di controllo Thumb
- pattern di controllo,tipo di controllo Thumb
- eventi, tipo di controllo Thumb
- supporto per il tipo di controllo Thumb
- Thumb (tipo di controllo)
- tipi di controllo, struttura ad albero per il tipo di controllo Thumb
- tipi di controllo, pattern di controllo per il tipo di controllo Thumb
- tipi di controllo, supporto per Thumb
- tipi di controllo,Thumb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fea75b39ae0b17be23886823d446667299e5f0df
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478787"
---
# <a name="thumb-control-type"></a>Tipo di controllo Thumb

Questo argomento fornisce informazioni sul supporto microsoft Automazione interfaccia utente per il **tipo di controllo Thumb.**

I controlli Thumb forniscono la funzionalità che consente lo spostamento o il trascinamento di un controllo, ad esempio un pulsante della barra di scorrimento, oppure il ridimensionato, ad esempio un widget per il ridimensionamento della finestra. Si noti che un controllo thumb non fornisce funzionalità di trascinamento della selezione. I controlli Thumb possono ricevere lo stato attivo del mouse ma non lo stato attivo della tastiera. Lo sviluppatore del controllo deve implementare il controllo in modo che funzioni nel modo appropriato, ovvero possa essere trascinato o ridimensionato.

Le sezioni seguenti definiscono la struttura ad Automazione interfaccia utente, le proprietà, i pattern di controllo e gli eventi necessari per il tipo di controllo **Thumb.** I Automazione interfaccia utente si applicano a tutti i controlli thumb in cui il framework o la piattaforma dell'interfaccia utente Automazione interfaccia utente supporto per i tipi di controllo e i pattern di controllo.

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Pattern di controllo obbligatori](#required-control-patterns)
-   [Eventi obbligatori](#required-events)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

La tabella seguente illustra un controllo tipico e una visualizzazione contenuto dell'albero Automazione interfaccia utente che riguarda i controlli thumb e descrive cosa può essere contenuto in ogni visualizzazione. Per altre informazioni sull'albero Automazione interfaccia utente, vedere Panoramica Automazione interfaccia utente [albero](uiauto-treeoverview.md).




| Visualizzazione controlli | Visualizzazione contenuto | 
|--------------|--------------|
| <ul><li>Thumb</li></ul> | (Non applicabile) | 




 

I controlli Thumb non vengono mai visualizzati nella visualizzazione contenuto perché esistono solo per essere manipolati con il mouse. Vengono esposti anche se un altro pattern di controllo, ad esempio il pattern di controllo [Scroll,](uiauto-implementingscroll.md) [transform](uiauto-implementingtransform.md) control pattern o [RangeValue,](uiauto-implementingrangevalue.md) è supportato nel contenitore del controllo thumb.

## <a name="relevant-properties"></a>Proprietà rilevanti

Nella tabella seguente sono elencate le Automazione interfaccia utente il cui valore o definizione è particolarmente rilevante per i controlli Thumb. Per altre informazioni sulle Automazione interfaccia utente, vedere Recupero di proprietà [da Automazione interfaccia utente Elements](uiauto-propertiesforclients.md).



| Proprietà di automazione interfaccia utente                                                                                              | valore      | Note                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Vedere le note. | Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata dell'Automazione interfaccia utente albero.                                                                                                                                                 |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vedere le note. | Il rettangolo più esterno che contiene l'intero controllo.                                                                                                                                                                                                     |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vedere le note. | Punto all'interno dell'area client visibile del controllo thumb.                                                                                                                                                                                                 |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Pollice**  |                                                                                                                                                                                                                                                              |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | FALSE      | Il controllo thumb non viene mai incluso nella visualizzazione contenuto dell'Automazione interfaccia utente albero.                                                                                                                                                                           |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | true       | Il controllo thumb è sempre incluso nella visualizzazione controlli dell'Automazione interfaccia utente albero.                                                                                                                                                                          |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Vedere le note. | Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà. Un controllo thumb può ricevere lo stato attivo se viene usato come oggetto "gripper" per il ridimensionamento di una finestra o di un riquadro. Un controllo thumb in un dispositivo di scorrimento o in una barra di scorrimento non deve mai ricevere lo stato attivo. |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULL       | I controlli Thumb non includono mai un'etichetta.                                                                                                                                                                                                                           |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vedere le note. | Stringa localizzata corrispondente al **tipo di** controllo Thumb. Il valore predefinito è "thumb" per en-US o english (Stati Uniti).                                                                                                                             |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | NULL       | Poiché il controllo thumb non è disponibile nella visualizzazione contenuto dell'albero Automazione interfaccia utente, non richiede un nome.                                                                                                                                        |



 

## <a name="required-control-patterns"></a>Pattern di controllo obbligatori

Nella tabella seguente sono elencati Automazione interfaccia utente di controllo personalizzati che devono essere supportati dai controlli Thumb. Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Pattern di controllo                                         | Supporto  | Note                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) | Obbligatoria | Consente lo spostamento del controllo Thumb sullo schermo. Poiché il controllo thumb in genere non può essere ridimensionato o ruotato, il [pattern di](uiauto-implementingtransform.md) controllo Trasforma supporta principalmente la [**funzione Move.**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-move) |



 

## <a name="required-events"></a>Eventi obbligatori

Nella tabella seguente sono elencati Automazione interfaccia utente eventi che i controlli Thumb devono supportare. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automazione interfaccia utente evento                                                                                                                   | Note                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**Interfaccia \_ utente Evento di modifica della proprietà BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md) |                                                                                                                            |
| [**Interfaccia \_ utente Evento di modifica della proprietà IsEnabledPropertyId.**](uiauto-automation-element-propids.md)                 | Se il controllo supporta la [**proprietà IsEnabled,**](uiauto-automation-element-propids.md) deve supportare questo evento.   |
| [**Interfaccia \_ utente Evento di modifica della proprietà IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)             | Se il controllo supporta la [**proprietà IsOffscreen,**](uiauto-automation-element-propids.md) deve supportare questo evento. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente](uiauto-controltypesoverview.md)
</dt> <dt>

[Cenni preliminari su automazione interfaccia utente](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




