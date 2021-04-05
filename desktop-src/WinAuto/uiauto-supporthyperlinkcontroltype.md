---
title: Tipo di controllo HyperLink
description: In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo HyperLink.
ms.assetid: 6dd16ae6-eff0-4913-8916-5092aec34f1f
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo HyperLink
- Automazione interfaccia utente, tipo di controllo HyperLink
- Automazione interfaccia utente, struttura ad albero per il tipo di controllo HyperLink
- Automazione interfaccia utente, proprietà per il tipo di controllo HyperLink
- Automazione interfaccia utente, pattern di controllo per il tipo di controllo HyperLink
- Automazione interfaccia utente, eventi per il tipo di controllo HyperLink
- strutture ad albero, tipo di controllo HyperLink
- Proprietà, tipo di controllo HyperLink
- pattern di controllo, tipo di controllo HyperLink
- eventi, tipo di controllo HyperLink
- supporto per il tipo di controllo HyperLink
- Hyperlink (tipo di controllo)
- tipi di controllo, struttura ad albero per il tipo di controllo HyperLink
- tipi di controllo, pattern di controllo per il tipo di controllo HyperLink
- tipi di controllo, supporto per collegamento ipertestuale
- tipi di controllo, collegamento ipertestuale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71547f37380aeb029e4f73f8d9b2286b285187ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710312"
---
# <a name="hyperlink-control-type"></a>Tipo di controllo HyperLink

In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo **Hyperlink** .

I controlli collegamento ipertestuale creano collegamenti che consentono agli utenti di spostarsi all'interno della stessa pagina o da una pagina all'altra.

Nelle sezioni seguenti vengono definiti la struttura ad albero, le proprietà, i pattern di controllo e gli eventi di automazione interfaccia utente necessari per il tipo di controllo **Hyperlink** . I requisiti di automazione interfaccia utente si applicano a tutti i controlli collegamento ipertestuale in cui la piattaforma/Framework dell'interfaccia utente integra il supporto di automazione interfaccia utente per i tipi di controllo e

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Pattern di controllo obbligatori](#required-control-patterns)
-   [Eventi obbligatori](#required-events)
-   [Osservazioni:](#remarks)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

Nella tabella seguente viene illustrata una tipica visualizzazione del controllo e del contenuto dell'albero di automazione interfaccia utente che riguarda i controlli collegamento ipertestuale e viene descritto il possibile contenuto di ogni visualizzazione. Per altre informazioni sull'albero di automazione interfaccia utente, vedere [Cenni preliminari sull'albero di automazione interfaccia utente](uiauto-treeoverview.md).



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
<li>Hyperlink</li>
</ul></td>
<td><ul>
<li>Hyperlink</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a>Proprietà rilevanti

La tabella seguente elenca le proprietà di automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per i controlli collegamento ipertestuale. Per altre informazioni sulle proprietà di automazione interfaccia utente, vedere [recupero di proprietà da elementi di automazione interfaccia utente](uiauto-propertiesforclients.md).



| Proprietà di automazione interfaccia utente                                                                                              | Valore         | Note                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_AUTOMATIONIDPROPERTYID UIA**](uiauto-automation-element-propids.md)                 | Vedere le note.    | Il valore di questa proprietà deve essere univoco in tutti i controlli in un'applicazione.                                                         |
| [**\_BOUNDINGRECTANGLEPROPERTYID UIA**](uiauto-automation-element-propids.md)       | Vedere le note.    | Il rettangolo più esterno che contiene l'intero controllo.                                                                                 |
| [**\_CLICKABLEPOINTPROPERTYID UIA**](uiauto-automation-element-propids.md)             | Vedere le note.    | Il punto selezionabile del controllo collegamento ipertestuale deve essere un punto che avvia il collegamento ipertestuale se viene selezionato con un puntatore del mouse.                     |
| [**\_CONTROLTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md)                   | **Collegamento ipertestuale** |                                                                                                                                          |
| [**\_ISCONTENTELEMENTPROPERTYID UIA**](uiauto-automation-element-propids.md)         | true          | Il controllo HyperLink viene sempre incluso nella visualizzazione contenuto dell'albero di automazione interfaccia utente.                                                  |
| [**\_ISCONTROLELEMENTPROPERTYID UIA**](uiauto-automation-element-propids.md)         | true          | Il controllo HyperLink viene sempre incluso nella visualizzazione controlli dell'albero di automazione interfaccia utente.                                                  |
| [**\_ISKEYBOARDFOCUSABLEPROPERTYID UIA**](uiauto-automation-element-propids.md)   | Vedere le note.    | Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.                                                                |
| [**\_LABELEDBYPROPERTYID UIA**](uiauto-automation-element-propids.md)                       | Vedere le note.    | Se è presente un'etichetta di testo statico, questa proprietà deve esporre un riferimento a tale controllo.                                                  |
| [**\_LOCALIZEDCONTROLTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md) | Vedere le note.    | Stringa localizzata corrispondente al tipo di controllo **Hyperlink** . Il valore predefinito è "Hyperlink" per en-US o inglese (Stati Uniti). |
| [**\_NAMEPROPERTYID UIA**](uiauto-automation-element-propids.md)                                 | Vedere le note.    | Il nome del controllo HyperLink è il testo visualizzato sullo schermo sotto forma di sottolineatura.                                                  |



 

## <a name="required-control-patterns"></a>Pattern di controllo obbligatori

La tabella seguente elenca i pattern di controllo di automazione interfaccia utente necessari per supportare i controlli collegamento ipertestuale. Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Pattern di controllo/proprietà del pattern                  | Supporto/valore                | Note                                                                                                                                                                                                                                                  |
|---------------------------------------------------|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) | Necessario                     | Tutti i controlli collegamento ipertestuale devono supportare il pattern di controllo [Invoke](uiauto-implementinginvoke.md) .                                                                                                                                                       |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)   | Dipende da                      | I controlli collegamento ipertestuale devono supportare il pattern di controllo [value](uiauto-implementingvalue.md) quando il collegamento contiene informazioni utilizzabili e significative per l'utente.                                                                              |
| [**Valore**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_value)      | Ad esempio, "https://www..". | Un URL per un indirizzo Internet o Intranet è un esempio di collegamento ipertestuale contenente informazioni significative per l'utente. Un collegamento a livello di codice, tuttavia, è significativo solo per un'applicazione e non è consigliato per la proprietà **value** . |



 

## <a name="required-events"></a>Eventi obbligatori

La tabella seguente elenca gli eventi di automazione interfaccia utente necessari per supportare i controlli collegamento ipertestuale. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



| Evento di automazione interfaccia utente                                                                                                                   | Note                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**\_AUTOMATIONFOCUSCHANGEDEVENTID UIA**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà BoundingRectanglePropertyId. |                                                                                                                            |
| [**\_Richiama \_ InvokedEventId**](uiauto-event-ids.md)                                                     |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsEnabledPropertyId.                 | Se il controllo supporta la proprietà [**IsEnabled**](uiauto-automation-element-propids.md) , deve supportare questo evento.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsOffscreenPropertyId.             | Se il controllo supporta la proprietà [**IsOffscreen**](uiauto-automation-element-propids.md) , deve supportare questo evento. |
| [**\_STRUCTURECHANGEDEVENTID UIA**](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="remarks"></a>Commenti

Il tipo di controllo collegamento ipertestuale deve essere applicato solo a un oggetto che, se selezionato, causa la navigazione; non deve essere applicato al contenitore del collegamento ipertestuale. Ad esempio, solo le "aree sensibili" selezionabili all'interno di una mappa immagine dovrebbero avere il tipo di controllo **Hyperlink** . Lo stesso vale per i collegamenti ipertestuali in un campo di testo o un contenitore di documenti. In questo caso, solo il testo o l'immagine del collegamento ipertestuale deve avere il tipo di controllo **Hyperlink** , non il contenitore.

Il pattern di controllo [Text](uiauto-implementingtextandtextrange.md) è ideale per il supporto di collegamenti ipertestuali incorporati in elementi di testo o documento.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente](uiauto-controltypesoverview.md)
</dt> <dt>

[Cenni preliminari su automazione interfaccia utente](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




