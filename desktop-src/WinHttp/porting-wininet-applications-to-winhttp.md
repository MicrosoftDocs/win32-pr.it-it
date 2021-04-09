---
description: I servizi HTTP di Microsoft Windows (WinHTTP) sono destinati a applicazioni server di livello intermedio e back-end che richiedono l'accesso a uno stack client HTTP.
ms.assetid: 5b0cf321-8f69-4526-a628-e6ca0f9d4a58
title: Porting di applicazioni WinINet a WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f64c4ecc825934d32b1d363f010bd04e1484428
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968552"
---
# <a name="porting-wininet-applications-to-winhttp"></a>Porting di applicazioni WinINet a WinHTTP

I servizi HTTP di Microsoft Windows (WinHTTP) sono destinati a applicazioni server di livello intermedio e back-end che richiedono l'accesso a uno stack client HTTP. [Microsoft Windows Internet (WinInet)](winhttp-start-page.md) fornisce uno stack client HTTP per le applicazioni client, nonché l'accesso ai protocolli File Transfer Protocol (FTP), SOCKSv4 e gopher. Questa panoramica può essere utile per determinare se il porting delle applicazioni WinINet a WinHTTP sarebbe vantaggioso. Vengono inoltre descritti i requisiti di conversione specifici.

-   [Aspetti da considerare prima di trasferire l'applicazione WinINet](#things-to-consider-before-porting-your-wininet-application)
-   [Equivalenti WinHTTP a funzioni WinINet](#winhttp-equivalents-to-wininet-functions)
-   [Gestione diversa delle richieste asincrone](#different-handling-of-asynchronous-requests)
-   [Differenze nelle notifiche di callback WinHTTP](#differences-in-winhttp-callback-notifications)
-   [Differenze di autenticazione](#authentication-differences)
-   [Differenze nelle transazioni HTTP protette](#differences-in-secure-http-transactions)

## <a name="things-to-consider-before-porting-your-wininet-application"></a>Aspetti da considerare prima di trasferire l'applicazione WinINet

Provare a trasferire l'applicazione WinINet a WinHTTP se l'applicazione può trarre vantaggio da:

-   Stack client HTTP indipendente dal server.
-   Utilizzo dello stack ridotto a icona.
-   Scalabilità di un'applicazione server.
-   Meno dipendenze dalle API correlate alla piattaforma.
-   Supporto per la rappresentazione del thread.
-   Stack HTTP adatto ai servizi.
-   Accesso all'oggetto [**WinHttpRequest**](winhttprequest.md) di scripting.

Non considerare la possibilità di trasferire l'applicazione WinINet a WinHTTP se deve supportare una o più delle seguenti operazioni:

-   Protocollo FTP o gopher dallo stack HTTP.
-   Supporto per il protocollo SOCKSv4 per la comunicazione con i proxy SOCKS.
-   Servizi di connessione remota automatici.

Se si decide di trasferire l'applicazione in WinHTTP, le sezioni seguenti illustrano il processo di conversione.

Per un'applicazione di esempio per WinINet e WinHTTP, confrontare l'esempio AsyncDemo per WinINet con l'esempio AsyncDemo per WinHTTP.

## <a name="winhttp-equivalents-to-wininet-functions"></a>Equivalenti WinHTTP a funzioni WinINet

Nella tabella seguente sono elencate le funzioni WinINet correlate allo stack client HTTP insieme agli equivalenti WinHTTP.

Se l'applicazione richiede funzioni WinINet non elencate, non trasferire l'applicazione in WinHTTP.



| WinINet (funzione)                                                       | Equivalente WinHTTP                                                                                                                                                                                     | Modifiche rilevanti                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**HttpAddRequestHeaders**](/windows/desktop/api/wininet/nf-wininet-httpaddrequestheadersa)             | [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)                                                                                                                                           | Nessuna.                                                                                                                                                                                                                                                                                                                                |
| [**HttpEndRequest**](/windows/desktop/api/wininet/nf-wininet-httpendrequesta)                           | [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse)                                                                                                                                               | Il valore di contesto viene impostato con [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) o [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption). Le opzioni di richiesta sono impostate con [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest). [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) deve essere chiamato dopo l'invio di una richiesta.                      |
| [**HttpOpenRequest**](/windows/desktop/api/wininet/nf-wininet-httpopenrequesta)                         | [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)                                                                                                                                                       | Il valore di contesto viene impostato con [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) o [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption).                                                                                                                                                                                                      |
| [**HttpQueryInfo**](/windows/desktop/api/wininet/nf-wininet-httpqueryinfoa)                             | [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders)                                                                                                                                                     | Nessuna.                                                                                                                                                                                                                                                                                                                                |
| [**HttpSendRequest**](/windows/desktop/api/wininet/nf-wininet-httpsendrequesta)                         | [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)                                                                                                                                                       | Il valore di contesto può essere impostato con [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).                                                                                                                                                                                                                                                  |
| [**HttpSendRequestEx**](/windows/desktop/api/wininet/nf-wininet-httpsendrequestexa)                     | [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)                                                                                                                                                       | Impossibile fornire i buffer.                                                                                                                                                                                                                                                                                                          |
| [**InternetCanonicalizeUrl**](/windows/desktop/api/wininet/nf-wininet-internetcanonicalizeurla)         | Nessun equivalente                                                                                                                                                                                          | Gli URL vengono ora inseriti in formato canonico in [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest).                                                                                                                                                                                                                                              |
| [**InternetCheckConnection**](/windows/desktop/api/wininet/nf-wininet-internetcheckconnectiona)         | Nessun equivalente                                                                                                                                                                                          | Non implementato in WinHTTP.                                                                                                                                                                                                                                                                                                          |
| [**InternetCloseHandle**](/windows/desktop/api/wininet/nf-wininet-internetclosehandle)                 | [**WinHttpCloseHandle**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpclosehandle)                                                                                                                                                       | La chiusura di un handle padre in WinHTTP non chiude in modo ricorsivo gli handle figlio.                                                                                                                                                                                                                                                         |
| [**InternetCombineUrl**](/windows/desktop/api/wininet/nf-wininet-internetcombineurla)                   | Nessun equivalente                                                                                                                                                                                          | Gli URL possono essere assemblati con la funzione [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) .                                                                                                                                                                                                                                                |
| [**InternetConfirmZoneCrossing**](/windows/desktop/api/wininet/nf-wininet-internetconfirmzonecrossing) | Nessun equivalente                                                                                                                                                                                          | Non implementato in WinHTTP.                                                                                                                                                                                                                                                                                                          |
| [**InternetConnect**](/windows/desktop/api/wininet/nf-wininet-internetconnecta)                         | [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect)                                                                                                                                                               | Il valore di contesto viene impostato con [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) o [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption). Le opzioni di richiesta sono impostate con [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest). Le credenziali utente sono impostate con [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials).                                 |
| [**InternetCrackUrl**](/windows/desktop/api/wininet/nf-wininet-internetcrackurla)                       | [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl)                                                                                                                                                             | Comportamento opposto del flag di \_ escape di ICU: con [**InternetCrackUrl**](/windows/desktop/api/wininet/nf-wininet-internetcrackurla), questo flag fa in modo che le sequenze di escape (% XX) vengano convertite in caratteri, ma con [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl), i caratteri che devono essere preceduti da un carattere di escape in una richiesta HTTP devono essere convertiti in sequenze di escape. |
| [**InternetCreateUrl**](/windows/desktop/api/wininet/nf-wininet-internetcreateurla)                     | [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl)                                                                                                                                                           | Nessuna.                                                                                                                                                                                                                                                                                                                                |
| [**InternetErrorDlg**](/windows/desktop/api/wininet/nf-wininet-interneterrordlg)                       | Nessun equivalente                                                                                                                                                                                          | Poiché WinHTTP è destinato alle applicazioni lato server, non implementa alcuna interfaccia utente.                                                                                                                                                                                                                                   |
| [**InternetGetCookie**](/windows/desktop/api/wininet/nf-wininet-internetgetcookiea)                     | Nessun equivalente                                                                                                                                                                                          | WinHTTP non rende persistenti i dati tra le sessioni e non può accedere ai cookie WinINet.                                                                                                                                                                                                                                                    |
| [**InternetOpen**](/windows/desktop/api/wininet/nf-wininet-internetopena)                               | [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen)                                                                                                                                                                     | Nessuna.                                                                                                                                                                                                                                                                                                                                |
| [**InternetOpenUrl**](/windows/desktop/api/wininet/nf-wininet-internetopenurla)                         | [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect), [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest), [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest), [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) | Questa funzionalità è disponibile nelle funzioni WinHTTP elencate.                                                                                                                                                                                                                                                                     |
| [**La InternetQueryDataAvailable**](/windows/desktop/api/wininet/nf-wininet-internetquerydataavailable)   | [**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable)                                                                                                                                         | Nessun parametro riservato.                                                                                                                                                                                                                                                                                                              |
| [**InternetQueryOption**](/windows/desktop/api/wininet/nf-wininet-internetqueryoptiona)                 | [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)                                                                                                                                                       | WinHTTP offre un diverso set di opzioni da WinINet. Per ulteriori informazioni e opzioni offerte da WinHTTP, vedere [**flag di opzione**](option-flags.md).                                                                                                                                                                               |
| [**InternetReadFile**](/windows/desktop/api/wininet/nf-wininet-internetreadfile)                       | [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata)                                                                                                                                                             | Nessuna.                                                                                                                                                                                                                                                                                                                                |
| [**InternetReadFileEx**](/windows/desktop/api/wininet/nf-wininet-internetreadfileexa)                   | [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata)                                                                                                                                                             | Anziché una struttura, il buffer è un'area di memoria richiamata con un puntatore.                                                                                                                                                                                                                                                  |
| [**InternetSetOption**](/windows/desktop/api/wininet/nf-wininet-internetsetoptiona)                     | [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)                                                                                                                                                           | Nessuna.                                                                                                                                                                                                                                                                                                                                |
| [**InternetSetStatusCallback**](/windows/desktop/api/wininet/nf-wininet-internetsetstatuscallback)     | [**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback)                                                                                                                                           | Per ulteriori informazioni, vedere la sezione relativa alla gestione diversa delle richieste asincrone in questo argomento.                                                                                                                                                                                                                                               |
| [**InternetTimeFromSystemTime**](/windows/desktop/api/wininet/nf-wininet-internettimefromsystemtime)   | [**WinHttpTimeFromSystemTime**](/windows/desktop/api/Winhttp/nf-winhttp-winhttptimefromsystemtime)                                                                                                                                         | Nessuna.                                                                                                                                                                                                                                                                                                                                |
| [**InternetTimeToSystemTime**](/windows/desktop/api/wininet/nf-wininet-internettimetosystemtime)       | [**WinHttpTimeToSystemTime**](/windows/desktop/api/Winhttp/nf-winhttp-winhttptimetosystemtime)                                                                                                                                             | Nessuna.                                                                                                                                                                                                                                                                                                                                |
| [**InternetWriteFile**](/windows/desktop/api/wininet/nf-wininet-internetwritefile)                     | [**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata)                                                                                                                                                           | Nessuna.                                                                                                                                                                                                                                                                                                                                |



 

## <a name="different-handling-of-asynchronous-requests"></a>Gestione diversa delle richieste asincrone

Tenere presente che in WinINet e WinHTTP alcune funzioni possono completare richieste asincrone in modo sincrono o asincrono. L'applicazione deve gestire una situazione di questo tipo. Esistono differenze significative nel modo in cui WinINet e WinHTTP gestiscono queste funzioni potenzialmente asincrone.

WinINet

-   Completamento sincrono: se una chiamata di funzione WinINet potenzialmente asincrona viene completata in modo sincrono, i parametri OUT della funzione restituiscono i risultati dell'operazione. Quando si verifica un errore, recuperare il codice di errore chiamando [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) dopo la chiamata di funzione WinInet.

-   Completamento asincrono: se una chiamata di funzione potenzialmente asincrona viene completata in modo asincrono, i risultati dell'operazione e gli eventuali errori sono accessibili nella funzione di callback. La funzione di callback viene eseguita su un thread di lavoro, non sul thread che ha effettuato la chiamata di funzione iniziale.

In altre parole, l'applicazione deve duplicare la logica per gestire i risultati di tali operazioni in due posizioni: entrambe immediatamente dopo la chiamata di funzione e nella funzione di callback.

WinHTTP semplifica questo modello consentendo di implementare la logica operativa solo nella funzione di callback, che riceve una notifica di completamento indipendentemente dal fatto che l'operazione sia stata completata in modo sincrono o asincrono. Quando è abilitata l'operazione asincrona, i parametri OUT delle funzioni WinHTTP non restituiscono dati significativi e devono essere impostati su **null**.

L'unica differenza significativa tra il completamento asincrono e sincrono in WinHTTP, dal punto di vista dell'applicazione, è la posizione in cui viene eseguita la funzione di callback.

WinHTTP

-   Completamento sincrono: quando un'operazione viene completata in modo sincrono, i risultati vengono restituiti in una funzione di callback che viene eseguita nello stesso thread della chiamata di funzione originale.

-   Completamento asincrono: quando un'operazione viene completata in modo asincrono, i risultati vengono restituiti in una funzione di callback che viene eseguita in un thread di lavoro.

Anche se la maggior parte degli errori può essere gestita interamente all'interno della funzione di callback, è necessario che le applicazioni WinHTTP siano ancora preparate affinché una funzione restituisca **false** a causa di un errore di \_ parametro non valido \_ o di un altro errore simile recuperato chiamando [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

Diversamente da WinINet, che può eseguire contemporaneamente più operazioni asincrone, WinHTTP impone un criterio di un'operazione asincrona in sospeso per ogni handle di richiesta. Se un'operazione è in sospeso e viene chiamata un'altra funzione WinHTTP, la seconda funzione ha esito negativo e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce l'errore \_ operazione non valida \_ .

WinHTTP semplifica questo modello consentendo di implementare la logica operativa solo nella funzione di callback, che riceve una notifica di completamento indipendentemente dal fatto che l'operazione sia stata completata in modo sincrono o asincrono. Quando è abilitata l'operazione asincrona, i parametri OUT delle funzioni WinHTTP non restituiscono dati significativi e devono essere impostati su **null**.

## <a name="differences-in-winhttp-callback-notifications"></a>Differenze nelle notifiche di callback WinHTTP

La funzione di callback status riceve gli aggiornamenti sullo stato delle operazioni tramite flag di notifica. In WinHTTP le notifiche vengono selezionate utilizzando il parametro *dwNotificationFlags* della funzione [**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback) . Usare il flag di **\_ richiamata WinHTTP per tutte le \_ \_ \_ notifiche** per ricevere notifiche di tutti gli aggiornamenti di stato.

Le notifiche che indicano una determinata operazione sono denominate notifiche di completamento o solo completamenti. In WinINet ogni volta che la funzione di callback riceve un completamento, il parametro *lpvStatusInformation* contiene una struttura di [**\_ \_ risultati asincrona Internet**](/windows/desktop/api/wininet/ns-wininet-internet_async_result) . In WinHTTP questa struttura non è disponibile per tutti i completamenti. È importante esaminare la pagina di riferimento per il [**\_ \_ callback di stato WinHTTP**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback), che contiene informazioni sulle notifiche e il tipo di dati che è possibile prevedere per ognuno di essi.

In WinHTTP, un singolo completamento, **\_ errore di \_ \_ richiesta stato \_ callback WinHTTP**, indica che un'operazione non è riuscita. Tutti gli altri completamenti indicano un'operazione completata correttamente.

Sia WinINet che WinHTTP utilizzano un valore di contesto definito dall'utente per passare informazioni dal thread principale alla funzione di callback dello stato, che può essere eseguita su un thread di lavoro. In WinINet, il valore di contesto usato dalla funzione di callback dello stato viene impostato chiamando una delle diverse funzioni. In WinHTTP, il valore del contesto viene impostato solo con [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) o [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption). Per questo motivo, in WinHTTP è possibile che si verifichi una notifica prima dell'impostazione di un valore di contesto. Se la funzione di callback riceve una notifica prima dell'impostazione del valore di contesto, l'applicazione deve essere pronta a ricevere **null** nel parametro *dwContext* della funzione di callback.

## <a name="authentication-differences"></a>Differenze di autenticazione

In WinINet le credenziali utente vengono impostate chiamando la funzione [**InternetSetOption**](/windows/desktop/api/wininet/nf-wininet-internetsetoptiona) , usando codice simile a quello fornito nell'esempio di codice seguente.

``` syntax
// Use the WinINet InternetSetOption function to set the 
// user credentials to the user name contained in strUsername 
// and the password to the contents of strPassword.
       
InternetSetOption( hRequest, INTERNET_OPTION_PROXY_USERNAME, 
                   strUsername, strlen(strUsername) + 1 );

InternetSetOption( hRequest, INTERNET_OPTION_PROXY_PASSWORD, 
                   strPassword, strlen(strPassword) + 1 );
```

Per motivi di compatibilità, le credenziali utente possono essere impostate in modo analogo in WinHTTP usando la funzione [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) , ma questa operazione non è consigliata perché può comportare una vulnerabilità di sicurezza.

Al contrario, quando un'applicazione riceve un codice di stato 401 in WinHTTP, il metodo consigliato per impostare le credenziali è per prima cosa identificare uno schema di autenticazione usando [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes) e, in secondo luogo, impostare le credenziali usando [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials). Nell'esempio di codice riportato di seguito viene illustrato come eseguire questa operazione.

``` syntax
DWORD dwSupportedSchemes;
DWORD dwPrefered;
DWORD dwTarget;

// Obtain the supported and first schemes.
WinHttpQueryAuthSchemes( hRequest, &dwSupportedSchemes, &dwPrefered, &dwTarget );

// Set the credentials before resending the request.
WinHttpSetCredentials( hRequest, dwTarget, dwPrefered, strUsername, strPassword, NULL );
```

Poiché non esiste un equivalente a [**InternetErrorDlg**](/windows/desktop/api/wininet/nf-wininet-interneterrordlg) in WinHTTP, le applicazioni che ottengono le credenziali tramite un'interfaccia utente devono fornire una propria interfaccia.

Diversamente da WinINet, WinHTTP non memorizza nella cache le password. Per ogni richiesta è necessario specificare le credenziali utente valide.

WinHTTP non supporta lo schema DPA (Distributed Password Authentication) supportato da WinINet. Tuttavia, WinHTTP supporta Microsoft Passport 1,4. Per ulteriori informazioni sull'utilizzo dell'autenticazione Passport in WinHTTP, vedere [autenticazione Passport in WinHTTP](passport-authentication-in-winhttp.md).

WinHTTP non si basa sulle impostazioni di Internet Explorer per determinare il criterio di accesso automatico. Il criterio di accesso automatico viene invece impostato con [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption). Per ulteriori informazioni sull'autenticazione in WinHTTP, inclusi i criteri di accesso automatico, vedere [autenticazione in WinHTTP](authentication-in-winhttp.md).

## <a name="differences-in-secure-http-transactions"></a>Differenze nelle transazioni HTTP protette

In WinINet avviare una sessione protetta usando [**HttpOpenRequest**](/windows/desktop/api/wininet/nf-wininet-httpopenrequesta) o [**InternetConnect**](/windows/desktop/api/wininet/nf-wininet-internetconnecta), ma in WinHTTP è necessario chiamare [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) usando il flag di **\_ \_ sicurezza WinHTTP flag** .

In una transazione HTTP sicura, è possibile usare i certificati del server per autenticare un server per il client. In WinINet, se un certificato del server contiene errori, [**HttpSendRequest**](/windows/desktop/api/wininet/nf-wininet-httpsendrequesta) ha esito negativo e fornisce informazioni dettagliate sugli errori del certificato.

In WinHttp gli errori del certificato del server vengono gestiti in base alla versione come segue:

-   A partire da WinHttp 5,1, se un certificato del server ha esito negativo o contiene errori, la chiamata a [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) segnala un **\_ \_ \_ \_ errore di protezione dello stato di callback WinHTTP** nella funzione di callback. Se l'errore generato da **WinHttpSendRequest** viene ignorato, le chiamate successive a [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) avranno esito negativo e si verificherà un errore di \_ annullamento dell'operazione WinHTTP \_ \_ .
-   In WinHTTP 5,0 gli errori nei certificati del server non consentono, per impostazione predefinita, la mancata riuscita di una richiesta. Al contrario, gli errori vengono segnalati nella funzione di callback con la notifica di **\_ \_ \_ \_ errore di protezione dello stato di callback WinHTTP** .

In alcune piattaforme precedenti, WinINet supportava i protocolli PCT (Private Communication Technology) e/o fortezza, sebbene non sia in Windows XP.

WinHTTP non supporta i protocolli PCT e fortezza su qualsiasi piattaforma, ma si basa su Secure Sockets Layer (SSL) 2,0, SSL 3,0 o Transport Layer Security (TLS) 1,0.

 

 
