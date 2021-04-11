---
title: Memorizzazione nella cache (Windows Internet)
description: Le funzioni WinINet hanno un supporto di memorizzazione nella cache integrato semplice, ma flessibile.
ms.assetid: 44c268c9-a745-432a-8540-60d7e7d2cb2d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e753d826ec3abe580b94158296562208dcbed44
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104118786"
---
# <a name="caching-windows-internet"></a>Memorizzazione nella cache (Windows Internet)

Le funzioni WinINet hanno un supporto di memorizzazione nella cache integrato semplice, ma flessibile. Tutti i dati recuperati dalla rete vengono memorizzati nella cache sul disco rigido e recuperati per le richieste successive. L'applicazione può controllare la memorizzazione nella cache per ogni richiesta. Per le richieste HTTP dal server, vengono memorizzate nella cache anche la maggior parte delle intestazioni ricevute. Quando una richiesta HTTP viene soddisfatta dalla cache, anche le intestazioni memorizzate nella cache vengono restituite al chiamante. In questo modo, il download dei dati viene semplificato, indipendentemente dal fatto che i dati provengano dalla cache o dalla rete.

Le applicazioni devono allocare correttamente un buffer per ottenere i risultati desiderati quando si utilizzano le funzioni di memorizzazione nella cache degli URL persistenti. Per ulteriori informazioni, vedere [utilizzo dei buffer](appendix-b-using-buffers.md).

## <a name="cache-behavior-during-response-processing"></a>Comportamento della cache durante l'elaborazione della risposta

La cache di WinINet è conforme alle direttive di controllo della cache HTTP descritte in RFC 2616. Le direttive di controllo della cache e i flag del set di applicazioni determinano ciò che può essere memorizzato nella cache. Tuttavia, WinINet determina ciò che viene effettivamente memorizzato nella cache in base ai criteri seguenti:

-   WinINet memorizza nella cache solo le risposte HTTP e FTP.
-   Solo le risposte ben corrette possono essere archiviate da una cache e usate in una risposta a una richiesta successiva. Le risposte ben corrette sono definite come risposte che restituiscono correttamente.
-   Per impostazione predefinita, WinINet memorizza nella cache le risposte con esito positivo, a meno che una direttiva di controllo della cache dal server o un flag definito dall'applicazione denoti specificamente che la risposta potrebbe non essere memorizzata nella cache.
-   In generale, le risposte al verbo GET vengono memorizzate nella cache se vengono soddisfatti i requisiti elencati in precedenza. Le risposte ai verbi PUT e POST non vengono memorizzate nella cache in qualsiasi circostanza.
-   Gli elementi verranno memorizzati nella cache anche quando la cache è piena. Se un elemento aggiunto inserisce la cache sul limite delle dimensioni, viene pianificato il scavenger della cache. Per impostazione predefinita, nella cache non è garantito che gli elementi rimangano più di 10 minuti. Per altre informazioni, vedere la sezione [cache Scavenger](#cache-scavenger) riportata di seguito.
-   HTTPS viene memorizzato nella cache per impostazione predefinita. Questa operazione viene gestita da un'impostazione globale che non può essere sottoposta a override dalle direttive della cache definite dall'applicazione. Per eseguire l'override dell'impostazione globale, selezionare l'applet Opzioni Internet nel pannello di controllo e passare alla scheda Avanzate. Selezionare la casella "non salvare le pagine crittografate su disco" nella sezione "sicurezza".

## <a name="cache-scavenger"></a>Scavenger cache

Il scavenger della cache pulisce periodicamente gli elementi dalla cache. Se un elemento viene aggiunto alla cache e la cache è piena, l'elemento viene aggiunto alla cache e il scavenger della cache è pianificato. Se il scavenger della cache completa un ciclo di scavenging e la cache non ha raggiunto il limite della cache, il Scavenger viene pianificato per un altro round quando un altro elemento viene aggiunto alla cache. In generale, il Scavenger viene pianificato quando un elemento aggiunto inserisce la cache sul limite delle dimensioni. Per impostazione predefinita, la durata minima della cache è impostata su 10 minuti, se non diversamente specificato in una direttiva di controllo della cache. Quando viene avviato lo scavenger della cache, non c'è alcuna garanzia che gli elementi meno recenti siano i primi a essere eliminati dalla cache.

La cache è condivisa tra tutte le applicazioni WinINet nel computer per lo stesso utente. A partire da Windows Vista e Windows Server 2008, le dimensioni della cache sono impostate su 1/32A per la dimensione del disco, con una dimensione minima di 8MB e una dimensione massima di 50 MB.

## <a name="using-flags-to-control-caching"></a>Utilizzo di flag per il controllo della memorizzazione nella cache

I flag di memorizzazione nella cache consentono a un'applicazione di controllare quando e come viene utilizzata la cache. Questi flag possono essere usati singolarmente o in combinazione con il parametro *dwFlags* in funzioni che accedono a informazioni o risorse su Internet. Per impostazione predefinita, le funzioni archiviano tutti i dati scaricati da Internet.

I flag seguenti possono essere utilizzati per controllare la memorizzazione nella cache.



| Valore                                                                                                                                                  | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ Async della cache del flag Internet \_**](api-flags.md)                                                                            | Questo flag non ha alcun effetto.                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**\_cache del flag Internet se la rete ha \_ \_ \_ \_ esito negativo**](api-flags.md)                                                              | Restituisce la risorsa dalla cache se la richiesta di rete per la risorsa ha esito negativo a causa di un [errore di \_ \_ \_ reimpostazione della connessione Internet](wininet-errors.md) o di [errore \_ Internet \_ non è in grado di \_ connettersi](wininet-errors.md) . Questo flag viene usato da [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).                                                                                                              |
| [**\_flag Internet \_ dont \_ cache**](api-flags.md)                                                                              | Non memorizza nella cache i dati, in locale o in qualsiasi gateway. Identico al valore preferito, [**il \_ flag \_ Internet \_ Nessuna \_ scrittura nella cache**](api-flags.md).                                                                                                                                                                                                                                                                                 |
|                                                                                                                                                        | Indica che si tratta di un invio di form.                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**Internet \_ flag inviato dal flag Internet \_ \_ della cache**](api-flags.md)[**\_ \_ \_ Invia form**](api-flags.md) | Non esegue richieste di rete. Tutte le entità vengono restituite dalla cache. Se l'elemento richiesto non è presente nella cache, viene restituito un errore appropriato, ad esempio file di errore \_ \_ non \_ trovato. Solo la funzione [**Internetopn**](/windows/desktop/api/Wininet/nf-wininet-internetopena) usa questo flag.                                                                                                                                                                                                       |
| [**\_nuovo flag Internet \_ FWD \_**](api-flags.md)                                                                                  | Indica che la funzione deve utilizzare la copia della risorsa attualmente nella cache Internet. La data di scadenza e altre informazioni sulla risorsa non sono controllate. Se l'elemento richiesto non viene trovato nella cache Internet, il sistema tenta di individuare la risorsa nella rete. Questo valore è stato introdotto in Microsoft Internet Explorer 5 ed è associato alle operazioni dei pulsanti **Avanti** e **indietro** di Internet Explorer. |
| [**\_ \_ collegamento ipertestuale flag Internet**](api-flags.md)                                                                                 | Impone all'applicazione di ricaricare una risorsa se non è stata restituita alcuna ora di scadenza e se la risorsa è stata archiviata nella cache.                                                                                                                                                                                                                                                                                                                  |
| [**FLAG INTERNET che \_ \_ rende \_ persistente**](api-flags.md)                                                                    | Non più supportata.                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**il \_ flag Internet \_ deve \_ memorizzare nella cache la \_ richiesta**](api-flags.md)                                                             | Determina la creazione di un file temporaneo se il file non può essere memorizzato nella cache. Si tratta di un valore identico a quello preferito, il [**\_ file di \_ richiesta \_ del flag Internet**](api-flags.md).                                                                                                                                                                                                                                                                            |
| [**\_file con flag Internet \_ necessario \_**](api-flags.md)                                                                                | Determina la creazione di un file temporaneo se il file non può essere memorizzato nella cache.                                                                                                                                                                                                                                                                                                                                                                                               |
| [**\_flag Internet \_ senza \_ \_ scrittura cache**](api-flags.md)                                                                     | Rifiuta qualsiasi tentativo da parte della funzione di archiviare i dati scaricati da Internet nella cache. Questo flag è necessario se l'applicazione non desidera che le risorse scaricate vengano archiviate localmente.                                                                                                                                                                                                                                                               |
| [**\_flag Internet \_ Nessuna \_ interfaccia utente**](api-flags.md)                                                                                        | Disabilita la finestra di dialogo dei cookie. Questo flag può essere usato da [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (solo richieste http).                                                                                                                                                                                                                                                                                          |
| [**\_flag Internet \_ offline**](api-flags.md)                                                                                     | Impedisce all'applicazione di inviare richieste alla rete. Tutte le richieste vengono risolte utilizzando le risorse archiviate nella cache. Se la risorsa non è presente nella cache, viene restituito un errore appropriato, ad esempio file di errore \_ \_ non \_ trovato.                                                                                                                                                                                                                            |
| [**\_flag Internet \_ pragma \_ NoCache**](api-flags.md)                                                                      | Impone la risoluzione della richiesta da parte del server di origine, anche se nel proxy esiste una copia memorizzata nella cache. La funzione [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (solo per le richieste HTTP e HTTPS) e la funzione [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) usano questo flag.                                                                                                                                                                                               |
| [**\_ricarica del flag Internet \_**](api-flags.md)                                                                                       | Impone la funzione per recuperare la risorsa richiesta direttamente da Internet. Le informazioni scaricate vengono memorizzate nella cache.                                                                                                                                                                                                                                                                                                                     |
| [**risincronizzazione del \_ flag Internet \_**](api-flags.md)                                                                         | Fa in modo che un'applicazione esegua un download condizionale della risorsa da Internet. Se la versione archiviata nella cache è aggiornata, le informazioni vengono scaricate dalla cache. In caso contrario, le informazioni vengono ricaricate dal server.                                                                                                                                                                                                                   |



 

## <a name="persistent-caching-functions"></a>Funzioni di Caching permanenti

I client che necessitano di servizi di memorizzazione nella cache permanenti utilizzano le funzioni di Caching permanenti per consentire alle applicazioni di salvare i dati nella file system locale per un uso successivo, ad esempio in situazioni in cui un collegamento a larghezza di banda ridotta limita l'accesso ai dati o l'accesso non è disponibile.

Le funzioni della cache forniscono la memorizzazione nella cache persistente e l'esplorazione offline. A meno che non venga specificato in modo esplicito nessun flag di [**\_ \_ \_ \_ scrittura**](api-flags.md) nella cache, le funzioni memorizzano nella cache tutti i dati scaricati dalla rete. Le risposte ai dati POST non vengono memorizzate nella cache.

## <a name="using-the-persistent-url-cache-functions"></a>Uso delle funzioni di cache URL persistenti

Le seguenti funzioni di cache URL persistenti consentono a un'applicazione di accedere e modificare le informazioni archiviate nella cache.



| Funzione                                                           | Descrizione                                                                                                                                                   |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CommitUrlCacheEntryA**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya)               | Memorizza nella cache i dati nel file specificato nell'archivio della cache e li associa all'URL specificato.                                                                  |
| [**CommitUrlCacheEntryW**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentryw)               | Memorizza nella cache i dati nel file specificato nell'archivio della cache e li associa all'URL specificato.                                                                  |
| [**CreateUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya)                 | Alloca l'archiviazione della cache richiesta e crea un nome di file locale per salvare la voce della cache che corrisponde al nome dell'origine.                           |
| [**CreateUrlCacheGroup**](/windows/desktop/api/Wininet/nf-wininet-createurlcachegroup)                 | Genera un'identificazione del gruppo di cache.                                                                                                                       |
| [**DeleteUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-deleteurlcacheentry)                 | Rimuove il file associato al nome di origine dalla cache, se il file esiste.                                                                          |
| [**DeleteUrlCacheGroup**](/windows/desktop/api/Wininet/nf-wininet-deleteurlcachegroup)                 | Rilascia un **GROUPID** e qualsiasi stato associato nel file di indice della cache.                                                                                      |
| [**FindCloseUrlCache**](/windows/desktop/api/Wininet/nf-wininet-findcloseurlcache)                     | Chiude l'handle di enumerazione specificato.                                                                                                                      |
| [**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya)           | Inizia l'enumerazione della cache.                                                                                                                          |
| [**FindFirstUrlCacheEntryEx**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentryexa)       | Avvia un'enumerazione filtrata della cache.                                                                                                                   |
| [**FindNextUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentrya)             | Recupera la voce successiva nella cache.                                                                                                                        |
| [**FindNextUrlCacheEntryEx**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentryexa)         | Recupera la voce successiva in un'enumerazione della cache filtrata.                                                                                                     |
| [**GetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa)               | Recupera le informazioni su una voce della cache.                                                                                                                    |
| [**GetUrlCacheEntryInfoEx**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoexa)           | Cerca l'URL dopo aver tradotto tutti i reindirizzamenti memorizzati nella cache che verrebbero applicati in modalità offline da [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).           |
| [**ReadUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-readurlcacheentrystream)         | Legge i dati memorizzati nella cache da un flusso aperto utilizzando [**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama).                            |
| [**RetrieveUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea)     | Recupera una voce della cache dalla cache sotto forma di file.                                                                                                 |
| [**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama) | Fornisce il modo più efficiente e indipendente dall'implementazione per accedere ai dati della cache.                                                                   |
| [**SetUrlCacheEntryGroup**](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentrygroup)             | Aggiunge o rimuove voci da un gruppo di cache.                                                                                                                   |
| [**SetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentryinfoa)               | Imposta i membri specificati della struttura [**delle \_ \_ \_ informazioni sulla voce della cache Internet**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) .                                                |
| [**UnlockUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentryfile)         | Sblocca la voce della cache che è stata bloccata quando il file è stato recuperato per l'uso dalla cache da parte di [**RetrieveUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea). |
| [**UnlockUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentrystream)     | Chiude il flusso recuperato utilizzando [**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama).                                           |



 

### <a name="enumerating-the-cache"></a>Enumerazione della cache

Le funzioni [**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya) e [**FindNextUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentrya) enumerano le informazioni archiviate nella cache. [**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya) avvia l'enumerazione accettando un criterio di ricerca, un buffer e una dimensione del buffer per creare un handle e restituire la prima voce della cache. [**FindNextUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentrya) accetta l'handle creato da [**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya), un buffer e una dimensione del buffer per restituire la voce della cache successiva.

Entrambe le funzioni archiviano una struttura di [**\_ \_ \_ informazioni sulla voce della cache Internet**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) nel buffer. La dimensione di questa struttura varia per ogni voce. Se la dimensione del buffer passata a una delle due funzioni è insufficiente, la funzione ha esito negativo e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce un errore di \_ buffer insufficiente \_ . La variabile della dimensione del buffer contiene la dimensione del buffer necessaria per recuperare la voce della cache. È necessario allocare un buffer della dimensione indicata dalla variabile della dimensione del buffer e la funzione deve essere chiamata nuovamente con il nuovo buffer.

La struttura delle [**\_ \_ \_ informazioni sulla voce della cache Internet**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) contiene le dimensioni della struttura, l'URL delle informazioni memorizzate nella cache, il nome del file locale, il tipo di voce della cache, il conteggio di utilizzo, la frequenza di riscontri, le dimensioni, l'ora dell'Ultima modifica, la scadenza, l'ultimo accesso, l'ora dell'ultima sincronizzazione, le informazioni di intestazione,

La funzione [**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya) accetta un criterio di ricerca, un buffer che archivia la struttura delle [**\_ \_ \_ informazioni sulla voce della cache Internet**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) e le dimensioni del buffer. Attualmente, viene implementato solo il criterio di ricerca predefinito, che restituisce tutte le voci della cache.

Dopo che la cache è stata enumerata, l'applicazione deve chiamare [**FindCloseUrlCache**](/windows/desktop/api/Wininet/nf-wininet-findcloseurlcache) per chiudere l'handle di enumerazione della cache.

Nell'esempio seguente viene visualizzato l'URL di ogni voce della cache in una casella di riepilogo, ovvero **IDC \_**. USA \_ \_ \_ la dimensione massima delle informazioni sulla voce della cache \_ per allocare inizialmente un buffer, perché le versioni precedenti dell'API WinInet non enumerano la cache in modo corretto. Le versioni successive enumerano correttamente la cache e non è previsto alcun limite per le dimensioni della cache. Tutte le applicazioni in esecuzione su computer con la versione dell'API WinINet da Internet Explorer 4,0 devono allocare un buffer con le dimensioni richieste. Per ulteriori informazioni, vedere [utilizzo dei buffer](appendix-b-using-buffers.md).


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



### <a name="retrieving-cache-entry-information"></a>Recupero delle informazioni sulla voce della cache

La funzione [**GetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa) consente di recuperare la struttura delle [**\_ \_ \_ informazioni sulla voce della cache Internet**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) per l'URL specificato. Questa struttura contiene le dimensioni della struttura, l'URL delle informazioni memorizzate nella cache, il nome del file locale, il tipo di voce della cache, il conteggio di utilizzo, la velocità di hit, le dimensioni, l'ora dell'Ultima modifica, la scadenza, l'ultimo accesso, l'ora dell'ultima sincronizzazione, le informazioni di intestazione, le dimensioni delle informazioni

[**GetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa) accetta un URL, un buffer per la struttura delle [**\_ \_ \_ informazioni sulla voce della cache Internet**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) e le dimensioni del buffer. Se l'URL viene trovato, le informazioni vengono copiate nel buffer. In caso contrario, la funzione ha esito negativo e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce il file di errore \_ \_ non \_ trovato. Se la dimensione del buffer non è sufficiente per archiviare le informazioni sulla voce della cache, la funzione ha esito negativo e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce un errore di \_ buffer insufficiente \_ . Le dimensioni necessarie per recuperare le informazioni vengono archiviate nella variabile di dimensione del buffer.

[**GetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa) non esegue l'analisi dell'URL, quindi un URL che contiene un ancoraggio ( \# ) non verrà trovato nella cache, anche se la risorsa è memorizzata nella cache. Se, ad esempio, viene passato l'URL " https://example.com/example.htm\#sample ", la funzione restituisce il \_ file \_ di errore non \_ trovato anche se " https://example.com/example.htm " si trova nella cache.

Nell'esempio seguente vengono recuperate le informazioni relative alla voce della cache per l'URL specificato. La funzione Visualizza quindi le informazioni di intestazione nella casella di modifica **IDC \_ CacheDump** .


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

Un'applicazione usa le funzioni [**CreateUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya) e [**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya) per creare una voce della cache.

[**CreateUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya) accetta l'URL, le dimensioni del file previsto e l'estensione del nome file. La funzione crea quindi un nome file locale per salvare la voce della cache che corrisponde all'URL e all'estensione del nome di file.

Utilizzando il nome file locale, scrivere i dati nel file locale. Dopo che i dati sono stati scritti nel file locale, l'applicazione deve chiamare [**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya).

[**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya) accetta l'URL, il nome file locale, la scadenza, l'ora dell'Ultima modifica, il tipo di voce della cache, le informazioni di intestazione, le dimensioni delle informazioni di intestazione e l'estensione del nome file. La funzione memorizza quindi nella cache i dati nel file specificato nell'archiviazione della cache e li associa all'URL specificato.

Nell'esempio seguente viene usato il nome file locale, creato da una precedente chiamata a [**CreateUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya), archiviato nella casella di testo **IDC \_ LocalFile**, per archiviare il testo dalla casella di testo, **IDC \_ CacheDump**, nella voce della cache. Dopo che i dati sono stati scritti nel file usando **fopen**, **fprintf** e **fclose**, viene eseguito il commit della voce usando [**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya).


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

La funzione [**DeleteUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-deleteurlcacheentry) accetta un URL e rimuove il file di cache associato. Se il file di cache non esiste, la funzione ha esito negativo e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce il file di errore \_ \_ non \_ trovato. Se il file di cache è attualmente bloccato o in uso, la funzione ha esito negativo e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce un errore di \_ accesso \_ negato. Il file viene eliminato quando è sbloccato.

### <a name="retrieving-cache-entry-files"></a>Recupero dei file di voce della cache

Per le applicazioni che richiedono il nome file di una risorsa, usare le funzioni [**RetrieveUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea) e [**UnlockUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentryfile) . Le applicazioni che non richiedono il nome file devono usare le funzioni [**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama), [**ReadUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-readurlcacheentrystream)e [**UnlockUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentrystream) per recuperare le informazioni nella cache.

[**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama) non esegue l'analisi dell'URL, quindi un URL che contiene un ancoraggio ( \# ) non verrà trovato nella cache, anche se la risorsa è memorizzata nella cache. Se, ad esempio, viene passato l'URL " https://example.com/example.htm\#sample ", la funzione restituisce il \_ file \_ di errore non \_ trovato anche se " https://example.com/example.htm " si trova nella cache.

[**RetrieveUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea) accetta un URL, un buffer che archivia la struttura delle [**\_ \_ \_ informazioni sulla voce della cache Internet**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) e le dimensioni del buffer. La funzione viene recuperata e bloccata per il chiamante.

Una volta utilizzate le informazioni nel file, l'applicazione deve chiamare [**UnlockUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentryfile) per sbloccare il file.

### <a name="cache-groups"></a>Gruppi di cache

Per creare un gruppo di cache, è necessario chiamare la funzione [**CreateUrlCacheGroup**](/windows/desktop/api/Wininet/nf-wininet-createurlcachegroup) per generare un **GROUPID** per il gruppo di cache. È possibile aggiungere voci al gruppo di cache specificando l'URL della voce della cache e il \_ flag di aggiunta del gruppo della cache Internet \_ \_ alla funzione [**SetUrlCacheEntryGroup**](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentrygroup) . Per rimuovere una voce della cache da un gruppo, passare l'URL della voce della cache e \_ il \_ flag di rimozione del gruppo della cache Internet \_ a [**SetUrlCacheEntryGroup**](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentrygroup).

Le funzioni [**FindFirstUrlCacheEntryEx**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentryexa) e [**FindNextUrlCacheEntryEx**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentryexa) possono essere utilizzate per enumerare le voci in un gruppo di cache specificato. Al termine dell'enumerazione, la funzione deve chiamare [**FindCloseUrlCache**](/windows/desktop/api/Wininet/nf-wininet-findcloseurlcache).

## <a name="handling-structures-with-variable-size-information"></a>Gestione di strutture con informazioni sulle dimensioni delle variabili

La cache può contenere informazioni sulle dimensioni variabili per ogni URL archiviato. Questo si riflette nella struttura [**delle \_ \_ \_ informazioni sulla voce della cache Internet**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) . Quando le funzioni della cache restituiscono questa struttura, creano un buffer che corrisponde sempre alle dimensioni [**delle \_ \_ \_ informazioni sulla voce della cache Internet**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) più tutte le informazioni sulle dimensioni delle variabili. Se un membro del puntatore non è **null**, fa riferimento all'area di memoria immediatamente dopo la struttura. Durante la copia del buffer restituito da una funzione in un altro buffer, i membri del puntatore devono essere corretti in modo che puntino alla posizione appropriata nel nuovo buffer, come illustrato nell'esempio seguente.

``` syntax
lpDstCEInfo->lpszSourceUrlName = 
    (LPINTERNET_CACHE_ENTRY_INFO) ((LPBYTE) lpSrcCEInfo + 
       ((DWORD)(lpOldCEInfo->lpszSourceUrlName) - (DWORD)lpOldCEInfo));
```

Alcune funzioni della cache hanno esito negativo e il \_ \_ messaggio di errore buffer insufficiente se si specifica un buffer troppo piccolo per contenere le informazioni relative alla voce della cache recuperate dalla funzione. In questo caso, la funzione restituisce anche la dimensione richiesta del buffer. È quindi possibile allocare un buffer di dimensioni appropriate e chiamare di nuovo la funzione.

> [!Note]  
> WinINet non supporta le implementazioni del server. Inoltre, non deve essere utilizzato da un servizio. Per le implementazioni o i servizi del server, usare i [Servizi http di Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 
