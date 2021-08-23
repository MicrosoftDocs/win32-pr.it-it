---
title: Tipo di controllo SemanticZoom
description: Questo argomento fornisce informazioni sul supporto Automazione interfaccia utente per il tipo di controllo SemanticZoom.
ms.assetid: 37C14610-431F-46BF-97B6-CB476EA1642D
keywords:
- Automazione interfaccia utente,supporto per il tipo di controllo SemanticZoom
- Automazione interfaccia utente,Tipo di controllo SemanticZoom
- Automazione interfaccia utente,struttura ad albero per il tipo di controllo SemanticZoom
- Automazione interfaccia utente,proprietà per il tipo di controllo SemanticZoom
- Automazione interfaccia utente,pattern di controllo per il tipo di controllo SemanticZoom
- Automazione interfaccia utente,events per il tipo di controllo SemanticZoom
- strutture ad albero, tipo di controllo SemanticZoom
- proprietà,Tipo di controllo SemanticZoom
- pattern di controllo, tipo di controllo SemanticZoom
- eventi, tipo di controllo SemanticZoom
- supporto per il tipo di controllo SemanticZoom
- Tipo di controllo SemanticZoom
- tipi di controllo, struttura ad albero per il tipo di controllo SemanticZoom
- tipi di controllo,pattern di controllo per il tipo di controllo SemanticZoom
- tipi di controllo, supporto per SemanticZoom
- tipi di controllo,SemanticZoom
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49609b7bc2b3958b6041bcf3a8c2c6442ce38501f95ff75a6c0f2145d497436f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118825478"
---
# <a name="semanticzoom-control-type"></a>Tipo di controllo SemanticZoom

Questo argomento fornisce informazioni sul supporto Automazione interfaccia utente per il tipo di controllo **SemanticZoom.**

Lo zoom semantico è una tecnica introdotta in Windows 8 per presentare ed esplorare grandi set di dati o contenuti correlati all'interno di una singola visualizzazione, ad esempio un album di foto, un elenco di app o una rubrica. Lo zoom semantico usa due modalità distinte di classificazione, o *livelli di zoom*, per organizzare e presentare il contenuto. La modalità di basso livello *(o ingrandita)* visualizza gli elementi in una struttura semplice e "all-up". e la modalità di alto livello (o *ingrandita)* visualizza gli elementi in gruppi, consentendo all'utente di spostarsi rapidamente ed esplorare il contenuto. Ad esempio, lo zoom di un elenco di città potrebbe cambiare in un elenco di stati contenenti tali città. Lo zoom di un elenco di programmi potrebbe cambiare in un elenco di gruppi di programmi logici.

Per altre informazioni sullo zoom semantico usato in modo specifico per le app Windows Store, vedere [Linee guida per lo zoom semantico.](/windows/uwp/controls-and-patterns/semantic-zoom)

Il modello di utilizzo per il **tipo di controllo SemanticZoom** è insolito perché esiste principalmente per l'accesso a livello di codice. Microsoft Automazione interfaccia utente client possono monitorare e modificare il controllo Zoom semantico per controllare lo stato ingrandito dell'elenco. Gli utenti che non usano assistive technology in genere modificano il controllo Zoom semantico direttamente tramite movimenti tocco o tasti di scelta rapida.

Le sezioni seguenti definiscono la struttura ad Automazione interfaccia utente, le proprietà, i pattern di controllo e gli eventi necessari per il tipo di **controllo SemanticZoom.** I Automazione interfaccia utente requisiti si applicano a tutti i controlli Zoom semantico in cui il framework o la piattaforma dell'interfaccia utente integra Automazione interfaccia utente per i tipi di controllo e i pattern di controllo.

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Proprietà e pattern di controllo necessari](#required-control-patterns-and-properties)
-   [Eventi obbligatori](#required-events)
-   [Osservazioni:](#remarks)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

La tabella seguente illustra un controllo tipico e una visualizzazione contenuto dell'albero Automazione interfaccia utente che riguarda il tipo di controllo **SemanticZoom** e descrive ciò che può essere contenuto in ogni visualizzazione. Per altre informazioni sull'albero Automazione interfaccia utente, vedere panoramica Automazione interfaccia utente [albero](uiauto-treeoverview.md).



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
<li>[SemanticZoom]
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
<li>[SemanticZoom]
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

Nella tabella seguente sono elencate Automazione interfaccia utente proprietà il cui valore o definizione è particolarmente rilevante per i controlli che implementano il tipo di controllo **SemanticZoom.** Per altre informazioni sulle Automazione interfaccia utente, vedere Recupero di proprietà [da Automazione interfaccia utente elementi](uiauto-propertiesforclients.md).



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
<td>Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata dell'Automazione interfaccia utente albero.</td>
</tr>
<tr class="even">
<td><a href="uiauto-automation-element-propids.md"><strong>UIA_BoundingRectanglePropertyId</strong></a></td>
<td>Vedere le note.</td>
<td>Il rettangolo più esterno che contiene l'intero controllo.</td>
</tr>
<tr class="odd">
<td><a href="uiauto-automation-element-propids.md"><strong>UIA_ClickablePointPropertyId</strong></a></td>
<td>Vedere le note.</td>
<td>Se il controllo elenco ha un punto selezionabile (un punto su cui è possibile fare clic per fare in modo che l'elenco prenda lo stato attivo), tale punto deve essere esposto tramite questa proprietà. Se il valore della proprietà <a href="uiauto-automation-element-propids.md"><strong>UIA_IsOffscreenPropertyId</strong></a> è <strong>TRUE,</strong>il tentativo di recuperare questa proprietà comporta l'errore <a href="uiauto-error-codes.md"><strong>UIA_E_NOCLICKABLEPOINT</strong></a> errore.</td>
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
<td>Se è presente un'etichetta di testo statica, questa proprietà deve esporre un riferimento a tale controllo.</td>
</tr>
<tr class="odd">
<td><a href="uiauto-automation-element-propids.md"><strong>UIA_LocalizedControlTypePropertyId</strong></a></td>
<td>Vedere le note.</td>
<td>Stringa localizzata corrispondente al tipo <strong>di controllo SemanticZoom.</strong> Il valore predefinito è &quot; zoom &quot; semantico per en-US o inglese (Stati Uniti).
<blockquote>
[!Note]<br />
Alcuni framework lo concatenavano come &quot; semanticzoom &quot; .
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="uiauto-automation-element-propids.md"><strong>UIA_NamePropertyId</strong></a></td>
<td>Vedere le note.</td>
<td>Una stringa vuota è accettabile o è possibile specificare un nome più utile, purché non contenga il termine zoom semantico , che renderebbe confusa la combinazione di tipo di controllo e nome.</td>
</tr>
</tbody>
</table>



 

## <a name="required-control-patterns-and-properties"></a>Proprietà e pattern di controllo necessari

Nella tabella seguente sono elencati i Automazione interfaccia utente di controllo necessari per essere supportati da tutti i controlli Zoom semantico. Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Pattern di controllo/proprietà del pattern                  | Supporto/valore | Note                                                                                                                                                                                                                                                                                                                                                          |
|---------------------------------------------------|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) | Dipende da       | I controlli Zoom semantico [supportano il pattern di](uiauto-implementingtoggle.md) controllo Toggle per consentire l'a attivazione o la disattivazione dello zoom. [**ToggleState \_ Off**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate) corrisponde allo stato flat, all-up e [**ToggleState \_ On**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate) corrisponde alla visualizzazione con zoom indietro di alto livello. |



 

## <a name="required-events"></a>Eventi obbligatori

Nella tabella seguente sono elencati Automazione interfaccia utente eventi di zoom semantici che i controlli sono necessari per supportare. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automazione interfaccia utente evento                                                                                                                   | Note                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**Interfaccia \_ utente Evento di modifica della proprietà BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md) |                                                                                                                            |
| [**Interfaccia \_ utente Evento di modifica della proprietà IsEnabledPropertyId.**](uiauto-automation-element-propids.md)                 | Se il controllo supporta la [**proprietà IsEnabled,**](uiauto-automation-element-propids.md) deve supportare questo evento.   |
| [**Interfaccia \_ utente Evento di modifica della proprietà IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)             | Se il controllo supporta la [**proprietà IsOffscreen,**](uiauto-automation-element-propids.md) deve supportare questo evento. |
| [**Interfaccia \_ utente Evento di modifica della proprietà ToggleToggleStatePropertyId.**](uiauto-control-pattern-propids.md)    |                                                                                                                            |



 

## <a name="remarks"></a>Commenti

Se un'interfaccia utente ha un pulsante visibile per attivare o disattivare il comportamento del controllo Zoom semantico, questo pulsante non deve avere un tipo di controllo **SemanticZoom.** Si tratta di un'operazione contro intuitiva, ma il tipo di controllo **SemanticZoom** caratterizza il contenitore del contenuto di zoom, non un pulsante che controlla lo zoom. Tale pulsante può essere rappresentato semplicemente come tipo [di controllo Button](uiauto-supportbuttoncontroltype.md) con il pattern di controllo [Toggle.](uiauto-implementingtoggle.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente](uiauto-controltypesoverview.md)
</dt> <dt>

[Cenni preliminari su automazione interfaccia utente](uiauto-uiautomationoverview.md)
</dt> </dl>

 

