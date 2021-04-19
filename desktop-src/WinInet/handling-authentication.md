---
title: Gestione dell'autenticazione
description: Alcuni proxy e server richiedono l'autenticazione prima di concedere l'accesso alle risorse su Internet.
ms.assetid: f3752031-30d3-4e35-8eae-1d4971b66bc2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e82d8cd93f1010c71560d856793ad06d8bc5d9d5
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380855"
---
# <a name="handling-authentication"></a>Gestione dell'autenticazione

Alcuni proxy e server richiedono l'autenticazione prima di concedere l'accesso alle risorse su Internet. Le funzioni WinINet supportano l'autenticazione server e proxy per le sessioni HTTP. L'autenticazione dei server ftp deve essere gestita dalla [**funzione InternetConnect.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) Attualmente l'autenticazione del gateway FTP non è supportata.

## <a name="about-http-authentication"></a>Informazioni sull'autenticazione HTTP

Se è necessaria l'autenticazione, l'applicazione client riceve un codice di stato 401, se il server richiede l'autenticazione o 407, se il proxy richiede l'autenticazione. Con il codice di stato, il proxy o il server invia una o più intestazioni di risposta di autenticazione: Proxy-Authenticate (per l'autenticazione proxy) o WWW-Authenticate (per l'autenticazione del server).

Ogni intestazione di risposta di autenticazione contiene uno schema di autenticazione disponibile e un'area di autenticazione. Se sono supportati più schemi di autenticazione, il server restituisce più intestazioni di risposta di autenticazione. Il valore dell'area di autenticazione fa distinzione tra maiuscole e minuscole e definisce uno spazio di protezione nel proxy o nel server. Ad esempio, l'intestazione "WWW-Authenticate: Basic Realm="example"" è un esempio di intestazione restituita quando è necessaria l'autenticazione del server.

L'applicazione client che ha inviato la richiesta può autenticarsi includendo un campo di intestazione Authorization con la richiesta. L'intestazione Authorization conterrà lo schema di autenticazione e la risposta appropriata richiesta da tale schema. Ad esempio, l'intestazione "Authorization: Basic" verrà aggiunta alla richiesta e inviata nuovamente al server se il client ha ricevuto l'intestazione di risposta di autenticazione \<username:password> "WWW-Authenticate: Basic Realm="example"".

Esistono due tipi generali di schemi di autenticazione:

-   Schema di autenticazione di base, in cui il nome utente e la password vengono inviati in testo non crittografato al server.
-   Schemi challenge-response, che consentono un formato challenge-response.

Lo schema di autenticazione di base è basato sul modello che un client deve autenticare con un nome utente e una password per ogni area di autenticazione. Il server invia nuovamente la richiesta con un'intestazione Authorization che include un nome utente e una password validi.

Gli schemi challenge-response consentono un'autenticazione più sicura. Se una richiesta richiede l'autenticazione usando uno schema challenge-response, al client vengono restituiti il codice di stato appropriato e le intestazioni Authenticate. Il client deve quindi inviare nuovamente la richiesta con una negoziazione. Il server restituirebbe un codice di stato appropriato con una richiesta di verifica e il client richiederebbe quindi di inviare nuovamente la richiesta con la risposta appropriata per ottenere il servizio richiesto.

Nella tabella seguente sono elencati gli schemi di autenticazione, il tipo di autenticazione, la DLL che li supporta e una descrizione dello schema.



| Schema                                    | Tipo               | DLL                  | Descrizione                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------------|--------------------|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Base (testo non crittografato)                         | basic              | Wininet.dll          | Usa una stringa con codifica Base64 che contiene il nome utente e la password.                                                                                                                                                                                                                                                                             |
| Digest                                    | challenge-response | Digest.dll           | Schema challenge-response che sfida l'uso di un valore nonce (una stringa di dati specificata dal server). Una risposta valida contiene un checksum del nome utente, della password, del valore nonce specificato, del metodo HTTP e dell'URI Uniform Resource Identifier richiesta. Il supporto per l'autenticazione del digest è stato introdotto in Microsoft Internet Explorer 5. |
| NT LAN Manager (NTLM)                     | challenge-response | Winsspi.dll          | Schema challenge-response che basa la richiesta sul nome utente.                                                                                                                                                                                                                                                                             |
| Microsoft Network (MSN)                   | challenge-response | Msnsspc.dll          | The Microsoft Network di autenticazione.                                                                                                                                                                                                                                                                                                     |
| Distributed Password Authentication (DPA) | challenge-response | Msapsspc.dll         | Analogamente all'autenticazione MSN, viene usato anche da Microsoft Network.                                                                                                                                                                                                                                                                           |
| Autenticazione della passphrase remota (RPA)    | Compuserve         | Rpawinet.dll, da.dll | Schema di autenticazione CompuServe. Per altre informazioni, vedere Specifiche [del meccanismo RPA.](https://www.compuserve.com/)                                                                                                                                                                                                    |



 

Per qualsiasi elemento diverso dall'autenticazione di base, le chiavi del Registro di sistema devono essere impostate oltre all'installazione della DLL appropriata.

Se è necessaria l'autenticazione, nella chiamata a [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)deve essere usato il flag [ \_ KEEP \_ \_ CONNECTION](api-flags.md) di INTERNET FLAG . Il flag INTERNET FLAG KEEP CONNECTION è necessario per NTLM e altri tipi di autenticazione per mantenere la connessione durante \_ il completamento del processo di \_ \_ autenticazione. Se la connessione non viene mantenuta, il processo di autenticazione deve essere riavviato con il proxy o il server.

Le [**funzioni InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) [**e HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) vengono completate correttamente anche quando è necessaria l'autenticazione. La differenza è che i dati restituiti nei file di intestazione e [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) riceveranno una pagina HTML che informa l'utente del codice di stato.

### <a name="registering-authentication-keys"></a>Registrazione delle chiavi di autenticazione

INTERNET OPEN TYPE PRECONFIG esamina i valori del Registro \_ \_ di sistema \_ **ProxyEnable,** **ProxyServer** e **ProxyOverride.** Questi valori si trovano in **HKEY \_ CURRENT \_ USER** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** Internet \\ **Settings**.

Per gli schemi di autenticazione diversi da Basic, è necessario aggiungere una chiave al Registro di sistema in **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Internet Explorer** \\ **Security**. Un **valore DWORD,** **Flags,** deve essere impostato con il valore appropriato. L'elenco seguente mostra i valori possibili per il **valore Flags.**

-   PLUGIN \_ AUTH \_ FLAGS UNIQUE CONTEXT PER \_ \_ \_ \_ TCPIP (value=0x01)

    Ogni Transmission Control Protocol/Internet Protocol (TCP/IP) contiene un contesto diverso. In caso contrario, viene passato un nuovo contesto per ogni area di autenticazione o modello di URL di blocco.

-   I \_ FLAG DI AUTENTICAZIONE DEL \_ \_ PLUG-IN \_ POSSONO GESTIRE \_ L'INTERFACCIA UTENTE (value=0x02)

    Questa DLL può gestire il proprio input utente.

-   I \_ FLAG DI AUTENTICAZIONE DEL \_ \_ PLUG-IN POSSONO GESTIRE NESSUN \_ \_ \_ PASSWD (value=0x04)

    Questa DLL potrebbe essere in grado di eseguire un'autenticazione senza richiedere all'utente una password.

-   PLUGIN \_ AUTH \_ FLAGS NO REALM \_ \_ (value=0x08)

    Questa DLL non usa una stringa dell'area di autenticazione HTTP standard. Tutti i dati che sembra essere un'area di autenticazione sono dati specifici dello schema.

-   I \_ FLAG DI AUTENTICAZIONE DEL \_ \_ \_ PLUG-IN \_ KEEP-ALIVE NON SONO OBBLIGATORI \_ (value=0x10)

    Questa DLL non richiede una connessione permanente per la sequenza challenge-response.

Ad esempio, per aggiungere l'autenticazione NTLM, la chiave NTLM deve essere aggiunta a **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Internet Explorer** \\ **Security**. In **HKEY \_ LOCAL \_ MACHINE** SOFTWARE Microsoft Internet Explorer Security NTLM è necessario aggiungere il valore stringa DLLFile e un \\  \\  \\  \\  \\  **valore DWORD,** **Flags.**  **DLLFile** deve essere impostato su Winsspi.dll **e Flags** deve essere impostato su 0x08.

### <a name="server-authentication"></a>Autenticazione del server

Quando un server riceve una richiesta che richiede l'autenticazione, il server restituisce un messaggio di codice di stato 401. In tale messaggio, il server deve includere una o più intestazioni WWW-Authenticate risposta. Queste intestazioni includono i metodi di autenticazione disponibili per il server. WinINet sceglie il primo metodo che riconosce.

L'autenticazione di base offre una sicurezza debole a meno che il canale non sia prima crittografato con SSL o PCT.

La [**funzione InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) può essere usata per ottenere i dati del nome utente e della password dall'utente oppure un'interfaccia utente personalizzata può essere progettata per ottenere i dati.

Un'interfaccia personalizzata può usare la [**funzione InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) per impostare i valori [INTERNET OPTION \_ \_ PASSWORD](option-flags.md) e [INTERNET OPTION \_ \_ USERNAME](option-flags.md) e quindi inviare nuovamente la richiesta al server.

### <a name="proxy-authentication"></a>Autenticazione proxy

Quando un client tenta di usare un proxy che richiede l'autenticazione, il proxy restituisce un messaggio di codice di stato 407 al client. In questo messaggio, il proxy deve includere una o più intestazioni Proxy-Authenticate risposta. Queste intestazioni includono i metodi di autenticazione disponibili dal proxy. WinINet sceglie il primo metodo che riconosce.

La [**funzione InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) può essere usata per ottenere i dati relativi a nome utente e password dall'utente oppure è possibile creare un'interfaccia utente personalizzata.

Un'interfaccia personalizzata può usare la [**funzione InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) per impostare i valori [INTERNET OPTION PROXY \_ \_ \_ PASSWORD](option-flags.md) e [INTERNET OPTION PROXY \_ \_ \_ USERNAME](option-flags.md) e quindi inviare nuovamente la richiesta al proxy.

Se non sono impostati nome utente e password del proxy, WinINet tenta di usare il nome utente e la password per il server. Questo comportamento consente ai client di implementare la stessa interfaccia utente personalizzata usata per gestire l'autenticazione del server.

## <a name="handling-http-authentication"></a>Gestione dell'autenticazione HTTP

L'autenticazione HTTP può essere gestita con [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) o con una funzione personalizzata che usa [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) o aggiunge le proprie intestazioni di autenticazione. [**InternetErrorDlg può**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) esaminare le intestazioni associate a un handle [**HINTERNET**](appendix-a-hinternet-handles.md) per trovare gli errori nascosti, ad esempio i codici di stato da un proxy o un server. [**InternetSetOption può**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) essere usato per impostare il nome utente e la password per il proxy e il server. Per l'autenticazione MSN e DPA, è necessario usare [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) per impostare il nome utente e la password.

Per qualsiasi funzione personalizzata che aggiunge intestazioni WWW-Authenticate o Proxy-Authenticate, il flag [INTERNET \_ FLAG NO \_ \_ AUTH](api-flags.md) deve essere impostato per disabilitare l'autenticazione.

L'esempio seguente illustra come [**usare InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) per gestire l'autenticazione HTTP.


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



Nell'esempio dwErrorCode viene usato per archiviare eventuali errori associati alla chiamata a [**HttpSendRequest.**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) [**HttpSendRequest viene**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) completato correttamente, anche se il proxy o il server richiede l'autenticazione. Quando il flag FLAGS ERROR UI FILTER FOR ERRORS viene passato a \_ \_ \_ \_ \_ [**InternetErrorDlg,**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg)la funzione verifica la presenza di eventuali errori nascosti nelle intestazioni. Questi errori nascosti includono tutte le richieste di autenticazione. [**InternetErrorDlg visualizza**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) la finestra di dialogo appropriata per richiedere all'utente i dati necessari. I flag FLAGS ERROR UI FLAGS GENERATE DATA e FLAGS ERROR UI FLAGS CHANGE OPTIONS devono essere passati anche a InternetErrorDlg, in modo che la funzione costruisca la struttura dei dati appropriata per l'errore e archivi i risultati della finestra di dialogo \_ \_ \_ \_ \_ \_ \_ \_ \_ nell'handle \_ [**HINTERNET.**](appendix-a-hinternet-handles.md) [](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg)

Nell'esempio di codice seguente viene illustrato come gestire l'autenticazione [**tramite InternetSetOption.**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)


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
> WinINet non supporta le implementazioni del server. Inoltre, non deve essere usato da un servizio. Per le implementazioni o i servizi del server usare [i servizi HTTP di Microsoft Windows (WinHTTP).](/windows/desktop/WinHttp/winhttp-start-page)

 

 

 