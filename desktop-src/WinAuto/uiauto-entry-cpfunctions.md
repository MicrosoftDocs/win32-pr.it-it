---
title: Funzioni del pattern di controllo deprecate
description: Funzioni del pattern di controllo deprecate
ms.assetid: 06434b07-7592-4909-8c4e-064382bdbf98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f646f9a9e3139d487785e344b9d3fc242b1a40e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395470"
---
# <a name="deprecated-control-pattern-functions"></a>Funzioni del pattern di controllo deprecate

> [!Note]  
> Le funzioni del pattern di controllo descritte in questa sezione sono deprecate. Le applicazioni client devono usare le interfacce Component Object Model (COM) descritte nelle sezioni seguenti:
>
> -   [Interfacce degli elementi di automazione interfaccia utente per i client](uiauto-entry-uiautoclientinterfaces.md)
> -   [Interfaccia della condizione di proprietà per i client](uiauto-client-propconditioninterfaces.md)
> -   [Interfacce del pattern di controllo per i client](uiauto-client-controlpatterninterfaces.md)
> -   [Interfacce di gestione degli eventi per i client](uiauto-client-eventhandlinginterfaces.md)
> -   [Interfacce Factory proxy per i client](uiauto-client-proxyfactoryinterfaces.md)

 

## <a name="in-this-section"></a>Contenuto della sezione



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Funzione</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-dockpattern_setdockposition"><strong>DockPattern_SetDockPosition</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente Microsoft.
</blockquote>
<br/> Ancora l'elemento di automazione interfaccia utente in corrispondenza della <em>impostata su DockPosition</em> richiesta all'interno di un contenitore di ancoraggio.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-expandcollapsepattern_collapse"><strong>ExpandCollapsePattern_Collapse</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Nasconde tutti i nodi, i controlli o il contenuto discendente dell'elemento di automazione interfaccia utente.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-expandcollapsepattern_expand"><strong>ExpandCollapsePattern_Expand</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Espande un controllo sullo schermo in modo da visualizzare altre informazioni.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-gridpattern_getitem"><strong>GridPattern_GetItem</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Ottiene il nodo per un elemento in una griglia.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-invokepattern_invoke"><strong>InvokePattern_Invoke</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Invia una richiesta per l'attivazione di un controllo e l'avvio dell'azione singola e non ambigua corrispondente.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-itemcontainerpattern_finditembyproperty"><strong>ItemContainerPattern_FindItemByProperty</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Recupera un nodo all'interno di un nodo contenitore, in base al valore di una proprietà specificata.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-legacyiaccessiblepattern_dodefaultaction"><strong>LegacyIAccessiblePattern_DoDefaultAction</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Esegue l'azione predefinita Microsoft Active Accessibility per l'elemento.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-legacyiaccessiblepattern_getiaccessible"><strong>LegacyIAccessiblePattern_GetIAccessible</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Recupera un oggetto <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible"><strong>IAccessible</strong></a> che corrisponde all'elemento di automazione interfaccia utente.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-legacyiaccessiblepattern_select"><strong>LegacyIAccessiblePattern_Select</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Esegue una selezione di Microsoft Active Accessibility.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-legacyiaccessiblepattern_setvalue"><strong>LegacyIAccessiblePattern_SetValue</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Imposta la proprietà del valore di Microsoft Active Accessibility per il nodo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-multipleviewpattern_getviewname"><strong>MultipleViewPattern_GetViewName</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Recupera il nome di una visualizzazione specifica del controllo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-multipleviewpattern_setcurrentview"><strong>MultipleViewPattern_SetCurrentView</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Imposta un controllo su un layout diverso.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-rangevaluepattern_setvalue"><strong>RangeValuePattern_SetValue</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Imposta il valore di un controllo che ha un intervallo numerico.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-scrollitempattern_scrollintoview"><strong>ScrollItemPattern_ScrollIntoView</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Scorre l'area di contenuto di un oggetto contenitore per visualizzare l'elemento di automazione interfaccia utente all'interno dell'area visibile (viewport) del contenitore.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-scrollpattern_scroll"><strong>ScrollPattern_Scroll</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Scorre l'area attualmente visibile dell'area di contenuto del <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-scrollamount"><strong>ScrollAmount</strong></a>specificato, orizzontalmente, verticalmente o entrambi.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-scrollpattern_setscrollpercent"><strong>ScrollPattern_SetScrollPercent</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Scorre un contenitore in una posizione specifica orizzontalmente, verticalmente o entrambi.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-selectionitempattern_addtoselection"><strong>SelectionItemPattern_AddToSelection</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Aggiunge un elemento non selezionato a una selezione in un controllo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-selectionitempattern_removefromselection"><strong>SelectionItemPattern_RemoveFromSelection</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Rimuove un elemento dalla selezione in un contenitore di selezione.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-selectionitempattern_select"><strong>SelectionItemPattern_Select</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Seleziona un elemento in un contenitore di selezione.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-synchronizedinputpattern_cancel"><strong>SynchronizedInputPattern_Cancel</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Causa l'interruzione dell'ascolto da parte del provider di automazione interfaccia utente per l'input del mouse o della tastiera.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-synchronizedinputpattern_startlistening"><strong>SynchronizedInputPattern_StartListening</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Fa in modo che il provider di automazione interfaccia utente inizi ad ascoltare l'input del mouse o della tastiera.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_get_documentrange"><strong>TextPattern_get_DocumentRange</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Ottiene l'intervallo di testo per l'intero documento.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_get_supportedtextselection"><strong>TextPattern_get_SupportedTextSelection</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Verifica se il contenuto del contenitore di testo può essere selezionato e deselezionato.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_getselection"><strong>TextPattern_GetSelection</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Ottiene l'intervallo corrente del testo selezionato da un contenitore di testo che supporta il pattern di testo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_getvisibleranges"><strong>TextPattern_GetVisibleRanges</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Recupera una matrice di intervalli di testo non contigui da un contenitore di testo in cui ogni intervallo di testo inizia con la prima riga parzialmente visibile fino alla fine dell'ultima riga parzialmente visibile. Un layout a più colonne, ad esempio, in cui le colonne vengono parzialmente esposte all'esterno dell'area visibile del viewport e il contenuto passa dalla parte inferiore di una colonna alla parte superiore della successiva.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_rangefromchild"><strong>TextPattern_RangeFromChild</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Ottiene l'intervallo di testo su cui si estende un determinato nodo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_rangefrompoint"><strong>TextPattern_RangeFromPoint</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Recupera l'intervallo di testo degenerato (vuoto) più vicino alle coordinate dello schermo specificate.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_addtoselection"><strong>TextRange_AddToSelection</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Aggiunge alla raccolta esistente del testo evidenziato in un contenitore di testo che supporta più selezioni non contigue evidenziando il testo supplementare corrispondente agli endpoint <em>iniziale</em> e <em>finale</em> dell'intervallo di testo chiamante.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_clone"><strong>TextRange_Clone</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Copia un intervallo di testo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_compare"><strong>TextRange_Compare</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Confronta due intervalli di testo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_compareendpoints"><strong>TextRange_CompareEndpoints</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Restituisce un valore che indica se due intervalli di testo hanno endpoint identici.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_expandtoenclosingunit"><strong>TextRange_ExpandToEnclosingUnit</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Espande l'intervallo di testo a un'unità più grande o più piccola, ad esempio carattere, parola, riga o pagina.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_findattribute"><strong>TextRange_FindAttribute</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Cerca in una direzione specificata la prima parte di testo che supporta un attributo di testo specificato.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_findtext"><strong>TextRange_FindText</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Restituisce il primo intervallo di testo nella direzione specificata che contiene il testo che il client sta cercando.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_getattributevalue"><strong>TextRange_GetAttributeValue</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Ottiene il valore di un attributo di testo per un intervallo di testo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_getboundingrectangles"><strong>TextRange_GetBoundingRectangles</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Recupera il numero minimo di rettangoli di delimitazione che possono racchiudere l'intervallo, un rettangolo per riga.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_getchildren"><strong>TextRange_GetChildren</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Restituisce tutti gli elementi di automazione interfaccia utente contenuti all'interno dell'intervallo di testo specificato.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_getenclosingelement"><strong>TextRange_GetEnclosingElement</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Restituisce il nodo per il provider più piccolo successivo che copre l'intervallo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_gettext"><strong>TextRange_GetText</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Restituisce il testo in un intervallo di testo, fino a un numero di caratteri specificato.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_move"><strong>TextRange_Move</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Sposta l'intervallo di testo del numero di unità specificato richiesto dal client.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_moveendpointbyrange"><strong>TextRange_MoveEndpointByRange</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Sposta un endpoint di un intervallo nell'endpoint di un altro intervallo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_moveendpointbyunit"><strong>TextRange_MoveEndpointByUnit</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Sposta un endpoint dell'intervallo del numero di unità specificato.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_removefromselection"><strong>TextRange_RemoveFromSelection</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Rimuove il testo selezionato, corrispondente all'intervallo di testo chiamante <em>TextPatternRangeEndpoint_Start</em> e <em>TextPatternRangeEndpoint_End</em> endpoint, da una raccolta esistente di testo selezionato in un contenitore di testo che supporta selezioni multiple non contigue.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_scrollintoview"><strong>TextRange_ScrollIntoView</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Scorre il testo in modo che l'intervallo specificato sia visibile nel viewport.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_select"><strong>TextRange_Select</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Seleziona un intervallo di testo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-togglepattern_toggle"><strong>TogglePattern_Toggle</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Consente di impostare un controllo sullo stato successivo supportato.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-transformpattern_move"><strong>TransformPattern_Move</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Sposta un elemento in una posizione specificata sullo schermo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-transformpattern_resize"><strong>TransformPattern_Resize</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Ridimensiona un elemento sullo schermo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-transformpattern_rotate"><strong>TransformPattern_Rotate</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Ruota un elemento sullo schermo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-valuepattern_setvalue"><strong>ValuePattern_SetValue</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Imposta il valore di testo di un elemento.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-virtualizeditempattern_realize"><strong>VirtualizedItemPattern_Realize</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Rende l'elemento virtuale completamente accessibile come elemento di automazione interfaccia utente.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-windowpattern_close"><strong>WindowPattern_Close</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Chiude una finestra aperta.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-windowpattern_setwindowvisualstate"><strong>WindowPattern_SetWindowVisualState</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Imposta lo stato di visualizzazione di una finestra; ad esempio, per ingrandire una finestra.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-windowpattern_waitforinputidle"><strong>WindowPattern_WaitForInputIdle</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Comporta il blocco del codice chiamante per il lasso di tempo specificato o finché il processo associato non entra in stato di inattività, in base alla prima condizione che viene soddisfatta.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Client di automazione interfaccia utente](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 

 





