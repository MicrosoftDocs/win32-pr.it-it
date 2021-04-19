---
description: Gestione dei cookie in WinHTTP
ms.assetid: ef0f0847-05f6-4477-8e48-e0bea66314ab
title: Gestione dei cookie in WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e3b596225dc3c741ab9ed0139a63e343e7afb3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319817"
---
# <a name="cookie-handling-in-winhttp"></a>Gestione dei cookie in WinHTTP

I dati della sessione HTTP vengono passati tra il client e il server nell'intestazione del cookie della richiesta o della risposta. Il server invia i cookie al client nell'intestazione set-cookie della risposta e l'API WinHTTP invia nuovamente il cookie del server al server nell'intestazione del cookie della richiesta. Le specifiche di gestione dei cookie, descritte in RFC 2109 (HTTP State Management Mechanism), vengono implementate per impostazione predefinita in WinHTTP. Le specifiche di gestione dei cookie recenti, descritte in RFC 2964, non sono supportate da WinHTTP.

WinHTTP ottiene il cookie dall'intestazione Server Set-Cookie e lo archivia in una cache per ogni singola sessione. Questo cookie viene inviato nuovamente alle richieste successive nella stessa sessione WinHTTP in cui la destinazione corrisponde all'origine del cookie. L'API WinHTTP rigenera l'intestazione del cookie di richiesta per ogni tappa della richiesta.

L'elenco seguente descrive diverse opzioni che le applicazioni client WinHTTP possono usare per gestire i cookie:

-   Gestione automatica dei cookie: WinHTTP gestisce automaticamente i cookie e l'applicazione client non esegue alcuna gestione personalizzata dei cookie.
-   Disabilita gestione automatica dei cookie: la gestione automatica dei cookie nell'API WinHTTP è disabilitata e non vengono inviati cookie.
-   Specificare manualmente tutti i cookie: la gestione automatica dei cookie è disabilitata e l'applicazione client aggiunge o rimuove tutte le intestazioni dei cookie per ogni richiesta nella sessione.
-   Gestione automatica dei cookie: combinare la gestione automatica e manuale dei cookie.

## <a name="disabling-automatic-cookie-handling"></a>Disabilitazione della gestione automatica dei cookie

Per disabilitare la gestione dei cookie, l'applicazione client WinHTTP chiama la funzione [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) con il parametro *DWOPTION* impostato su WinHTTP \_ opzione \_ Disabilita \_ funzionalità e il parametro *lpBuffer* impostato su WinHTTP \_ disabilitare \_ cookie. Il parametro *HINTERNET* può essere un handle di sessione o un handle di richiesta. Quando la gestione dei cookie è disabilitata su un handle di richiesta che ha inviato una richiesta precedente, il client deve rimuovere manualmente le intestazioni dei cookie di richiesta esistenti con la funzione [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) prima di inviare la richiesta successiva. Per ulteriori informazioni, vedere [rimozione delle intestazioni dei cookie](#removing-cookie-headers).

**Nota**  L'applicazione client deve impostare tutti i cookie della sessione dopo la disabilitazione della modalità automatica.

## <a name="manually-specifying-all-cookies"></a>Specifica manuale di tutti i cookie

Quando la gestione automatica dei cookie è disabilitata, l'applicazione client WinHTTP dispone dell'opzione per specificare manualmente tutti i cookie. Per impostare manualmente il cookie, l'applicazione chiama [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) specificando l'intestazione del cookie nel parametro *pwszHeaders* . L'applicazione client deve cancellare tutte le intestazioni dei cookie prima di inviare di nuovo la richiesta.

L'applicazione client deve anche modificare l'intestazione del cookie quando la richiesta è stata reindirizzata. Per modificare il cookie sulle richieste reindirizzate, il client specifica una funzione di callback con [**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback) che risponde al caso di callback di reindirizzamento. Il gestore di callback deve cancellare il cookie inviato in precedenza sulla richiesta chiamando [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders). Per ulteriori informazioni sulla rimozione delle intestazioni dei cookie, vedere [rimozione delle intestazioni dei cookie](#removing-cookie-headers).

## <a name="manual-and-automatic-cookie-handling"></a>Gestione manuale e automatica dei cookie

Le applicazioni client WinHTTP possono combinare il meccanismo di gestione automatica dei cookie WinHTTP con la gestione manuale dei cookie. L'applicazione aggiunge cookie personalizzati all'intestazione del cookie generata automaticamente prima di inviare la richiesta con la funzione [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) . Il cookie personalizzato deve essere la prima intestazione del cookie nella richiesta per l'API WinHTTP per memorizzare correttamente il cookie nella cache. L'applicazione client deve anche rimuovere i cookie inviati alle richieste precedenti prima di inviare nuovamente una richiesta sullo stesso handle di richiesta. Per ulteriori informazioni, vedere Rimozione delle intestazioni dei cookie.

I cookie aggiunti a una richiesta prima della chiamata a [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) sono inclusi in tutte le richieste WinHTTP inviate per conto delle successive chiamate **WinHttpSendRequest** e [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) . È possibile che l'applicazione client elimini l'intestazione del cookie quando la richiesta è stata reindirizzata. Per cancellare il cookie sulle richieste reindirizzate, il client specifica una funzione di callback con [**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback) che risponde al caso di callback di reindirizzamento. Il gestore di callback deve cancellare il cookie inviato in precedenza sulla richiesta chiamando [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders). La funzione di callback non può impostare nuovi cookie personalizzati nel callback di reindirizzamento. Il client deve attendere il completamento di **WinHttpReceiveResponse** prima di aggiungere nuovi cookie per la chiamata **WinHttpSendRequest** successiva.

## <a name="removing-cookie-headers"></a>Rimozione delle intestazioni cookie

È possibile che l'applicazione client WinHTTP debba cancellare il cookie di richiesta esistente prima di inviare nuovamente una richiesta per impedire che i cookie inviati alle richieste precedenti vengano inviati nuovamente alla richiesta corrente. Per ulteriori informazioni, vedere la nota seguente. Tenere inoltre presente che i cookie non devono essere cancellati prima che la prima richiesta venga inviata sull'handle della richiesta. Il client può cancellare i cookie esistenti chiamando [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) con un'intestazione cookie vuota nel parametro *pwszHeaders* e il flag \_ \_ di sostituzione del flag ADDREQ WinHTTP \_ impostato nel parametro *dwModifier* . Nell'esempio di codice seguente viene illustrato come cancellare l'intestazione del cookie nella richiesta.

``` syntax
WinHttpAddRequestHeaders( hRequest, 
                          L"Cookie:", 
                          -1, 
                          WINHTTP_ADDREQ_FLAG_REPLACE);
```

L'API WinHTTP presenta diversi comportamenti di gestione dei cookie per le versioni del sistema operativo precedenti a Windows XP con Service Pack 2 (SP2) e Windows Server 2003 con Service Pack 1 (SP1).

* * Windows XP con SP2 e versioni successive e Windows Server 2003 con SP1 e versioni successive: * *

L'API WinHTTP Cancella tutti i cookie inviati alle richieste precedenti per l'handle della richiesta. Il client può aggiungere manualmente nuove intestazioni dei cookie prima di ogni chiamata a WinHttpSendRequest. Se la funzionalità di gestione automatica dei cookie dell'API WinHTTP non è stata disabilitata, l'API WinHTTP aggiungerà l'intestazione del nuovo cookie (o aggiungerà una nuova intestazione del cookie se l'applicazione client non è stata aggiunta manualmente) al cookie dal server.

* * Windows XP con SP2 e Windows Server 2003 con SP1: * *

L'API WinHTTP non cancella l'intestazione del cookie di richiesta dopo il completamento di [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) . I cookie inviati nelle richieste precedenti verranno inviati nuovamente in chiamate successive a [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest). L'applicazione client WinHTTP deve cancellare le intestazioni dei cookie esistenti prima di inviare nuovamente una richiesta nell'handle di richiesta.

 

 



