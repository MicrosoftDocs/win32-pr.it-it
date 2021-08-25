---
description: L'elenco seguente fornisce descrizioni concise di ogni funzione Winsock. Per altre informazioni su qualsiasi funzione, fare clic sul nome della funzione.
ms.assetid: edafb5f9-09fe-4f8e-9651-4002b6f622f4
title: Funzioni Winsock
ms.topic: article
ms.date: 10/01/2019
ms.openlocfilehash: 5057a2fa7ff113da3c8e5f9077f9dfb1df83c3a390546b9d49d2d4b94db3625e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860721"
---
# <a name="winsock-functions"></a>Funzioni Winsock

L'elenco seguente fornisce descrizioni concise di ogni funzione Winsock. Per altre informazioni su qualsiasi funzione, fare clic sul nome della funzione.

| Funzione | Descrizione |
|-|-|
| [**Accettare**](/windows/win32/api/Winsock2/nf-winsock2-accept) | Consente un tentativo di connessione in ingresso su un socket. |
| [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex) | Accetta una nuova connessione, restituisce l'indirizzo locale e remoto e riceve il primo blocco di dati inviato dall'applicazione client. |
| [**Associare**](/windows/win32/api/winsock/nf-winsock-bind) | Associa un indirizzo locale a un socket. |
| [**closesocket**](/windows/win32/api/winsock/nf-winsock-closesocket) | Chiude un socket esistente. |
| [**connettersi**](/windows/win32/api/Winsock2/nf-winsock2-connect) | Stabilisce una connessione a un socket specificato. |
| [**ConnectEx**](/windows/win32/api/Mswsock/nc-mswsock-lpfn_connectex) | Stabilisce una connessione a un socket specificato e facoltativamente invia i dati una volta stabilita la connessione. Supportato solo nei socket orientati alla connessione. |
| [**DisconnectEx**](/previous-versions/windows/desktop/legacy/ms737757(v=vs.85)) | Chiude una connessione in un socket e consente di riutilizzare l'handle del socket. |
| [**EnumProtocols**](/windows/win32/api/Nspapi/nf-nspapi-enumprotocolsa) | Recupera informazioni su un set specificato di protocolli di rete attivi in un host locale. |
| [**freeaddrinfo**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfo) | Libera le informazioni sull'indirizzo che la [**funzione getaddrinfo alloca**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) dinamicamente nelle [**strutture addrinfo.**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) |
| [**FreeAddrInfoEx**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfoex) | Libera le informazioni sull'indirizzo che la [**funzione GetAddrInfoEx**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa) alloca dinamicamente nelle [**strutture addrinfoex.**](/windows/win32/api/Ws2def/ns-ws2def-addrinfoexw) |
| [**FreeAddrInfoW**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfow) | Libera le informazioni sugli indirizzi che la [**funzione GetAddrInfoW**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfow) alloca dinamicamente nelle [**strutture addrinfoW.**](/windows/win32/api/Ws2def/ns-ws2def-addrinfow) |
| [**gai \_ strerror**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-gai_strerrora) | Assiste nella stampa dei messaggi di errore in base a errori EAI \_ \* restituiti dalla [**funzione getaddrinfo.**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) |
| [**GetAcceptExSockaddrs**](/windows/win32/api/mswsock/nf-mswsock-getacceptexsockaddrs) | Analizza i dati ottenuti da una chiamata alla [**funzione AcceptEx.**](/windows/win32/api/mswsock/nf-mswsock-acceptex) |
| [**GetAddressByName**](/windows/win32/api/Nspapi/nf-nspapi-getaddressbynamea) | Esegue una query su uno spazio dei nomi o su un set di spazi dei nomi predefiniti per recuperare le informazioni sull'indirizzo di rete per un servizio di rete specificato. Questo processo è noto come risoluzione dei nomi di servizio. Un servizio di rete può anche usare la funzione per ottenere informazioni sull'indirizzo locale che può usare con la [**funzione bind.**](/windows/win32/api/winsock/nf-winsock-bind) |
| [**getaddrinfo**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) | Fornisce la conversione indipendente dal protocollo da un nome host ANSI a un indirizzo. |
| [**GetAddrInfoEx**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa) | Fornisce la risoluzione dei nomi indipendente dal protocollo con parametri aggiuntivi per qualificare i provider di spazi dei nomi che devono gestire la richiesta. |
| [**GetAddrInfoExCancel**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexcancel) | Annulla un'operazione asincrona tramite [**la funzione GetAddrInfoEx.**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa) |
| [**GetAddrInfoExOverlappedResult**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexoverlappedresult) | Ottiene il codice restituito per una **struttura OVERLAPPED** utilizzata da un'operazione asincrona per la [**funzione GetAddrInfoEx.**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa) |
| [**GetAddrInfoW**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfow) | Fornisce la conversione indipendente dal protocollo da un nome host Unicode a un indirizzo. |
| [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) | Recupera le informazioni sull'host corrispondenti a un indirizzo di rete. |
| [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) | Recupera le informazioni sull'host corrispondenti a un nome host da un database host. Deprecato: usare [**invece getaddrinfo.**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) |
| [**gethostname**](/windows/win32/api/winsock/nf-winsock-gethostname) | Recupera il nome host standard per il computer locale. |
| [**GetHostNameW**](/windows/win32/api/Winsock2/nf-winsock2-gethostnamew) | Recupera il nome host standard per il computer locale come stringa Unicode. |
| [**getipv4sourcefilter**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getipv4sourcefilter) | Recupera lo stato del filtro multicast per un socket IPv4. |
| [**GetNameByType**](/windows/win32/api/Nspapi/nf-nspapi-getnamebytypea) | Recupera il nome di un servizio di rete per il tipo di servizio specificato. |
| [**getnameinfo**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) | Fornisce la risoluzione dei nomi da un indirizzo IPv4 o IPv6 a un nome host ANSI e da un numero di porta al nome del servizio ANSI. |
| [**GetNameInfoW**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getnameinfow) | Fornisce la risoluzione dei nomi da un indirizzo IPv4 o IPv6 a un nome host Unicode e da un numero di porta al nome del servizio Unicode. |
| [**getpeername**](/windows/win32/api/winsock/nf-winsock-getpeername) | Recupera l'indirizzo del peer a cui è connesso un socket. |
| [**getprotobyname**](/windows/win32/api/winsock/nf-winsock-getprotobyname) | Recupera le informazioni sul protocollo corrispondenti a un nome di protocollo. |
| [**getprotobynumber**](/windows/win32/api/winsock/nf-winsock-getprotobynumber) | Recupera le informazioni sul protocollo corrispondenti a un numero di protocollo. |
| [**getservbyname**](/windows/win32/api/winsock/nf-winsock-getservbyname) | Recupera le informazioni sul servizio corrispondenti a un nome di servizio e a un protocollo. |
| [**getservbyport**](/windows/win32/api/winsock/nf-winsock-getservbyport) | Recupera le informazioni sul servizio corrispondenti a una porta e a un protocollo. |
| [**GetService**](/windows/win32/api/Nspapi/nf-nspapi-getservicea) | Recupera informazioni su un servizio di rete nel contesto di un set di spazi dei nomi predefiniti o di uno spazio dei nomi specificato. |
| [**getsockname**](/windows/win32/api/winsock/nf-winsock-getsockname) | Recupera il nome locale per un socket. |
| [**getsockopt**](/windows/win32/api/winsock/nf-winsock-getsockopt) | Recupera un'opzione socket. |
| [**getsourcefilter**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getsourcefilter) | Recupera lo stato del filtro multicast per un socket IPv4 o IPv6. |
| [**GetTypeByName**](/windows/win32/api/Nspapi/nf-nspapi-gettypebynamea) | Recupera un GUID del tipo di servizio per un servizio di rete specificato in base al nome. |
| [**htond**](/windows/win32/api/Winsock2/nf-winsock2-htond) | Converte un **valore double dall'host** all'ordine dei byte di rete TCP/IP (big-endian). |
| [**htonf**](/windows/win32/api/Winsock2/nf-winsock2-htonf) | Converte un **float dall'host** all'ordine dei byte di rete TCP/IP (big-endian). |
| [**htonl**](/windows/win32/api/winsock/nf-winsock-htonl) | Converte un **valore u \_ long dall'host** all'ordine dei byte di rete TCP/IP (big-endian). |
| [**htonll**](/windows/win32/api/Winsock2/nf-winsock2-htonll) | Converte un **\_ \_ int64 senza** segno dall'host all'ordine dei byte di rete TCP/IP (big-endian). |
| [**hton**](/windows/win32/api/winsock/nf-winsock-htons) | Converte un **valore u \_ short dall'host** all'ordine dei byte di rete TCP/IP (big-endian). |
| [**inet \_ addr**](/windows/win32/api/winsock2/nf-winsock2-inet_addr) | Converte una stringa contenente un indirizzo (Ipv4) tratteggiato del protocollo Internet in un indirizzo appropriato per la [**struttura in \_ addr.**](/windows/win32/api/winsock2/ns-winsock2-in_addr) |
| [**inet \_ ntoa**](/windows/win32/api/winsock2/nf-winsock2-inet_ntoa) | Converte un indirizzo di rete Internet (IPv4) in una stringa in formato punto standard Internet. |
| [**InetNtop**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-inetntopw) | converte un indirizzo di rete Internet IPv4 o IPv6 in una stringa in formato Standard Internet. La versione ANSI di questa funzione è [**inet \_ ntop**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-inetntopw). |
| [**InetPton**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-inetptonw) | Converte un indirizzo di rete Internet IPv4 o IPv6 nel formato di presentazione di testo standard nel formato binario numerico. La versione ANSI di questa funzione è [**inet \_ pton**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-inetptonw). |
| [**ioctlsocket**](/windows/win32/api/winsock/nf-winsock-ioctlsocket) | Controlla la modalità di I/O di un socket. |
| [**Ascolta**](/windows/win32/api/Winsock2/nf-winsock2-listen) | Inserisce un socket in uno stato in cui è in ascolto di una connessione in ingresso. |
| [**ntohd**](/windows/win32/api/Winsock2/nf-winsock2-ntohd) | Converte un **valore \_ \_ int64** senza segno dall'ordine di rete TCP/IP all'ordine dei byte dell'host (ovvero little endian nei processori Intel) e restituisce **un valore double.** |
| [**ntohf**](/windows/win32/api/Winsock2/nf-winsock2-ntohf) | Converte un **valore \_ \_ int32** senza segno dall'ordine di rete TCP/IP all'ordine dei byte dell'host (ovvero little endian nei processori Intel) e restituisce un **valore float.** |
| [**ntohl**](/windows/win32/api/winsock/nf-winsock-ntohl) | Converte un u long dall'ordine di rete TCP/IP all'ordine dei \_ byte dell'host (ovvero little endian nei processori Intel). |
| [**ntohll**](/windows/win32/api/Winsock2/nf-winsock2-ntohll) | Converte un **valore \_ \_ int64** senza segno dall'ordine di rete TCP/IP all'ordine dei byte dell'host (ovvero little endian nei processori Intel). |
| [**ntohs**](/windows/win32/api/winsock/nf-winsock-ntohs) | Converte un valore u short dall'ordine dei byte della rete TCP/IP all'ordine dei \_ byte dell'host (ovvero little endian nei processori Intel). |
| [**Recv**](/windows/win32/api/winsock/nf-winsock-recv) | Riceve dati da un socket connesso o associato. |
| [**recvfrom**](/windows/win32/api/winsock/nf-winsock-recvfrom) | Riceve un datagramma e archivia l'indirizzo di origine. |
| [**RIOCloseCompletionQueue**](/previous-versions/windows/desktop/legacy/hh448837(v=vs.85)) | Chiude una coda di completamento esistente usata per la notifica di completamento dell'I/O inviando e ricevendo richieste con le estensioni di I/O registrate in Winsock. |
| [**RIOCreateCompletionQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion) | Crea una coda di completamento I/O di una dimensione specifica da usare con le estensioni di I/O registrate in Winsock. |
| [**RIOCreateRequestQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue) | Crea un descrittore di socket di I/O registrato usando un socket specificato e le code di completamento I/O da usare con le estensioni di I/O registrate winsock. |
| [**RIODequeueCompletion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion) | Rimuove le voci da una coda di completamento I/O da usare con le estensioni di I/O registrate in Winsock. |
| [**RIODeregisterBuffer**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer) | Annulla la registrazione di un buffer registrato usato con le estensioni di I/O registrate in Winsock. |
| [**RIONotify**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify) | Registra il metodo da usare per il comportamento delle notifiche con una coda di completamento I/O da usare con le estensioni di I/O registrate in Winsock. |
| [**RIOReceive**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceive) | Riceve i dati di rete su un socket TCP I/O registrato connesso o su un socket UDP di I/O registrato associato da usare con le estensioni di I/O registrate winsock. |
| [**RIOReceiveEx**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceiveex) | Riceve i dati di rete su un socket TCP I/O registrato connesso o su un socket UDP di I/O registrato associato con opzioni aggiuntive da usare con le estensioni di I/O registrate winsock. |
| [**RIORegisterBuffer**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85)) | Registra un [**\_ BUFFERID RIO,**](rio-bufferid.md)un descrittore di buffer registrato, con un buffer specificato da usare con le estensioni di I/O registrate di Winsock. |
| [**RIOResizeCompletionQueue**](/previous-versions/windows/desktop/legacy/hh437202(v=vs.85)) | Ridimensiona una coda di completamento I/O in modo che sia più grande o più piccola per l'uso con le estensioni di I/O registrate in Winsock. |
| [**RIOResizeRequestQueue**](/previous-versions/windows/desktop/legacy/hh437204(v=vs.85)) | Ridimensiona una coda di richieste in modo che sia più grande o più piccola per l'uso con le estensioni di I/O registrate winsock. |
| [**RIOSEND**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riosend) | Invia i dati di rete su un socket TCP I/O registrato connesso o su un socket UDP di I/O registrato associato da usare con le estensioni di I/O registrate winsock. |
| [**RIOSendEx**](/previous-versions/windows/desktop/legacy/hh437216(v=vs.85)) | Invia i dati di rete su un socket TCP I/O registrato connesso o su un socket UDP di I/O registrato associato con opzioni aggiuntive da usare con le estensioni di I/O registrate winsock. |
| [**Selezionare**](/windows/win32/api/Winsock2/nf-winsock2-select) | Determina lo stato di uno o più socket, in attesa, se necessario, di eseguire operazioni di I/O sincrone. |
| [**Invia**](/windows/win32/api/Winsock2/nf-winsock2-send) | Invia dati su un socket connesso. |
| [**Sendto**](/windows/win32/api/winsock/nf-winsock-sendto) | Invia dati a una destinazione specifica. |
| [**SetAddrInfoEx**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-setaddrinfoexa) | Registra un host e un nome di servizio insieme agli indirizzi associati con un provider dello spazio dei nomi specifico. |
| [**setipv4sourcefilter**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-setipv4sourcefilter) | Imposta lo stato del filtro multicast per un socket IPv4. |
| [**SetService**](/windows/win32/api/Nspapi/nf-nspapi-setservicea) | Registra o rimuove dal Registro di sistema un servizio di rete all'interno di uno o più spazi dei nomi. Può anche aggiungere o rimuovere un tipo di servizio di rete all'interno di uno o più spazi dei nomi. |
| [**SetSocketMediaStreamingMode**](/windows/win32/api/Socketapi/nf-socketapi-setsocketmediastreamingmode) | Indica se la rete deve essere utilizzata per il trasferimento di file multimediali di streaming che richiedono qualità del servizio. |
| [**Setsockopt**](/windows/win32/api/winsock/nf-winsock-setsockopt) | Imposta un'opzione socket. |
| [**setsourcefilter**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-setsourcefilter) | Imposta lo stato del filtro multicast per un socket IPv4 o IPv6. |
| [**Arresto**](/windows/win32/api/winsock/nf-winsock-shutdown) | Disabilita gli invii o le ricevute su un socket. |
| [**Socket**](/windows/win32/api/Winsock2/nf-winsock2-socket) | Crea un socket associato a un provider di servizi specifico. |
| [**Transmitfile**](/windows/win32/api/mswsock/nf-mswsock-transmitfile) | Trasmette i dati dei file su un handle di socket connesso. |
| [**TransmitPackets**](/windows/win32/api/Mswsock/nc-mswsock-lpfn_transmitpackets) | Trasmette dati in memoria o dati di file su un socket connesso. |
| [**WSAAccept**](/windows/win32/api/Winsock2/nf-winsock2-wsaaccept) | Accetta in modo condizionale una connessione basata sul valore restituito di una funzione di condizione, fornisce le specifiche di qualità del flusso del servizio e consente il trasferimento dei dati di connessione. |
| [**WSAAddressToString**](/windows/win32/api/Winsock2/nf-winsock2-wsaaddresstostringa) | Converte tutti i componenti di una [**struttura sockaddr**](sockaddr-2.md) in una rappresentazione di stringa leggibile dell'indirizzo. |
| [**WSAAsyncGetHostByAddr**](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyaddr) | Recupera in modo asincrono le informazioni sull'host che corrispondono a un indirizzo. |
| [**WSAAsyncGetHostByName**](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyname) | Recupera in modo asincrono le informazioni sull'host che corrispondono a un nome host. |
| [**WSAAsyncGetProtoByName**](/windows/win32/api/winsock/nf-winsock-wsaasyncgetprotobyname) | Recupera in modo asincrono le informazioni sul protocollo che corrispondono a un nome di protocollo. |
| [**WSAAsyncGetProtoByNumber**](/windows/win32/api/winsock/nf-winsock-wsaasyncgetprotobynumber) | Recupera in modo asincrono le informazioni sul protocollo che corrispondono a un numero di protocollo. |
| [**WSAAsyncGetServByName**](/windows/win32/api/winsock/nf-winsock-wsaasyncgetservbyname) | Recupera in modo asincrono le informazioni sul servizio che corrispondono a un nome di servizio e a una porta. |
| [**WSAAsyncGetServByPort**](/windows/win32/api/winsock/nf-winsock-wsaasyncgetservbyport) | Recupera in modo asincrono le informazioni sul servizio che corrispondono a una porta e a un protocollo. |
| [**WSAAsyncSelect**](/windows/win32/api/winsock/nf-winsock-wsaasyncselect) | Richiede Windows notifica basata su messaggi degli eventi di rete per un socket. |
| [**WSACancelAsyncRequest**](/windows/win32/api/winsock/nf-winsock-wsacancelasyncrequest) | Annulla un'operazione asincrona incompleta. |
| [**WSACleanup**](/windows/win32/api/winsock/nf-winsock-wsacleanup) | Termina l'utilizzo del32.DLL \_ Ws2. |
| [**WSACloseEvent**](/windows/win32/api/Winsock2/nf-winsock2-wsacloseevent) | Chiude un handle dell'oggetto evento aperto. |
| [**WSAConnect**](/windows/win32/api/Winsock2/nf-winsock2-wsaconnect) | Stabilisce una connessione a un'altra applicazione socket, scambia i dati di connessione e specifica la qualità del servizio necessaria in base alla struttura [**FLOWSPEC**](/windows/win32/api/qos/ns-qos-flowspec) specificata. |
| [**WSAConnectByList**](/windows/win32/api/Winsock2/nf-winsock2-wsaconnectbylist) | Stabilisce una connessione a uno di una raccolta di possibili endpoint rappresentati da un set di indirizzi di destinazione (nomi host e porte). |
| [**WSAConnectByName**](/windows/win32/api/Winsock2/nf-winsock2-wsaconnectbynamea) | Stabilisce una connessione a un'altra applicazione socket su un host e una porta specificati |
| [**WSACreateEvent**](/windows/win32/api/Winsock2/nf-winsock2-wsacreateevent) | Crea un nuovo oggetto evento. |
| [**WSADeleteSocketPeerTargetName**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-wsadeletesocketpeertargetname) | Rimuove l'associazione tra un nome di destinazione peer e un indirizzo IP per un socket. |
| [**WSADuplicateSocket**](/windows/win32/api/Winsock2/nf-winsock2-wsaduplicatesocketa) | Restituisce una struttura che può essere utilizzata per creare un nuovo descrittore di socket per un socket condiviso. |
| [**WSAEnumNameSpaceProviders**](/windows/win32/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa) | Recupera informazioni sugli spazi dei nomi disponibili. |
| [**WSAEnumNameSpaceProvidersEx**](/windows/win32/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersexa) | Recupera informazioni sugli spazi dei nomi disponibili. |
| [**WSAEnumNetworkEvents**](/windows/win32/api/Winsock2/nf-winsock2-wsaenumnetworkevents) | Individua le occorrenze degli eventi di rete per il socket indicato, cancella i record degli eventi di rete interni e reimposta gli oggetti evento (facoltativo). |
| [**WSAEnumProtocols**](/windows/win32/api/Winsock2/nf-winsock2-wsaenumprotocolsa) | Recupera informazioni sui protocolli di trasporto disponibili. |
| [**WSAEventSelect**](/windows/win32/api/Winsock2/nf-winsock2-wsaeventselect) | Specifica un oggetto evento da associare al set specificato di eventi di rete FD \_ XXX. |
| [**\_\_WSAFDIsSet**](/windows/win32/api/winsock/nf-winsock-__wsafdisset) | Specifica se un socket è incluso in un set di descrittori di socket. |
| [**WSAGetFailConnectOnIcmpError**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetfailconnectonicmperror) | Esegue una query sullo stato [**dell'TCP_FAIL_CONNECT_ON_ICMP_ERROR**](./ipproto-tcp-socket-options.md) socket. |
| [**WSAGetIcmpErrorInfo**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsageticmperrorinfo) | Esegue una query sull'indirizzo di origine di un errore ICMP ricevuto su un socket TCP durante l'installazione della connessione. |
| [**WSAGetIPUserMtu**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetipusermtu) | Recupera l'MTU del livello IP definito dall'utente per un socket. |
| [**WSAGetLastError**](/windows/win32/api/winsock/nf-winsock-wsagetlasterror) | Restituisce lo stato dell'errore per l'ultima operazione non riuscita. |
| [**WSAGetOverlappedResult**](/windows/win32/api/Winsock2/nf-winsock2-wsagetoverlappedresult) | Recupera i risultati di un'operazione sovrapposta sul socket specificato. |
| [**WSAGetQOSByName**](/windows/win32/api/Winsock2/nf-winsock2-wsagetqosbyname) | Inizializza una [**struttura QOS**](/windows/win32/api/winsock2/ns-winsock2-qos) basata su un modello denominato oppure fornisce un buffer per recuperare un'enumerazione dei nomi di modello disponibili. |
| [**WSAGetServiceClassInfo**](/windows/win32/api/Winsock2/nf-winsock2-wsagetserviceclassinfoa) | Recupera le informazioni sulla classe (schema) relative a una classe di servizio specificata da un provider dello spazio dei nomi specificato. |
| [**WSAGetServiceClassNameByClassId**](/windows/win32/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida) | Recupera il nome del servizio associato al tipo specificato. |
| [**WSAGetUdpRecvMaxCoalescedSize**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetudprecvmaxcoalescedsize) | Recupera le dimensioni massime di un messaggio ricevuto e coalesced per un socket UDP. |
| [**WSAGetUdpSendMessageSize**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetudpsendmessagesize) | Recupera le dimensioni del messaggio di segmentazione per un socket UDP. |
| [**WSAHtonl**](/windows/win32/api/Winsock2/nf-winsock2-wsahtonl) | Converte un oggetto u \_ long dall'ordine dei byte dell'host all'ordine dei byte di rete. |
| [**WSAHtons**](/windows/win32/api/Winsock2/nf-winsock2-wsahtons) | Converte un valore u \_ short dall'ordine dei byte dell'host all'ordine dei byte di rete. |
| [**WSAImpersonateSocketPeer**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-wsaimpersonatesocketpeer) | Usato per rappresentare l'entità di sicurezza corrispondente a un peer socket per eseguire l'autorizzazione a livello di applicazione. |
| [**WSAInstallServiceClass**](/windows/win32/api/Winsock2/nf-winsock2-wsainstallserviceclassa) | Registra uno schema della classe di servizio all'interno di uno spazio dei nomi. |
| [**Wsaioctl**](/windows/win32/api/Winsock2/nf-winsock2-wsaioctl) | Controlla la modalità di un socket. |
| [**WSAJoinLeaf**](/windows/win32/api/Winsock2/nf-winsock2-wsajoinleaf) | Unisce un nodo foglia a una sessione multipoint, scambia i dati di connessione e specifica la qualità del servizio necessaria in base alle strutture specificate. |
| [**WSALookupServiceBegin**](/windows/win32/api/Winsock2/nf-winsock2-wsalookupservicebegina) | Avvia una query client vincolata dalle informazioni contenute in una [**struttura WSAQUERYSET.**](/windows/win32/api/Winsock2/ns-winsock2-wsaquerysetw) |
| [**WSALookupServiceEnd**](/windows/win32/api/Winsock2/nf-winsock2-wsalookupserviceend) | Libera l'handle usato dalle chiamate precedenti a [**WSALookupServiceBegin**](/windows/win32/api/Winsock2/nf-winsock2-wsalookupservicebegina) e [**WSALookupServiceNext.**](/windows/win32/api/Winsock2/nf-winsock2-wsalookupservicenexta) |
| [**WSALookupServiceNext**](/windows/win32/api/Winsock2/nf-winsock2-wsalookupservicenexta) | Recuperare le informazioni sul servizio richieste. |
| [**WSANSPIoctl**](/windows/win32/api/Winsock2/nf-winsock2-wsanspioctl) | Sviluppatori per effettuare chiamate di controllo I/O a uno spazio dei nomi registrato. |
| [**WSANtohl**](/windows/win32/api/Winsock2/nf-winsock2-wsantohl) | Converte un oggetto u \_ long dall'ordine dei byte di rete all'ordine dei byte dell'host. |
| [**WSANtohs**](/windows/win32/api/Winsock2/nf-winsock2-wsantohs) | Converte un valore u \_ short dall'ordine dei byte di rete all'ordine dei byte dell'host. |
| [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) | Determina lo stato di uno o più socket. |
| [**WSAProviderConfigChange**](/windows/win32/api/Winsock2/nf-winsock2-wsaproviderconfigchange) | Notifica all'applicazione quando viene modificata la configurazione del provider. |
| [**WSAQuerySocketSecurity**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity) | Esegue query sulle informazioni sulla sicurezza applicata a una connessione in un socket. |
| [**WSARecv**](/windows/win32/api/Winsock2/nf-winsock2-wsarecv) | Riceve i dati da un socket connesso. |
| [**WSARecvDisconnect**](/windows/win32/api/Winsock2/nf-winsock2-wsarecvdisconnect) | Termina la ricezione su un socket e recupera i dati di disconnessione se il socket è orientato alla connessione. |
| [**WSARecvEx**](/windows/win32/api/mswsock/nf-mswsock-wsarecvex) | Riceve i dati da un socket connesso. |
| [**WSARecvFrom**](/windows/win32/api/Winsock2/nf-winsock2-wsarecvfrom) | Riceve un datagramma e archivia l'indirizzo di origine. |
| [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) | Riceve dati e informazioni di controllo facoltative dai socket connessi e non connessi. |
| [**WSARemoveServiceClass**](/windows/win32/api/Winsock2/nf-winsock2-wsaremoveserviceclass) | Rimuove definitivamente lo schema della classe di servizio dal Registro di sistema. |
| [**WSAResetEvent**](/windows/win32/api/Winsock2/nf-winsock2-wsaresetevent) | Reimposta lo stato dell'oggetto evento specificato su non associato. |
| [**WSARevertImpersonation**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-wsarevertimpersonation) | Termina la rappresentazione di un peer socket. |
| [**WSASend**](/windows/win32/api/Winsock2/nf-winsock2-wsasend) | Invia dati su un socket connesso. |
| [**WSASendDisconnect**](/windows/win32/api/Winsock2/nf-winsock2-wsasenddisconnect) | Avvia la terminazione della connessione per il socket e invia i dati di disconnessione. |
| [**WSASendMsg**](/windows/win32/api/winsock2/nf-winsock2-wsasendmsg) | Invia dati e informazioni di controllo facoltative da socket connessi e non connessi. |
| [**WSASendTo**](/windows/win32/api/Winsock2/nf-winsock2-wsasendto) | Invia dati a una destinazione specifica, usando operazioni di I/O sovrapposte, se applicabile. |
| [**WSASetEvent**](/windows/win32/api/Winsock2/nf-winsock2-wsasetevent) | Imposta lo stato dell'oggetto evento specificato su segnalato. |
| [**WSASetFailConnectOnIcmpError**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetfailconnectonicmperror) | Imposta lo stato [**dell'opzione TCP_FAIL_CONNECT_ON_ICMP_ERROR**](./ipproto-tcp-socket-options.md) socket. |
| [**WSASetIPUserMtu**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetipusermtu) | Imposta l'MTU del livello IP definito dall'utente in un socket. |
| [**WSASetLastError**](/windows/win32/api/winsock/nf-winsock-wsasetlasterror) | Imposta il codice di errore. |
| [**WSASetService**](/windows/win32/api/Winsock2/nf-winsock2-wsasetservicea) | Registra o rimuove dal Registro di sistema un'istanza del servizio all'interno di uno o più spazi dei nomi. |
| [**WSASetSocketPeerTargetName**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) | Consente di specificare il nome di destinazione peer (SPN) corrispondente a un indirizzo IP peer. Questo nome di destinazione deve essere specificato dalle applicazioni client per identificare in modo sicuro il peer che deve essere autenticato. |
| [**WSASetSocketSecurity**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity) | Abilita e applica la sicurezza per un socket. |
| [**WSASetUdpRecvMaxCoalescedSize**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetudprecvmaxcoalescedsize) | Imposta le dimensioni massime di un messaggio coalesced impostato su un socket UDP. |
| [**WSASetUdpSendMessageSize**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetudpsendmessagesize) | Imposta le dimensioni del messaggio di segmentazione in un socket UDP. |
| [**WSASocket**](/windows/win32/api/Winsock2/nf-winsock2-wsasocketa) | Crea un socket associato a un provider di servizi di trasporto specifico. |
| [**WSAStartup**](/windows/win32/api/winsock/nf-winsock-wsastartup) | Avvia l'uso di WS2 \_32.DLL da parte di un processo. |
| [**WSAStringToAddress**](/windows/win32/api/Winsock2/nf-winsock2-wsastringtoaddressa) | Converte una stringa numerica in una [**struttura sockaddr.**](sockaddr-2.md) |
| [**WSAWaitForMultipleEvents**](/windows/win32/api/Winsock2/nf-winsock2-wsawaitformultipleevents) | Restituisce quando uno o tutti gli oggetti evento specificati sono nello stato segnalato o quando scade l'intervallo di timeout. |
