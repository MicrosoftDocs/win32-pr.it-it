---
description: Microsoft Windows servizi HTTP (WinHTTP) è destinato alle applicazioni server di livello intermedio e back-end che richiedono l'accesso a uno stack di client HTTP.
ms.assetid: 5b0cf321-8f69-4526-a628-e6ca0f9d4a58
title: Porting di applicazioni WinINet in WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b111cd79e7ce7edfb09d43993ee2735ce09275f51c58bcfad319fb073dccc5b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052009"
---
# <a name="porting-wininet-applications-to-winhttp"></a>Porting di applicazioni WinINet in WinHTTP

Microsoft Windows servizi HTTP (WinHTTP) è destinato alle applicazioni server di livello intermedio e back-end che richiedono l'accesso a uno stack di client HTTP. [Microsoft Windows Internet (WinINet)](winhttp-start-page.md) fornisce uno stack di client HTTP per le applicazioni client, nonché l'accesso ai protocolli File Transfer Protocol (FTP), SOCKSv4 e Gopher. Questa panoramica consente di determinare se la portabilità delle applicazioni WinINet in WinHTTP sarebbe utile. Vengono inoltre descritti i requisiti di conversione specifici.

-   [Aspetti da considerare prima di eseguire la portabilità dell'applicazione WinINet](#things-to-consider-before-porting-your-wininet-application)
-   [Equivalenti WinHTTP alle funzioni WinINet](#winhttp-equivalents-to-wininet-functions)
-   [Gestione diversa delle richieste asincrone](#different-handling-of-asynchronous-requests)
-   [Differenze nelle notifiche di callback WinHTTP](#differences-in-winhttp-callback-notifications)
-   [Differenze di autenticazione](#authentication-differences)
-   [Differenze nelle transazioni HTTP protette](#differences-in-secure-http-transactions)

## <a name="things-to-consider-before-porting-your-wininet-application"></a>Aspetti da considerare prima di eseguire la portabilità dell'applicazione WinINet

Valutare la possibilità di eseguire la portabilità dell'applicazione WinINet in WinHTTP se l'applicazione può trarre vantaggio da:

-   Stack di client HTTP indipendente dal server.
-   Utilizzo dello stack ridotto al minimo.
-   Scalabilità di un'applicazione server.
-   Meno dipendenze dalle API correlate alla piattaforma.
-   Supporto per la rappresentazione di thread.
-   Stack HTTP descrittivo per i servizi.
-   Accesso all'oggetto [**WinHttpRequest**](winhttprequest.md) gestibile da script.

Non prendere in considerazione la portabilità dell'applicazione WinINet in WinHTTP se deve supportare uno o più degli elementi seguenti:

-   Protocollo FTP o Gopher dallo stack HTTP.
-   Supporto per il protocollo SOCKSv4 per la comunicazione con i proxy SOCKS.
-   Servizi di connessione remota automatici.

Se si decide di convertire l'applicazione in WinHTTP, le sezioni seguenti illustrano il processo di conversione.

Per un'applicazione di esempio sia per WinINet che per WinHTTP, confrontare l'esempio AsyncDemo per WinINet con l'esempio AsyncDemo per WinHTTP.

## <a name="winhttp-equivalents-to-wininet-functions"></a>Equivalenti WinHTTP alle funzioni WinINet

La tabella seguente elenca le funzioni WinINet correlate allo stack di client HTTP insieme agli equivalenti WinHTTP.

Se l'applicazione richiede funzioni WinINet non elencate, non convertire l'applicazione in WinHTTP.



| Funzione WinINet                                                       | Equivalente WinHTTP                                                                                                                                                                                     | Modifiche di cui è possibile fare di più                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**HttpAddRequestHeaders**](/windows/desktop/api/wininet/nf-wininet-httpaddrequestheadersa)             | [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)                                                                                                                                           | Nessuno.                                                                                                                                                                                                                                                                                                                                |
| [**HttpEndRequest**](/windows/desktop/api/wininet/nf-wininet-httpendrequesta)                           | [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse)                                                                                                                                               | Il valore di contesto viene impostato [**con WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) o [**WinHttpSetOption.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) Le opzioni di richiesta vengono impostate [**con WinHttpOpenRequest.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) deve essere chiamato dopo l'invio di una richiesta.                      |
| [**HttpOpenRequest**](/windows/desktop/api/wininet/nf-wininet-httpopenrequesta)                         | [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)                                                                                                                                                       | Il valore di contesto viene impostato [**con WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) o [**WinHttpSetOption.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)                                                                                                                                                                                                      |
| [**HttpQueryInfo**](/windows/desktop/api/wininet/nf-wininet-httpqueryinfoa)                             | [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders)                                                                                                                                                     | Nessuno.                                                                                                                                                                                                                                                                                                                                |
| [**HttpSendRequest**](/windows/desktop/api/wininet/nf-wininet-httpsendrequesta)                         | [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)                                                                                                                                                       | Il valore di contesto può essere impostato [**con WinHttpSendRequest.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)                                                                                                                                                                                                                                                  |
| [**HttpSendRequestEx**](/windows/desktop/api/wininet/nf-wininet-httpsendrequestexa)                     | [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)                                                                                                                                                       | Non è possibile specificare buffer.                                                                                                                                                                                                                                                                                                          |
| [**InternetCanonicalizeUrl**](/windows/desktop/api/wininet/nf-wininet-internetcanonicalizeurla)         | Nessun equivalente                                                                                                                                                                                          | Gli URL vengono ora inseriti in formato canonico in [**WinHttpOpenRequest.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)                                                                                                                                                                                                                                              |
| [**InternetCheckConnection**](/windows/desktop/api/wininet/nf-wininet-internetcheckconnectiona)         | Nessun equivalente                                                                                                                                                                                          | Non implementato in WinHTTP.                                                                                                                                                                                                                                                                                                          |
| [**InternetCloseHandle**](/windows/desktop/api/wininet/nf-wininet-internetclosehandle)                 | [**WinHttpCloseHandle**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpclosehandle)                                                                                                                                                       | La chiusura di un handle padre in WinHTTP non chiude in modo ricorsivo gli handle figlio.                                                                                                                                                                                                                                                         |
| [**InternetCombineUrl**](/windows/desktop/api/wininet/nf-wininet-internetcombineurla)                   | Nessun equivalente                                                                                                                                                                                          | Gli URL possono essere assemblati con [**la funzione WinHttpCreateUrl.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl)                                                                                                                                                                                                                                                |
| [**InternetConfirmZoneCrossing**](/windows/desktop/api/wininet/nf-wininet-internetconfirmzonecrossing) | Nessun equivalente                                                                                                                                                                                          | Non implementato in WinHTTP.                                                                                                                                                                                                                                                                                                          |
| [**InternetConnetti**](/windows/desktop/api/wininet/nf-wininet-internetconnecta)                         | [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect)                                                                                                                                                               | Il valore di contesto viene impostato [**con WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) o [**WinHttpSetOption.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) Le opzioni di richiesta vengono impostate [**con WinHttpOpenRequest.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) Le credenziali utente vengono impostate con [**WinHttpSetCredentials.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials)                                 |
| [**InternetUrl**](/windows/desktop/api/wininet/nf-wininet-internetcrackurla)                       | [**WinHttpUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl)                                                                                                                                                             | Comportamento opposto del flag ESCAPE ICU: con InternetUrl , questo flag fa sì che le sequenze di escape (%xx) siano convertite in caratteri, ma con \_ [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl), fa sì che i caratteri che devono essere preceduti da caratteri di escape in una richiesta HTTP siano convertiti in sequenze di escape. [](/windows/desktop/api/wininet/nf-wininet-internetcrackurla) |
| [**InternetCreateUrl**](/windows/desktop/api/wininet/nf-wininet-internetcreateurla)                     | [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl)                                                                                                                                                           | Nessuno.                                                                                                                                                                                                                                                                                                                                |
| [**InternetErrorDlg**](/windows/desktop/api/wininet/nf-wininet-interneterrordlg)                       | Nessun equivalente                                                                                                                                                                                          | Poiché WinHTTP è destinato alle applicazioni lato server, non implementa alcuna interfaccia utente.                                                                                                                                                                                                                                   |
| [**InternetGetCookie**](/windows/desktop/api/wininet/nf-wininet-internetgetcookiea)                     | Nessun equivalente                                                                                                                                                                                          | WinHTTP non rende persistenti i dati tra le sessioni e non può accedere ai cookie WinINet.                                                                                                                                                                                                                                                    |
| [**InternetApri**](/windows/desktop/api/wininet/nf-wininet-internetopena)                               | [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen)                                                                                                                                                                     | Nessuno.                                                                                                                                                                                                                                                                                                                                |
| [**Internetopenurl**](/windows/desktop/api/wininet/nf-wininet-internetopenurla)                         | [**WinHttpConnect,**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) [**WinHttpOpenRequest,**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) [**WinHttpSendRequest,**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) | Questa funzionalità è disponibile nelle funzioni WinHTTP elencate.                                                                                                                                                                                                                                                                     |
| [**InternetQueryDataAvailable**](/windows/desktop/api/wininet/nf-wininet-internetquerydataavailable)   | [**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable)                                                                                                                                         | Nessun parametro riservato.                                                                                                                                                                                                                                                                                                              |
| [**InternetQueryOption**](/windows/desktop/api/wininet/nf-wininet-internetqueryoptiona)                 | [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)                                                                                                                                                       | WinHTTP offre un set di opzioni diverso da WinINet. Per altre informazioni e opzioni offerte da WinHTTP, vedere [**Flag di opzione.**](option-flags.md)                                                                                                                                                                               |
| [**InternetReadFile**](/windows/desktop/api/wininet/nf-wininet-internetreadfile)                       | [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata)                                                                                                                                                             | Nessuno.                                                                                                                                                                                                                                                                                                                                |
| [**InternetReadFileEx**](/windows/desktop/api/wininet/nf-wininet-internetreadfileexa)                   | [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata)                                                                                                                                                             | Anziché una struttura , il buffer è un'area di memoria indirizzata con un puntatore .                                                                                                                                                                                                                                                  |
| [**Internetsetoption**](/windows/desktop/api/wininet/nf-wininet-internetsetoptiona)                     | [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)                                                                                                                                                           | Nessuno.                                                                                                                                                                                                                                                                                                                                |
| [**InternetSetStatusCallback**](/windows/desktop/api/wininet/nf-wininet-internetsetstatuscallback)     | [**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback)                                                                                                                                           | Per altre informazioni, vedere "Gestione diversa delle richieste asincrone" in questo argomento.                                                                                                                                                                                                                                               |
| [**InternetTimeFromSystemTime**](/windows/desktop/api/wininet/nf-wininet-internettimefromsystemtime)   | [**WinHttpTimeFromSystemTime**](/windows/desktop/api/Winhttp/nf-winhttp-winhttptimefromsystemtime)                                                                                                                                         | Nessuno.                                                                                                                                                                                                                                                                                                                                |
| [**InternetTimeToSystemTime**](/windows/desktop/api/wininet/nf-wininet-internettimetosystemtime)       | [**WinHttpTimeToSystemTime**](/windows/desktop/api/Winhttp/nf-winhttp-winhttptimetosystemtime)                                                                                                                                             | Nessuno.                                                                                                                                                                                                                                                                                                                                |
| [**InternetWriteFile**](/windows/desktop/api/wininet/nf-wininet-internetwritefile)                     | [**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata)                                                                                                                                                           | Nessuno.                                                                                                                                                                                                                                                                                                                                |



 

## <a name="different-handling-of-asynchronous-requests"></a>Gestione diversa delle richieste asincrone

Tenere presente che in WinINet e WinHTTP alcune funzioni possono completare richieste asincrone in modo sincrono o asincrono. L'applicazione deve gestire entrambe le situazioni. Esistono differenze significative nel modo in cui WinINet e WinHTTP gestiscono queste funzioni potenzialmente asincrone.

Wininet

-   Completamento sincrono: se una chiamata di funzione WinINet potenzialmente asincrona viene completata in modo sincrono, i parametri OUT della funzione restituiscono i risultati dell'operazione. Quando si verifica un errore, recuperare il codice di errore chiamando [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) dopo la chiamata alla funzione WinINet.

-   Completamento asincrono: se una chiamata di funzione potenzialmente asincrona viene completata in modo asincrono, i risultati dell'operazione e gli eventuali errori sono accessibili nella funzione di callback. La funzione di callback viene eseguita su un thread di lavoro, non sul thread che ha eseguito la chiamata di funzione iniziale.

In altre parole, l'applicazione deve duplicare la logica per gestire i risultati di queste operazioni in due posizioni: sia immediatamente dopo la chiamata di funzione che nella funzione di callback.

WinHTTP semplifica questo modello consentendo di implementare la logica operativa solo nella funzione di callback, che riceve una notifica di completamento indipendentemente dal fatto che l'operazione sia stata completata in modo sincrono o asincrono. Quando l'operazione asincrona è abilitata, i parametri OUT delle funzioni WinHTTP non restituiscono dati significativi e devono essere impostati su **NULL.**

L'unica differenza significativa tra il completamento asincrono e sincrono in WinHTTP, dal punto di vista dell'applicazione, è la posizione in cui viene eseguita la funzione di callback.

WinHTTP

-   Completamento sincrono: quando un'operazione viene completata in modo sincrono, i risultati vengono restituiti in una funzione di callback che viene eseguita nello stesso thread della chiamata di funzione originale.

-   Completamento asincrono: quando un'operazione viene completata in modo asincrono, i risultati vengono restituiti in una funzione di callback eseguita in un thread di lavoro.

Anche se la maggior parte degli errori può essere gestita interamente all'interno della funzione di callback, le applicazioni WinHTTP devono comunque essere preparate per la restituzione di **FALSE** da parte di una funzione a causa di UN ERRORE INVALID PARAMETER o di un altro errore simile recuperato chiamando \_ \_ [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

A differenza di WinINet, che può eseguire più operazioni asincrone contemporaneamente, WinHTTP applica un criterio di un'operazione asincrona in sospeso per ogni handle di richiesta. Se un'operazione è in sospeso e viene chiamata un'altra funzione WinHTTP, la seconda funzione ha esito negativo e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce ERROR \_ INVALID \_ OPERATION.

WinHTTP semplifica questo modello consentendo di implementare la logica operativa solo nella funzione di callback, che riceve una notifica di completamento indipendentemente dal fatto che l'operazione sia stata completata in modo sincrono o asincrono. Quando l'operazione asincrona è abilitata, i parametri OUT delle funzioni WinHTTP non restituiscono dati significativi e devono essere impostati su **NULL.**

## <a name="differences-in-winhttp-callback-notifications"></a>Differenze nelle notifiche di callback WinHTTP

La funzione di callback dello stato riceve aggiornamenti sullo stato delle operazioni tramite flag di notifica. In WinHTTP le notifiche vengono selezionate usando *il parametro dwNotificationFlags* della [**funzione WinHttpSetStatusCallback.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback) Usare il flag **WINHTTP \_ CALLBACK FLAG ALL \_ \_ \_ NOTIFICATIONS** per ricevere una notifica di tutti gli aggiornamenti dello stato.

Le notifiche che indicano che una determinata operazione è stata completata vengono chiamate notifiche di completamento o solo completamenti. In WinINet, ogni volta che la funzione di callback riceve un completamento, il *parametro lpvStatusInformation* contiene una [**struttura INTERNET \_ ASYNC \_ RESULT.**](/windows/desktop/api/wininet/ns-wininet-internet_async_result) In WinHTTP questa struttura non è disponibile per tutti i completamenti. È importante esaminare la pagina di riferimento per [**WINHTTP \_ STATUS \_ CALLBACK,**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback)che contiene informazioni sulle notifiche e sul tipo di dati previsto per ognuna.

In WinHTTP un singolo completamento, **WINHTTP \_ CALLBACK STATUS \_ REQUEST \_ \_ ERROR,** indica che un'operazione non è riuscita. Tutti gli altri completamenti indicano un'operazione riuscita.

Sia WinINet che WinHTTP usano un valore di contesto definito dall'utente per passare informazioni dal thread principale alla funzione di callback di stato, che può essere eseguita in un thread di lavoro. In WinINet il valore di contesto usato dalla funzione di callback dello stato viene impostato chiamando una delle diverse funzioni. In WinHTTP il valore di contesto viene impostato solo con [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) [**o WinHttpSetOption.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) Per questo scopo, è possibile che in WinHTTP venga eseguita una notifica prima dell'impostazione di un valore di contesto. Se la funzione di callback riceve una notifica prima dell'impostazione del valore di contesto, l'applicazione deve essere preparata a ricevere **NULL** nel *parametro dwContext* della funzione di callback.

## <a name="authentication-differences"></a>Differenze di autenticazione

In WinINet le credenziali utente vengono impostate chiamando la [**funzione InternetSetOption,**](/windows/desktop/api/wininet/nf-wininet-internetsetoptiona) usando codice simile a quello fornito nell'esempio di codice seguente.

``` syntax
// Use the WinINet InternetSetOption function to set the 
// user credentials to the user name contained in strUsername 
// and the password to the contents of strPassword.
       
InternetSetOption( hRequest, INTERNET_OPTION_PROXY_USERNAME, 
                   strUsername, strlen(strUsername) + 1 );

InternetSetOption( hRequest, INTERNET_OPTION_PROXY_PASSWORD, 
                   strPassword, strlen(strPassword) + 1 );
```

Per motivi di compatibilità, le credenziali utente possono essere impostate in modo analogo in WinHTTP usando la [**funzione WinHttpSetOption,**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) ma questa operazione non è consigliata perché può rappresentare una vulnerabilità di sicurezza.

Quando invece un'applicazione riceve un codice di stato 401 in WinHTTP, il metodo consigliato per impostare le credenziali è identificare prima uno schema di autenticazione usando [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes) e, in secondo luogo, impostare le credenziali [**usando WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials). Nell'esempio di codice seguente viene illustrato come eseguire questa operazione.

``` syntax
DWORD dwSupportedSchemes;
DWORD dwPrefered;
DWORD dwTarget;

// Obtain the supported and first schemes.
WinHttpQueryAuthSchemes( hRequest, &dwSupportedSchemes, &dwPrefered, &dwTarget );

// Set the credentials before resending the request.
WinHttpSetCredentials( hRequest, dwTarget, dwPrefered, strUsername, strPassword, NULL );
```

Poiché non esiste alcun equivalente a [**InternetErrorDlg**](/windows/desktop/api/wininet/nf-wininet-interneterrordlg) in WinHTTP, le applicazioni che ottengono credenziali tramite un'interfaccia utente devono fornire la propria interfaccia.

A differenza di WinINet, WinHTTP non memorizza le password nella cache. È necessario specificare credenziali utente valide per ogni richiesta.

WinHTTP non supporta lo schema DPA (Distributed Password Authentication) supportato da WinINet. WinHTTP, tuttavia, supporta Microsoft Passport 1.4. Per altre informazioni sull'uso dell'autenticazione Passport in WinHTTP, vedere [Passport Authentication in WinHTTP](passport-authentication-in-winhttp.md).

WinHTTP non si basa sulle impostazioni Internet Explorer per determinare i criteri di accesso automatico. I criteri di accesso automatico vengono invece impostati con [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption). Per altre informazioni sull'autenticazione in WinHTTP, inclusi i criteri di accesso automatico, vedere [Autenticazione in WinHTTP](authentication-in-winhttp.md).

## <a name="differences-in-secure-http-transactions"></a>Differenze nelle transazioni HTTP protette

In WinINet avviare una sessione protetta usando [**HttpOpenRequest**](/windows/desktop/api/wininet/nf-wininet-httpopenrequesta) o [**InternetConnect,**](/windows/desktop/api/wininet/nf-wininet-internetconnecta)ma in WinHTTP è necessario chiamare [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) usando il flag **WINHTTP \_ FLAG \_ SECURE.**

In una transazione HTTP sicura, i certificati server possono essere usati per autenticare un server nel client. In WinINet, se un certificato del server contiene errori, [**HttpSendRequest**](/windows/desktop/api/wininet/nf-wininet-httpsendrequesta) ha esito negativo e fornisce informazioni dettagliate sugli errori del certificato.

In WinHttp gli errori del certificato server vengono gestiti in base alla versione, come indicato di seguito:

-   A partire da WinHttp 5.1, se un certificato server ha esito negativo o contiene errori, la chiamata a [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) segnala un ERRORE SICURO DI STATO CALLBACK **WINHTTP \_ \_ \_ \_** nella funzione di callback. Se l'errore generato da **WinHttpSendRequest** viene ignorato, le chiamate successive [**a WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) hanno esito negativo e viene restituito un errore \_ ERROR WINHTTP OPERATION \_ \_ CANCELLED.
-   In WinHTTP 5.0 gli errori nei certificati server non causano, per impostazione predefinita, l'esito negativo di una richiesta. Gli errori vengono invece segnalati nella funzione di callback con la **notifica WINHTTP \_ CALLBACK STATUS \_ SECURE \_ \_ FAILURE.**

In alcune piattaforme precedenti WinINet supportava i protocolli PCT (Private Communication Technology) e/o Fortezza, anche se non Windows XP.

WinHTTP non supporta i protocolli PCT e Fortezza su qualsiasi piattaforma e si basa invece su Secure Sockets Layer (SSL) 2.0, SSL 3.0 o Transport Layer Security (TLS) 1.0.

 

 
