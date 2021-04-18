---
title: Tipo di controllo pane
description: In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo pane.
ms.assetid: 2a5d69dc-6880-4610-b481-4371637472ed
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo pane
- Automazione interfaccia utente, tipo di controllo pane
- Automazione interfaccia utente, struttura ad albero per il tipo di controllo pane
- Automazione interfaccia utente, proprietà per il tipo di controllo pane
- Automazione interfaccia utente, pattern di controllo per il tipo di controllo pane
- Automazione interfaccia utente, eventi per il tipo di controllo pane
- strutture ad albero, tipo di controllo pane
- Proprietà, tipo di controllo pane
- pattern di controllo, tipo di controllo pane
- eventi, tipo di controllo pane
- supporto per il tipo di controllo pane
- Pane (tipo di controllo)
- tipi di controllo, struttura ad albero per il tipo di controllo pane
- tipi di controllo, pattern di controllo per il tipo di controllo pane
- tipi di controllo, supporto per il riquadro
- tipi di controllo, riquadro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51b7f22e6fb302ebb160a174c27c61119b8f09fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104565027"
---
# <a name="pane-control-type"></a>Tipo di controllo pane

In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo **pane** .

Il tipo di controllo **pane** è per aree potenzialmente scorrevoli con contenuto diversi. Viene usato per rappresentare un oggetto all'interno di un frame o di una finestra del documento. Gli utenti possono spostarsi tra i controlli del riquadro e all'interno del contenuto del riquadro corrente. I controlli riquadro rappresentano un livello di raggruppamento inferiore rispetto alle finestre o ai documenti, ma superiore ai singoli controlli. L'utente si sposta tra i riquadri premendo TAB, F6 o CTRL+TAB, a seconda del contesto.

Nelle sezioni seguenti vengono definiti la struttura ad albero, le proprietà, i pattern di controllo e gli eventi di automazione interfaccia utente necessari per il tipo di controllo **pane** . I requisiti di automazione interfaccia utente si applicano a tutti i controlli riquadro in cui la piattaforma/Framework dell'interfaccia utente integra il supporto di automazione interfaccia utente per i tipi di controllo e i pattern

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Pattern di controllo obbligatori](#required-control-patterns)
-   [Eventi obbligatori](#required-events)
-   [Esempio di tipo di controllo Pane](#pane-control-type-example)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

Nella tabella seguente viene illustrata una tipica visualizzazione del controllo e del contenuto dell'albero di automazione interfaccia utente relativo ai controlli riquadro e viene descritto il possibile contenuto di ogni visualizzazione. Per altre informazioni sull'albero di automazione interfaccia utente, vedere [Cenni preliminari sull'albero di automazione interfaccia utente](uiauto-treeoverview.md).



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
<li>Riquadro</li>
</ul></td>
<td><ul>
<li>Riquadro</li>
</ul></td>
</tr>
</tbody>
</table>



 

Un controllo riquadro viene sempre visualizzato nelle visualizzazioni controlli e contenuto. Non esporre un oggetto layout come riquadro nel controllo o nella visualizzazione contenuto se l'oggetto viene utilizzato solo per la presentazione visiva.

## <a name="relevant-properties"></a>Proprietà rilevanti

La tabella seguente elenca le proprietà di automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per i controlli riquadro. Per altre informazioni sulle proprietà di automazione interfaccia utente, vedere [recupero di proprietà da elementi di automazione interfaccia utente](uiauto-propertiesforclients.md).



| Proprietà di automazione interfaccia utente                                                                                              | Valore      | Note                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ACCESSKEYPROPERTYID UIA**](uiauto-automation-element-propids.md)                       | Vedere le note. | Se una combinazione di tasti specifica sposta lo stato attivo sul riquadro, le informazioni devono essere esposte tramite questa proprietà.                                                                                                                                                                                                      |
| [**\_AUTOMATIONIDPROPERTYID UIA**](uiauto-automation-element-propids.md)                 | Vedere le note. | Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata della struttura ad albero di automazione interfaccia utente.                                                                                                                                                                                                          |
| [**\_BOUNDINGRECTANGLEPROPERTYID UIA**](uiauto-automation-element-propids.md)       | Vedere le note. | Il rettangolo più esterno che contiene l'intero controllo.                                                                                                                                                                                                                                                              |
| [**\_CLICKABLEPOINTPROPERTYID UIA**](uiauto-automation-element-propids.md)             | Vedere le note. | Questa proprietà espone un punto selezionabile del controllo riquadro che fa sì che il riquadro assuma lo stato attivo quando viene selezionato.                                                                                                                                                                                                |
| [**\_CONTROLTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md)                   | **Riquadro**   |                                                                                                                                                                                                                                                                                                                       |
| [**\_HELPTEXTPROPERTYID UIA**](uiauto-automation-element-propids.md)                         | Vedere le note. | Il testo della Guida per i controlli riquadro deve illustrare lo scopo del frame e il modo in cui si riferisce ad altri frame. Una descrizione è necessaria se lo scopo e la relazione dei frame non sono deselezionati dal valore della [**proprietà \_ NamePropertyId di UIA**](uiauto-automation-element-propids.md) . |
| [**\_ISCONTENTELEMENTPROPERTYID UIA**](uiauto-automation-element-propids.md)         | true       | Il controllo riquadro viene sempre incluso nella visualizzazione contenuto dell'albero di automazione interfaccia utente.                                                                                                                                                                                                                                    |
| [**\_ISCONTROLELEMENTPROPERTYID UIA**](uiauto-automation-element-propids.md)         | true       | Il controllo riquadro viene sempre incluso nella visualizzazione controlli dell'albero di automazione interfaccia utente.                                                                                                                                                                                                                                    |
| [**\_ISKEYBOARDFOCUSABLEPROPERTYID UIA**](uiauto-automation-element-propids.md)   | Vedere le note. | Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.                                                                                                                                                                                                                                             |
| [**\_LABELEDBYPROPERTYID UIA**](uiauto-automation-element-propids.md)                       | Vedere le note. | I controlli riquadro in genere non hanno un'etichetta statica. Se è presente un'etichetta di testo statico, l'etichetta deve essere esposta tramite questa proprietà.                                                                                                                                                                                      |
| [**\_LOCALIZEDCONTROLTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md) | Vedere le note. | Stringa localizzata corrispondente al tipo di controllo **pane** . Il valore predefinito è "pane" per en-US o inglese (Stati Uniti).                                                                                                                                                                                        |
| [**\_NAMEPROPERTYID UIA**](uiauto-automation-element-propids.md)                                 | Vedere le note. | Il valore di questa proprietà deve essere sempre un titolo chiaro, conciso e significativo.                                                                                                                                                                                                                                     |



 

## <a name="required-control-patterns"></a>Pattern di controllo obbligatori

La tabella seguente elenca i pattern di controllo di automazione interfaccia utente che devono essere supportati dai controlli riquadro. Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Pattern di controllo                                         | Supporto | Note                                                                                                                                                                                         |
|---------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider)           | Dipende da | Implementare il pattern di controllo [Dock](uiauto-implementingdock.md) se il controllo riquadro può essere ancorato.                                                                                          |
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)       | Dipende da | Implementare il pattern di controllo [Scroll](uiauto-implementingscroll.md) se è possibile scorrere il controllo riquadro.                                                                                    |
| [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) | Dipende da | Implementare il pattern di controllo [Transform](uiauto-implementingtransform.md) se il controllo riquadro può essere spostato, ridimensionato o ruotato sullo schermo.                                              |
| [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider)       | Mai   | Se l'elemento deve implementare il pattern di controllo [Window](uiauto-implementingwindow.md) , il controllo deve essere basato sul tipo di controllo [Window](uiauto-supportwindowcontroltype.md) . |



 

## <a name="required-events"></a>Eventi obbligatori

La tabella seguente elenca gli eventi di automazione interfaccia utente necessari per supportare i controlli riquadro. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



| Evento di automazione interfaccia utente                                                                                                                                        | Note                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**\_ASYNCCONTENTLOADEDEVENTID UIA**](uiauto-event-ids.md)                                                                   |                                                                                                                            |
| [**\_AUTOMATIONFOCUSCHANGEDEVENTID UIA**](uiauto-event-ids.md)                                                           |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà BoundingRectanglePropertyId.                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsOffscreenPropertyId.                                  | Se il controllo supporta la proprietà [**IsOffscreen**](uiauto-automation-element-propids.md) , deve supportare questo evento. |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ScrollHorizontallyScrollablePropertyId.   | Se il controllo supporta il pattern di controllo [Scroll](uiauto-implementingscroll.md) , deve supportare questo evento.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ScrollHorizontalScrollPercentPropertyId. | Se il controllo supporta il pattern di controllo [Scroll](uiauto-implementingscroll.md) , deve supportare questo evento.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ScrollHorizontalViewSizePropertyId.           | Se il controllo supporta il pattern di controllo [Scroll](uiauto-implementingscroll.md) , deve supportare questo evento.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ScrollVerticallyScrollablePropertyId.       | Se il controllo supporta il pattern di controllo [Scroll](uiauto-implementingscroll.md) , deve supportare questo evento.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ScrollVerticalScrollPercentPropertyId.     | Se il controllo supporta il pattern di controllo [Scroll](uiauto-implementingscroll.md) , deve supportare questo evento.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ScrollVerticalViewSizePropertyId.               | Se il controllo supporta il pattern di controllo [Scroll](uiauto-implementingscroll.md) , deve supportare questo evento.           |
| [**\_STRUCTURECHANGEDEVENTID UIA**](uiauto-event-ids.md)                                                                       |                                                                                                                            |



 

## <a name="pane-control-type-example"></a>Esempio di tipo di controllo Pane

Nell'immagine seguente viene illustrato un controllo che implementa il tipo di controllo **pane** .

![screenshot che mostra l'esempio di un controllo riquadro](images/panexmpl.jpg)



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Albero di automazione interfaccia utente-visualizzazione controlli</th>
<th>Albero di automazione interfaccia utente-visualizzazione contenuto</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li>Riquadro
<ul>
<li>Tree (pattern Scroll)
<ul>
<li>TreeItem</li>
<li>...</li>
</ul></li>
</ul></li>
<li>Riquadro
<ul>
<li>Edit (pattern scroll)</li>
</ul></li>
</ul></td>
<td><ul>
<li>Riquadro
<ul>
<li>Tree (pattern Scroll)
<ul>
<li>TreeItem</li>
<li>...</li>
</ul></li>
<li>Riquadro
<ul>
<li>Edit (pattern scroll)</li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente](uiauto-controltypesoverview.md)
</dt> <dt>

[Cenni preliminari su automazione interfaccia utente](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




