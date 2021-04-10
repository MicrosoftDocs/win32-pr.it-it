---
title: Abilitazione della funzionalità Internet
description: Prima di utilizzare le funzioni WinINet, l'applicazione deve tentare di effettuare una connessione a Internet tramite la funzione InternetAttemptConnect.
ms.assetid: 80747c0d-5a09-4ffa-a0ca-b051b82acbf8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adb44fadaf0726b81618dde19105da7517673a00
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047227"
---
# <a name="enabling-internet-functionality"></a>Abilitazione della funzionalità Internet

Prima di utilizzare le funzioni WinINet, l'applicazione deve tentare di effettuare una connessione a Internet tramite la funzione [**InternetAttemptConnect**](/windows/desktop/api/Wininet/nf-wininet-internetattemptconnect) . Questa funzione chiama la finestra di dialogo di connessione remota per avviare una connessione a Internet o controllare se esiste già una connessione. Se questa funzione ha esito negativo, l'applicazione può accedere alla modalità offline, che consente di accedere alle informazioni memorizzate nella cache durante le connessioni precedenti a Internet.

Utilizzare la funzione [**InternetCheckConnection**](/windows/desktop/api/Wininet/nf-wininet-internetcheckconnectiona) per verificare la connessione a Internet. Tenta di effettuare il ping del server designato dall'URL passato alla funzione. Se \_ viene impostato il flag di connessione del flag ICC \_ Force \_ e l'URL è **null**, la funzione verifica se è presente una voce nel database del server per il server più vicino. Se ne esiste una, la funzione effettua il ping del server.

Utilizzare quindi la funzione [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) per stabilire le caratteristiche della connessione Internet utilizzata dall'applicazione client. [**Internetopn**](/windows/desktop/api/Wininet/nf-wininet-internetopena) crea l'handle [**HINTERNET**](appendix-a-hinternet-handles.md) radice utilizzato per stabilire sessioni FTP [http](http-sessions.md)[](ftp-sessions.md) . [**Internetopn**](/windows/desktop/api/Wininet/nf-wininet-internetopena) non verifica la connessione a Internet per verificare che le caratteristiche passate alla funzione siano corrette.

Usare la funzione [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) per creare una sessione specifica. [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) Inizializza una sessione per il sito specificato usando gli argomenti passati e crea un handle [**HINTERNET**](appendix-a-hinternet-handles.md) che è un ramo dall'handle radice. [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) non tenta di accedere o stabilire una connessione al sito specificato, tranne nel caso di una sessione FTP. Le funzioni [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)e [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) usano l'handle creato da [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) per stabilire una connessione al sito specificato.

## <a name="using-internetopen"></a>Uso di InternetOpen

Per abilitare una connessione a Internet, è necessario creare un handle [**HINTERNET**](appendix-a-hinternet-handles.md) radice usando [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena). Informazioni sull'agente utente (l'applicazione che chiama le funzioni Internet), il tipo di accesso a Internet, i nomi dei proxy, gli host e gli indirizzi che ignorano il proxy e il comportamento vengono passati a [**Internetopn**](/windows/desktop/api/Wininet/nf-wininet-internetopena).

### <a name="setting-the-user-agent"></a>Impostazione dell'agente utente

L'applicazione chiamante deve assegnare a una stringa che contiene il nome dell'applicazione o dell'entità che accede a Internet al parametro *lpszAgent* di [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena). Questa stringa viene utilizzata come agente utente nel protocollo HTTP. Ad esempio, in Microsoft Internet Explorer viene utilizzato "Microsoft Internet Explorer".

### <a name="setting-access-types"></a>Impostazione di tipi di accesso

[**Internetopn**](/windows/desktop/api/Wininet/nf-wininet-internetopena) supporta tre tipi di accesso:

-   USA INTERNET \_ Open \_ Type \_ Direct se il sistema in cui è in esecuzione l'applicazione usa una connessione diretta a Internet. I parametri *lpszProxyName* e *LpszProxyBypass* di [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) non vengono usati e devono essere impostati su **null**.
-   Utilizzare il \_ \_ proxy di tipo Internet aperto \_ se il sistema in cui viene eseguita l'applicazione utilizza uno o più server proxy per accedere a Internet. [**Internetopn**](/windows/desktop/api/Wininet/nf-wininet-internetopena) usa i server proxy indicati da *lpszProxyName* e ignora il proxy per qualsiasi nome host o indirizzo IP specificato da *lpszProxyBypass*.
-   Utilizzare la \_ \_ preconfigurazione di tipo Internet Open \_ per indicare all'applicazione di recuperare la configurazione dal registro di sistema. Si tratta in genere della scelta migliore, perché la maggior parte delle applicazioni che includono i Web browser utilizzano questa opzione.

\_ \_ La preconfigurazione di Internet Open Type \_ esamina i valori del registro di sistema **ProxyEnable**, **ProxyServer** e **ProxyOverride**. Questi valori si trovano in "HKEY \_ Current \_ User \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Internet Settings".

Se **ProxyEnable** è zero, l'applicazione usa Internet \_ Open \_ Type \_ Direct. In caso contrario, l'applicazione \_ Usa \_ \_ il proxy di tipo Internet Open e usa le informazioni **ProxyServer** e **ProxyOverride** .

Le funzioni WinINet forniscono supporto per i proxy di tipo SOCKS solo se è installato Internet Explorer. L'installazione di Internet Explorer include il file di Wsock32n.dll, che è necessario per supportare i proxy SOCKS. Wsock32n.dll non è ridistribuibile.

### <a name="listing-proxy-servers"></a>Elenco di server proxy

WinINet riconosce due tipi di proxy: proxy di tipo CERN (solo HTTP) e proxy FTP TIS (solo FTP). Se Internet Explorer è installato, WinINet supporta anche i proxy di tipo SOCKS. Per impostazione predefinita, [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) presuppone che il proxy specificato sia un proxy CERN. Se il tipo di accesso è impostato su \_ Internet Open \_ Type \_ Direct o Internet \_ Open \_ Type \_ preconfig, il parametro *lpszProxyName* di [**internetopn**](/windows/desktop/api/Wininet/nf-wininet-internetopena) deve essere impostato su **null**. In caso contrario, il valore passato a *lpszProxyName* deve contenere i proxy in una stringa delimitata da spazi. Gli elenchi proxy possono contenere il numero di porta utilizzato per accedere al proxy.

Per elencare un proxy per un protocollo specifico, la stringa deve seguire il formato "" <protocol> <protocol> ://<\_ nome proxy> "". I protocolli validi sono HTTP, HTTPS e FTP. Ad esempio, per elencare un proxy FTP, una stringa valida è "" FTP = FTP://FTP \_ \_ nome proxy: 21 "", dove \_ nome proxy FTP \_ è il nome del proxy FTP e 21 è il numero di porta che deve essere usato per accedere al proxy. Se il proxy usa il numero di porta predefinito per quel protocollo, il numero di porta può essere omesso. Se il nome di un proxy è elencato da solo, viene usato come proxy predefinito per i protocolli per i quali non è specificato un proxy specifico. Ad esempio, "" http = https://http\_proxy other "" utilizzerebbe il \_ proxy HTTP per qualsiasi operazione http, mentre tutti gli altri protocolli useranno altri.

Per impostazione predefinita, la funzione presuppone che il proxy specificato da *lpszProxyName* sia un proxy CERN. Un'applicazione può specificare più di un proxy, inclusi proxy diversi per i diversi protocolli. Se ad esempio si specifica "" FTP = FTP://FTP-GW HTTP = https://jericho:99 proxy "", le richieste FTP vengono effettuate tramite il proxy FTP-GW, che è in ascolto sulla porta 21 e le richieste HTTP vengono effettuate tramite un proxy CERN chiamato Jericho, che è in ascolto sulla porta 99. In caso contrario, le richieste HTTP vengono effettuate tramite il proxy CERN denominato proxy, che è in ascolto sulla porta 80. Si noti che se l'applicazione usa solo FTP, ad esempio, non è necessario specificare "" FTP = FTP://FTP-GW: 21 "". Potrebbe specificare solo "" FTP-GW "". Un'applicazione è necessaria solo per specificare i nomi di protocollo se usa più di un protocollo per handle restituito da [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).

### <a name="listing-the-proxy-bypass"></a>Elenco del bypass proxy

I nomi host o gli indirizzi IP che non devono essere inviati al proxy possono essere elencati nell'elenco proxy bypass. Questo elenco può contenere caratteri jolly, " \* ", che fanno sì che l'applicazione ignori il server proxy per gli indirizzi che soddisfano il criterio specificato. Per elencare più indirizzi e nomi host, separarli con punti e virgola nella stringa di bypass del proxy. Se <local> viene specificata la macro "", la funzione ignora il proxy per qualsiasi nome host che non contiene un punto.

Per impostazione predefinita, WinINet ignorerà il proxy per le richieste che utilizzano i nomi host "localhost", "loopback", "127.0.0.1" o " \[ :: 1 \] ". Questo comportamento è dovuto al fatto che un server proxy remoto non risolve questi indirizzi in modo corretto.

**Internet Explorer 9:** È possibile rimuovere il computer locale dall'elenco proxy bypass usando la macro "<-loopback>".

Nell'esempio seguente vengono illustrate le chiamate di esempio a [**Internetopn**](/windows/desktop/api/Wininet/nf-wininet-internetopena) usando stringhe di bypass proxy diverse. I commenti sopra ogni chiamata descrivono l'effetto della stringa di bypass sui nomi host a cui si accede dall'handle [**HINTERNET**](appendix-a-hinternet-handles.md) creato.


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

Per iniziare una sessione, la funzione [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) deve creare un handle dall'handle radice restituito dalla funzione [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) . [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) imposta l'indirizzo del server, il numero di porta, il nome utente, la password e il tipo di servizio.

[**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) usa l'handle [**HINTERNET**](appendix-a-hinternet-handles.md) radice creato da [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) per stabilire un handle di sessione. Se il flag di [ \_ flag \_ asincrono Internet](api-flags.md) è stato impostato nella chiamata a [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena), la chiamata a [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) deve includere un valore di contesto diverso da zero.

Il nome del server può contenere il nome host (ad esempio, "www.servername.com") o il numero IP del sito in formato ASCII punteggiato-decimale (ad esempio, "10.0.1.45").

La porta del server è il numero di porta TCP/IP (Transmission Control Protocol/Internet Protocol) a cui connettersi nel server. [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) utilizza la porta predefinita per il tipo di servizio selezionato se \_ viene utilizzato il valore del numero di porta non valido Internet \_ \_ . Le tabelle seguenti contengono le impostazioni predefinite della porta del server per WinINet.



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
<td>Utilizzare la porta predefinita per i server FTP (porta 21).</td>
</tr>
<tr class="even">
<td>INTERNET_DEFAULT_GOPHER_PORT</td>
<td>Utilizzare la porta predefinita per i server Gopher (porta 70).
<blockquote>
[!Note]<br />
Windows XP e Windows Server 2003 R2 e versioni precedenti.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>INTERNET_DEFAULT_HTTP_PORT</td>
<td>Utilizzare la porta predefinita per i server http (porta 80).</td>
</tr>
<tr class="even">
<td>INTERNET_DEFAULT_HTTPS_PORT</td>
<td>Utilizzare la porta predefinita per i server HTTPS (porta 443).</td>
</tr>
<tr class="odd">
<td>INTERNET_DEFAULT_SOCKS_PORT</td>
<td>Usare la porta predefinita per i server del firewall SOCKS (porta 1080).</td>
</tr>
</tbody>
</table>



 

### <a name="defining-the-user-name-and-password"></a>Definizione del nome utente e della password

Il valore di *lpszUsername* è l'indirizzo di una stringa con terminazione **null** che contiene il nome dell'utente che esegue l'accesso. Se questo parametro è **null**, la funzione userà un valore predefinito appropriato, ad eccezione di http. Un parametro **null** in http fa in modo che il server restituisca un errore. Per il protocollo FTP, il valore predefinito è anonimo.

Il valore di *lpszPassword* è l'indirizzo di una stringa con terminazione **null** che contiene la password di accesso. Se *lpszUsername* e *LpszPassword* sono entrambi **null**, la funzione userà la password anonima predefinita. Nel caso di FTP, la password anonima predefinita corrisponde al nome di posta elettronica dell'utente. Se *lpszUsername* non è **null** e *lpszPassword* è **null**, la funzione userà una password vuota. Sono disponibili quattro possibili impostazioni di *lpszUsername* e *lpszPassword*, che producono i comportamenti illustrati nella tabella seguente.



| *lpszUsername*      | *lpszPassword*      | Nome utente inviato al server FTP | Password inviata al server FTP |
|---------------------|---------------------|------------------------------|-----------------------------|
| **NULL**            | **NULL**            | Anonimo                  | Nome di posta elettronica dell'utente           |
| Stringa non **null** | **NULL**            | *lpszUsername*               | ""                          |
| **NULL**            | Stringa non **null** | ERRORE                        | ERRORE                       |
| Stringa non **null** | Stringa non **null** | *lpszUsername*               | *lpszPassword*              |



 

Queste informazioni possono essere modificate usando le funzioni [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) e [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) . [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) modifica i valori di nome utente e password, mentre [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) Visualizza una finestra di dialogo che richiede il nome utente e la password appropriati.

### <a name="defining-the-session"></a>Definizione della sessione

Per definire la sessione stabilita, impostare il tipo di servizio, i flag e il valore di contesto per [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).

Per [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)sono disponibili due tipi di servizio: \_ FTP servizio Internet \_ e \_ http servizio Internet \_ . Il \_ servizio Internet \_ http viene usato per le sessioni HTTP e HTTPS.

[Internet \_ FLAG \_ passive](api-flags.md) è l'unico flag specifico del servizio usato dalle funzioni WinInet. Questo flag può essere impostato quando il tipo di servizio è \_ FTP servizio Internet per \_ utilizzare la semantica FTP passiva.

Per tutte le operazioni sincrone, il valore di *dwContext* deve essere impostato su zero. Se le operazioni asincrone sono state stabilite impostando il flag del [ \_ flag \_ asincrono per Internet](api-flags.md) nella chiamata a [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena), è necessario specificare un valore diverso da zero per *dwContext*. Per ulteriori informazioni sulle operazioni asincrone, vedere [configurazione di operazioni asincrone](common-functions.md).

Per le sessioni FTP, [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) tenta di stabilire una connessione al server su Internet. Per le sessioni HTTP, [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) non stabilisce una connessione finché un'altra funzione non tenta di ottenere informazioni dal server.

> [!Note]  
> WinINet non supporta le implementazioni del server. Inoltre, non deve essere utilizzato da un servizio. Per le implementazioni o i servizi del server, usare i [Servizi http di Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

