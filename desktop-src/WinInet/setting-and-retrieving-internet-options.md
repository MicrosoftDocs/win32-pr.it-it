---
title: Impostazione e recupero delle opzioni Internet
description: In questo argomento viene descritto come impostare e recuperare le opzioni Internet utilizzando le funzioni InternetSetOption e InternetQueryOption.
ms.assetid: b596a4a9-c34a-402a-af76-b930fe5f0901
keywords:
- Impostazione e recupero delle opzioni Internet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 418bf21620cf7b7c4426844c95a39ef1fde04e11
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872830"
---
# <a name="setting-and-retrieving-internet-options"></a>Impostazione e recupero delle opzioni Internet

In questo argomento viene descritto come impostare e recuperare le opzioni Internet utilizzando le funzioni [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) e [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) .

Le opzioni Internet possono essere impostate o recuperate da un handle [**HINTERNET**](appendix-a-hinternet-handles.md) specificato o dalle impostazioni correnti in Microsoft Internet Explorer.

-   [Passaggi di implementazione](#implementation-steps)
    -   [Scelta delle opzioni Internet](#choosing-internet-options)
    -   [Scelta dell'handle HINTERNET](#choosing-the-hinternet-handle)
    -   [Impostazione o recupero delle opzioni](#setting-or-retrieving-the-options)
-   [Ambito dell'handle HINTERNET](#scope-of-hinternet-handle)
-   [Impostazione delle singole opzioni](#setting-individual-options)
-   [Recupero di singole opzioni](#retrieving-individual-options)
    -   [Esempio completo](#complete-sample)
-   [Impostazione delle opzioni di connessione](#setting-connection-options)
-   [Recupero delle opzioni di connessione](#retrieving-connection-options)
-   [Argomenti correlati](#related-topics)

## <a name="implementation-steps"></a>Passaggi di implementazione

Per impostare o recuperare le opzioni Internet, completare le operazioni seguenti:

-   [Scelta delle opzioni Internet](#choosing-internet-options)
-   [Scelta dell'handle HINTERNET](#choosing-the-hinternet-handle)
-   [Impostazione o recupero delle opzioni](#setting-or-retrieving-the-options)

### <a name="choosing-internet-options"></a>Scelta delle opzioni Internet

Poiché sono disponibili numerose opzioni Internet, è importante scegliere le opzioni corrette. Molte opzioni Internet influiscono sul comportamento delle funzioni WinINet e di Internet Explorer:

Ad esempio, è possibile:

-   Gestire l'autenticazione di base del server e del proxy impostando nomi utente e password.
-   Impostare o recuperare la stringa agente utente utilizzata dai server per identificare le funzionalità dell'applicazione client o del browser.
-   Recupera il tipo di handle dell'handle [**HINTERNET**](appendix-a-hinternet-handles.md) specificato.

Per ulteriori informazioni e per un elenco delle opzioni Internet, vedere [**flag di opzione**](option-flags.md).

In Internet Explorer 5 e versioni successive è possibile impostare o recuperare alcune opzioni da una connessione Internet specifica utilizzando [**Internet \_ per ogni \_ \_ \_ elenco**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) di opzioni Conn e le strutture di opzioni Internet [**\_ per \_ conn \_**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) . Per ulteriori informazioni e un elenco di opzioni che è possibile impostare o recuperare da una connessione Internet specifica, vedere il membro **dwOptions** della struttura di [**Internet \_ per ogni \_ \_ opzione conn**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) .

### <a name="choosing-the-hinternet-handle"></a>Scelta dell'handle HINTERNET

L'handle [**HINTERNET**](appendix-a-hinternet-handles.md) usato per impostare o recuperare le opzioni Internet determina l'ambito dell'operazione. Tutti gli handle creati tramite questo handle erediteranno le opzioni impostate in questo handle.

Ad esempio, le applicazioni client che richiedono un proxy con autenticazione, probabilmente non richiedono l'impostazione del nome utente e della password del proxy ogni volta che l'applicazione tenta di accedere a una risorsa Internet. Se tutte le richieste su una determinata connessione vengono gestite dallo stesso proxy, l'impostazione del nome utente e della password del proxy in un tipo di connessione [**HINTERNET**](appendix-a-hinternet-handles.md) handle, ovvero un handle creato da una chiamata a [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta), consentirebbe a qualsiasi chiamata derivata da questo handle **HINTERNET** di utilizzare lo stesso nome utente e la stessa password del proxy. L'impostazione del nome utente e della password del proxy ogni volta che un handle **HINTERNET** viene creato da [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) richiederebbe un sovraccarico aggiuntivo e non necessario. Tenere presente che se l'applicazione utilizza un proxy che richiede l'autenticazione, è necessario impostare le credenziali del proxy per ogni nuova connessione.

### <a name="setting-or-retrieving-the-options"></a>Impostazione o recupero delle opzioni

Quando sono state determinate le opzioni Internet e l'handle [**HINTERNET**](appendix-a-hinternet-handles.md) da usare, recuperare le opzioni Internet. Per impostare o recuperare le opzioni, chiamare [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) o [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).

## <a name="scope-of-hinternet-handle"></a>Ambito dell'handle HINTERNET

L'handle [**HINTERNET**](appendix-a-hinternet-handles.md) usato per impostare o recuperare le opzioni Internet determina le azioni per le quali sono valide le opzioni.

Questi handle hanno tre livelli:

-   L'handle [**HINTERNET**](appendix-a-hinternet-handles.md) radice (creato da una chiamata a [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)) conterrà tutte le opzioni Internet che interessano questa istanza di WinInet.
-   Handle [**HINTERNET**](appendix-a-hinternet-handles.md) che si connettono a un server (creato da una chiamata a [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta))
-   Handle [**HINTERNET**](appendix-a-hinternet-handles.md) associati a una risorsa o a un'enumerazione di risorse in un determinato server.

Oltre ai vari handle [**HINTERNET**](appendix-a-hinternet-handles.md) , un'applicazione può utilizzare anche **null** per impostare o recuperare i valori predefiniti delle opzioni Internet utilizzate da Internet Explorer e dalle funzioni WinInet. Impostazione delle opzioni Internet quando si usa **null** come handle per modificare i valori predefiniti delle opzioni, attualmente archiviate nel registro di sistema. Le applicazioni client non devono utilizzare le funzioni del registro di sistema per modificare i valori predefiniti delle opzioni Internet, perché l'implementazione della modalità di archiviazione delle opzioni può essere modificata in futuro.

La tabella seguente elenca il tipo di handle [**HINTERNET**](appendix-a-hinternet-handles.md) e l'ambito delle opzioni Internet associate.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tipo di handle</th>
<th>Ambito</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>NULL</strong></td>
<td>Impostazioni predefinite delle opzioni per Internet Explorer.</td>
</tr>
<tr class="even">
<td>INTERNET_HANDLE_TYPE_CONNECT_FTP</td>
<td>Impostazioni delle opzioni per la connessione a un server FTP. Queste opzioni influiscono su qualsiasi operazione avviata da questo handle <a href="appendix-a-hinternet-handles.md"><strong>HINTERNET</strong></a> , ad esempio download di file.</td>
</tr>
<tr class="odd">
<td>INTERNET_HANDLE_TYPE_CONNECT_GOPHER</td>
<td>Impostazioni delle opzioni per la connessione a un server gopher. Queste opzioni influiscono su qualsiasi operazione avviata da questo handle <a href="appendix-a-hinternet-handles.md"><strong>HINTERNET</strong></a> , ad esempio download di file.
<blockquote>
[!Note]<br />
Windows XP e Windows Server 2003 R2 e versioni precedenti.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>INTERNET_HANDLE_TYPE_CONNECT_HTTP</td>
<td>Impostazioni delle opzioni per la connessione a un server HTTP. Queste opzioni influiscono su qualsiasi operazione avviata da questo handle <a href="appendix-a-hinternet-handles.md"><strong>HINTERNET</strong></a> , ad esempio download di file.</td>
</tr>
<tr class="odd">
<td>INTERNET_HANDLE_TYPE_FILE_REQUEST</td>
<td>Impostazioni delle opzioni associate alla richiesta di file.</td>
</tr>
<tr class="even">
<td>INTERNET_HANDLE_TYPE_FTP_FILE</td>
<td>Impostazioni delle opzioni associate a questo download di risorsa FTP.</td>
</tr>
<tr class="odd">
<td>INTERNET_HANDLE_TYPE_FTP_FILE_HTML</td>
<td>Impostazioni delle opzioni associate a questo download di risorsa FTP formattato in HTML.</td>
</tr>
<tr class="even">
<td>INTERNET_HANDLE_TYPE_FTP_FIND</td>
<td>Impostazioni delle opzioni associate a questa ricerca di file in un server FTP.</td>
</tr>
<tr class="odd">
<td>INTERNET_HANDLE_TYPE_FTP_FIND_HTML</td>
<td>Impostazioni delle opzioni associate a questa ricerca di file in un server FTP formattato in HTML.</td>
</tr>
<tr class="even">
<td>INTERNET_HANDLE_TYPE_GOPHER_FILE</td>
<td>Impostazioni delle opzioni associate a questo download di risorsa gopher.
<blockquote>
[!Note]<br />
Windows XP e Windows Server 2003 R2 e versioni precedenti.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>INTERNET_HANDLE_TYPE_GOPHER_FILE_HTML</td>
<td>Le impostazioni delle opzioni associate a questo download di risorsa Gopher sono state formattate in HTML.
<blockquote>
[!Note]<br />
Windows XP e Windows Server 2003 R2 e versioni precedenti.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>INTERNET_HANDLE_TYPE_GOPHER_FIND</td>
<td>Impostazioni delle opzioni associate a questa ricerca di file in un server gopher.
<blockquote>
[!Note]<br />
Windows XP e Windows Server 2003 R2 e versioni precedenti.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>INTERNET_HANDLE_TYPE_GOPHER_FIND_HTML</td>
<td>Impostazioni delle opzioni associate a questa ricerca di file in un server gopher formattato in HTML.
<blockquote>
[!Note]<br />
Windows XP e Windows Server 2003 R2 e versioni precedenti.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>INTERNET_HANDLE_TYPE_HTTP_REQUEST</td>
<td>Impostazioni delle opzioni associate a questa richiesta HTTP.</td>
</tr>
<tr class="odd">
<td>INTERNET_HANDLE_TYPE_INTERNET</td>
<td>Impostazioni delle opzioni associate a questa istanza delle funzioni WinINet.</td>
</tr>
</tbody>
</table>



 

## <a name="setting-individual-options"></a>Impostazione delle singole opzioni

Dopo aver determinato le opzioni Internet che si desidera impostare e l'ambito interessato da queste opzioni, l'impostazione delle opzioni Internet non è complessa. È sufficiente chiamare la funzione [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) con l'handle [**HINTERNET**](appendix-a-hinternet-handles.md) desiderato, il flag di opzione Internet e un buffer che contiene le informazioni che si desidera impostare.

Nell'esempio seguente viene illustrato come impostare il nome utente e la password del proxy in un handle [**HINTERNET**](appendix-a-hinternet-handles.md) specificato.


```C++
// strUsername is a string buffer of cchMax characters or less.
// It contains the proxy user name.
size_t cchMax = 80;
size_t cchUserLength, cchPasswordLength;
HRESULT hr = StringCchLength(strUsername, cchMax, &cchUserLength);

if (SUCCEEDED(hr))
{
   // hOpen is the HINTERNET handle created by InternetConnect.
   InternetSetOption(hConnect, INTERNET_OPTION_PROXY_USERNAME,
      strUsername, DWORD(cchUserLength)+1);
}
else
{
   // Insert error handling code here.
}

// strPassword is the string buffer that contains the proxy password.
hr = StringCchLength(strPassword, cchMax, &cchPasswordLength);

InternetSetOption(hOpen, INTERNET_OPTION_PROXY_PASSWORD,
    strPassword, DWORD(cchPasswordLength)+1);
```



## <a name="retrieving-individual-options"></a>Recupero di singole opzioni

È possibile recuperare le opzioni Internet utilizzando la funzione [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) . Per recuperare le opzioni Internet:

1.  Determinare le dimensioni del buffer necessarie per recuperare le informazioni sull'opzione Internet.

    È possibile determinare le dimensioni del buffer usando **null** per l'indirizzo del buffer e passandogli una dimensione del buffer pari a zero.

    ```C++
    DWORD dwSize;
    InternetQueryOption(NULL, INTERNET_OPTION_USER_AGENT, NULL, &dwSize);
    ```

    

    Il valore restituito da [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) è la quantità di memoria necessaria per recuperare le informazioni, in byte.

2.  Allocare una memoria per il buffer.
    ```C++
    char *lpszData;
    lpszData = new char[dwSize];
    ```

    

3.  Recuperare i dati.
    ```C++
    InternetQueryOption( NULL, 
                         INTERNET_OPTION_USER_AGENT,
                         lpszData, &dwSize );
    ```

    

4.  Liberare la memoria.
    ```C++
    delete [] lpszData;
    ```

    

### <a name="complete-sample"></a>Esempio completo

Di seguito è riportato l'esempio completo usato nella sezione precedente. In questo esempio viene illustrato come recuperare la stringa agente utente predefinita.


```C++
// This call determines the required buffer size.
DWORD dwSize;
InternetQueryOption(NULL, INTERNET_OPTION_USER_AGENT, NULL, &dwSize);

// Allocate the necessary memory.
char *lpszData;
lpszData = new char[dwSize];

// Call InternetQueryOption again with the provided buffer.
InternetQueryOption( NULL, 
                     INTERNET_OPTION_USER_AGENT,
                     lpszData, &dwSize );

// Insert code here to use the user agent string data.

// Free the allocated memory.
delete [] lpszData;
```



## <a name="setting-connection-options"></a>Impostazione delle opzioni di connessione

In Internet Explorer 5 e versioni successive, è possibile impostare le opzioni Internet per una connessione specifica. In precedenza, tutte le connessioni condividevano le stesse impostazioni delle opzioni Internet. Per impostare le opzioni per una connessione specifica:

1.  Creare una struttura [**Internet \_ per ogni \_ \_ \_ elenco di opzioni conn**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) .
2.  Allocare la memoria per le singole opzioni Internet che si desidera impostare per la connessione.
3.  Impostare le opzioni in [**Internet \_ per \_ \_**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) le strutture delle opzioni conn.
4.  Impostare le opzioni usando [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).

Nell'esempio di codice seguente viene illustrato come impostare i dati proxy per una connessione LAN.


```C++
BOOL SetConnectionOptions()
{
    INTERNET_PER_CONN_OPTION_LIST list;
    BOOL    bReturn;
    DWORD   dwBufSize = sizeof(list);

    // Fill the list structure.
    list.dwSize = sizeof(list);

    // NULL == LAN, otherwise connectoid name.
    list.pszConnection = NULL;

    // Set three options.
    list.dwOptionCount = 3;
    list.pOptions = new INTERNET_PER_CONN_OPTION[3];

    // Ensure that the memory was allocated.
    if(NULL == list.pOptions)
    {
        // Return FALSE if the memory wasn't allocated.
        return FALSE;
    }

    // Set flags.
    list.pOptions[0].dwOption = INTERNET_PER_CONN_FLAGS;
    list.pOptions[0].Value.dwValue = PROXY_TYPE_DIRECT |
        PROXY_TYPE_PROXY;

    // Set proxy name.
    list.pOptions[1].dwOption = INTERNET_PER_CONN_PROXY_SERVER;
    list.pOptions[1].Value.pszValue = TEXT("https://proxy:80");

    // Set proxy override.
    list.pOptions[2].dwOption = INTERNET_PER_CONN_PROXY_BYPASS;
    list.pOptions[2].Value.pszValue = TEXT("local");

    // Set the options on the connection.
    bReturn = InternetSetOption(NULL,
        INTERNET_OPTION_PER_CONNECTION_OPTION, &list, dwBufSize);

    // Free the allocated memory.
    delete [] list.pOptions;

    return bReturn;
}
```



## <a name="retrieving-connection-options"></a>Recupero delle opzioni di connessione

In Internet Explorer 5 e versioni successive è possibile recuperare le opzioni Internet da una connessione specifica. Per recuperare le opzioni da una particolare connessione:

1.  Creare una struttura [**Internet \_ per ogni \_ \_ \_ elenco di opzioni conn**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) .
2.  Allocare la memoria per le singole opzioni Internet da recuperare dalla connessione.
3.  Specificare le opzioni tramite [**Internet per le strutture di \_ \_ \_ Opzioni conn**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) .
4.  Recuperare le opzioni usando [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).
5.  Usare i dati di opzione.
6.  Liberare la memoria, allocata per conservare i dati delle opzioni, usando la funzione [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) .

> [!Note]  
> WinINet non supporta le implementazioni del server. Inoltre, non deve essere utilizzato da un servizio. Per le implementazioni o i servizi del server, usare i [Servizi http di Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione dell'autenticazione](handling-authentication.md)
</dt> <dt>

[Handle HINTERNET](appendix-a-hinternet-handles.md)
</dt> </dl>

 

