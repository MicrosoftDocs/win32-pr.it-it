---
title: Tipo di controllo SemanticZoom
description: In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente per il tipo di controllo SemanticZoom.
ms.assetid: 37C14610-431F-46BF-97B6-CB476EA1642D
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo SemanticZoom
- Automazione interfaccia utente, tipo di controllo SemanticZoom
- Automazione interfaccia utente, struttura ad albero per il tipo di controllo SemanticZoom
- Automazione interfaccia utente, proprietà per il tipo di controllo SemanticZoom
- Automazione interfaccia utente, pattern di controllo per il tipo di controllo SemanticZoom
- Automazione interfaccia utente, eventi per il tipo di controllo SemanticZoom
- strutture ad albero, tipo di controllo SemanticZoom
- Proprietà, tipo di controllo SemanticZoom
- pattern di controllo, tipo di controllo SemanticZoom
- eventi, tipo di controllo SemanticZoom
- supporto per il tipo di controllo SemanticZoom
- Tipo di controllo SemanticZoom
- tipi di controllo, struttura ad albero per il tipo di controllo SemanticZoom
- tipi di controllo, pattern di controllo per il tipo di controllo SemanticZoom
- tipi di controllo, supporto per SemanticZoom
- tipi di controllo, SemanticZoom
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b17d4712aa4f10489081b1b5d0f69fed849080bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104117791"
---
# <a name="semanticzoom-control-type"></a>Tipo di controllo SemanticZoom

In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente per il tipo di controllo **SemanticZoom** .

Lo zoom semantico è una tecnica introdotta in Windows 8 per la presentazione e lo spostamento di grandi set di dati o contenuti correlati in una singola visualizzazione, ad esempio un album di foto, un elenco di app o una rubrica. Lo zoom semantico usa due modalità distinte di classificazione o *livelli di zoom* per organizzare e presentare il contenuto. La modalità di basso livello (o *zoom avanti*) Visualizza gli elementi in una struttura Flat, "all-up"; e la modalità di alto livello (o *Zoom* indietro) Visualizza gli elementi in gruppi, consentendo all'utente di spostarsi rapidamente ed esplorare il contenuto. Ad esempio, lo zoom di un elenco di città potrebbe cambiare in un elenco di Stati che contengono tali città. Lo zoom di un elenco di programmi potrebbe variare in un elenco di gruppi di programmi logici.

Per altre informazioni sullo zoom semantico usato per le app di Windows Store, vedere [linee guida per lo zoom semantico](/windows/uwp/controls-and-patterns/semantic-zoom).

Il modello di utilizzo per il tipo di controllo **SemanticZoom** è insolito perché esiste principalmente per l'accesso a livello di codice. I client di automazione interfaccia utente Microsoft possono monitorare e manipolare il controllo zoom semantico per controllare lo stato di ingrandimento dell'elenco. Gli utenti che non usano la tecnologia per l'accessibilità in genere manipolano il controllo dello zoom semantico direttamente tramite movimenti tocco o tasti di scelta rapida.

Nelle sezioni seguenti vengono definiti la struttura ad albero, le proprietà, i pattern di controllo e gli eventi di automazione interfaccia utente necessari per il tipo di controllo **SemanticZoom** . I requisiti di automazione interfaccia utente si applicano a tutti i controlli zoom semantici in cui la piattaforma/Framework dell'interfaccia utente integra il supporto di automazione interfaccia utente per tipi di controllo e pattern di controllo

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Pattern di controllo e proprietà obbligatori](#required-control-patterns-and-properties)
-   [Eventi obbligatori](#required-events)
-   [Osservazioni:](#remarks)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

Nella tabella seguente viene illustrata una tipica visualizzazione del controllo e del contenuto della struttura ad albero di automazione interfaccia utente relativa al tipo di controllo **SemanticZoom** e viene descritto il possibile contenuto di ogni visualizzazione. Per altre informazioni sull'albero di automazione interfaccia utente, vedere [Cenni preliminari sull'albero di automazione interfaccia utente](uiauto-treeoverview.md).



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
<li>Elenco
<ul>
<li>SemanticZoom
<ul>
<li>ListItem (0 o più)</li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li>Elenco
<ul>
<li>ListItem (0 o più)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

Oppure:



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
<li>SemanticZoom
<ul>
<li>Elenco
<ul>
<li>ListItem (0 o più)</li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li>Elenco
<ul>
<li>ListItem (0 o più)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a>Proprietà rilevanti

La tabella seguente elenca le proprietà di automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per i controlli che implementano il tipo di controllo **SemanticZoom** . Per altre informazioni sulle proprietà di automazione interfaccia utente, vedere [recupero di proprietà da elementi di automazione interfaccia utente](uiauto-propertiesforclients.md).



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Proprietà di automazione interfaccia utente</th>
<th>Valore</th>
<th>Note</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="uiauto-automation-element-propids.md"><strong>UIA_AutomationIdPropertyId</strong></a></td>
<td>Vedere le note.</td>
<td>Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata della struttura ad albero di automazione interfaccia utente.</td>
</tr>
<tr class="even">
<td><a href="uiauto-automation-element-propids.md"><strong>UIA_BoundingRectanglePropertyId</strong></a></td>
<td>Vedere le note.</td>
<td>Il rettangolo più esterno che contiene l'intero controllo.</td>
</tr>
<tr class="odd">
<td><a href="uiauto-automation-element-propids.md"><strong>UIA_ClickablePointPropertyId</strong></a></td>
<td>Vedere le note.</td>
<td>Se il controllo elenco ha un punto selezionabile, ovvero un punto su cui è possibile fare clic per fare in modo che l'elenco abbia lo stato attivo, tale punto deve essere esposto tramite questa proprietà. Se il valore della proprietà <a href="uiauto-automation-element-propids.md"><strong>UIA_IsOffscreenPropertyId</strong></a> è <strong>true</strong>, il tentativo di recuperare questa proprietà comporta l'errore <a href="uiauto-error-codes.md"><strong>UIA_E_NOCLICKABLEPOINT</strong></a> .</td>
</tr>
<tr class="even">
<td><a href="uiauto-automation-element-propids.md"><strong>UIA_ControlTypePropertyId</strong></a></td>
<td><strong>SemanticZoom</strong></td>

</tr>
<tr class="odd">
<td><a href="uiauto-automation-element-propids.md"><strong>UIA_IsContentElementPropertyId</strong></a></td>
<td>true</td>

</tr>
<tr class="even">
<td><a href="uiauto-automation-element-propids.md"><strong>UIA_IsControlElementPropertyId</strong></a></td>
<td>true</td>

</tr>
<tr class="odd">
<td><a href="uiauto-automation-element-propids.md"><strong>UIA_IsKeyboardFocusablePropertyId</strong></a></td>
<td>FALSE</td>

</tr>
<tr class="even">
<td><a href="uiauto-automation-element-propids.md"><strong>UIA_LabeledByPropertyId</strong></a></td>
<td>Vedere le note.</td>
<td>Se è presente un'etichetta di testo statico, questa proprietà deve esporre un riferimento a tale controllo.</td>
</tr>
<tr class="odd">
<td><a href="uiauto-automation-element-propids.md"><strong>UIA_LocalizedControlTypePropertyId</strong></a></td>
<td>Vedere le note.</td>
<td>Stringa localizzata corrispondente al tipo di controllo <strong>SemanticZoom</strong> . Il valore predefinito è &quot; zoom semantico &quot; per en-US o inglese (Stati Uniti).
<blockquote>
[!Note]<br />
Alcuni Framework sono stati concatenati come &quot; SemanticZoom &quot; .
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="uiauto-automation-element-propids.md"><strong>UIA_NamePropertyId</strong></a></td>
<td>Vedere le note.</td>
<td>Una stringa vuota è accettabile, oppure è possibile specificare un nome più utile, purché non contenga il termine zoom semantico, che renderebbe la combinazione di tipo di controllo e nome confuso.</td>
</tr>
</tbody>
</table>



 

## <a name="required-control-patterns-and-properties"></a>Pattern di controllo e proprietà obbligatori

La tabella seguente elenca i pattern di controllo di automazione interfaccia utente che devono essere supportati da tutti i controlli zoom semantici. Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Pattern di controllo/proprietà del pattern                  | Supporto/valore | Note                                                                                                                                                                                                                                                                                                                                                          |
|---------------------------------------------------|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) | Dipende da       | I controlli zoom semantico supportano il pattern di controllo di [attivazione/](uiauto-implementingtoggle.md) disattivazione per consentire l'abilitazione o la disabilitazione dello zoom. [**ToggleState \_ Off**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate) corrisponde allo stato Flat, all-up e [**ToggleState \_ on**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate) corrisponde alla vista di alto livello, con zoom indietro. |



 

## <a name="required-events"></a>Eventi obbligatori

La tabella seguente elenca gli eventi di automazione interfaccia utente necessari per supportare i controlli zoom semantici. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



| Evento di automazione interfaccia utente                                                                                                                   | Note                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà BoundingRectanglePropertyId. |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsEnabledPropertyId.                 | Se il controllo supporta la proprietà [**IsEnabled**](uiauto-automation-element-propids.md) , deve supportare questo evento.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsOffscreenPropertyId.             | Se il controllo supporta la proprietà [**IsOffscreen**](uiauto-automation-element-propids.md) , deve supportare questo evento. |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento di modifica della proprietà ToggleToggleStatePropertyId.    |                                                                                                                            |



 

## <a name="remarks"></a>Commenti

Se un'interfaccia utente dispone di un pulsante visibile per impostare il comportamento del controllo zoom semantico, questo pulsante non deve avere un tipo di controllo **SemanticZoom** . Si tratta di un valore non intuitivo, ma il tipo di controllo **SemanticZoom** caratterizza il contenitore del contenuto di zoom, non un pulsante che controlla lo zoom. Un pulsante di questo tipo può essere rappresentato semplicemente come un tipo di controllo [Button](uiauto-supportbuttoncontroltype.md) con il pattern di controllo dell' [interruttore](uiauto-implementingtoggle.md) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente](uiauto-controltypesoverview.md)
</dt> <dt>

[Cenni preliminari su automazione interfaccia utente](uiauto-uiautomationoverview.md)
</dt> </dl>

 

