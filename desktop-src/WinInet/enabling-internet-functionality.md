---
title: Abilitazione della funzionalità Internet
description: Prima di usare le funzioni WinINet, l'applicazione deve tentare di stabilire una connessione a Internet usando la funzione InternetAttemptConnect.
ms.assetid: 80747c0d-5a09-4ffa-a0ca-b051b82acbf8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 303567942bc94754c1f2a7735851501a4f53036dbd8059420a059a6b632576d0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119570201"
---
# <a name="enabling-internet-functionality"></a>Abilitazione della funzionalità Internet

Prima di usare le funzioni WinINet, l'applicazione deve tentare di stabilire una connessione a Internet usando la [**funzione InternetAttemptConnect.**](/windows/desktop/api/Wininet/nf-wininet-internetattemptconnect) Questa funzione chiama la finestra di dialogo di connessione remota per avviare una connessione a Internet o verificare se esiste già una connessione. Se questa funzione ha esito negativo, l'applicazione può entrare in modalità offline, che consente di accedere alle informazioni memorizzate nella cache durante le connessioni precedenti a Internet.

Usare la [**funzione InternetCheckConnection**](/windows/desktop/api/Wininet/nf-wininet-internetcheckconnectiona) per controllare la connessione a Internet. Tenta di eseguire il ping del server designato dall'URL passato alla funzione. Se il flag FLAG ICC FORCE CONNECTION è impostato e l'URL è NULL, la funzione verifica se è presente una voce nel database del server per \_ \_ il server più \_ vicino.  Se ne esiste uno, la funzione esegue il ping del server.

Usare quindi la [**funzione InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) per stabilire le caratteristiche della connessione Internet utilizzata dall'applicazione client. [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) crea l'handle [**HINTERNET**](appendix-a-hinternet-handles.md) radice usato per stabilire [sessioni FTP HTTP.](http-sessions.md)[](ftp-sessions.md) [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) non testa la connessione a Internet per verificare che le caratteristiche passate alla funzione siano corrette.

Usare la [**funzione InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) per creare una sessione specifica. [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) inizializza una sessione per il sito specificato usando gli argomenti passati e crea un handle [**HINTERNET**](appendix-a-hinternet-handles.md) che è un ramo dell'handle radice. [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) non tenta di accedere o stabilire una connessione al sito specificato, tranne nel caso di una sessione FTP. [**Le funzioni FtpFindFirstFile,**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)e [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) usano l'handle creato da [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) per stabilire una connessione al sito specificato.

## <a name="using-internetopen"></a>Uso di InternetApri

Per abilitare una connessione a Internet, è necessario creare un handle [**HINTERNET**](appendix-a-hinternet-handles.md) radice usando [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena). Le informazioni sull'agente utente (l'applicazione che chiama le funzioni Internet), il tipo di accesso a Internet, i nomi proxy, gli host e gli indirizzi che ignorano il proxy e il comportamento vengono passati a [**InternetApri**](/windows/desktop/api/Wininet/nf-wininet-internetopena).

### <a name="setting-the-user-agent"></a>Impostazione dell'agente utente

L'applicazione chiamante deve fornire una stringa contenente il nome dell'applicazione o dell'entità che accede a Internet al parametro *lpszAgent* di [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena). Questa stringa viene usata come agente utente nel protocollo HTTP. Ad esempio, Microsoft Internet Explorer usa "Microsoft Internet Explorer".

### <a name="setting-access-types"></a>Impostazione dei tipi di accesso

[**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) supporta tre tipi di accesso:

-   Usare INTERNET OPEN TYPE DIRECT se il sistema in cui è in esecuzione l'applicazione \_ usa una connessione diretta a \_ \_ Internet. I *parametri lpszProxyName* e *lpszProxyBypass* di [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) non vengono usati e devono essere impostati su **NULL.**
-   Usare INTERNET OPEN TYPE PROXY se il sistema in cui è in esecuzione l'applicazione \_ usa uno o più server proxy per accedere a \_ \_ Internet. [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) usa i server proxy indicati da *lpszProxyName* e ignora il proxy per tutti i nomi host o gli indirizzi IP specificati da *lpszProxyBypass.*
-   Usare INTERNET \_ OPEN \_ TYPE \_ PRECONFIG per indicare all'applicazione di recuperare la configurazione dal Registro di sistema. Questa è in genere la scelta migliore, perché la maggior parte delle applicazioni, inclusi i Web browser, usa questa opzione.

INTERNET OPEN TYPE PRECONFIG esamina i valori del Registro \_ \_ di sistema \_ **ProxyEnable,** **ProxyServer** e **ProxyOverride.** Questi valori si trovano in "HKEY \_ CURRENT USER Software Microsoft Windows \_ \\ \\ \\ \\ CurrentVersion Internet \\ Impostazioni".

Se **ProxyEnable è** zero, l'applicazione usa INTERNET \_ OPEN TYPE \_ \_ DIRECT. In caso contrario, l'applicazione usa \_ INTERNET OPEN TYPE PROXY e usa le informazioni \_ \_ **ProxyServer** **e ProxyOverride.**

Le funzioni WinINet forniscono il supporto per i proxy di tipo SOCKS solo se Internet Explorer è installato. L'installazione Internet Explorer include il file Wsock32n.dll, necessario per supportare i proxy SOCKS. Wsock32n.dll non è ridistribuibile.

### <a name="listing-proxy-servers"></a>Elenco dei server proxy

WinINet riconosce due tipi di proxy: proxy di tipo CERN (solo HTTP) e proxy FTP TIS (solo FTP). Se Internet Explorer installato, WinINet supporta anche proxy di tipo SOCKS. [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) presuppone, per impostazione predefinita, che il proxy specificato sia un proxy CERN. Se il tipo di accesso è impostato su INTERNET OPEN TYPE DIRECT o \_ \_ INTERNET OPEN TYPE \_ \_ PRECONFIG, il parametro \_ \_ *lpszProxyName* di [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) deve essere impostato su **NULL.** In caso contrario, il valore passato a *lpszProxyName* deve contenere i proxy in una stringa delimitata da spazi. Gli elenchi di proxy possono contenere il numero di porta usato per accedere al proxy.

Per elencare un proxy per un protocollo specifico, la stringa deve seguire il formato "" <protocol> <protocol> ://<nome proxy \_>"". I protocolli validi sono HTTP, HTTPS e FTP. Ad esempio, per elencare un proxy FTP, una stringa valida sarebbe ""ftp=ftp://nome \_ proxy \_ ftp:21"", dove nome proxy ftp è il nome del proxy FTP e \_ 21 è il numero di porta che deve essere usato per accedere \_ al proxy. Se il proxy usa il numero di porta predefinito per il protocollo, il numero di porta può essere omesso. Se un nome proxy è elencato da solo, viene usato come proxy predefinito per tutti i protocolli per cui non è specificato un proxy specifico. Ad esempio, ""http= other"" userebbe il proxy HTTP per qualsiasi operazione HTTP, mentre tutti gli altri https://http\_proxy \_ protocolli ne userebbero altri.

Per impostazione predefinita, la funzione presuppone che il proxy specificato da *lpszProxyName* sia un proxy CERN. Un'applicazione può specificare più di un proxy, inclusi proxy diversi per i diversi protocolli. Ad esempio, se si specifica ""ftp=ftp://ftp-gw HTTP= proxy"", le richieste FTP vengono effettuate tramite il proxy ftp-gw, che è in ascolto sulla porta 21, e le richieste HTTP vengono effettuate tramite un proxy CERN denominato jericho, che è in ascolto sulla https://jericho:99 porta 99. In caso contrario, le richieste HTTP verrebbero effettuate tramite il proxy CERN denominato proxy, che è in ascolto sulla porta 80. Si noti che se l'applicazione usa solo FTP, ad esempio, non è necessario specificare ""ftp=ftp://ftp-gw:21"". Può specificare solo ""ftp-gw"". Un'applicazione deve specificare i nomi dei protocolli solo se usa più di un protocollo per ogni handle restituito da [**InternetApri**](/windows/desktop/api/Wininet/nf-wininet-internetopena).

### <a name="listing-the-proxy-bypass"></a>Elenco del bypass proxy

I nomi host o gli indirizzi IP che non devono essere inviati al proxy possono essere elencati nell'elenco di bypass del proxy. Questo elenco può contenere caratteri jolly, "", che causano il bypass del server proxy da parte dell'applicazione per gli \* indirizzi che si adattano al modello specificato. Per elencare più indirizzi e nomi host, separarli con punti e virgola nella stringa di bypass del proxy. Se viene specificata la macro "", la funzione ignora il proxy per <local> qualsiasi nome host che non contiene un punto.

Per impostazione predefinita, WinINet ignora il proxy per le richieste che usano i nomi host "localhost", "loopback", "127.0.0.1" o " \[ ::1 \] ". Questo comportamento si verifica perché un server proxy remoto in genere non risolve correttamente questi indirizzi.

**Internet Explorer 9:** È possibile rimuovere il computer locale dall'elenco di bypass proxy usando la macro "<-loopback>".

L'esempio seguente illustra le chiamate di esempio a [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) usando stringhe di bypass proxy diverse. I commenti precedenti a ogni chiamata descrivono l'effetto della stringa di bypass sui nomi host a cui si accede dall'handle [**HINTERNET**](appendix-a-hinternet-handles.md) creato.


```C++
HINTERNET hInternetRoot;

/* bypass the proxy for any host name that does not 
    contain a period */
hInternetRoot = InternetOpen(TEXT("WinInet Example"), 
    INTERNET_OPEN_TYPE_PROXY,TEXT("proxy"),TEXT("<local>"), 0);

/* bypass the proxy for any host name that starts with the 
    letters "ms" */
hInternetRoot = InternetOpen(TEXT("WinInet Example"), 
    INTERNET_OPEN_TYPE_PROXY,TEXT("proxy"),TEXT("ms*"), 0);

/* bypass the proxy for any host name that contains "int", 
    such as "internet" and "painter" */
hInternetRoot = InternetOpen(TEXT("WinInet Example"), 
    INTERNET_OPEN_TYPE_PROXY,TEXT("proxy"),TEXT("*int*"), 0);

/* bypass the proxy for the host name "example" and any 
    host name that contains "test" */
hInternetRoot = InternetOpen(TEXT("WinInet Example"), 
    INTERNET_OPEN_TYPE_PROXY,TEXT("proxy"),TEXT("example *test*"), 0);

/* Disable the loopback proxy bypass for localhost */
hInternetRoot = InternetOpen(TEXT("WinInet Example"), 
    INTERNET_OPEN_TYPE_PROXY,TEXT("127.0.0.1:8888"),TEXT("<-loopback>"), 0);
```



## <a name="using-internetconnect"></a>Uso di InternetConnect

Per avviare una sessione, la [**funzione InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) deve creare un handle dall'handle radice restituito dalla [**funzione InternetOpen.**](/windows/desktop/api/Wininet/nf-wininet-internetopena) [**InternetConnect imposta**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) l'indirizzo del server, il numero di porta, il nome utente, la password e il tipo di servizio.

[**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) usa l'handle [**HINTERNET**](appendix-a-hinternet-handles.md) radice creato da [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) per stabilire un handle di sessione. Se il flag [ \_ INTERNET FLAG \_ ASYNC](api-flags.md) è stato impostato nella chiamata a [**InternetOpen,**](/windows/desktop/api/Wininet/nf-wininet-internetopena)la chiamata a [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) deve includere un valore di contesto diverso da zero.

Il nome del server può contenere il nome host (ad esempio, "www.servername.com") o il numero IP del sito in formato ASCII virgolato decimale (ad esempio, "10.0.1.45").

La porta del server è Transmission Control Protocol/Internet Protocol (TCP/IP) a cui connettersi nel server. [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) usa la porta predefinita per il tipo di servizio selezionato se viene usato il valore \_ INTERNET INVALID PORT \_ \_ NUMBER. Le tabelle seguenti contengono le impostazioni predefinite delle porte del server per WinINet.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valore</th>
<th>Significato</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>INTERNET_DEFAULT_FTP_PORT</td>
<td>Usare la porta predefinita per i server ftp (porta 21).</td>
</tr>
<tr class="even">
<td>INTERNET_DEFAULT_GOPHER_PORT</td>
<td>Usare la porta predefinita per i server gopher (porta 70).
<blockquote>
[!Note]<br />
Windows SOLO XP e Windows Server 2003 R2 e versioni precedenti.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>INTERNET_DEFAULT_HTTP_PORT</td>
<td>Usare la porta predefinita per i server HTTP (porta 80).</td>
</tr>
<tr class="even">
<td>INTERNET_DEFAULT_HTTPS_PORT</td>
<td>Usare la porta predefinita per i server https (porta 443).</td>
</tr>
<tr class="odd">
<td>INTERNET_DEFAULT_SOCKS_PORT</td>
<td>Usare la porta predefinita per i server firewall SOCKS (porta 1080).</td>
</tr>
</tbody>
</table>



 

### <a name="defining-the-user-name-and-password"></a>Definizione di nome utente e password

Il valore *di lpszUsername* è l'indirizzo di una stringa con terminazione **Null** che contiene il nome dell'utente che sta accedendo. Se questo parametro è **NULL,** la funzione usa un valore predefinito appropriato, ad eccezione di HTTP. Un **parametro NULL** in HTTP causa la restituzione di un errore da parte del server. Per il protocollo FTP, il valore predefinito è anonimo.

Il valore di *lpszPassword* è l'indirizzo di una stringa con terminazione **Null** che contiene la password di accesso. Se sia *lpszUsername che* *lpszPassword* sono **NULL,** la funzione usa la password anonima predefinita. Nel caso di FTP, la password anonima predefinita è il nome di posta elettronica dell'utente. Se *lpszUsername* non è **NULL** e *lpszPassword* è **NULL,** la funzione usa una password vuota. Esistono quattro possibili impostazioni di *lpszUsername* e *lpszPassword*, che producono i comportamenti illustrati nella tabella seguente.



| *lpszUsername*      | *lpszPassword*      | Nome utente inviato al server FTP | Password inviata al server FTP |
|---------------------|---------------------|------------------------------|-----------------------------|
| **NULL**            | **NULL**            | "anonymous"                  | Nome di posta elettronica dell'utente           |
| Stringa non **NULL** | **NULL**            | *lpszUsername*               | ""                          |
| **NULL**            | Stringa non **NULL** | ERRORE                        | ERRORE                       |
| Stringa non **NULL** | Stringa non **NULL** | *lpszUsername*               | *lpszPassword*              |



 

Queste informazioni possono essere modificate usando le [**funzioni InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) [**e InternetErrorDlg.**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) [**InternetSetOption modifica**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) i valori di nome utente e password, mentre [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) visualizza una finestra di dialogo che richiede il nome utente e la password appropriati.

### <a name="defining-the-session"></a>Definizione della sessione

Per definire la sessione da stabilire, impostare il tipo di servizio, i flag e il valore di contesto per [**InternetConnect.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)

Sono disponibili due tipi di servizio per [**InternetConnect:**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)INTERNET \_ SERVICE FTP e INTERNET SERVICE \_ \_ \_ HTTP. INTERNET \_ SERVICE HTTP viene usato per le sessioni HTTP e \_ HTTPS.

[INTERNET \_ FLAG \_ PASSIVE](api-flags.md) è l'unico flag specifico del servizio usato dalle funzioni WinINet. Questo flag può essere impostato quando il tipo di servizio è \_ INTERNET SERVICE FTP per usare la \_ semantica FTP passiva.

Per tutte le operazioni sincrone, il valore *di dwContext* deve essere impostato su zero. Se le operazioni asincrone sono state stabilite impostando il flag [ \_ \_ ASYNC DEL](api-flags.md) FLAG INTERNET nella chiamata a [**InternetOpen,**](/windows/desktop/api/Wininet/nf-wininet-internetopena)per *dwContext* deve essere specificato un valore diverso da zero. Per altre informazioni sulle operazioni asincrone, vedere [Impostazione di operazioni asincrone](common-functions.md).

Per le sessioni FTP, [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) tenta di stabilire una connessione al server su Internet. Per le sessioni HTTP, [**InternetConnect non**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) stabilisce una connessione fino a quando un'altra funzione non tenta di ottenere informazioni dal server.

> [!Note]  
> WinINet non supporta le implementazioni del server. Inoltre, non deve essere usato da un servizio. Per le implementazioni o i servizi del server usare [Microsoft Windows servizi HTTP (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

