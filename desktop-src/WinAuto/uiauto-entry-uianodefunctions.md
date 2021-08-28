---
title: Funzioni dei nodi deprecate
description: Funzioni dei nodi deprecate
ms.assetid: 72833757-a356-4727-8fc8-77a60e26aa99
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d700c506ee0bb0baf41cdd2facb85b0e7153d57
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476167"
---
# <a name="deprecated-node-functions"></a>Funzioni dei nodi deprecate

> [!Note]  
> Le funzioni del pattern di controllo descritte in questa sezione sono deprecate. Le applicazioni client devono usare Component Object Model (COM) descritte nelle sezioni seguenti:
>
> -   [Automazione interfaccia utente interfacce degli elementi per i client](uiauto-entry-uiautoclientinterfaces.md)
> -   [Interfaccia della condizione di proprietà per i client](uiauto-client-propconditioninterfaces.md)
> -   [Interfacce dei pattern di controllo per i client](uiauto-client-controlpatterninterfaces.md)
> -   [Interfacce di gestione degli eventi per i client](uiauto-client-eventhandlinginterfaces.md)
> -   [Interfacce factory proxy per i client](uiauto-client-proxyfactoryinterfaces.md)

 

## <a name="in-this-section"></a>Contenuto della sezione




| Funzione | Descrizione | 
|----------|-------------|
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaaddevent"><strong>UiaAddEvent</strong></a><br /> | <blockquote>[!Note]<br />Questa funzione è deprecata. Le applicazioni client devono usare le interfacce COM Automazione interfaccia utente Microsoft.</blockquote><br /> Aggiunge un listener per gli eventi in un nodo nell'Automazione interfaccia utente albero.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaeventaddwindow"><strong>UiaEventAddWindow</strong></a><br /> | <blockquote>[!Note]<br />Questa funzione è deprecata. Le applicazioni client devono usare Automazione interfaccia utente interfacce COM.</blockquote><br /> Aggiunge una finestra al listener di eventi.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nc-uiautomationcoreapi-uiaeventcallback"><em>UiaEventCallback</em></a><br /> | <blockquote>[!Note]<br />Questa funzione è deprecata. Le applicazioni client devono usare Automazione interfaccia utente interfacce COM.</blockquote><br /> Funzione implementata dal client che viene chiamata Automazione interfaccia utente quando viene generato un evento sottoscritto dal client.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaeventremovewindow"><strong>UiaEventRemoveWindow</strong></a><br /> | <blockquote>[!Note]<br />Questa funzione è deprecata. Le applicazioni client devono usare Automazione interfaccia utente interfacce COM.</blockquote><br /> Rimuove una finestra dal listener di eventi.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiafind"><strong>UiaFind</strong></a><br /> | <blockquote>[!Note]<br />Questa funzione è deprecata. Le applicazioni client devono usare Automazione interfaccia utente interfacce COM.</blockquote><br /> Recupera uno o più nodi Automazione interfaccia utente corrispondenti ai criteri di ricerca.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiageterrordescription"><strong>UiaGetErrorDescription</strong></a><br /> | <blockquote>[!Note]<br />Questa funzione è deprecata. Le applicazioni client devono usare Automazione interfaccia utente interfacce COM.</blockquote><br /> Ottiene una stringa di errore in modo che possa essere passata al client. Questo metodo non viene usato direttamente dai client.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetpatternprovider"><strong>UiaGetPatternProvider</strong></a><br /> | <blockquote>[!Note]<br />Questa funzione è deprecata. Le applicazioni client devono usare Automazione interfaccia utente interfacce COM.</blockquote><br /> Recupera un pattern <em>di controllo</em>.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetpropertyvalue"><strong>UiaGetPropertyValue</strong></a><br /> | <blockquote>[!Note]<br />Questa funzione è deprecata. Le applicazioni client devono usare Automazione interfaccia utente interfacce COM.</blockquote><br /> Recupera il valore di una proprietà Automazione interfaccia utente proprietà .<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetrootnode"><strong>UiaGetRootNode</strong></a><br /> | <blockquote>[!Note]<br />Questa funzione è deprecata. Le applicazioni client devono usare Automazione interfaccia utente interfacce COM.</blockquote><br /> Recupera il nodo Automazione interfaccia utente radice.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetruntimeid"><strong>UiaGetRuntimeId</strong></a><br /> | <blockquote>[!Note]<br />Questa funzione è deprecata. Le applicazioni client devono usare Automazione interfaccia utente interfacce COM.</blockquote><br /> Recupera l'identificatore di runtime di un Automazione interfaccia utente nodo.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetupdatedcache"><strong>UiaGetUpdatedCache</strong></a><br /> | <blockquote>[!Note]<br />Questa funzione è deprecata. Le applicazioni client devono usare Automazione interfaccia utente interfacce COM.</blockquote><br /> Aggiorna la cache dei valori delle proprietà e dei pattern di controllo.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahpatternobjectfromvariant"><strong>UiaHPatternObjectFromVariant</strong></a><br /> | <blockquote>[!Note]<br />Questa funzione è deprecata. Le applicazioni client devono usare Automazione interfaccia utente interfacce COM.</blockquote><br /> Ottiene un oggetto pattern di controllo da un <a href="/windows/win32/api/oaidl/ns-oaidl-variant"><strong>tipo VARIANT.</strong></a><br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahtextrangefromvariant"><strong>UiaHTextRangeFromVariant</strong></a><br /> | <blockquote>[!Note]<br />Questa funzione è deprecata. Le applicazioni client devono usare Automazione interfaccia utente interfacce COM.</blockquote><br /> Ottiene un intervallo di testo da un <a href="/windows/win32/api/oaidl/ns-oaidl-variant"><strong>tipo VARIANT.</strong></a><br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahuianodefromvariant"><strong>UiaHUiaNodeFromVariant</strong></a><br /> | <blockquote>[!Note]<br />Questa funzione è deprecata. Le applicazioni client devono usare Automazione interfaccia utente interfacce COM.</blockquote><br /> Ottiene un HUIANODE da un <a href="/windows/win32/api/oaidl/ns-oaidl-variant"><strong>tipo VARIANT.</strong></a><br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uialookupid"><strong>UiaLookupId</strong></a><br /> | <blockquote>[!Note]<br />Questa funzione è deprecata. Le applicazioni client devono usare Automazione interfaccia utente interfacce COM.</blockquote><br /> Ottiene l'identificatore integer che può essere utilizzato nei metodi che richiedono PROPERTYID, PATTERNID, CONTROLTYPEID, TEXTATTRIBUTEID o EVENTID.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianavigate"><strong>UiaNavigate</strong></a><br /> | <blockquote>[!Note]<br />Questa funzione è deprecata. Le applicazioni client devono usare Automazione interfaccia utente interfacce COM.</blockquote><br /> Passa all'albero Automazione interfaccia utente, recuperando facoltativamente le informazioni memorizzate nella cache.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefromfocus"><strong>UiaNodeFromFocus</strong></a><br /> | <blockquote>[!Note]<br />Questa funzione è deprecata. Le applicazioni client devono usare Automazione interfaccia utente interfacce COM.</blockquote><br /> Recupera il nodo Automazione interfaccia utente per l'elemento dell'interfaccia utente che ha attualmente lo stato attivo per l'input.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefromhandle"><strong>UiaNodeFromHandle</strong></a><br /> | <blockquote>[!Note]<br />Questa funzione è deprecata. Le applicazioni client devono usare Automazione interfaccia utente interfacce COM.</blockquote><br /> Recupera il nodo Automazione interfaccia utente associato a una finestra.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefrompoint"><strong>UiaNodeFromPoint</strong></a><br /> | <blockquote>[!Note]<br />Questa funzione è deprecata. Le applicazioni client devono usare Automazione interfaccia utente interfacce COM.</blockquote><br /> Recupera il nodo Automazione interfaccia utente per l'elemento nel punto specificato.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianodefromprovider"><strong>UiaNodeFromProvider</strong></a><br /> | <blockquote>[!Note]<br />Questa funzione è deprecata. Le applicazioni client devono usare Automazione interfaccia utente interfacce COM.</blockquote><br /> Recupera il nodo Automazione interfaccia utente per un provider di elementi non elaborati.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uianoderelease"><strong>UiaNodeRelease</strong></a><br /> | <blockquote>[!Note]<br />Questa funzione è deprecata. Le applicazioni client devono usare Automazione interfaccia utente interfacce COM.</blockquote><br /> Elimina un nodo dalla memoria.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiapatternrelease"><strong>UiaPatternRelease</strong></a><br /> | <blockquote>[!Note]<br />Questa funzione è deprecata. Le applicazioni client devono usare Automazione interfaccia utente interfacce COM.</blockquote><br /> Elimina un oggetto modello allocato dalla memoria.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nc-uiautomationcoreapi-uiaprovidercallback"><em>UiaProviderCallback</em></a><br /> | <blockquote>[!Note]<br />Questa funzione è deprecata. Le applicazioni client devono usare Automazione interfaccia utente interfacce COM.</blockquote><br /> Funzione definita dall'applicazione chiamata da Automazione interfaccia utente ottenere un provider sul lato client per un elemento.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiarectisempty"><strong>UiaRectIsEmpty</strong></a><br /> | <blockquote>[!Note]<br />Questa funzione è deprecata. Le applicazioni client devono usare Automazione interfaccia utente interfacce COM.</blockquote><br /> Ottiene un valore booleano che specifica se tutte le coordinate di un rettangolo sono impostate su 0.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiarectsetempty"><strong>UiaRectSetEmpty</strong></a><br /> | <blockquote>[!Note]<br />Questa funzione è deprecata. Le applicazioni client devono usare Automazione interfaccia utente interfacce COM.</blockquote><br /> Imposta gli elementi di una <a href="/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiarect"><strong>struttura UiaRect</strong></a> su 0.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaregisterprovidercallback"><strong>UiaRegisterProviderCallback</strong></a><br /> | <blockquote>[!Note]<br />Questa funzione è deprecata. Le applicazioni client devono usare Automazione interfaccia utente interfacce COM.</blockquote><br /> Registra il metodo definito dall'applicazione chiamato da Automazione interfaccia utente ottenere un provider per un elemento .<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaremoveevent"><strong>UiaRemoveEvent</strong></a><br /> | <blockquote>[!Note]<br />Questa funzione è deprecata. Le applicazioni client devono usare Automazione interfaccia utente interfacce COM.</blockquote><br /> Rimuove un listener per gli eventi in un nodo nell'Automazione interfaccia utente albero.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiasetfocus"><strong>UiaSetFocus</strong></a><br /> | <blockquote>[!Note]<br />Questa funzione è deprecata. Le applicazioni client devono usare Automazione interfaccia utente interfacce COM.</blockquote><br /> Imposta lo stato attivo per l'input sull'elemento specificato nell'interfaccia utente.<br /> | 
| <a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiatextrangerelease"><strong>UiaTextRangeRelease</strong></a><br /> | <blockquote>[!Note]<br />Questa funzione è deprecata. Le applicazioni client devono usare Automazione interfaccia utente interfacce COM.</blockquote><br /> Elimina un oggetto intervallo di testo allocato dalla memoria.<br /> | 




 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Automazione interfaccia utente client](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 

