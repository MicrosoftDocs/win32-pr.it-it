---
title: Tipo di controllo Text
description: In questo argomento vengono fornite informazioni sul supporto Automazione interfaccia utente microsoft per il tipo di controllo Text.
ms.assetid: 69a3b243-8ee5-48e4-a01e-c7ad69b9a3aa
keywords:
- Automazione interfaccia utente,supporto per il tipo di controllo Text
- Automazione interfaccia utente,Tipo di controllo Testo
- Automazione interfaccia utente,struttura ad albero per il tipo di controllo Text
- Automazione interfaccia utente,proprietà per il tipo di controllo Text
- Automazione interfaccia utente,pattern di controllo per il tipo di controllo Text
- Automazione interfaccia utente,eventi per il tipo di controllo Text
- strutture ad albero, tipo di controllo Text
- proprietà, tipo di controllo Text
- pattern di controllo, tipo di controllo Text
- eventi, tipo di controllo Text
- supporto per il tipo di controllo Text
- Text (tipo di controllo)
- tipi di controllo, struttura ad albero per il tipo di controllo Text
- tipi di controllo, pattern di controllo per il tipo di controllo Text
- tipi di controllo, supporto per Text
- tipi di controllo,Testo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7e5e7175ca0a394352076a463a63c799e47b871e48641296c51f9f76f7b623e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098141"
---
# <a name="text-control-type"></a>Tipo di controllo Text

In questo argomento vengono fornite informazioni sul supporto Automazione interfaccia utente Microsoft per il **tipo di controllo** Text.

Un controllo di testo è un elemento dell'interfaccia utente di base che rappresenta una parte di testo sullo schermo.

Nelle sezioni seguenti vengono definiti i Automazione interfaccia utente struttura ad albero, le proprietà, i pattern di controllo e gli eventi per il **tipo di controllo** Text. I Automazione interfaccia utente si applicano a tutti i controlli albero in cui il framework o la piattaforma dell'interfaccia utente si integra Automazione interfaccia utente per i tipi di controllo e i pattern di controllo.

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Pattern di controllo obbligatori](#required-control-patterns)
-   [Eventi obbligatori](#required-events)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

La tabella seguente illustra un controllo tipico e una visualizzazione contenuto dell'albero Automazione interfaccia utente relativo ai controlli di testo e descrive gli elementi che possono essere contenuti in ogni visualizzazione. Per altre informazioni sull'albero Automazione interfaccia utente, vedere panoramica [Automazione interfaccia utente albero di .](uiauto-treeoverview.md)



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

I controlli di testo potrebbero non essere visualizzati nella visualizzazione contenuto dell'albero Automazione interfaccia utente perché il testo viene spesso visualizzato tramite la **proprietà Name** di un altro controllo. Ad esempio, il testo usato per etichettare un controllo casella combinata viene esposto tramite la proprietà **Name del** controllo. Poiché il controllo casella combinata si trova nella visualizzazione contenuto dell'albero Automazione interfaccia utente, il controllo di testo non deve essere presente. I controlli di testo possono avere elementi figlio nella visualizzazione contenuto se è presente un oggetto incorporato, ad esempio un collegamento ipertestuale.

## <a name="relevant-properties"></a>Proprietà rilevanti

La tabella seguente elenca le Automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per i controlli di testo. Per altre informazioni sulle Automazione interfaccia utente, vedere [Recupero di proprietà da Automazione interfaccia utente elementi](uiauto-propertiesforclients.md).



| Proprietà di automazione interfaccia utente                                                                                              | Valore      | Note                                                                                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Vedere le note. | Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata dell'Automazione interfaccia utente albero.                                                                                                                                                                                                                                        |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vedere le note. | Il rettangolo più esterno che contiene l'intero controllo.                                                                                                                                                                                                                                                                                            |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vedere le note. | Supportata se è presente un rettangolo di delimitazione. Se non tutti i punti all'interno del rettangolo di delimitazione sono selezionabili e l'elemento esegue hit testing specializzati, eseguire l'override e fornire un punto selezionabile.                                                                                                                                                |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Text**   |                                                                                                                                                                                                                                                                                                                                                     |
| [**\_IsContentElementPropertyId dell'interfaccia utente**](uiauto-automation-element-propids.md)         | Dipende da    | Il controllo testo è contenuto se contiene informazioni non esposte nella proprietà Name di un altro controllo.                                                                                                                                                                                                                                              |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | true       | Il controllo testo deve essere sempre un controllo.                                                                                                                                                                                                                                                                                                          |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Vedere le note. | Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.                                                                                                                                                                                                                                                                           |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULL       | I controlli Text non hanno un'etichetta di testo statico.                                                                                                                                                                                                                                                                                                      |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vedere le note. | Stringa localizzata corrispondente al **tipo di** controllo Text. Il valore predefinito è "text" per en-US o english (Stati Uniti).                                                                                                                                                                                                                      |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Vedere le note. | Il nome di un controllo di testo può essere il testo visualizzato. Tuttavia, se il controllo supporta anche il pattern [Text](uiauto-implementingtextandtextrange.md) e il testo è esteso, non usare il contenuto full-text come **valore Name.** Specificare invece un **valore Name** più breve, derivato da altre proprietà del controllo. |



 

## <a name="required-control-patterns"></a>Pattern di controllo obbligatori

Nella tabella seguente sono elencati i Automazione interfaccia utente di controllo personalizzati che devono essere supportati dai controlli di testo. Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Pattern di controllo                                         | Supporto | Note                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)   | Dipende da | Se il controllo testo è contenuto in un controllo tabella, il pattern [di controllo GridItem](uiauto-implementinggriditem.md) deve essere supportato.                                                                                                                            |
| [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) | Dipende da | Se il controllo testo è contenuto in un controllo tabella, il pattern [di controllo TableItem](uiauto-implementingtableitem.md) deve essere supportato.                                                                                                                          |
| [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider)           | Dipende da | Il testo deve supportare il pattern di controllo [Text](uiauto-implementingtextandtextrange.md) per una migliore accessibilità. tuttavia non è obbligatorio. Il pattern di controllo Text è utile quando il testo ha stili di formattazione e attributi, ad esempio colore, grassetto e corsivo. |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)         | Mai   | Un controllo di testo non supporta mai il [pattern di controllo](uiauto-implementingvalue.md) Value. Se il testo è modificabile, è il [tipo di controllo](uiauto-supporteditcontroltype.md) Edit.                                                                                    |



 

## <a name="required-events"></a>Eventi obbligatori

Nella tabella seguente sono elencati Automazione interfaccia utente eventi che i controlli di testo devono supportare. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automazione interfaccia utente evento                                                                                                                   | Note                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**Interfaccia \_ utente Evento di modifica della proprietà BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md) |                                                                                                                            |
| [**Interfaccia \_ utente Evento di modifica della proprietà IsEnabledPropertyId.**](uiauto-automation-element-propids.md)                 | Se il controllo supporta la [**proprietà IsEnabled,**](uiauto-automation-element-propids.md) deve supportare questo evento.   |
| [**Interfaccia \_ utente Evento di modifica della proprietà IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)             | Se il controllo supporta la [**proprietà IsOffscreen,**](uiauto-automation-element-propids.md) deve supportare questo evento. |
| [**Interfaccia \_ utente Evento di modifica**](uiauto-automation-element-propids.md) della proprietà NamePropertyId.                           |                                                                                                                            |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |
| [**\_TextChangedEventId dell'interfaccia utenteA \_**](uiauto-event-ids.md)                                                 | Se il controllo supporta il pattern [di controllo Text,](uiauto-implementingtextandtextrange.md) deve supportare questo evento.   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente](uiauto-controltypesoverview.md)
</dt> <dt>

[Cenni preliminari su automazione interfaccia utente](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




