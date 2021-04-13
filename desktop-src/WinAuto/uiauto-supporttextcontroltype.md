---
title: Tipo di controllo Text
description: In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo Text.
ms.assetid: 69a3b243-8ee5-48e4-a01e-c7ad69b9a3aa
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo Text
- Automazione interfaccia utente, tipo di controllo Text
- Automazione interfaccia utente, struttura ad albero per il tipo di controllo Text
- Automazione interfaccia utente, proprietà per il tipo di controllo Text
- Automazione interfaccia utente, pattern di controllo per il tipo di controllo Text
- Automazione interfaccia utente, eventi per il tipo di controllo Text
- strutture ad albero, tipo di controllo Text
- Proprietà, tipo di controllo Text
- pattern di controllo, tipo di controllo Text
- eventi, tipo di controllo Text
- supporto per il tipo di controllo Text
- Text (tipo di controllo)
- tipi di controllo, struttura ad albero per il tipo di controllo Text
- tipi di controllo, pattern di controllo per il tipo di controllo Text
- tipi di controllo, supporto del testo
- tipi di controllo, testo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 902b3c7c523417abde2c60e1f8039ad9f2c322b8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331100"
---
# <a name="text-control-type"></a>Tipo di controllo Text

In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo **Text** .

Un controllo testo è un elemento di base dell'interfaccia utente che rappresenta una parte di testo sullo schermo.

Nelle sezioni seguenti vengono definiti la struttura ad albero, le proprietà, i pattern di controllo e gli eventi di automazione interfaccia utente necessari per il tipo di controllo **Text** . I requisiti di automazione interfaccia utente si applicano a tutti i controlli struttura ad albero in cui la piattaforma/Framework dell'interfaccia utente integra il supporto di automazione interfaccia utente per i tipi di controllo e

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Pattern di controllo obbligatori](#required-control-patterns)
-   [Eventi obbligatori](#required-events)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

Nella tabella seguente viene illustrata una tipica visualizzazione del controllo e del contenuto dell'albero di automazione interfaccia utente relativo ai controlli testo e viene descritto il possibile contenuto di ogni visualizzazione. Per altre informazioni sull'albero di automazione interfaccia utente, vedere [Cenni preliminari sull'albero di automazione interfaccia utente](uiauto-treeoverview.md).



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
<li>Testo</li>
</ul></td>
<td><ul>
<li>Testo (se contenuto)</li>
</ul></td>
</tr>
</tbody>
</table>



 

Un controllo testo può essere usato da solo come etichetta o come testo statico in un form. Può anche essere contenuto all'interno della struttura di uno degli elementi seguenti:

-   [DataItem](uiauto-supportdataitemcontroltype.md)
-   [ListItem](uiauto-supportlistitemcontroltype.md)
-   [TreeItem](uiauto-supporttreeitemcontroltype.md)

I controlli testo potrebbero non essere visualizzati nella visualizzazione contenuto dell'albero di automazione interfaccia utente perché il testo viene spesso visualizzato tramite la proprietà **Name** di un altro controllo. Ad esempio, il testo usato per etichettare un controllo casella combinata viene esposto tramite la proprietà **Name** del controllo. Poiché il controllo casella combinata si trova nella visualizzazione contenuto dell'albero di automazione interfaccia utente, il controllo testo non deve essere presente. I controlli testo possono avere elementi figlio nella visualizzazione contenuto se è presente un oggetto incorporato, ad esempio un collegamento ipertestuale.

## <a name="relevant-properties"></a>Proprietà rilevanti

La tabella seguente elenca le proprietà di automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per i controlli testo. Per altre informazioni sulle proprietà di automazione interfaccia utente, vedere [recupero di proprietà da elementi di automazione interfaccia utente](uiauto-propertiesforclients.md).



| Proprietà di automazione interfaccia utente                                                                                              | Valore      | Note                                                                                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_AUTOMATIONIDPROPERTYID UIA**](uiauto-automation-element-propids.md)                 | Vedere le note. | Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata della struttura ad albero di automazione interfaccia utente.                                                                                                                                                                                                                                        |
| [**\_BOUNDINGRECTANGLEPROPERTYID UIA**](uiauto-automation-element-propids.md)       | Vedere le note. | Il rettangolo più esterno che contiene l'intero controllo.                                                                                                                                                                                                                                                                                            |
| [**\_CLICKABLEPOINTPROPERTYID UIA**](uiauto-automation-element-propids.md)             | Vedere le note. | Supportata se è presente un rettangolo di delimitazione. Se non tutti i punti all'interno del rettangolo di delimitazione sono selezionabili e l'elemento esegue un hit testing specializzato, eseguire l'override e fornire un punto selezionabile.                                                                                                                                                |
| [**\_CONTROLTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md)                   | **Text**   |                                                                                                                                                                                                                                                                                                                                                     |
| [**\_ISCONTENTELEMENTPROPERTYID UIA**](uiauto-automation-element-propids.md)         | Dipende da    | Il controllo testo è contenuto se contiene informazioni non esposte nella proprietà Name di un altro controllo.                                                                                                                                                                                                                                              |
| [**\_ISCONTROLELEMENTPROPERTYID UIA**](uiauto-automation-element-propids.md)         | true       | Il controllo testo deve essere sempre un controllo.                                                                                                                                                                                                                                                                                                          |
| [**\_ISKEYBOARDFOCUSABLEPROPERTYID UIA**](uiauto-automation-element-propids.md)   | Vedere le note. | Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.                                                                                                                                                                                                                                                                           |
| [**\_LABELEDBYPROPERTYID UIA**](uiauto-automation-element-propids.md)                       | NULL       | I controlli Text non hanno un'etichetta di testo statico.                                                                                                                                                                                                                                                                                                      |
| [**\_LOCALIZEDCONTROLTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md) | Vedere le note. | Stringa localizzata corrispondente al tipo di controllo **Text** . Il valore predefinito è "Text" per en-US o inglese (Stati Uniti).                                                                                                                                                                                                                      |
| [**\_NAMEPROPERTYID UIA**](uiauto-automation-element-propids.md)                                 | Vedere le note. | Il nome di un controllo testo può essere il testo visualizzato. Tuttavia, se il controllo supporta anche il modello di [testo](uiauto-implementingtextandtextrange.md) e il testo è esteso, non usare il contenuto full-text come valore del **nome** . Fornire invece un valore di **nome** più breve, derivato da altre proprietà del controllo. |



 

## <a name="required-control-patterns"></a>Pattern di controllo obbligatori

La tabella seguente elenca i pattern di controllo di automazione interfaccia utente che devono essere supportati dai controlli testo. Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Pattern di controllo                                         | Supporto | Note                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)   | Dipende da | Se il controllo di testo è contenuto in un controllo Table, è necessario che il pattern di controllo [GridItem](uiauto-implementinggriditem.md) sia supportato.                                                                                                                            |
| [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) | Dipende da | Se il controllo testo è contenuto in un controllo Table, è necessario che il pattern di controllo [TableItem](uiauto-implementingtableitem.md) sia supportato.                                                                                                                          |
| [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider)           | Dipende da | Il testo deve supportare il pattern di controllo [Text](uiauto-implementingtextandtextrange.md) per una migliore accessibilità; Tuttavia, non è obbligatorio. Il pattern di controllo Text è utile quando il testo ha stili di formattazione e attributi, ad esempio colore, grassetto e corsivo. |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)         | Mai   | Un controllo di testo non supporta mai il pattern di controllo [value](uiauto-implementingvalue.md) . Se il testo è modificabile, è il tipo di controllo [Edit](uiauto-supporteditcontroltype.md) .                                                                                    |



 

## <a name="required-events"></a>Eventi obbligatori

La tabella seguente elenca gli eventi di automazione interfaccia utente necessari per supportare i controlli testo. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



| Evento di automazione interfaccia utente                                                                                                                   | Note                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**\_AUTOMATIONFOCUSCHANGEDEVENTID UIA**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà BoundingRectanglePropertyId. |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsEnabledPropertyId.                 | Se il controllo supporta la proprietà [**IsEnabled**](uiauto-automation-element-propids.md) , deve supportare questo evento.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsOffscreenPropertyId.             | Se il controllo supporta la proprietà [**IsOffscreen**](uiauto-automation-element-propids.md) , deve supportare questo evento. |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà NamePropertyId.                           |                                                                                                                            |
| [**\_STRUCTURECHANGEDEVENTID UIA**](uiauto-event-ids.md)                                                  |                                                                                                                            |
| [**\_TextChangedEventId testo \_ UIA**](uiauto-event-ids.md)                                                 | Se il controllo supporta il pattern di controllo [Text](uiauto-implementingtextandtextrange.md) , deve supportare questo evento.   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente](uiauto-controltypesoverview.md)
</dt> <dt>

[Cenni preliminari su automazione interfaccia utente](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




