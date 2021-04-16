---
title: Tipo di controllo Button
description: In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo Button.
ms.assetid: a2942067-461c-4281-80cf-385e3c08c874
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo Button
- Automazione interfaccia utente, tipo di controllo Button
- Automazione interfaccia utente, struttura ad albero per il tipo di controllo Button
- Automazione interfaccia utente, proprietà per il tipo di controllo Button
- Automazione interfaccia utente, pattern di controllo per il tipo di controllo Button
- Automazione interfaccia utente, eventi per il tipo di controllo Button
- strutture ad albero, tipo di controllo Button
- Proprietà, tipo di controllo Button
- pattern di controllo, tipo di controllo Button
- eventi, tipo di controllo Button
- supporto per il tipo di controllo Button
- Button (tipo di controllo)
- tipi di controllo, struttura ad albero per il tipo di controllo Button
- tipi di controllo, pattern di controllo per il tipo di controllo Button
- tipi di controllo, supporto per Button
- tipi di controllo, pulsante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: def18e7094e297303a70fc0980bfdd0cb4413c0c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104222111"
---
# <a name="button-control-type"></a>Tipo di controllo Button

In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo **Button** .

Un pulsante è un oggetto che un utente usa per eseguire un'azione, ad esempio i pulsanti OK e Annulla in una finestra di dialogo. Il controllo Button è un controllo semplice da esporre perché esegue il mapping a un unico comando che l'utente desidera completare.

Nelle sezioni seguenti vengono definiti la struttura ad albero, le proprietà, i pattern di controllo e gli eventi di automazione interfaccia utente necessari per il tipo di controllo **Button** . I requisiti di automazione interfaccia utente si applicano a tutti i controlli Button in cui la piattaforma/Framework dell'interfaccia utente integra il supporto di automazione interfaccia utente per i tipi di controllo e i pattern

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Pattern di controllo obbligatori](#required-control-patterns)
-   [Eventi obbligatori](#required-events)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

Nella tabella seguente viene illustrata una tipica visualizzazione del controllo e del contenuto dell'albero di automazione interfaccia utente che riguarda i controlli Button e viene descritto il possibile contenuto di ogni visualizzazione. Per altre informazioni sull'albero di automazione interfaccia utente, vedere [Cenni preliminari sull'albero di automazione interfaccia utente](uiauto-treeoverview.md).



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
<li>Pulsante
<ul>
<li>Image (0 o più)</li>
<li>Text (0 o più)</li>
</ul></li>
</ul></td>
<td><ul>
<li>Pulsante</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a>Proprietà rilevanti

La tabella seguente elenca le proprietà di automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per i controlli che implementano il tipo di controllo **Button** , ad esempio i controlli Button. Per altre informazioni sulle proprietà di automazione interfaccia utente, vedere [recupero di proprietà da elementi di automazione interfaccia utente](uiauto-propertiesforclients.md).



| Proprietà di automazione interfaccia utente                                                                                              | Valore      | Note                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ACCELERATORKEYPROPERTYID UIA**](uiauto-automation-element-propids.md)             | Vedere le note. | Un controllo Button in genere supporta un tasto di scelta rapida per consentire all'utente finale di eseguire rapidamente l'azione rappresentata dal pulsante dalla tastiera.                                             |
| [**\_AUTOMATIONIDPROPERTYID UIA**](uiauto-automation-element-propids.md)                 | Vedere le note. | Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata della struttura ad albero di automazione interfaccia utente.                                                                                         |
| [**\_BOUNDINGRECTANGLEPROPERTYID UIA**](uiauto-automation-element-propids.md)       | Vedere le note. | Il rettangolo più esterno che contiene l'intero controllo.                                                                                                                                             |
| [**\_CLICKABLEPOINTPROPERTYID UIA**](uiauto-automation-element-propids.md)             | Vedere le note. | Supportata se è presente un rettangolo di delimitazione. Se non tutti i punti all'interno del rettangolo di delimitazione sono selezionabili e l'elemento esegue un hit testing specializzato, eseguire l'override e fornire un punto selezionabile. |
| [**\_CONTROLTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md)                   | **Button** |                                                                                                                                                                                                      |
| [**\_HELPTEXTPROPERTYID UIA**](uiauto-automation-element-propids.md)                         | Vedere le note. | Il testo della guida deve indicare quale sarà il risultato finale dell'attivazione del pulsante. Si tratta in genere dello stesso tipo di informazioni visualizzate tramite una descrizione comando.                                      |
| [**\_ISCONTENTELEMENTPROPERTYID UIA**](uiauto-automation-element-propids.md)         | true       | Il controllo Button deve essere sempre di contenuto.                                                                                                                                                           |
| [**\_ISCONTROLELEMENTPROPERTYID UIA**](uiauto-automation-element-propids.md)         | true       | Il controllo Button deve essere sempre un controllo.                                                                                                                                                         |
| [**\_ISKEYBOARDFOCUSABLEPROPERTYID UIA**](uiauto-automation-element-propids.md)   | Vedere le note. | Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.                                                                                                                            |
| [**\_LABELEDBYPROPERTYID UIA**](uiauto-automation-element-propids.md)                       | Null       | Ai controlli Button viene automaticamente applicata un'etichetta in base al relativo contenuto.                                                                                                                                                  |
| [**\_LOCALIZEDCONTROLTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md) | Vedere le note. | Stringa localizzata corrispondente al tipo di controllo **Button** . Il valore predefinito è "button" per en-US o inglese (Stati Uniti).                                                                   |
| [**\_NAMEPROPERTYID UIA**](uiauto-automation-element-propids.md)                                 | Vedere le note. | Il nome del controllo Button è il testo utilizzato per etichettarlo. Ogni volta che viene usata un'immagine per etichettare un pulsante, è necessario specificare il testo alternativo per la proprietà **Name** del pulsante.                        |



 

## <a name="required-control-patterns"></a>Pattern di controllo obbligatori

La tabella seguente elenca i pattern di controllo di automazione interfaccia utente che devono essere supportati da tutti i controlli Button. Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Pattern di controllo/proprietà del pattern                                  | Supporto/valore | Note                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Vedere le note.    | Quando un pulsante viene ospitato come figlio di un pulsante di suddivisione, il pulsante figlio può supportare il pattern di controllo [ExpandCollapse](uiauto-implementingexpandcollapse.md) anziché il pattern di controllo [Invoke](uiauto-implementinginvoke.md) o [interruttore](uiauto-implementingtoggle.md) . Il pattern di controllo ExpandCollapse può essere usato per l'apertura o la chiusura di un menu o di un'altra sottostruttura associata all'elemento Button. |
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)                 | Vedere le note.    | Tutti i pulsanti devono supportare il pattern di controllo [Invoke](uiauto-implementinginvoke.md) o il pattern di controllo di [attivazione/](uiauto-implementingtoggle.md) disattivione, ma non entrambi. Il pattern di controllo Invoke deve essere supportato quando il pulsante esegue un comando su richiesta dell'utente. Questo comando esegue il mapping a una singola operazione, ad esempio Taglia, Copia, Incolla o Elimina.                                                              |
| [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)                 | Vedere le note.    | Tutti i pulsanti devono supportare il pattern di controllo [Invoke](uiauto-implementinginvoke.md) o il pattern di controllo di [attivazione/](uiauto-implementingtoggle.md) disattivione, ma non entrambi. Il pattern di controllo di attivazione/disattivazione deve essere supportato se il pulsante può scorrere una serie di un massimo di tre stati. In genere viene interpretato come opzione di attivazione/disattivazione per funzionalità specifiche.                                                                        |



 

## <a name="required-events"></a>Eventi obbligatori

La tabella seguente elenca gli eventi di automazione interfaccia utente necessari per supportare i controlli Button. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



| Evento di automazione interfaccia utente                                                                                                                   | Note                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**\_AUTOMATIONFOCUSCHANGEDEVENTID UIA**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà BoundingRectanglePropertyId. |                                                                                                                            |
| [**\_Richiama \_ InvokedEventId**](uiauto-event-ids.md)                                                     | Se il controllo supporta il pattern di controllo [Invoke](uiauto-implementinginvoke.md) , deve supportare questo evento.           |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsEnabledPropertyId.                 | Se il controllo supporta la proprietà [**IsEnabled**](uiauto-automation-element-propids.md) , deve supportare questo evento.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsOffscreenPropertyId.             | Se il controllo supporta la proprietà [**IsOffscreen**](uiauto-automation-element-propids.md) , deve supportare questo evento. |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà NamePropertyId.                           |                                                                                                                            |
| [**\_STRUCTURECHANGEDEVENTID UIA**](uiauto-event-ids.md)                                                  |                                                                                                                            |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ToggleToggleStatePropertyId.    | Se il controllo supporta il pattern di controllo [interruttore](uiauto-implementingtoggle.md) , deve supportare questo evento.           |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente](uiauto-controltypesoverview.md)
</dt> <dt>

[Cenni preliminari su automazione interfaccia utente](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




