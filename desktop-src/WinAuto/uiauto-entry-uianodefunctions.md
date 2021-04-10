---
title: Funzioni del nodo deprecate
description: Funzioni del nodo deprecate
ms.assetid: 72833757-a356-4727-8fc8-77a60e26aa99
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7273ffd6c704c9db6408165d1eba3a293f3d1cf
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "103963528"
---
# <a name="deprecated-node-functions"></a>Funzioni del nodo deprecate

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
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaaddevent"><strong>UiaAddEvent</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente Microsoft.
</blockquote>
<br/> Aggiunge un listener per gli eventi in un nodo nell'albero di automazione interfaccia utente.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaeventaddwindow"><strong>UiaEventAddWindow</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Aggiunge una finestra al listener di eventi.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nc-uiautomationcoreapi-uiaeventcallback"><em>UiaEventCallback</em></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Funzione implementata dal client chiamata dall'automazione interfaccia utente quando viene generato un evento che il client ha sottoscritto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaeventremovewindow"><strong>UiaEventRemoveWindow</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Rimuove una finestra dal listener di eventi.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiafind"><strong>UiaFind</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Recupera uno o più nodi di automazione interfaccia utente che corrispondono ai criteri di ricerca.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiageterrordescription"><strong>UiaGetErrorDescription</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Ottiene una stringa di errore in modo che possa essere passata al client. Questo metodo non viene utilizzato direttamente dai client.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetpatternprovider"><strong>UiaGetPatternProvider</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Recupera un <em>pattern di controllo</em>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetpropertyvalue"><strong>UiaGetPropertyValue</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Recupera il valore di una proprietà di automazione interfaccia utente.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetrootnode"><strong>UiaGetRootNode</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Recupera il nodo di automazione interfaccia utente radice.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetruntimeid"><strong>UiaGetRuntimeId</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Recupera l'identificatore di runtime di un nodo di automazione interfaccia utente.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetupdatedcache"><strong>UiaGetUpdatedCache</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Aggiorna la cache dei valori delle proprietà e dei pattern di controllo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahpatternobjectfromvariant"><strong>UiaHPatternObjectFromVariant</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Ottiene un oggetto pattern di controllo da un tipo <a href="/windows/win32/api/oaidl/ns-oaidl-variant"><strong>Variant</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahtextrangefromvariant"><strong>UiaHTextRangeFromVariant</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Ottiene un intervallo di testo da un tipo <a href="/windows/win32/api/oaidl/ns-oaidl-variant"><strong>Variant</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahuianodefromvariant"><strong>UiaHUiaNodeFromVariant</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Ottiene un HUIANODE da un tipo <a href="/windows/win32/api/oaidl/ns-oaidl-variant"><strong>Variant</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uialookupid"><strong>UiaLookupId</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Ottiene l'identificatore di tipo integer che può essere utilizzato nei metodi che richiedono PROPERTYID, PATTERNID, CONTROLTYPEID, TEXTATTRIBUTEID o EVENTId.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianavigate"><strong>UiaNavigate</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Naviga nell'albero di automazione interfaccia utente, recuperando facoltativamente le informazioni memorizzate nella cache.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefromfocus"><strong>UiaNodeFromFocus</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Recupera il nodo di automazione interfaccia utente per l'elemento dell'interfaccia utente che ha attualmente lo stato attivo per l'input.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefromhandle"><strong>UiaNodeFromHandle</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Recupera il nodo di automazione interfaccia utente associato a una finestra.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefrompoint"><strong>UiaNodeFromPoint</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Recupera il nodo di automazione interfaccia utente per l'elemento in corrispondenza del punto specificato.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefromprovider"><strong>UiaNodeFromProvider</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Recupera il nodo di automazione interfaccia utente per un provider di elementi non elaborati.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianoderelease"><strong>UiaNodeRelease</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Elimina un nodo dalla memoria.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiapatternrelease"><strong>UiaPatternRelease</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Elimina un oggetto modello allocato dalla memoria.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nc-uiautomationcoreapi-uiaprovidercallback"><em>UiaProviderCallback</em></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Funzione definita dall'applicazione chiamata dall'automazione interfaccia utente per ottenere un provider sul lato client per un elemento.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiarectisempty"><strong>UiaRectIsEmpty</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Ottiene un valore booleano che specifica se le coordinate di un rettangolo sono impostate su 0.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiarectsetempty"><strong>UiaRectSetEmpty</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Imposta gli elementi di una struttura <a href="/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiarect"><strong>UiaRect</strong></a> su 0.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaregisterprovidercallback"><strong>UiaRegisterProviderCallback</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Registra il metodo definito dall'applicazione chiamato dall'automazione interfaccia utente per ottenere un provider per un elemento.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaremoveevent"><strong>UiaRemoveEvent</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Rimuove un listener per gli eventi in un nodo nell'albero di automazione interfaccia utente.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiasetfocus"><strong>UiaSetFocus</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Imposta lo stato attivo per l'input sull'elemento specificato nell'interfaccia utente.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiatextrangerelease"><strong>UiaTextRangeRelease</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa funzione è deprecata. Le applicazioni client devono invece usare le interfacce COM di automazione interfaccia utente.
</blockquote>
<br/> Elimina un oggetto intervallo di testo allocato dalla memoria.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Client di automazione interfaccia utente](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 

