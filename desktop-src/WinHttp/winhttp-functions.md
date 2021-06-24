---
description: Questo argomento identifica le funzioni fornite da WinHTTP.
ms.assetid: dcb56d5d-ed0d-49bb-95bf-940a49c033f1
title: Funzioni WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf5f9db8fcde5589a86556111bec6df3b2b18c76
ms.sourcegitcommit: 749dea42142dec076d41a8f26cb57ae8db46e848
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/24/2021
ms.locfileid: "112587746"
---
# <a name="winhttp-functions"></a>Funzioni WinHTTP

WinHTTP offre le funzioni seguenti:

<dl> <dt>

[**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)
</dt> <dd>

Aggiunge una o più intestazioni di richiesta HTTP all'handle della richiesta HTTP.

</dd> <dt>

[**WinHttpCheckPlatform**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcheckplatform)
</dt> <dd>

Determina se la piattaforma corrente è supportata da WinHTTP.

</dd> <dt>

[**WinHttpCloseHandle**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpclosehandle)
</dt> <dd>

Chiude un singolo [handle HINTERNET.](hinternet-handles-in-winhttp.md)

</dd> <dt>

[**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect)
</dt> <dd>

Specifica il server di destinazione iniziale di una richiesta HTTP.

</dd> <dt>

[**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl)
</dt> <dd>

Separa un URL nelle relative parti del componente, ad esempio il nome host e il percorso.

</dd> <dt>

[**WinHttpCreateProxyResolver**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateproxyresolver)
</dt> <dd>

Crea un handle per l'uso [**da parte di WinHttpGetProxyForUrlEx.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex)

</dd> <dt>

[**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl)
</dt> <dd>

Crea un URL dalle parti del componente, ad esempio il nome host e il percorso.

</dd> <dt>

[**WinHttpDetectAutoProxyConfigUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl)
</dt> <dd>

Trova l'URL per il file pac (Proxy Auto-Configuration). Questa funzione segnala l'URL del file PAC, ma non scarica il file.

</dd> <dt>

[**WinHttpFreeProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpfreeproxyresult)
</dt> <dd>

Libera i dati recuperati da una chiamata precedente a [**WinHttpGetProxyResult.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult)

</dd> <dt>

[**WinHttpFreeQueryConnectionGroupResult**](/windows/win32/api/Winhttp/nf-winhttp-winhttpfreequeryconnectiongroupresult)
</dt> <dd>

Libera la memoria allocata da una chiamata precedente a [WinHttpQueryConnectionGroup.](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryconnectiongroup)

</dd> <dt>

[**WinHttpGetDefaultProxyConfiguration**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetdefaultproxyconfiguration)
</dt> <dd>

Recupera la configurazione del proxy WinHTTP predefinita dal Registro di sistema.

</dd> <dt>

[**WinHTTPGetIeProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser)
</dt> <dd>

Ottiene la configurazione Internet Explorer proxy (IE) per l'utente corrente.

</dd> <dt>

[**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl)
</dt> <dd>

Recupera le informazioni proxy per l'URL specificato.

</dd> <dt>

[**WinHttpGetProxyForUrlEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex)
</dt> <dd>

Recupera le informazioni proxy per l'URL specificato.

</dd> <dt>

[**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult)
</dt> <dd>

Recupera i risultati di una chiamata a [**WinHttpGetProxyForUrlEx.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex)

</dd> <dt>

[**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen)
</dt> <dd>

Inizializza l'uso delle funzioni WinHTTP da parte di un'applicazione.

</dd> <dt>

[**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)
</dt> <dd>

Crea un handle di richiesta HTTP.

</dd> <dt>

[**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes)
</dt> <dd>

Restituisce gli schemi di autorizzazione supportati dal server.

</dd> <dt>

[**WinHttpQueryConnectionGroup**](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryconnectiongroup)
</dt> <dd>

Recupera una descrizione dello stato corrente delle connessioni di WinHttp.

</dd> <dt>

[**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable)
</dt> <dd>

Restituisce il numero di byte di dati immediatamente disponibili per la lettura [**con WinHttpReadData.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata)

</dd> <dt>

[**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders)
</dt> <dd>

Recupera le informazioni di intestazione associate a una richiesta HTTP.

</dd> <dt>

[**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)
</dt> <dd>

Esegue una query su un'opzione Internet sull'handle specificato.

</dd> <dt>

[**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata)
</dt> <dd>

Legge i dati da un handle aperto dalla [**funzione WinHttpOpenRequest.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)

</dd> <dt>

[**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse)
</dt> <dd>

Termina una richiesta HTTP avviata da [**WinHttpSendRequest.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)

</dd> <dt>

[**WinHttpResetAutoProxy**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpresetautoproxy)
</dt> <dd>

Reimposta il proxy automatico.

</dd> <dt>

[**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)
</dt> <dd>

Invia la richiesta specificata al server HTTP.

</dd> <dt>

[**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials)
</dt> <dd>

Passa le credenziali di autorizzazione necessarie al server.

</dd> <dt>

[**WinHttpSetDefaultProxyConfiguration**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetdefaultproxyconfiguration)
</dt> <dd>

Imposta la configurazione predefinita del proxy WinHTTP nel Registro di sistema.

</dd> <dt>

[**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)
</dt> <dd>

Imposta un'opzione Internet.

</dd> <dt>

[**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback)
</dt> <dd>

Configura una funzione di callback che WinHTTP può chiamare quando viene effettuato lo stato di avanzamento durante un'operazione.

</dd> <dt>

[**WinHttpSetTimeouts**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts)
</dt> <dd>

Imposta i vari timeout coinvolti nelle transazioni HTTP.

</dd> <dt>

[**WinHttpTimeFromSystemTime**](/windows/desktop/api/Winhttp/nf-winhttp-winhttptimefromsystemtime)
</dt> <dd>

Formatta una data e un'ora in base alla specifica HTTP versione 1.0.

</dd> <dt>

[**WinHttpTimeToSystemTime**](/windows/desktop/api/Winhttp/nf-winhttp-winhttptimetosystemtime)
</dt> <dd>

Accetta una stringa di data/ora HTTP e la converte in [**una struttura SYSTEMTIME.**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)

</dd> <dt>

[**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata)
</dt> <dd>

Scrive i dati della richiesta in un server HTTP.

</dd> <dt>

[**WinHttpWebSocketClose**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose)
</dt> <dd>

Chiude una connessione WebSocket.

</dd> <dt>

[**WinHttpWebSocketCompleteUpgrade**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketcompleteupgrade)
</dt> <dd>

Completa un handshake WebSocket avviato da [**WinHttpSendRequest.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)

</dd> <dt>

[**WinHttpWebSocketQueryCloseStatus**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketqueryclosestatus)
</dt> <dd>

Ottiene lo stato di chiusura inviato da un server.

</dd> <dt>

[**WinHttpWebSocketReceive**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketreceive)
</dt> <dd>

Riceve dati da una connessione WebSocket.

</dd> <dt>

[**WinHttpWebSocketSend**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketsend)
</dt> <dd>

Invia dati tramite una connessione WebSocket.

</dd> <dt>

[**WinHttpWebSocketShutdown**](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketshutdown)
</dt> <dd>

Invia un frame di chiusura a una connessione WebSocket.

</dd> </dl>

 

 
