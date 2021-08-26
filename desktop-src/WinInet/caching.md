---
title: Caching (Windows Internet)
description: Le funzioni WinINet hanno un supporto di memorizzazione nella cache incorporato semplice, ma flessibile.
ms.assetid: 44c268c9-a745-432a-8540-60d7e7d2cb2d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cea485e1c6fc8b2b474d217d940c715b65b45de8f7d211ad37bff9bdd9a4243b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955611"
---
# <a name="caching-windows-internet"></a>Caching (Windows Internet)

Le funzioni WinINet hanno un supporto di memorizzazione nella cache incorporato semplice, ma flessibile. Tutti i dati recuperati dalla rete vengono memorizzati nella cache del disco rigido e recuperati per le richieste successive. L'applicazione può controllare la memorizzazione nella cache in ogni richiesta. Per le richieste HTTP provenienti dal server, viene memorizzata anche la maggior parte delle intestazioni ricevute. Quando una richiesta HTTP viene soddisfatta dalla cache, anche le intestazioni memorizzate nella cache vengono restituite al chiamante. In questo modo il download dei dati è facile, indipendentemente dal fatto che i dati siano provenienti dalla cache o dalla rete.

Le applicazioni devono allocare correttamente un buffer per ottenere i risultati desiderati quando si usano le funzioni di memorizzazione nella cache degli URL permanenti. Per altre informazioni, vedere [Uso dei buffer](appendix-b-using-buffers.md).

## <a name="cache-behavior-during-response-processing"></a>Comportamento della cache durante l'elaborazione della risposta

La cache WinINet è conforme alle direttive di controllo della cache HTTP descritte in RFC 2616. Le direttive di controllo della cache e i flag del set di applicazioni determinano gli elementi che possono essere memorizzati nella cache. Tuttavia, WinINet determina ciò che viene effettivamente memorizzato nella cache in base al criterio seguente:

-   WinINet memorizza nella cache solo le risposte HTTP e FTP.
-   Solo le risposte ben comportate possono essere archiviate da una cache e usate in una risposta a una richiesta successiva. Le risposte con comportamento corretto sono definite come risposte che restituiscono correttamente.
-   Per impostazione predefinita, WinINet memorizza nella cache le risposte riuscite a meno che una direttiva cache-control dal server o un flag definito dall'applicazione denoti in modo specifico che la risposta potrebbe non essere memorizzata nella cache.
-   In generale, le risposte al verbo GET vengono memorizzate nella cache se vengono soddisfatti i requisiti elencati in precedenza. Le risposte ai verbi PUT e POST non vengono memorizzate nella cache in nessun caso.
-   Gli elementi verranno memorizzati nella cache anche quando la cache è piena. Se un elemento aggiunto inserisce la cache oltre il limite di dimensioni, lo scavenger della cache viene pianificato. Per impostazione predefinita, non è garantito che gli elementi rimangano più di 10 minuti nella cache. Per altre informazioni, vedere la sezione [Cache Scavenger](#cache-scavenger) riportata di seguito.
-   Https viene memorizzato nella cache per impostazione predefinita. Questa operazione viene gestita da un'impostazione globale che non può essere sottoposta a override dalle direttive della cache definite dall'applicazione. Per ignorare l'impostazione globale, selezionare l'applet Opzioni Internet nel pannello di controllo e passare alla scheda Avanzate. Selezionare la casella "Non salvare le pagine crittografate su disco" nella sezione "Sicurezza".

## <a name="cache-scavenger"></a>Cache Scavenger

Lo scavenger della cache pulisce periodicamente gli elementi dalla cache. Se un elemento viene aggiunto alla cache e la cache è piena, l'elemento viene aggiunto alla cache e viene pianificato lo scavenger della cache. Se lo scavenger della cache completa un round di scavenging e la cache non ha raggiunto il limite della cache, lo scavenger viene pianificato per un altro round quando viene aggiunto un altro elemento alla cache. In generale, lo scavenger viene pianificato quando un elemento aggiunto inserisce la cache oltre il limite di dimensioni. Per impostazione predefinita, il tempo minimo di memorizzazione nella cache è impostato su 10 minuti, a meno che non venga specificato diversamente in una direttiva cache-control. Quando viene avviato lo scavenger della cache, non è garantito che gli elementi meno recenti siano i primi a essere eliminati dalla cache.

La cache viene condivisa tra tutte le applicazioni WinINet nel computer per lo stesso utente. A partire da Windows Vista e Windows Server 2008 le dimensioni della cache sono impostate su 1/32 delle dimensioni del disco, con una dimensione minima di 8 MB e una dimensione massima di 50 MB.

## <a name="using-flags-to-control-caching"></a>Uso di flag per controllare Caching

I flag di memorizzazione nella cache consentono a un'applicazione di controllare quando e come usa la cache. Questi flag possono essere usati da soli o in combinazione con *il parametro dwFlags* nelle funzioni che accedono a informazioni o risorse su Internet. Per impostazione predefinita, le funzioni archiviano tutti i dati scaricati da Internet.

I flag seguenti possono essere usati per controllare la memorizzazione nella cache.



| Valore                                                                                                                                                  | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**INTERNET \_ FLAG \_ CACHE \_ ASYNC**](api-flags.md)                                                                            | Questo flag non ha alcun effetto.                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**INTERNET \_ FLAG CACHE IN CASO DI ERRORE DI \_ \_ \_ \_ RETE**](api-flags.md)                                                              | Restituisce la risorsa dalla cache se la richiesta di rete per la risorsa ha esito negativo a causa di un errore [ \_ DI REIMPOSTAZIONE \_ \_ ](wininet-errors.md) CONNESSIONE INTERNET o ERRORE IMPOSSIBILE CONNETTERSI A [ \_ INTERNET. \_ \_ ](wininet-errors.md) Questo flag viene usato da [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).                                                                                                              |
| [**INTERNET \_ FLAG \_ DONT \_ CACHE**](api-flags.md)                                                                              | Non memorizza nella cache i dati, in locale o in alcun gateway. Identico al valore preferito, [**INTERNET FLAG NO CACHE \_ \_ \_ \_ WRITE**](api-flags.md).                                                                                                                                                                                                                                                                                 |
|                                                                                                                                                        | Indica che si tratta di un invio di form.                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**INTERNET \_ INVIO \_ DEI MODULI FLAG \_**](api-flags.md)INTERNET FLAG DALLA [**\_ \_ \_ CACHE**](api-flags.md) | Non effettua richieste di rete. Tutte le entità vengono restituite dalla cache. Se l'elemento richiesto non è presente nella cache, viene restituito un errore appropriato, ad esempio ERROR \_ FILE \_ NOT \_ FOUND. Solo la [**funzione InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) usa questo flag.                                                                                                                                                                                                       |
| [**INTERNET \_ FLAG \_ FWD \_ BACK**](api-flags.md)                                                                                  | Indica che la funzione deve usare la copia della risorsa attualmente presente nella cache Internet. La data di scadenza e altre informazioni sulla risorsa non vengono controllate. Se l'elemento richiesto non viene trovato nella cache Internet, il sistema tenta di individuare la risorsa in rete. Questo valore è stato introdotto in Microsoft Internet Explorer 5  ed è associato alle **operazioni** dei pulsanti Avanti e Indietro di Internet Explorer. |
| [**COLLEGAMENTO IPERTESTUALE \_ DEL FLAG \_ INTERNET**](api-flags.md)                                                                                 | Forza il ricaricamento di una risorsa da parte dell'applicazione se non è stata restituita alcuna data e ora dell'ultima modifica quando la risorsa è stata archiviata nella cache.                                                                                                                                                                                                                                                                                                                  |
| [**IL FLAG INTERNET \_ \_ RENDE \_ PERSISTENTE**](api-flags.md)                                                                    | Non più supportata.                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**IL FLAG INTERNET \_ \_ DEVE \_ MEMORIZZARE NELLA CACHE LA \_ RICHIESTA**](api-flags.md)                                                             | Determina la creazione di un file temporaneo se il file non può essere memorizzato nella cache. È identico al valore preferito, [**INTERNET \_ FLAG NEED \_ \_ FILE**](api-flags.md).                                                                                                                                                                                                                                                                            |
| [**FILE NECESSARIO DEL FLAG INTERNET \_ \_ \_**](api-flags.md)                                                                                | Determina la creazione di un file temporaneo se il file non può essere memorizzato nella cache.                                                                                                                                                                                                                                                                                                                                                                                               |
| [**FLAG INTERNET \_ \_ NESSUNA SCRITTURA NELLA \_ \_ CACHE**](api-flags.md)                                                                     | Rifiuta qualsiasi tentativo della funzione di archiviare i dati scaricati da Internet nella cache. Questo flag è necessario se l'applicazione non vuole che le risorse scaricate siano archiviate in locale.                                                                                                                                                                                                                                                               |
| [**INTERFACCIA \_ UTENTE SENZA FLAG INTERNET \_ \_**](api-flags.md)                                                                                        | Disabilita la finestra di dialogo dei cookie. Questo flag può essere usato da [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (solo richieste HTTP).                                                                                                                                                                                                                                                                                          |
| [**INTERNET \_ FLAG \_ OFFLINE**](api-flags.md)                                                                                     | Impedisce all'applicazione di inviare richieste alla rete. Tutte le richieste vengono risolte usando le risorse archiviate nella cache. Se la risorsa non è presente nella cache, viene restituito un errore appropriato, ad esempio \_ ERROR FILE \_ NOT \_ FOUND.                                                                                                                                                                                                                            |
| [**INTERNET \_ FLAG \_ PRAGMA \_ NOCACHE**](api-flags.md)                                                                      | Forza la risoluzione della richiesta da parte del server di origine, anche se nel proxy esiste una copia memorizzata nella cache. La [**funzione InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (solo su richieste HTTP e HTTPS) e [**la funzione HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) usano questo flag.                                                                                                                                                                                               |
| [**RICARICAMENTO DEL FLAG INTERNET \_ \_**](api-flags.md)                                                                                       | Forza la funzione a recuperare la risorsa richiesta direttamente da Internet. Le informazioni scaricate vengono archiviate nella cache.                                                                                                                                                                                                                                                                                                                     |
| [**RISINCRONIZZAZIONE DEL FLAG INTERNET \_ \_**](api-flags.md)                                                                         | Consente a un'applicazione di eseguire un download condizionale della risorsa da Internet. Se la versione archiviata nella cache è corrente, le informazioni vengono scaricate dalla cache. In caso contrario, le informazioni vengono ricaricate dal server.                                                                                                                                                                                                                   |



 

## <a name="persistent-caching-functions"></a>Funzioni Caching persistenti

I client che necessitano di servizi di memorizzazione nella cache persistenti usano le funzioni di memorizzazione nella cache persistente per consentire alle applicazioni di salvare i dati nel file system locale per un uso successivo, ad esempio in situazioni in cui un collegamento a larghezza di banda bassa limita l'accesso ai dati o l'accesso non è affatto disponibile.

Le funzioni di cache forniscono la memorizzazione nella cache permanente e l'esplorazione offline. A meno che il flag [**INTERNET FLAG NO CACHE \_ \_ \_ \_ WRITE**](api-flags.md) non specifichi in modo esplicito alcuna memorizzazione nella cache, le funzioni memorizzano nella cache tutti i dati scaricati dalla rete. Le risposte ai dati POST non vengono memorizzate nella cache.

## <a name="using-the-persistent-url-cache-functions"></a>Uso delle funzioni di Cache URL persistente

Le funzioni di cache URL permanenti seguenti consentono a un'applicazione di accedere e modificare le informazioni archiviate nella cache.



| Funzione                                                           | Descrizione                                                                                                                                                   |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CommitUrlCacheEntryA**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya)               | Memorizza nella cache i dati nel file specificato nell'archivio della cache e i dati vengono associati all'URL specificato.                                                                  |
| [**CommitUrlCacheEntryW**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentryw)               | Memorizza nella cache i dati nel file specificato nell'archivio della cache e i dati vengono associati all'URL specificato.                                                                  |
| [**CreateUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya)                 | Alloca l'archiviazione cache richiesta e crea un nome file locale per salvare la voce della cache corrispondente al nome di origine.                           |
| [**CreateUrlCacheGroup**](/windows/desktop/api/Wininet/nf-wininet-createurlcachegroup)                 | Genera un'identificazione del gruppo di cache.                                                                                                                       |
| [**DeleteUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-deleteurlcacheentry)                 | Rimuove il file associato al nome di origine dalla cache, se il file esiste.                                                                          |
| [**DeleteUrlCacheGroup**](/windows/desktop/api/Wininet/nf-wininet-deleteurlcachegroup)                 | Rilascia un **GROUPID e** qualsiasi stato associato nel file di indice della cache.                                                                                      |
| [**FindCloseUrlCache**](/windows/desktop/api/Wininet/nf-wininet-findcloseurlcache)                     | Chiude l'handle di enumerazione specificato.                                                                                                                      |
| [**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya)           | Avvia l'enumerazione della cache.                                                                                                                          |
| [**FindFirstUrlCacheEntryEx**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentryexa)       | Avvia un'enumerazione filtrata della cache.                                                                                                                   |
| [**FindNextUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentrya)             | Recupera la voce successiva nella cache.                                                                                                                        |
| [**FindNextUrlCacheEntryEx**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentryexa)         | Recupera la voce successiva in un'enumerazione della cache filtrata.                                                                                                     |
| [**GetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa)               | Recupera informazioni su una voce della cache.                                                                                                                    |
| [**GetUrlCacheEntryInfoEx**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoexa)           | Cerca l'URL dopo aver traslato eventuali reindirizzamenti memorizzati nella cache che verrebbero applicati in modalità offline da [**HttpSendRequest.**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)           |
| [**ReadUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-readurlcacheentrystream)         | Legge i dati memorizzati nella cache da un flusso aperto tramite [**RetrieveUrlCacheEntryStream.**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama)                            |
| [**RetrieveUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea)     | Recupera una voce della cache dalla cache sotto forma di file.                                                                                                 |
| [**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama) | Fornisce il modo più efficiente e indipendente dall'implementazione per accedere ai dati della cache.                                                                   |
| [**SetUrlCacheEntryGroup**](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentrygroup)             | Aggiunge o rimuove voci da un gruppo di cache.                                                                                                                   |
| [**SetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentryinfoa)               | Imposta i membri specificati della struttura [**INTERNET \_ CACHE ENTRY \_ \_ INFO.**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa)                                                |
| [**UnlockUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentryfile)         | Sblocca la voce della cache bloccata quando il file è stato recuperato per l'uso dalla cache [**da RetrieveUrlCacheEntryFile.**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea) |
| [**UnlockUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentrystream)     | Chiude il flusso recuperato utilizzando [**RetrieveUrlCacheEntryStream.**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama)                                           |



 

### <a name="enumerating-the-cache"></a>Enumerazione della cache

Le [**funzioni FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya) [**e FindNextUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentrya) enumerano le informazioni archiviate nella cache. [**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya) avvia l'enumerazione usando un criterio di ricerca, un buffer e una dimensione del buffer per creare un handle e restituire la prima voce della cache. [**FindNextUrlCacheEntry accetta**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentrya) l'handle creato da [**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya), un buffer e una dimensione del buffer per restituire la voce della cache successiva.

Entrambe le funzioni archiviano una struttura [**INTERNET CACHE ENTRY \_ \_ \_ INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) nel buffer. Le dimensioni di questa struttura variano per ogni voce. Se le dimensioni del buffer passate a una delle funzioni non sono sufficienti, la funzione ha esito negativo e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce ERROR \_ INSUFFICIENT \_ BUFFER. La variabile buffer size contiene le dimensioni del buffer necessarie per recuperare la voce della cache. È necessario allocare un buffer delle dimensioni indicate dalla variabile di dimensione del buffer e chiamare nuovamente la funzione con il nuovo buffer.

La struttura [**INTERNET \_ CACHE ENTRY \_ \_ INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) contiene le dimensioni della struttura, l'URL delle informazioni memorizzate nella cache, il nome del file locale, il tipo di voce della cache, il numero di utilizzi, la frequenza di riscontri, le dimensioni, l'ora dell'ultima modifica, la scadenza, l'ultimo accesso, l'ora dell'ultima sincronizzazione, le informazioni sull'intestazione, le dimensioni delle informazioni di intestazione e l'estensione del nome file.

La [**funzione FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya) accetta un criterio di ricerca, un buffer che archivia la struttura [**INTERNET CACHE ENTRY \_ \_ \_ INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) e le dimensioni del buffer. Attualmente, viene implementato solo il criterio di ricerca predefinito, che restituisce tutte le voci della cache.

Dopo l'enumerazione della cache, l'applicazione deve chiamare [**FindCloseUrlCache per**](/windows/desktop/api/Wininet/nf-wininet-findcloseurlcache) chiudere l'handle di enumerazione della cache.

Nell'esempio seguente viene visualizzato l'URL di ogni voce della cache in una casella di **riepilogo, IDC \_ CacheList**. Usa MAX CACHE ENTRY INFO SIZE per allocare inizialmente un buffer, poiché le versioni precedenti \_ \_ \_ dell'API WinINet non enumerano correttamente \_ la cache. Le versioni successive enumerano correttamente la cache e non è previsto alcun limite per le dimensioni della cache. Tutte le applicazioni eseguite in computer con la versione dell'API WinINet Internet Explorer 4.0 devono allocare un buffer delle dimensioni richieste. Per altre informazioni, vedere [Uso dei buffer.](appendix-b-using-buffers.md)


```C++
int WINAPI EnumerateCacheOld(HWND hX)
{
    DWORD dwEntrySize;
    LPINTERNET_CACHE_ENTRY_INFO lpCacheEntry;
    DWORD MAX_CACHE_ENTRY_INFO_SIZE = 4096;
    HANDLE hCacheDir;
    int nCount=0;

    SendDlgItemMessage(hX,IDC_CacheList,LB_RESETCONTENT,0,0);
    
    SetCursor(LoadCursor(NULL,IDC_WAIT));

    dwEntrySize = MAX_CACHE_ENTRY_INFO_SIZE;
    lpCacheEntry = (LPINTERNET_CACHE_ENTRY_INFO) new char[dwEntrySize];
    lpCacheEntry->dwStructSize = dwEntrySize;

again:

    hCacheDir = FindFirstUrlCacheEntry(NULL,
                                       lpCacheEntry,
                                       &dwEntrySize);
    if (!hCacheDir)                                             
    {
        delete[]lpCacheEntry;
        switch(GetLastError())
        {
            case ERROR_NO_MORE_ITEMS: 
                TCHAR tempout[80];
                _stprintf_s(tempout, 
                            80,   
                            TEXT("The number of cache entries = %d \n"),
                            nCount);
                MessageBox(hX,tempout,TEXT("Cache Enumeration"),MB_OK);
                FindCloseUrlCache(hCacheDir);
                SetCursor(LoadCursor(NULL,IDC_ARROW));
                return TRUE;
                break;
            case ERROR_INSUFFICIENT_BUFFER:
                lpCacheEntry = (LPINTERNET_CACHE_ENTRY_INFO) 
                                new char[dwEntrySize];
                lpCacheEntry->dwStructSize = dwEntrySize;
                goto again;
                break;
            default:
                ErrorOut( hX,GetLastError(),
                          TEXT("FindNextUrlCacheEntry Init"));
                FindCloseUrlCache(hCacheDir);
                SetCursor(LoadCursor(NULL,IDC_ARROW));
                return FALSE;
        }
    }

    SendDlgItemMessage(hX,IDC_CacheList,LB_ADDSTRING,
                       0,(LPARAM)(lpCacheEntry->lpszSourceUrlName));
    nCount++;
    delete (lpCacheEntry);

    do 
    {
        dwEntrySize = MAX_CACHE_ENTRY_INFO_SIZE;
        lpCacheEntry = (LPINTERNET_CACHE_ENTRY_INFO) new char[dwEntrySize];
        lpCacheEntry->dwStructSize = dwEntrySize;

retry:
        if (!FindNextUrlCacheEntry(hCacheDir,
                                   lpCacheEntry, 
                                   &dwEntrySize))
        {
            delete[]lpCacheEntry;
            switch(GetLastError())
            {
                case ERROR_NO_MORE_ITEMS: 
                    TCHAR tempout[80];
                    _stprintf_s(tempout,
                                80,
                                TEXT("The number of cache entries = %d \n"),nCount);
                    MessageBox(hX,
                               tempout,
                               TEXT("Cache Enumeration"),MB_OK);
                    FindCloseUrlCache(hCacheDir);
                    return TRUE;
                    break;
                case ERROR_INSUFFICIENT_BUFFER:
                    lpCacheEntry = 
                             (LPINTERNET_CACHE_ENTRY_INFO) 
                              new char[dwEntrySize];
                    lpCacheEntry->dwStructSize = dwEntrySize;
                    goto retry;
                    break;
                default:
                    ErrorOut(hX,
                             GetLastError(),
                             TEXT("FindNextUrlCacheEntry Init"));
                    FindCloseUrlCache(hCacheDir);
                    return FALSE;
            }
        }

        SendDlgItemMessage(hX,
                           IDC_CacheList,LB_ADDSTRING,
                           0,
                          (LPARAM)(lpCacheEntry->lpszSourceUrlName));
        nCount++;
        delete[] lpCacheEntry;        
    }  while (TRUE);

    SetCursor(LoadCursor(NULL,IDC_ARROW));
    return TRUE;        
}
```



### <a name="retrieving-cache-entry-information"></a>Recupero di informazioni sulle voci della cache

La [**funzione GetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa) consente di recuperare la struttura [**INTERNET CACHE ENTRY \_ \_ \_ INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) per l'URL specificato. Questa struttura contiene le dimensioni della struttura, l'URL delle informazioni memorizzate nella cache, il nome del file locale, il tipo di voce della cache, il numero di utilizzi, la frequenza di riscontri, le dimensioni, l'ora dell'ultima modifica, la scadenza, l'ultimo accesso, l'ora dell'ultima sincronizzazione, le informazioni sull'intestazione, le dimensioni delle informazioni di intestazione e l'estensione del nome file.

[**GetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa) accetta un URL, un buffer per una struttura [**INTERNET CACHE ENTRY \_ \_ \_ INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) e le dimensioni del buffer. Se l'URL viene trovato, le informazioni vengono copiate nel buffer. In caso contrario, la funzione ha esito negativo e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce ERROR \_ FILE NOT \_ \_ FOUND. Se le dimensioni del buffer non sono sufficienti per archiviare le informazioni sulla voce della cache, la funzione ha esito negativo e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce ERROR \_ INSUFFICIENT \_ BUFFER. Le dimensioni necessarie per recuperare le informazioni vengono archiviate nella variabile delle dimensioni del buffer.

[**GetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa) non esegue alcuna analisi dell'URL, quindi un URL che contiene un ancoraggio ( ) non verrà trovato nella cache, anche se la risorsa viene \# memorizzata nella cache. Ad esempio, se viene passato l'URL " ", la funzione restituisce ERROR FILE NOT FOUND anche se https://example.com/example.htm\#sample " " si trova nella \_ \_ \_ https://example.com/example.htm cache.

Nell'esempio seguente vengono recuperate le informazioni sulla voce della cache per l'URL specificato. La funzione visualizza quindi le informazioni sull'intestazione nella **casella di modifica IDC \_ CacheDump.**


```C++
int WINAPI GetCacheEntryInfo(HWND hX,LPTSTR lpszUrl)
{
    DWORD dwEntrySize=0;
    LPINTERNET_CACHE_ENTRY_INFO lpCacheEntry;

    SetCursor(LoadCursor(NULL,IDC_WAIT));
    if (!GetUrlCacheEntryInfo(lpszUrl,NULL,&dwEntrySize))
    {
        if (GetLastError()!=ERROR_INSUFFICIENT_BUFFER)
        {
            ErrorOut(hX,GetLastError(),TEXT("GetUrlCacheEntryInfo"));
            SetCursor(LoadCursor(NULL,IDC_ARROW));
            return FALSE;
        }
        else
            lpCacheEntry = (LPINTERNET_CACHE_ENTRY_INFO) 
                            new char[dwEntrySize];
    }
    else
        return FALSE; // should not be successful w/ NULL buffer
                      // and 0 size

    if (!GetUrlCacheEntryInfo(lpszUrl,lpCacheEntry,&dwEntrySize))
    {
        ErrorOut(hX,GetLastError(),TEXT("GetUrlCacheEntryInfo"));
        SetCursor(LoadCursor(NULL,IDC_ARROW));
        return FALSE;
    }
    else
    {
        if ((lpCacheEntry->dwHeaderInfoSize)!=0)
        {
            LPSTR(lpCacheEntry->lpHeaderInfo)
                                [lpCacheEntry->dwHeaderInfoSize]=TEXT('\0');
            SetDlgItemText(hX,IDC_Headers,
                           lpCacheEntry->lpHeaderInfo);
        }
        else
        {
            SetDlgItemText(hX,IDC_Headers,TEXT("None"));
        }

        SetCursor(LoadCursor(NULL,IDC_ARROW));
        return TRUE;
    }
        
}
```



### <a name="creating-a-cache-entry"></a>Creazione di una voce della cache

Un'applicazione usa [**le funzioni CreateUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya) [**e CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya) per creare una voce della cache.

[**CreateUrlCacheEntry accetta**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya) l'URL, le dimensioni del file previste e l'estensione del nome file. La funzione crea quindi un nome file locale per salvare la voce della cache che corrisponde all'URL e all'estensione del nome file.

Usando il nome del file locale, scrivere i dati nel file locale. Dopo che i dati sono stati scritti nel file locale, l'applicazione deve chiamare [**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya).

[**CommitUrlCacheEntry accetta**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya) l'URL, il nome del file locale, la scadenza, l'ora dell'ultima modifica, il tipo di voce della cache, le informazioni di intestazione, le dimensioni delle informazioni di intestazione e l'estensione del nome file. La funzione memorizza quindi nella cache i dati nel file specificato nell'archivio della cache e lo associa all'URL specificato.

Nell'esempio seguente viene utilizzato il nome del file locale, creato da una precedente chiamata a [**CreateUrlCacheEntry,**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya)archiviato nella casella di testo **IDC \_ LocalFile**, per archiviare il testo della casella di testo **IDC \_ CacheDump** nella voce della cache. Dopo che i dati sono stati scritti nel file usando **fopen**, **fprintf** e **fclose**, viene eseguito il commit della voce [**usando CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya).


```C++
int WINAPI CommitEntry(HWND hX)
{
    LPTSTR lpszUrl, lpszExt, lpszFileName;
    LPTSTR lpszData,lpszSize;
    DWORD dwSize;
    DWORD dwEntryType=0;
    FILE *lpfCacheEntry;
    LPFILETIME lpdtmExpire, lpdtmLastModified;
    LPSYSTEMTIME lpdtmSysTime;
    errno_t err;

    if( SendDlgItemMessage(hX,IDC_RBNormal,BM_GETCHECK,0,0) )
    {
        dwEntryType = dwEntryType + NORMAL_CACHE_ENTRY;
    }
    else if( SendDlgItemMessage(hX,IDC_RBSticky, BM_GETCHECK,0,0) )
    {
        dwEntryType = dwEntryType + STICKY_CACHE_ENTRY;
    }
    else if(SendDlgItemMessage( hX,IDC_RBSparse, BM_GETCHECK,0,0) )
    {
        dwEntryType = dwEntryType + SPARSE_CACHE_ENTRY;
    }
 

    if( SendDlgItemMessage(hX,IDC_RBCookie, BM_GETCHECK,0,0))
    {
            dwEntryType = dwEntryType + COOKIE_CACHE_ENTRY;
    }
    else if( SendDlgItemMessage(hX,IDC_RBUrl, BM_GETCHECK,0,0) )
    {
        dwEntryType = dwEntryType + URLHISTORY_CACHE_ENTRY;
    }


    if( SendDlgItemMessage(hX,IDC_RBNone, BM_GETCHECK,0,0) )
    {
        dwEntryType=0;
    }
        
    lpdtmSysTime = new SYSTEMTIME;
    lpdtmExpire = new FILETIME;
    lpdtmLastModified = new FILETIME;

    GetLocalTime(lpdtmSysTime);
    SystemTimeToFileTime(lpdtmSysTime,lpdtmExpire);
    SystemTimeToFileTime(lpdtmSysTime,lpdtmLastModified);
    delete(lpdtmSysTime);

    lpszUrl = new TCHAR[MAX_PATH];
    lpszFileName = new TCHAR[MAX_PATH];
    lpszExt = new TCHAR[5];
    lpszSize = new TCHAR[10];

    GetDlgItemText(hX,IDC_SourceURL,lpszUrl,MAX_PATH);
    GetDlgItemText(hX,IDC_LocalFile,lpszFileName,MAX_PATH);
    GetDlgItemText(hX,IDC_FileExt,lpszExt,5);

    GetDlgItemText(hX,IDC_SizeLow,lpszSize,10);
    dwSize = (DWORD)_ttol(lpszSize);
    delete(lpszSize);

    if (dwSize==0)
    {
        if((MessageBox(hX,
                       TEXT("Incorrect File Size.\nUsing 8000 characters, Okay?\n"),
                       TEXT("Commit Entry"),MB_YESNO))
                        ==IDYES)
        {
            dwSize = 8000;
        }
        else
        {
            return FALSE;
        }
    }

    lpszData = new TCHAR[dwSize];
    GetDlgItemText(hX,IDC_CacheDump,lpszData,dwSize);
        
     err = _tfopen_s(&lpfCacheEntry,lpszFileName,_T("w"));
     if (err)
        return FALSE;
    fprintf(lpfCacheEntry,"%s",lpszData);
    fclose(lpfCacheEntry);
    delete(lpszData);

    if ( !CommitUrlCacheEntry( lpszUrl, 
                               lpszFileName, 
                               *lpdtmExpire,
                               *lpdtmLastModified, 
                               dwEntryType,
                               NULL,
                               0,
                               lpszExt,
                               0) )
    {
        ErrorOut(hX,GetLastError(),TEXT("Commit Cache Entry"));
        delete(lpszUrl);
        delete(lpszFileName);
        delete(lpszExt);
        delete(lpdtmExpire);
        delete(lpdtmLastModified);
        return FALSE;
    }
    else
    {
        delete(lpszUrl);
        delete(lpszFileName);
        delete(lpszExt);
        delete(lpdtmExpire);
        delete(lpdtmLastModified);
        return TRUE;
    }
}
```



### <a name="deleting-a-cache-entry"></a>Eliminazione di una voce della cache

La [**funzione DeleteUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-deleteurlcacheentry) accetta un URL e rimuove il file di cache associato. Se il file di cache non esiste, la funzione ha esito negativo e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce ERROR \_ FILE NOT \_ \_ FOUND. Se il file di cache è attualmente bloccato o in uso, la funzione ha esito negativo e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce ERROR \_ ACCESS \_ DENIED. Il file viene eliminato quando viene sbloccato.

### <a name="retrieving-cache-entry-files"></a>Recupero di file di voci della cache

Per le applicazioni che richiedono il nome file di una risorsa, usare le funzioni [**RetrieveUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea) [**e UnlockUrlCacheEntryFile.**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentryfile) Le applicazioni che non richiedono il nome file devono usare le funzioni [**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama), [**ReadUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-readurlcacheentrystream)e [**UnlockUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentrystream) per recuperare le informazioni nella cache.

[**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama) non esegue alcuna analisi dell'URL, quindi un URL che contiene un ancoraggio ( ) non verrà trovato nella cache, anche se la risorsa viene \# memorizzata nella cache. Ad esempio, se viene passato l'URL " ", la funzione restituisce ERROR FILE NOT FOUND anche se https://example.com/example.htm\#sample " " si trova nella \_ \_ \_ https://example.com/example.htm cache.

[**RetrieveUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea) accetta un URL, un buffer che archivia la struttura [**INTERNET CACHE ENTRY \_ \_ \_ INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) e le dimensioni del buffer. La funzione viene recuperata e bloccata per il chiamante.

Dopo aver usato le informazioni nel file, l'applicazione deve chiamare [**UnlockUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentryfile) per sbloccare il file.

### <a name="cache-groups"></a>Gruppi di cache

Per creare un gruppo di cache, [**è necessario chiamare la funzione CreateUrlCacheGroup**](/windows/desktop/api/Wininet/nf-wininet-createurlcachegroup) per generare un **GROUPID** per il gruppo di cache. È possibile aggiungere voci al gruppo di cache fornendo l'URL della voce della cache e il flag INTERNET CACHE GROUP ADD alla \_ \_ funzione \_ [**SetUrlCacheEntryGroup.**](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentrygroup) Per rimuovere una voce della cache da un gruppo, passare l'URL della voce della cache e il flag INTERNET CACHE GROUP REMOVE a \_ \_ \_ [**SetUrlCacheEntryGroup.**](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentrygroup)

Le [**funzioni FindFirstUrlCacheEntryEx**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentryexa) e [**FindNextUrlCacheEntryEx**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentryexa) possono essere usate per enumerare le voci in un gruppo di cache specificato. Al termine dell'enumerazione, la funzione deve chiamare [**FindCloseUrlCache**](/windows/desktop/api/Wininet/nf-wininet-findcloseurlcache).

## <a name="handling-structures-with-variable-size-information"></a>Gestione delle strutture con informazioni sulle dimensioni delle variabili

La cache può contenere informazioni sulle dimensioni variabili per ogni URL archiviato. Ciò si riflette nella struttura [**INTERNET \_ CACHE ENTRY \_ \_ INFO.**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) Quando le funzioni della cache restituiscono questa struttura, creano un buffer che è sempre la dimensione di [**INTERNET \_ CACHE ENTRY \_ \_ INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) più eventuali informazioni sulle dimensioni delle variabili. Se un membro puntatore non è **NULL,** punta all'area di memoria immediatamente dopo la struttura . Durante la copia del buffer restituito da una funzione in un altro buffer, i membri del puntatore devono essere fissi in modo che puntino alla posizione appropriata nel nuovo buffer, come illustrato nell'esempio seguente.

``` syntax
lpDstCEInfo->lpszSourceUrlName = 
    (LPINTERNET_CACHE_ENTRY_INFO) ((LPBYTE) lpSrcCEInfo + 
       ((DWORD)(lpOldCEInfo->lpszSourceUrlName) - (DWORD)lpOldCEInfo));
```

Alcune funzioni della cache hanno esito negativo e viene visualizzato il messaggio di errore ERROR INSUFFICIENT BUFFER se si specifica un buffer troppo piccolo per contenere le informazioni sulle voci della \_ \_ cache recuperate dalla funzione. In questo caso, la funzione restituisce anche le dimensioni richieste del buffer. È quindi possibile allocare un buffer delle dimensioni appropriate e chiamare di nuovo la funzione .

> [!Note]  
> WinINet non supporta le implementazioni del server. Inoltre, non deve essere usato da un servizio. Per le implementazioni o i servizi server, [usare Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 
