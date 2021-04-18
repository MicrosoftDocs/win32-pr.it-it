---
title: Tipo di controllo ScrollBar
description: In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo ScrollBar.
ms.assetid: c89ca087-3e93-4e86-ac79-731e3e7a361d
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo ScrollBar
- Automazione interfaccia utente, tipo di controllo ScrollBar
- Automazione interfaccia utente, struttura ad albero per il tipo di controllo ScrollBar
- Automazione interfaccia utente, proprietà per il tipo di controllo ScrollBar
- Automazione interfaccia utente, pattern di controllo per il tipo di controllo ScrollBar
- Automazione interfaccia utente, eventi per il tipo di controllo ScrollBar
- strutture ad albero, tipo di controllo ScrollBar
- Proprietà, tipo di controllo ScrollBar
- pattern di controllo, tipo di controllo ScrollBar
- eventi, tipo di controllo ScrollBar
- supporto per il tipo di controllo ScrollBar
- Tipo di controllo ScrollBar
- tipi di controllo, struttura ad albero per il tipo di controllo ScrollBar
- tipi di controllo, pattern di controllo per il tipo di controllo ScrollBar
- tipi di controllo, supporto per ScrollBar
- tipi di controllo, barra di scorrimento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2168401c313dd9139f44ba615de945802b307d64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298567"
---
# <a name="scrollbar-control-type"></a>Tipo di controllo ScrollBar

In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo **ScrollBar** .

I controlli barra di scorrimento consentono agli utenti di scorrere il contenuto all'interno di una finestra o un contenitore di elementi. Il controllo è costituito da un set di pulsanti e da un controllo Thumb.

Nelle sezioni seguenti vengono definiti la struttura ad albero, le proprietà, i pattern di controllo e gli eventi di automazione interfaccia utente necessari per il tipo di controllo **ScrollBar** . I requisiti di automazione interfaccia utente si applicano a tutti i controlli barra di scorrimento in cui la piattaforma/Framework dell'interfaccia utente integra il supporto di automazione interfaccia utente per i tipi di controllo e i pattern

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Pattern di controllo obbligatori](#required-control-patterns)
-   [Eventi obbligatori](#required-events)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

Nella tabella seguente viene illustrata una tipica visualizzazione del controllo e del contenuto dell'albero di automazione interfaccia utente relativo ai controlli barra di scorrimento e viene descritto il possibile contenuto di ogni visualizzazione. Per altre informazioni sull'albero di automazione interfaccia utente, vedere [Cenni preliminari sull'albero di automazione interfaccia utente](uiauto-treeoverview.md).



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
<li>Button (0, 2 o 4)</li>
<li>Thumb (0 o 1)</li>
</ul></li>
</ul></td>
<td>Non applicabile. Il controllo barra di scorrimento non dispone di contenuto.</td>
</tr>
</tbody>
</table>



 

Il controllo barra di scorrimento può avere da zero a cinque elementi figlio. Poiché il sottoalbero contiene più di un controllo Button, l'elemento deve impostare un valore specifico di [**\_ AutomationIdPropertyId**](uiauto-automation-element-propids.md) per ogni elemento in modo da renderlo individuabile per gli strumenti di test automatizzati.

## <a name="relevant-properties"></a>Proprietà rilevanti

La tabella seguente elenca le proprietà di automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per i controlli barra di scorrimento. Si noti che un controllo barra di scorrimento non dispone mai di contenuto; la relativa funzionalità viene esposta tramite il pattern di controllo [Scroll](uiauto-implementingscroll.md) , che è supportato nel contenitore sottoposto a scorrimento.

Per altre informazioni sulle proprietà di automazione interfaccia utente, vedere [recupero di proprietà da elementi di automazione interfaccia utente](uiauto-propertiesforclients.md).



| Proprietà di automazione interfaccia utente                                                                                              | Valore         | Note                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_AUTOMATIONIDPROPERTYID UIA**](uiauto-automation-element-propids.md)                 | Vedere le note.    | Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata della struttura ad albero di automazione interfaccia utente.                                                                                                                                                                                                                                                                                                                                                                    |
| [**\_BOUNDINGRECTANGLEPROPERTYID UIA**](uiauto-automation-element-propids.md)       | Vedere le note.    | Il rettangolo più esterno che contiene l'intero controllo.                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**\_CLICKABLEPOINTPROPERTYID UIA**](uiauto-automation-element-propids.md)             | NaN           | Il controllo barra di scorrimento non dispone di punti selezionabili.                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**\_CONTROLTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md)                   | **ScrollBar** | Questo valore è uguale per tutti i framework. Le barre di scorrimento che funzionano come dispositivi di scorrimento devono usare il tipo di controllo [Slider](uiauto-supportslidercontroltype.md) .                                                                                                                                                                                                                                                                                                                        |
| [**\_ISCONTENTELEMENTPROPERTYID UIA**](uiauto-automation-element-propids.md)         | FALSE         | Il controllo barra di scorrimento non è mai un elemento di contenuto. Se la barra di scorrimento è un controllo autonomo, deve soddisfare il tipo di controllo [Slider](uiauto-supportslidercontroltype.md) e restituire [**\_ SliderControlTypeId**](uiauto-controltype-ids.md) per la proprietà [**IUIAutomationElement:: CurrentControlType**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentcontroltype) (o [**CachedControlType**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedcontroltype)). |
| [**\_ISCONTROLELEMENTPROPERTYID UIA**](uiauto-automation-element-propids.md)         | true          | Il controllo barra di scorrimento viene sempre incluso nella visualizzazione controlli dell'albero di automazione interfaccia utente.                                                                                                                                                                                                                                                                                                                                                                                        |
| [**\_ISKEYBOARDFOCUSABLEPROPERTYID UIA**](uiauto-automation-element-propids.md)   | Vedere le note.    | Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà. Un controllo barra di scorrimento assume raramente lo stato attivo, ma in questo caso lo stato attivo deve rimanere sul controllo barra di scorrimento, non sui pulsanti figlio o sul pollice. L'utente deve essere in grado di eseguire tutte le azioni di scorrimento usando i tasti freccia su e freccia giù (o freccia destra e freccia sinistra) oppure la pagina su e i tasti PGGIÙ.                                                                |
| [**\_LABELEDBYPROPERTYID UIA**](uiauto-automation-element-propids.md)                       | NULL          | Le barre di scorrimento non hanno etichette.                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**\_LOCALIZEDCONTROLTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md) | Vedere le note.    | Stringa localizzata corrispondente al tipo di controllo **ScrollBar** . Il valore predefinito è "barra di scorrimento" per en-US o inglese (Stati Uniti).                                                                                                                                                                                                                                                                                                                                       |
| [**\_NAMEPROPERTYID UIA**](uiauto-automation-element-propids.md)                                 | NULL          | Il controllo barra di scorrimento non include elementi di contenuto e non è necessario impostare la proprietà [**\_ NamePropertyId di UIA**](uiauto-automation-element-propids.md) .                                                                                                                                                                                                                                                                                           |
| [**\_ORIENTATIONPROPERTYID UIA**](uiauto-automation-element-propids.md)                   | Vedere le note.    | Il controllo barra di scorrimento deve sempre esporre il relativo orientamento orizzontale o verticale.                                                                                                                                                                                                                                                                                                                                                                                               |



 

## <a name="required-control-patterns"></a>Pattern di controllo obbligatori

La tabella seguente elenca i pattern di controllo di automazione interfaccia utente che devono essere supportati da tutti i controlli barra di scorrimento. Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).

> [!Note]  
> Quando una barra di scorrimento viene usata come controllo solo per la manipolazione del mouse, non supporta pattern di controllo. Se viene usata come controllo dispositivo di scorrimento all'interno di un'applicazione, è necessario assegnare il tipo di controllo [Slider](uiauto-supportslidercontroltype.md) .

 



| Pattern di controllo                                           | Supporto | Note                                                                                                                                                                                                                          |
|-----------------------------------------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) | Dipende da | È necessario che il pattern di controllo [RangeValue](uiauto-implementingrangevalue.md) sia supportato solo se il pattern di controllo [Scroll](uiauto-implementingscroll.md) non è supportato nel contenitore con la barra di scorrimento. |
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)         | Mai   | Il pattern di controllo [Scroll](uiauto-implementingscroll.md) non è mai supportato direttamente nella barra di scorrimento.                                                                                                                     |



 

## <a name="required-events"></a>Eventi obbligatori

La tabella seguente elenca gli eventi di automazione interfaccia utente che sono necessari per supportare i controlli barra di scorrimento. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



| Evento di automazione interfaccia utente                                                                                                                   | Note                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**\_AUTOMATIONFOCUSCHANGEDEVENTID UIA**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà BoundingRectanglePropertyId. |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsEnabledPropertyId.                 | Se il controllo supporta la proprietà [**IsEnabled**](uiauto-automation-element-propids.md) , deve supportare questo evento.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsOffscreenPropertyId.             | Se il controllo supporta la proprietà [**IsOffscreen**](uiauto-automation-element-propids.md) , deve supportare questo evento. |
| [**\_STRUCTURECHANGEDEVENTID UIA**](uiauto-event-ids.md)                                                  |                                                                                                                            |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà RangeValueValuePropertyId.        | Se il controllo supporta il pattern di controllo [RangeValue](uiauto-implementingrangevalue.md) , deve supportare questo evento.   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente](uiauto-controltypesoverview.md)
</dt> <dt>

[Cenni preliminari su automazione interfaccia utente](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




