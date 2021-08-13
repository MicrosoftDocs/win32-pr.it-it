---
title: Tipo di controllo ScrollBar
description: Questo argomento fornisce informazioni sul supporto di Microsoft Automazione interfaccia utente per il tipo di controllo ScrollBar.
ms.assetid: c89ca087-3e93-4e86-ac79-731e3e7a361d
keywords:
- Automazione interfaccia utente,supporto per il tipo di controllo ScrollBar
- Automazione interfaccia utente,Tipo di controllo ScrollBar
- Automazione interfaccia utente,struttura ad albero per il tipo di controllo ScrollBar
- Automazione interfaccia utente,proprietà per il tipo di controllo ScrollBar
- Automazione interfaccia utente,pattern di controllo per il tipo di controllo ScrollBar
- Automazione interfaccia utente,eventi per il tipo di controllo ScrollBar
- strutture ad albero, tipo di controllo ScrollBar
- proprietà,Tipo di controllo ScrollBar
- pattern di controllo,tipo di controllo ScrollBar
- eventi, tipo di controllo ScrollBar
- supporto per il tipo di controllo ScrollBar
- Tipo di controllo ScrollBar
- tipi di controllo, struttura ad albero per il tipo di controllo ScrollBar
- tipi di controllo,pattern di controllo per il tipo di controllo ScrollBar
- tipi di controllo, supporto per ScrollBar
- tipi di controllo,ScrollBar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a25d0398ca8e094e1dbec5e06eb725f3e9d7edbb5c193fdc3699e166b118142
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119413371"
---
# <a name="scrollbar-control-type"></a>Tipo di controllo ScrollBar

Questo argomento fornisce informazioni sul supporto microsoft Automazione interfaccia utente per il **tipo di controllo ScrollBar.**

I controlli barra di scorrimento consentono agli utenti di scorrere il contenuto all'interno di una finestra o un contenitore di elementi. Il controllo è costituito da un set di pulsanti e da un controllo thumb.

Le sezioni seguenti definiscono la struttura ad Automazione interfaccia utente, le proprietà, i pattern di controllo e gli eventi necessari per il **tipo di controllo ScrollBar.** I Automazione interfaccia utente si applicano a tutti i controlli barra di scorrimento in cui il framework o la piattaforma dell'interfaccia utente si integra Automazione interfaccia utente per i tipi di controllo e i pattern di controllo.

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Pattern di controllo obbligatori](#required-control-patterns)
-   [Eventi obbligatori](#required-events)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

La tabella seguente illustra un controllo tipico e una visualizzazione contenuto dell'albero Automazione interfaccia utente che riguarda i controlli barra di scorrimento e descrive cosa può essere contenuto in ogni visualizzazione. Per altre informazioni sull'albero Automazione interfaccia utente, vedere [Automazione interfaccia utente Tree Overview](uiauto-treeoverview.md).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Visualizzazione controlli</th>
<th>Visualizzazione contenuto</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li>ScrollBar
<ul>
<li>Pulsante (0, 2 o 4)</li>
<li>Thumb (0 o 1)</li>
</ul></li>
</ul></td>
<td>Non applicabile. Il controllo barra di scorrimento non ha contenuto.</td>
</tr>
</tbody>
</table>



 

Il controllo barra di scorrimento può avere da zero a cinque elementi figlio. Poiché il sottoalbero ha più di un controllo pulsante, l'elemento deve impostare un valore [**\_ AutomationIdPropertyId**](uiauto-automation-element-propids.md) dell'interfaccia utente specifico su ogni elemento per renderlo individuabile per gli strumenti di test automatizzati.

## <a name="relevant-properties"></a>Proprietà rilevanti

La tabella seguente elenca le proprietà Automazione interfaccia utente il cui valore o definizione è particolarmente rilevante per i controlli barra di scorrimento. Si noti che un controllo barra di scorrimento non ha mai contenuto; la relativa funzionalità viene esposta tramite il pattern di controllo [Scroll,](uiauto-implementingscroll.md) supportato nel contenitore da scorrere.

Per altre informazioni sulle Automazione interfaccia utente, vedere Recupero di proprietà [da Automazione interfaccia utente elementi](uiauto-propertiesforclients.md).



| Proprietà di automazione interfaccia utente                                                                                              | Valore         | Note                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Vedere le note.    | Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata dell'Automazione interfaccia utente albero.                                                                                                                                                                                                                                                                                                                                                                    |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vedere le note.    | Il rettangolo più esterno che contiene l'intero controllo.                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | NaN           | Il controllo barra di scorrimento non dispone di punti selezionabili.                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **ScrollBar** | Questo valore è uguale per tutti i framework. Le barre di scorrimento che funzionano come dispositivi di scorrimento devono usare il [tipo di controllo Slider.](uiauto-supportslidercontroltype.md)                                                                                                                                                                                                                                                                                                                        |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | FALSE         | Il controllo barra di scorrimento non è mai un elemento di contenuto. Se la barra di scorrimento è un controllo autonomo, deve soddisfare il tipo di controllo [Slider](uiauto-supportslidercontroltype.md) e restituire [**UIA \_ SliderControlTypeId**](uiauto-controltype-ids.md) per la proprietà [**IUIAutomationElement::CurrentControlType**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentcontroltype) (o [**CachedControlType).**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedcontroltype) |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | true          | Il controllo barra di scorrimento è sempre incluso nella visualizzazione controlli dell'Automazione interfaccia utente albero.                                                                                                                                                                                                                                                                                                                                                                                        |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Vedere le note.    | Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà. Un controllo barra di scorrimento prende raramente lo stato attivo, ma quando lo fa, lo stato attivo deve rimanere sul controllo stesso della barra di scorrimento, non sui pulsanti figlio o sulla casella di scorrimento. L'utente deve essere in grado di eseguire tutte le azioni di scorrimento usando i tasti FRECCIA SU e FRECCIA GIÙ (o FRECCIA DESTRA e FRECCIA SINISTRA) o i tasti PGGIS e PGGIUTO.                                                                |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULL          | Le barre di scorrimento non hanno etichette.                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vedere le note.    | Stringa localizzata corrispondente al **tipo di controllo ScrollBar.** Il valore predefinito è "barra di scorrimento" per en-US o inglese (Stati Uniti).                                                                                                                                                                                                                                                                                                                                       |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | NULL          | Il controllo barra di scorrimento non include elementi di contenuto e non è necessario impostare la proprietà [**\_ UIA NamePropertyId.**](uiauto-automation-element-propids.md)                                                                                                                                                                                                                                                                                           |
| [**UIA \_ OrientationPropertyId**](uiauto-automation-element-propids.md)                   | Vedere le note.    | Il controllo barra di scorrimento deve sempre esporre il relativo orientamento orizzontale o verticale.                                                                                                                                                                                                                                                                                                                                                                                               |



 

## <a name="required-control-patterns"></a>Pattern di controllo obbligatori

Nella tabella seguente sono elencati i Automazione interfaccia utente di controllo necessari per essere supportati da tutti i controlli barra di scorrimento. Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).

> [!Note]  
> Quando una barra di scorrimento viene usata come controllo solo per la manipolazione del mouse, non supporta i pattern di controllo. Se viene usato come controllo dispositivo di scorrimento all'interno di un'applicazione, deve essere specificato il [tipo di controllo Dispositivo](uiauto-supportslidercontroltype.md) di scorrimento.

 



| Pattern di controllo                                           | Supporto | Note                                                                                                                                                                                                                          |
|-----------------------------------------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) | Dipende da | Il [pattern di controllo RangeValue](uiauto-implementingrangevalue.md) deve essere supportato solo se il pattern di controllo [Scroll](uiauto-implementingscroll.md) non è supportato nel contenitore con la barra di scorrimento. |
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)         | Mai   | Il [pattern di](uiauto-implementingscroll.md) controllo Scroll non è mai supportato direttamente sulla barra di scorrimento.                                                                                                                     |



 

## <a name="required-events"></a>Eventi obbligatori

Nella tabella seguente sono elencati Automazione interfaccia utente eventi che i controlli barra di scorrimento devono supportare. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automazione interfaccia utente evento                                                                                                                   | Note                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**Interfaccia \_ utente Evento di modifica della proprietà BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md) |                                                                                                                            |
| [**Interfaccia \_ utente Evento di modifica della proprietà IsEnabledPropertyId.**](uiauto-automation-element-propids.md)                 | Se il controllo supporta la [**proprietà IsEnabled,**](uiauto-automation-element-propids.md) deve supportare questo evento.   |
| [**Interfaccia \_ utente Evento di modifica della proprietà IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)             | Se il controllo supporta la [**proprietà IsOffscreen,**](uiauto-automation-element-propids.md) deve supportare questo evento. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |
| [**Interfaccia \_ utente Evento di modifica della proprietà RangeValueValuePropertyId.**](uiauto-control-pattern-propids.md)        | Se il controllo supporta il pattern [di controllo RangeValue,](uiauto-implementingrangevalue.md) deve supportare questo evento.   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente](uiauto-controltypesoverview.md)
</dt> <dt>

[Cenni preliminari su automazione interfaccia utente](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




