---
title: Tipo di controllo Table
description: In questo argomento vengono fornite informazioni sul supporto Automazione interfaccia utente microsoft per il tipo di controllo Table.
ms.assetid: 508db2af-1ca3-4003-8e1f-6e225cf79b7a
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo Table
- Automazione interfaccia utente,Tipo di controllo Tabella
- Automazione interfaccia utente,struttura ad albero per il tipo di controllo Tabella
- Automazione interfaccia utente,properties per il tipo di controllo Table
- Automazione interfaccia utente,pattern di controllo per il tipo di controllo Table
- Automazione interfaccia utente,eventi per il tipo di controllo Table
- strutture ad albero, tipo di controllo Table
- proprietà, tipo di controllo Tabella
- pattern di controllo, tipo di controllo Table
- eventi, tipo di controllo Table
- supporto per il tipo di controllo Table
- Table (tipo di controllo)
- tipi di controllo, struttura ad albero per tipo di controllo Table
- tipi di controllo, pattern di controllo per il tipo di controllo Table
- tipi di controllo, supporto per Table
- tipi di controllo, tabella
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0badb06cfc449140162663625f3fa7282f9c1589
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470078"
---
# <a name="table-control-type"></a>Tipo di controllo Table

In questo argomento vengono fornite informazioni sul supporto di Microsoft Automazione interfaccia utente per il **tipo di controllo** Table.

I controlli Tabella contengono righe e colonne di testo e, facoltativamente, intestazioni di riga e intestazioni di colonna.

Le sezioni seguenti definiscono la struttura ad Automazione interfaccia utente struttura ad albero, le proprietà, i pattern di controllo e gli eventi per il **tipo di controllo** Table. I Automazione interfaccia utente si applicano a tutti i controlli tabella in cui il framework o la piattaforma dell'interfaccia utente si integra Automazione interfaccia utente per i tipi di controllo e i pattern di controllo.

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Pattern di controllo obbligatori](#required-control-patterns)
-   [Eventi obbligatori](#required-events)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

La tabella seguente illustra un controllo tipico e una visualizzazione contenuto dell'albero Automazione interfaccia utente relativo ai controlli tabella e descrive cosa può essere contenuto in ogni visualizzazione. Per altre informazioni sull'albero Automazione interfaccia utente, vedere panoramica [Automazione interfaccia utente albero.](uiauto-treeoverview.md)




| Visualizzazione controlli | Visualizzazione contenuto | 
|--------------|--------------|
| <ul><li>Tabella<ul><li>Text (0 o 1)</li><li>Intestazione (0 o più)</li><li>Vari controlli (0 o più)</li></ul></li></ul> | <ul><li>Tabella<ul><li>Testo (1 o più)</li><li>Vari controlli (0 o più)</li></ul></li></ul> | 




 

Se un controllo tabella include intestazioni di riga o colonna, devono essere esposti nella visualizzazione controlli dell'Automazione interfaccia utente dati. Non è necessario che la visualizzazione contenuto esponga queste informazioni perché è possibile accedervi [**tramite IUIAutomationTablePattern.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtablepattern)

## <a name="relevant-properties"></a>Proprietà rilevanti

La tabella seguente elenca le proprietà Automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per i controlli tabella. Per altre informazioni sulle Automazione interfaccia utente, vedere [Recupero di proprietà da Automazione interfaccia utente elementi](uiauto-propertiesforclients.md).



| Proprietà di automazione interfaccia utente                                                                                              | valore      | Note                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Vedere le note. | Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata dell'Automazione interfaccia utente albero.                                                                                                                      |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Vedere le note. | Il rettangolo più esterno che contiene l'intero controllo.                                                                                                                                                                          |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Vedere le note. | Supportata se è presente un rettangolo di delimitazione. Se non tutti i punti all'interno del rettangolo di delimitazione sono selezionabili e l'elemento esegue hit testing specializzati, eseguire l'override e fornire un punto selezionabile.                              |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Tabella**  |                                                                                                                                                                                                                                   |
| [**UIA \_ DescribedByPropertyId**](uiauto-automation-element-propids.md)                   | Vedere le note. | Se la tabella viene annotata mediante altri elementi dell'interfaccia utente, ad esempio un elemento di testo contenente la descrizione della tabella, la proprietà DescribedBy deve esporre un riferimento all'elemento di automazione del controllo testo.           |
| [**UIA \_ HelpTextPropertyId**](uiauto-automation-element-propids.md)                         | Vedere le note. | Altri dettagli sullo scopo della tabella devono essere esposti tramite questa proprietà se non è sufficientemente spiegato dalla proprietà [**\_ NamePropertyId**](uiauto-automation-element-propids.md) dell'interfaccia utente.      |
| [**\_IsContentElementPropertyId dell'interfaccia utente**](uiauto-automation-element-propids.md)         | true       | Il controllo tabella deve sempre essere visualizzato nella visualizzazione contenuto dell'Automazione interfaccia utente struttura ad albero.                                                                                                                                               |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | true       | Il controllo tabella deve sempre essere visualizzato nella visualizzazione controlli dell'Automazione interfaccia utente struttura ad albero.                                                                                                                                               |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Vedere le note. | Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.                                                                                                                                                         |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Vedere le note. | Se è presente un'etichetta di testo statico, questa proprietà deve esporre un riferimento all'elemento di automazione del controllo.                                                                                                                |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Vedere le note. | Stringa localizzata corrispondente al **tipo di** controllo Table. Il valore predefinito è "table" per en-US o english (Stati Uniti).                                                                                                  |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Vedere le note. | Il controllo tabella in genere ottiene il valore per il nome da un'etichetta di testo statico. Se non è presente un'etichetta di testo statico, l'elemento deve assegnare una proprietà Name che deve essere sempre disponibile per spiegare lo scopo della tabella. |



 

## <a name="required-control-patterns"></a>Pattern di controllo obbligatori

Nella tabella seguente sono elencati Automazione interfaccia utente i pattern di controllo che devono essere supportati da tutti i controlli tabella. Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Pattern di controllo                                         | Supporto                     | Note                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider)           | Obbligatoria                    | Poiché il controllo tabella contiene elementi presentati in una griglia, supporta sempre il pattern [di controllo Grid.](uiauto-implementinggrid.md)                                                                                                                                                    |
| [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)   | Obbligatorio con oggetti figlio | Gli oggetti interni di una tabella devono supportare i [pattern di controllo GridItem](uiauto-implementinggriditem.md) e [TableItem.](uiauto-implementingtableitem.md) La tabella stessa non deve supportare il pattern di controllo GridItem o TableItem a meno che la tabella non sia parte di un'altra tabella.  |
| [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider)         | Obbligatoria                    | Il controllo tabella può sempre avere intestazioni associate al contenuto.                                                                                                                                                                                                                       |
| [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) | Obbligatorio con oggetti figlio | Gli oggetti interni di una tabella devono supportare sia i [pattern di controllo GridItem](uiauto-implementinggriditem.md) che [TableItem.](uiauto-implementingtableitem.md) La tabella stessa non deve supportare il pattern di controllo GridItem o TableItem, a meno che la tabella non faccia parte di un'altra tabella. |



 

## <a name="required-events"></a>Eventi obbligatori

Nella tabella seguente sono elencati Automazione interfaccia utente eventi che i controlli tabella devono supportare. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



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

 

 




