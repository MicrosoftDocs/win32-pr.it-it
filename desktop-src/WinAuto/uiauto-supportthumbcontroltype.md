---
title: Tipo di controllo Thumb
description: In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo Thumb.
ms.assetid: 3b1d6802-cfd4-4b07-80a0-2950ca7f4e96
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo Thumb
- Automazione interfaccia utente, tipo di controllo Thumb
- Automazione interfaccia utente, struttura ad albero per il tipo di controllo Thumb
- Automazione interfaccia utente, proprietà per il tipo di controllo Thumb
- Automazione interfaccia utente, pattern di controllo per il tipo di controllo Thumb
- Automazione interfaccia utente, eventi per il tipo di controllo Thumb
- strutture ad albero, tipo di controllo Thumb
- Proprietà, tipo di controllo Thumb
- pattern di controllo, tipo di controllo Thumb
- eventi, tipo di controllo Thumb
- supporto per il tipo di controllo Thumb
- Thumb (tipo di controllo)
- tipi di controllo, struttura ad albero per il tipo di controllo Thumb
- tipi di controllo, pattern di controllo per il tipo di controllo Thumb
- tipi di controllo, supporto per Thumb
- tipi di controllo, Thumb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8faf60fab30f54d3ed3e4b5a9f49628a3a35be5b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396743"
---
# <a name="thumb-control-type"></a>Tipo di controllo Thumb

In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo **Thumb** .

I controlli Thumb forniscono la funzionalità che consente lo spostamento o il trascinamento di un controllo, ad esempio un pulsante della barra di scorrimento, oppure il ridimensionato, ad esempio un widget per il ridimensionamento della finestra. Si noti che un controllo Thumb non fornisce funzionalità di trascinamento della selezione. I controlli Thumb possono ricevere lo stato attivo del mouse ma non lo stato attivo della tastiera. Lo sviluppatore del controllo deve implementare il controllo in modo che funzioni nel modo appropriato, ovvero possa essere trascinato o ridimensionato.

Nelle sezioni seguenti vengono definiti la struttura ad albero, le proprietà, i pattern di controllo e gli eventi di automazione interfaccia utente necessari per il tipo di controllo **Thumb** . I requisiti di automazione interfaccia utente applicano tutti i controlli Thumb in cui la piattaforma/Framework dell'interfaccia utente integra il supporto di automazione interfaccia utente per tipi di controllo e pattern di controllo.

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Pattern di controllo obbligatori](#required-control-patterns)
-   [Eventi obbligatori](#required-events)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

Nella tabella seguente viene illustrata una tipica visualizzazione del controllo e del contenuto dell'albero di automazione interfaccia utente relativo ai controlli Thumb e viene descritto il possibile contenuto di ogni visualizzazione. Per altre informazioni sull'albero di automazione interfaccia utente, vedere [Cenni preliminari sull'albero di automazione interfaccia utente](uiauto-treeoverview.md).



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
<li>Thumb</li>
</ul></td>
<td>(Non applicabile)</td>
</tr>
</tbody>
</table>



 

I controlli Thumb non vengono mai visualizzati nella visualizzazione contenuto perché esistono solo per essere modificati con il mouse. Sono esposti anche se un altro pattern di controllo, ad esempio il pattern di controllo [Scroll](uiauto-implementingscroll.md) , il pattern di controllo [Transform](uiauto-implementingtransform.md) o il pattern di controllo [RangeValue](uiauto-implementingrangevalue.md) , è supportato nel contenitore del controllo Thumb.

## <a name="relevant-properties"></a>Proprietà rilevanti

La tabella seguente elenca le proprietà di automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per i controlli Thumb. Per altre informazioni sulle proprietà di automazione interfaccia utente, vedere [recupero di proprietà da elementi di automazione interfaccia utente](uiauto-propertiesforclients.md).



| Proprietà di automazione interfaccia utente                                                                                              | Valore      | Note                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_AUTOMATIONIDPROPERTYID UIA**](uiauto-automation-element-propids.md)                 | Vedere le note. | Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata della struttura ad albero di automazione interfaccia utente.                                                                                                                                                 |
| [**\_BOUNDINGRECTANGLEPROPERTYID UIA**](uiauto-automation-element-propids.md)       | Vedere le note. | Il rettangolo più esterno che contiene l'intero controllo.                                                                                                                                                                                                     |
| [**\_CLICKABLEPOINTPROPERTYID UIA**](uiauto-automation-element-propids.md)             | Vedere le note. | Punto all'interno dell'area client visibile del controllo Thumb.                                                                                                                                                                                                 |
| [**\_CONTROLTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md)                   | **Thumb**  |                                                                                                                                                                                                                                                              |
| [**\_ISCONTENTELEMENTPROPERTYID UIA**](uiauto-automation-element-propids.md)         | FALSE      | Il controllo Thumb non è mai incluso nella visualizzazione contenuto dell'albero di automazione interfaccia utente.                                                                                                                                                                           |
| [**\_ISCONTROLELEMENTPROPERTYID UIA**](uiauto-automation-element-propids.md)         | true       | Il controllo Thumb viene sempre incluso nella visualizzazione controlli dell'albero di automazione interfaccia utente.                                                                                                                                                                          |
| [**\_ISKEYBOARDFOCUSABLEPROPERTYID UIA**](uiauto-automation-element-propids.md)   | Vedere le note. | Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà. Un controllo Thumb può ricevere lo stato attivo se viene usato come oggetto "pinza" per dimensionare una finestra o un riquadro. Un controllo Thumb in un dispositivo di scorrimento o una barra di scorrimento non deve mai ricevere lo stato attivo. |
| [**\_LABELEDBYPROPERTYID UIA**](uiauto-automation-element-propids.md)                       | NULL       | I controlli Thumb non includono mai un'etichetta.                                                                                                                                                                                                                           |
| [**\_LOCALIZEDCONTROLTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md) | Vedere le note. | Stringa localizzata corrispondente al tipo di controllo **Thumb** . Il valore predefinito è "thumb" per en-US o inglese (Stati Uniti).                                                                                                                             |
| [**\_NAMEPROPERTYID UIA**](uiauto-automation-element-propids.md)                                 | NULL       | Poiché il controllo Thumb non è disponibile nella visualizzazione contenuto dell'albero di automazione interfaccia utente, non richiede un nome.                                                                                                                                        |



 

## <a name="required-control-patterns"></a>Pattern di controllo obbligatori

La tabella seguente elenca i pattern di controllo di automazione interfaccia utente che devono essere supportati dai controlli Thumb. Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Pattern di controllo                                         | Supporto  | Note                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) | Necessario | Consente lo spostamento del controllo Thumb sullo schermo. Poiché non è in genere possibile ridimensionare o ruotare il controllo Thumb, il pattern di controllo [Transform](uiauto-implementingtransform.md) supporta principalmente la funzione [**Move**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-move) . |



 

## <a name="required-events"></a>Eventi obbligatori

La tabella seguente elenca gli eventi di automazione interfaccia utente necessari per supportare i controlli Thumb. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



| Evento di automazione interfaccia utente                                                                                                                   | Note                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**\_AUTOMATIONFOCUSCHANGEDEVENTID UIA**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà BoundingRectanglePropertyId. |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsEnabledPropertyId.                 | Se il controllo supporta la proprietà [**IsEnabled**](uiauto-automation-element-propids.md) , deve supportare questo evento.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsOffscreenPropertyId.             | Se il controllo supporta la proprietà [**IsOffscreen**](uiauto-automation-element-propids.md) , deve supportare questo evento. |
| [**\_STRUCTURECHANGEDEVENTID UIA**](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente](uiauto-controltypesoverview.md)
</dt> <dt>

[Cenni preliminari su automazione interfaccia utente](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




