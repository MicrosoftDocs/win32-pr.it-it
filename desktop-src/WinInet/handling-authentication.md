---
title: Gestione dell'autenticazione
description: Alcuni proxy e server richiedono l'autenticazione prima di concedere l'accesso alle risorse su Internet.
ms.assetid: f3752031-30d3-4e35-8eae-1d4971b66bc2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36a8eaa38f61f0d97f1f543e0623313aa196aab7
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "104047526"
---
# <a name="handling-authentication"></a>Gestione dell'autenticazione

Alcuni proxy e server richiedono l'autenticazione prima di concedere l'accesso alle risorse su Internet. Le funzioni WinINet supportano l'autenticazione server e proxy per le sessioni HTTP. L'autenticazione dei server FTP deve essere gestita dalla funzione [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) . Attualmente, l'autenticazione del gateway FTP non è supportata.

## <a name="about-http-authentication"></a>Informazioni sull'autenticazione HTTP

Se è richiesta l'autenticazione, l'applicazione client riceve un codice di stato 401, se il server richiede l'autenticazione, o 407, se il proxy richiede l'autenticazione. Con il codice di stato, il proxy o il server invia uno o più, autenticare le intestazioni di risposta: proxy-Authenticate (per l'autenticazione proxy) o WWW-Authenticate (per l'autenticazione server).

Ogni intestazione della risposta di autenticazione contiene uno schema di autenticazione disponibile e un'area di autenticazione. Se sono supportati più schemi di autenticazione, il server restituisce più intestazioni di risposta di autenticazione. Il valore dell'area di autenticazione fa distinzione tra maiuscole e minuscole e definisce uno spazio di protezione sul proxy o sul server. Ad esempio, l'intestazione "WWW-Authenticate: Basic realm =" example "" è un esempio di un'intestazione restituita quando è richiesta l'autenticazione server.

L'applicazione client che ha inviato la richiesta può autenticarsi con l'inclusione di un campo di intestazione dell'autorizzazione con la richiesta. L'intestazione di autorizzazione conterrà lo schema di autenticazione e la risposta appropriata richiesta da tale schema. Ad esempio, l'intestazione "Authorization: Basic <username: password>" viene aggiunta alla richiesta e inviata nuovamente al server se il client ha ricevuto l'intestazione di risposta di autenticazione "WWW-Authenticate: Basic realm =" example "".

Esistono due tipi generali di schemi di autenticazione:

-   Schema di autenticazione di base, in cui il nome utente e la password vengono inviati in testo non crittografato al server.
-   Schemi di richiesta-risposta che consentono un formato di richiesta-risposta.

Lo schema di autenticazione di base è basato sul modello che un client deve autenticarsi con un nome utente e una password per ogni area di autenticazione. Il server di Invia la richiesta se viene inviato nuovamente con un'intestazione di autorizzazione che include un nome utente e una password validi.

Gli schemi di richiesta-risposta consentono un'autenticazione più sicura. Se per una richiesta è necessaria l'autenticazione tramite uno schema di verifica della risposta, il codice di stato appropriato e le intestazioni di autenticazione vengono restituiti al client. Il client deve quindi inviare nuovamente la richiesta con una negoziazione. Il server restituirà un codice di stato appropriato con una richiesta di verifica e il client dovrà quindi inviare nuovamente la richiesta con la risposta appropriata per ottenere il servizio richiesto.

Nella tabella seguente sono elencati gli schemi di autenticazione, il tipo di autenticazione, la DLL che li supporta e una descrizione dello schema.



| Schema                                    | Tipo               | DLL                  | Descrizione                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------------|--------------------|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Di base (testo non crittografato)                         | basic              | Wininet.dll          | Usa una stringa con codifica Base64 che contiene il nome utente e la password.                                                                                                                                                                                                                                                                             |
| Digest                                    | richiesta-risposta | Digest.dll           | Schema di richiesta-risposta che richiede l'uso di un valore nonce, ovvero una stringa di dati specificata dal server. Una risposta valida contiene un checksum del nome utente, la password, il valore nonce specificato, il metodo HTTP e la Uniform Resource Identifier richiesta (URI). Il supporto per l'autenticazione del digest è stato introdotto in Microsoft Internet Explorer 5. |
| NT LAN Manager (NTLM)                     | richiesta-risposta | Winsspi.dll          | Uno schema di richiesta-risposta che basa la richiesta sul nome utente.                                                                                                                                                                                                                                                                             |
| Rete Microsoft (MSN)                   | richiesta-risposta | Msnsspc.dll          | Schema di autenticazione di The Microsoft Network.                                                                                                                                                                                                                                                                                                     |
| Autenticazione della password distribuita | richiesta-risposta | Msapsspc.dll         | Simile all'autenticazione MSN e viene usato anche dalla rete Microsoft.                                                                                                                                                                                                                                                                           |
| Autenticazione passphrase remota (RPA)    | CompuServe         | Rpawinet.dll, da.dll | Schema di autenticazione CompuServe. Per ulteriori informazioni, vedere le [specifiche del meccanismo RPA](https://www.compuserve.com/).                                                                                                                                                                                                    |



 

Per qualsiasi elemento diverso dall'autenticazione di base, è necessario configurare le chiavi del registro di sistema oltre all'installazione della DLL appropriata.

Se è necessaria l'autenticazione, nella chiamata a [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)è necessario usare il flag [Internet \_ \_ Keep \_ Connection](api-flags.md) . Il \_ contrassegno Internet flag \_ Keep \_ Connection è necessario per NTLM e altri tipi di autenticazione per mantenere la connessione durante il completamento del processo di autenticazione. Se la connessione non viene mantenuta, il processo di autenticazione deve essere riavviato con il proxy o il server.

Le funzioni [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) e [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) vengono completate correttamente anche quando è richiesta l'autenticazione. La differenza è che i dati restituiti nei file di intestazione e [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) riceveranno una pagina HTML che informa l'utente del codice di stato.

### <a name="registering-authentication-keys"></a>Registrazione delle chiavi di autenticazione

\_ \_ La preconfigurazione di Internet Open Type \_ esamina i valori del registro di sistema **ProxyEnable**, **ProxyServer** e **ProxyOverride**. Questi valori si trovano in **HKEY \_ Current \_ User** \\ **software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Internet Settings**.

Per gli schemi di autenticazione diversi da Basic è necessario aggiungere una chiave al registro di sistema in **HKEY \_ Local \_ Machine** \\ **software** \\ **Microsoft** \\ **Internet Explorer** \\ **Security**. È necessario impostare un valore **DWORD** , **Flags**, con il valore appropriato. Nell'elenco seguente sono indicati i valori possibili per il valore dei **flag** .

-   Flag di autenticazione plug-in il \_ \_ \_ \_ contesto univoco \_ per \_ Tcpip (value = 0x01)

    Ogni socket TCP/IP (Transmission Control Protocol/Internet Protocol) contiene un contesto diverso. In caso contrario, viene passato un nuovo contesto per ogni modello di area di autenticazione o di URL di blocco.

-   I flag di autenticazione plug-in \_ \_ \_ possono \_ gestire l' \_ interfaccia utente (value = 0x02)

    Questa DLL può gestire il proprio input utente.

-   I flag di autenticazione plug-in \_ \_ \_ possono \_ gestire \_ Nessuna \_ password (valore = 0x04)

    Questa DLL può essere in grado di eseguire un'autenticazione senza richiedere una password all'utente.

-   Flag di autenticazione plug-in \_ \_ \_ senza \_ area di autenticazione (valore = 0x08)

    Questa DLL non usa una stringa dell'area di autenticazione HTTP standard. Qualsiasi dato che sembra essere un'area di autenticazione è costituito da dati specifici dello schema.

-   I flag di autenticazione plug-in \_ \_ \_ Keep \_ Alive \_ non sono \_ necessari (valore = 0x10)

    Questa DLL non richiede una connessione permanente per la relativa sequenza di richiesta-risposta.

Ad esempio, per aggiungere l'autenticazione NTLM, è necessario aggiungere la chiave NTLM a **HKEY \_ Local \_ Machine** \\ **software** \\ **Microsoft** \\ **Internet Explorer** \\ **Security**. In **HKEY \_ Local \_ Machine** \\ **software** \\ **Microsoft** \\ **Internet Explorer** \\ **Security** \\ **NTLM**, è necessario aggiungere il valore stringa **DLLFile** e un valore **DWORD** , **Flags**. **DLLFile** deve essere impostato su Winsspi.dll e i **flag** devono essere impostati su 0x08.

### <a name="server-authentication"></a>Autenticazione del server

Quando un server riceve una richiesta che richiede l'autenticazione, il server restituisce un messaggio di codice di stato 401. Nel messaggio, il server deve includere una o più intestazioni di risposta WWW-Authenticate. Queste intestazioni includono i metodi di autenticazione disponibili per il server. WinINet sceglie il primo metodo che riconosce.

L'autenticazione di base garantisce una sicurezza debole, a meno che il canale non sia stato crittografato per la prima volta con SSL o PCT.

La funzione [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) può essere utilizzata per ottenere i dati del nome utente e della password dall'utente oppure un'interfaccia utente personalizzata può essere progettata per ottenere i dati.

Un'interfaccia personalizzata può usare la funzione [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) per impostare la [ \_ \_ password dell'opzione Internet](option-flags.md) e i valori del [ \_ \_ nome utente dell'opzione Internet](option-flags.md) , quindi inviare nuovamente la richiesta al server.

### <a name="proxy-authentication"></a>Autenticazione proxy

Quando un client tenta di usare un proxy che richiede l'autenticazione, il proxy restituisce un messaggio di codice di stato 407 al client. Nel messaggio, il proxy deve includere una o più intestazioni di risposta Proxy-Authenticate. Queste intestazioni includono i metodi di autenticazione disponibili dal proxy. WinINet sceglie il primo metodo che riconosce.

La funzione [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) può essere usata per ottenere i dati relativi a nome utente e password dall'utente oppure è possibile progettare un'interfaccia utente personalizzata.

Un'interfaccia personalizzata può usare la funzione [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) per impostare la [ \_ \_ \_ password del proxy dell'opzione Internet](option-flags.md) e il [ \_ \_ \_ nome utente del proxy di opzione Internet](option-flags.md) e quindi inviare nuovamente la richiesta al proxy.

Se non è impostato alcun nome utente e password proxy, WinINet tenta di utilizzare il nome utente e la password per il server. Questo comportamento consente ai client di implementare la stessa interfaccia utente personalizzata utilizzata per gestire l'autenticazione del server.

## <a name="handling-http-authentication"></a>Gestione dell'autenticazione HTTP

L'autenticazione HTTP può essere gestita con [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) o con una funzione personalizzata che usa [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) o aggiunge le proprie intestazioni di autenticazione. [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) può esaminare le intestazioni associate a un handle [**HINTERNET**](appendix-a-hinternet-handles.md) per trovare errori nascosti, ad esempio codici di stato da un proxy o un server. [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) può essere utilizzato per impostare il nome utente e la password per il proxy e il server. Per l'autenticazione MSN e DPA, è necessario usare [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) per impostare il nome utente e la password.

Per qualsiasi funzione personalizzata che aggiunge le proprie intestazioni WWW-Authenticate o Proxy-Authenticate, il [ \_ flag Internet \_ nessun \_ ](api-flags.md) flag di autenticazione deve essere impostato per disabilitare l'autenticazione.

Nell'esempio seguente viene illustrato come utilizzare [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) per gestire l'autenticazione HTTP.


```C++
HINTERNET hOpenHandle,  hConnectHandle, hResourceHandle;
DWORD dwError, dwErrorCode;
HWND hwnd = GetConsoleWindow();

hOpenHandle = InternetOpen(TEXT("Example"),
                           INTERNET_OPEN_TYPE_PRECONFIG, 
                           NULL, NULL, 0);

hConnectHandle = InternetConnect(hOpenHandle,
                                 TEXT("www.server.com"), 
                                 INTERNET_INVALID_PORT_NUMBER,
                                 NULL,
                                 NULL, 
                                 INTERNET_SERVICE_HTTP,
                                 0,0);

hResourceHandle = HttpOpenRequest(hConnectHandle, TEXT("GET"),
                                  TEXT("/premium/default.htm"),
                                  NULL, NULL, NULL, 
                                  INTERNET_FLAG_KEEP_CONNECTION, 0);

resend:

HttpSendRequest(hResourceHandle, NULL, 0, NULL, 0);

// dwErrorCode stores the error code associated with the call to
// HttpSendRequest.  

dwErrorCode = hResourceHandle ? ERROR_SUCCESS : GetLastError();

dwError = InternetErrorDlg(hwnd, hResourceHandle, dwErrorCode, 
                           FLAGS_ERROR_UI_FILTER_FOR_ERRORS | 
                           FLAGS_ERROR_UI_FLAGS_CHANGE_OPTIONS |
                           FLAGS_ERROR_UI_FLAGS_GENERATE_DATA,
                           NULL);

if (dwError == ERROR_INTERNET_FORCE_RETRY)
    goto resend;

// Insert code to read the data from the hResourceHandle
// at this point.

```



Nell'esempio, dwErrorCode viene usato per archiviare gli eventuali errori associati alla chiamata a [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta). [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) viene completato correttamente, anche se il proxy o il server richiede l'autenticazione. Quando il \_ flag del \_ filtro dell'interfaccia utente per i flag Error \_ per gli \_ \_ errori viene passato a [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg), la funzione controlla le intestazioni per individuare eventuali errori nascosti. Questi errori nascosti includono qualsiasi richiesta di autenticazione. [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) Visualizza la finestra di dialogo appropriata per richiedere all'utente i dati necessari. I flag \_ dell' \_ interfaccia utente degli errori \_ di flag \_ generano \_ dati e flag \_ errore flag interfaccia utente i flag \_ \_ \_ \_ delle opzioni di modifica devono essere passati anche a [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg), in modo che la funzione costruisca la struttura dei dati appropriata per l'errore e archivia i risultati della finestra di dialogo nell'handle [**HINTERNET**](appendix-a-hinternet-handles.md) .

Nell'esempio di codice riportato di seguito viene illustrato il modo in cui l'autenticazione può essere gestita utilizzando [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).


```C++
HINTERNET hOpenHandle,  hResourceHandle, hConnectHandle;
DWORD dwStatus;
DWORD dwStatusSize = sizeof(dwStatus);
char strUsername[64], strPassword[64];

// Normally, hOpenHandle, hResourceHandle,
// and hConnectHandle need to be properly assigned.

hOpenHandle = InternetOpen(TEXT("Example"),
                           INTERNET_OPEN_TYPE_PRECONFIG,
                           NULL, NULL, 0);
hConnectHandle = InternetConnect(hOpenHandle,
                                 TEXT("www.server.com"),
                                 INTERNET_INVALID_PORT_NUMBER,
                                 NULL,
                                 NULL,
                                 INTERNET_SERVICE_HTTP,
                                 0,0);

hResourceHandle = HttpOpenRequest(hConnectHandle, TEXT("GET"),
                                  TEXT("/premium/default.htm"),
                                  NULL, NULL, NULL,
                                  INTERNET_FLAG_KEEP_CONNECTION,
                                  0);

resend:

HttpSendRequest(hResourceHandle, NULL, 0, NULL, 0);

HttpQueryInfo(hResourceHandle, HTTP_QUERY_FLAG_NUMBER |
              HTTP_QUERY_STATUS_CODE, &dwStatus, &dwStatusSize, NULL);

switch (dwStatus)
{
    // cchUserLength is the length of strUsername and
    // cchPasswordLength is the length of strPassword.
    DWORD cchUserLength, cchPasswordLength;

    case HTTP_STATUS_PROXY_AUTH_REQ: // Proxy Authentication Required
        // Insert code to set strUsername and strPassword.

        // Insert code to safely determine cchUserLength and
        // cchPasswordLength. Insert appropriate error handling code.
        InternetSetOption(hResourceHandle,
                          INTERNET_OPTION_PROXY_USERNAME,
                          strUsername,
                          cchUserLength+1);

        InternetSetOption(hResourceHandle,
                          INTERNET_OPTION_PROXY_PASSWORD,
                          strPassword,
                          cchPasswordLength+1);
        goto resend;
        break;

    case HTTP_STATUS_DENIED:     // Server Authentication Required.
        // Insert code to set strUsername and strPassword.

        // Insert code to safely determine cchUserLength and
        // cchPasswordLength. Insert error handling code as
        // appropriate.
        InternetSetOption(hResourceHandle, INTERNET_OPTION_USERNAME,
                          strUsername, cchUserLength+1);
        InternetSetOption(hResourceHandle, INTERNET_OPTION_PASSWORD,
                          strPassword, cchPasswordLength+1);
        goto resend;
        break;
}

// Insert code to read the data from the hResourceHandle
// at this point.

```



> [!Note]  
> WinINet non supporta le implementazioni del server. Inoltre, non deve essere utilizzato da un servizio. Per le implementazioni o i servizi del server, usare i [Servizi http di Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 