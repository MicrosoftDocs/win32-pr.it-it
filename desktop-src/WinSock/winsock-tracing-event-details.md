---
description: Dettagli traccia eventi di rete Winsock
ms.assetid: f0386bd3-15d0-45f3-82c9-365d1c9f59c5
title: Dettagli traccia eventi di rete Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 588363420aee9c3b04f4f8060bbd9c77b9cc3232
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232789"
---
# <a name="winsock-network-event-tracing-details"></a>Dettagli traccia eventi di rete Winsock

Di seguito vengono illustrati tutti gli eventi di rete Winsock che possono essere tracciati e vengono descritti i parametri e le informazioni registrate.

## <a name="socket-creation"></a>Creazione socket

ID evento = 1

Livello = 4 (informazioni)

Per la creazione del socket vengono tracciati gli eventi Winsock seguenti:

-   Handle di socket creati dalle chiamate alle funzioni [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) o [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) .
-   Handle di socket accettati sui socket in ascolto.
-   Handle di socket creati dalle chiamate alla funzione [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) .
-   Gli handle di socket riutilizzati dalle chiamate alle funzioni [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex) o [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex) .

Per un evento di creazione del socket vengono registrati i parametri seguenti:



| Parametro                                                                                                        | Descrizione                                                                            |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Processo<br/>                 | Indirizzo della struttura EPROCESS del kernel per il processo.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint<br/>             | Indirizzo del socket del kernel Winsock utilizzato come identificatore univoco per un socket.<br/> |
| <span id="SocketType"></span><span id="sockettype"></span><span id="SOCKETTYPE"></span>SocketType<br/>     | Tipo di socket.<br/>                                                     |
| <span id="Protocol"></span><span id="protocol"></span><span id="PROTOCOL"></span>Protocollo<br/>             | Protocollo del socket.<br/>                                                 |
| <span id="UserModePid"></span><span id="usermodepid"></span><span id="USERMODEPID"></span>UserModePid<br/> | ID processo in modalità utente che ha creato il socket.<br/>                           |



 

## <a name="socket-bind"></a>Binding socket

ID evento = 2 (IPv4), ID evento = 3 (IPv6)

Livello = 4 (informazioni)

Per un'operazione di associazione vengono tracciati gli eventi Winsock seguenti:

-   Associazione implicita o esplicita di un handle di socket.

Per un evento di binding vengono registrati i parametri seguenti:



| Parametro                                                                                            | Descrizione                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Processo<br/>     | Indirizzo della struttura EPROCESS del kernel per il processo.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint<br/> | Indirizzo del socket del kernel Winsock utilizzato come identificatore univoco per un socket.<br/> |
| <span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Indirizzo<br/>     | Indirizzo IP locale.<br/>                                                       |
| <span id="Port"></span><span id="port"></span><span id="PORT"></span>Porta<br/>                 | Numero di porta IP locale.<br/>                                                   |
| <span id="Status"></span><span id="status"></span><span id="STATUS"></span>Stato<br/>         | Stato o codice di errore restituito per l'operazione di associazione.<br/>                   |



 

## <a name="failed-bind"></a>Associazione non riuscita

ID evento = 40

Livello = 4 (informazioni)

Per un'operazione di associazione non riuscita vengono tracciati gli eventi Winsock seguenti:

-   Associazione implicita o esplicita di un handle di socket che ha esito negativo.

Vengono registrati i seguenti parametri per un evento di binding non riuscito:



| Parametro                                                                                            | Descrizione                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Processo<br/>     | Indirizzo della struttura EPROCESS del kernel per il processo.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint<br/> | Indirizzo del socket del kernel Winsock utilizzato come identificatore univoco per un socket.<br/> |
| <span id="Error"></span><span id="error"></span><span id="ERROR"></span>Errore<br/>             | Codice di errore restituito per l'operazione di associazione non riuscita.<br/>                     |



 

## <a name="socket-connect"></a>Connessione socket

ID evento = 4 (IPv4), ID evento = 5 (IPv6)

Livello = 4 (informazioni)

Gli eventi Winsock seguenti sono tracciati per una richiesta di operazione di connessione (una chiamata alla funzione [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect), [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex), [**WSAConnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect), [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)o [**con WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) ):

-   Connessione di un socket a una destinazione per un socket orientato alla connessione o senza connessione.

Per un evento Connect vengono registrati i parametri seguenti:



| Parametro                                                                                            | Descrizione                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Processo<br/>     | Indirizzo della struttura EPROCESS del kernel per il processo.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint<br/> | Indirizzo del socket del kernel Winsock utilizzato come identificatore univoco per un socket.<br/> |
| <span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Indirizzo<br/>     | Indirizzo IP remoto.<br/>                                                      |
| <span id="Port"></span><span id="port"></span><span id="PORT"></span>Porta<br/>                 | Numero di porta IP remoto.<br/>                                                  |



 

## <a name="connect-completed"></a>Connessione completata

ID evento = 6

Livello = 4 (informazioni)

Per una connessione completata, vengono tracciati gli eventi Winsock seguenti:

-   L'operazione di connessione è stata completata.

I parametri seguenti vengono registrati per un evento di connessione completata:



| Parametro                                                                                            | Descrizione                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Processo<br/>     | Indirizzo della struttura EPROCESS del kernel per il processo.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint<br/> | Indirizzo del socket del kernel Winsock utilizzato come identificatore univoco per un socket.<br/> |
| <span id="Error"></span><span id="error"></span><span id="ERROR"></span>Errore<br/>             | Codice di errore restituito per l'operazione di connessione.<br/>                          |



 

## <a name="afd-initiated-abort"></a>Interruzione AFD-Initiated

ID evento = 7

Livello = 4 (informazioni)

Gli eventi Winsock seguenti sono tracciati per le interruzioni avviate da Winsock o per le operazioni di annullamento:

-   Interruzione causata da dati di ricezione non letti memorizzati nel buffer dopo la chiusura.
-   Interruzione dopo una chiamata alla funzione [**Shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) con il parametro *How* impostato su SD \_ Receive e una chiamata alla funzione [**chiamata closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) con la ricezione dei dati in sospeso.
-   Interruzione dopo un tentativo non riuscito di scaricare l'endpoint.
-   Si è verificata un'interruzione dopo un errore interno di Winsock.
-   Interruzione a causa di una connessione con errori e dell'applicazione che in precedenza richiedeva che la connessione venisse interrotta in determinate circostanze. Un esempio di questo caso è costituito da un'applicazione che è stata impostata in modo che venga \_ sospesa con un timeout di zero e che nella connessione siano ancora presenti dati non riconosciuti.
-   Interruzione su una connessione non completamente associata all'accettazione dell'endpoint.
-   Interruzione di una chiamata non riuscita alla funzione [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) o [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex) .
-   Interruzione a causa di un'operazione di ricezione non riuscita.
-   Interruzione a causa di un evento Plug and Play.
-   Interruzione a causa di una richiesta di scaricamento non riuscita.
-   Interruzione a causa di una richiesta di ricezione dati accelerata non riuscita.
-   Interruzione a causa di una richiesta di invio non riuscita.
-   Interruzione causata dalla richiesta di invio annullata.
-   Interruzione causata da un oggetto annullato chiamato sulla funzione [**TransmitPackets**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_transmitpackets) .

I parametri seguenti vengono registrati per un'operazione di interruzione o annullamento avviata da Winsock:



| Parametro                                                                                            | Descrizione                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Processo<br/>     | Indirizzo della struttura EPROCESS del kernel per il processo.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint<br/> | Indirizzo del socket del kernel Winsock utilizzato come identificatore univoco per un socket.<br/> |
| <span id="Reason"></span><span id="reason"></span><span id="REASON"></span>Motivo<br/>         | Motivo dell'operazione di interruzione o annullamento.<br/>                               |



 

## <a name="transport-initiated-abort"></a>Interruzione Transport-Initiated

ID evento = 8

Livello = 4 (informazioni)

Gli eventi Winsock seguenti sono tracciati per le operazioni di interruzione o annullamento avviate dal trasporto:

-   Reimpostazione indicata dal trasporto.

I parametri seguenti vengono registrati per un'operazione di interruzione o annullamento avviata da Winsock:



| Parametro                                                                                            | Descrizione                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Processo<br/>     | Indirizzo della struttura EPROCESS del kernel per il processo.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint<br/> | Indirizzo del socket del kernel Winsock utilizzato come identificatore univoco per un socket.<br/> |
| <span id="Reason"></span><span id="reason"></span><span id="REASON"></span>Motivo<br/>         | Motivo dell'operazione di interruzione o annullamento.<br/>                               |



 

## <a name="failed-send-request"></a>Richiesta di invio non riuscita

ID evento = 9

Livello = 4 (informazioni)

Gli eventi Winsock seguenti sono tracciati per individuare eventuali errori nelle richieste [**Send**](/windows/desktop/api/Winsock2/nf-winsock2-send) o [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) :

-   Errori restituiti nelle richieste [**Send**](/windows/desktop/api/Winsock2/nf-winsock2-send) o [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) non riuscite.

I parametri seguenti vengono registrati per le richieste di invio che generano un errore:



| Parametro                                                                                            | Descrizione                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Processo<br/>     | Indirizzo della struttura EPROCESS del kernel per il processo.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint<br/> | Indirizzo del socket del kernel Winsock utilizzato come identificatore univoco per un socket.<br/> |
| <span id="Error"></span><span id="error"></span><span id="ERROR"></span>Errore<br/>             | Codice di errore restituito per l'operazione.<br/>                                  |



 

## <a name="failed-wsasendmsg-request"></a>Richiesta WsaSendMsg non riuscita

ID evento = 10

Livello = 4 (informazioni)

Gli eventi Winsock seguenti sono tracciati per gli errori nelle richieste [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) :

-   Errori restituiti nelle richieste [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) non riuscite.

I parametri seguenti vengono registrati per le richieste di invio che generano un errore:



| Parametro                                                                                            | Descrizione                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Processo<br/>     | Indirizzo della struttura EPROCESS del kernel per il processo.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint<br/> | Indirizzo del socket del kernel Winsock utilizzato come identificatore univoco per un socket.<br/> |
| <span id="Error"></span><span id="error"></span><span id="ERROR"></span>Errore<br/>             | Codice di errore restituito per l'operazione.<br/>                                  |



 

## <a name="failed-recv-request"></a>Richiesta ricezione non riuscita

ID evento = 11

Livello = 4 (informazioni)

Gli eventi Winsock seguenti sono tracciati per individuare eventuali errori nelle richieste [**ricezione**](/windows/desktop/api/winsock/nf-winsock-recv), [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv)o [**chiamata WSARecvEx**](/windows/win32/api/mswsock/nf-mswsock-wsarecvex) :

-   Errori restituiti sulle richieste di ricezione non riuscite.

I parametri seguenti vengono registrati per le richieste di invio che generano un errore:



| Parametro                                                                                            | Descrizione                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Processo<br/>     | Indirizzo della struttura EPROCESS del kernel per il processo.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint<br/> | Indirizzo del socket del kernel Winsock utilizzato come identificatore univoco per un socket.<br/> |
| <span id="Error"></span><span id="error"></span><span id="ERROR"></span>Errore<br/>             | Codice di errore restituito per l'operazione.<br/>                                  |



 

## <a name="failed-recvfrom-request"></a>Richiesta recvfrom non riuscita

ID evento = 12

Livello = 4 (informazioni)

Gli eventi Winsock seguenti sono tracciati per gli errori nelle richieste [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) o [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) :

-   Errori restituiti nelle richieste [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) o [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) non riuscite.

I parametri seguenti vengono registrati per una richiesta [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) o [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) che genera un errore:



| Parametro                                                                                            | Descrizione                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Processo<br/>     | Indirizzo della struttura EPROCESS del kernel per il processo.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint<br/> | Indirizzo del socket del kernel Winsock utilizzato come identificatore univoco per un socket.<br/> |
| <span id="Error"></span><span id="error"></span><span id="ERROR"></span>Errore<br/>             | Codice di errore restituito per l'operazione.<br/>                                  |



 

## <a name="socket-close"></a>Chiusura socket

ID evento = 13

Livello = 4 (informazioni)

Gli eventi Winsock seguenti sono tracciati per le operazioni di chiusura del socket:

-   Un handle socket è chiuso.

I parametri seguenti vengono registrati per un evento di chiusura del socket:



| Parametro                                                                                            | Descrizione                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Processo<br/>     | Indirizzo della struttura EPROCESS del kernel per il processo.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint<br/> | Indirizzo del socket del kernel Winsock utilizzato come identificatore univoco per un socket.<br/> |
| <span id="Error"></span><span id="error"></span><span id="ERROR"></span>Errore<br/>             | Valore restituito per l'operazione di chiusura del socket.<br/>                            |



 

## <a name="socket-cleanup"></a>Pulitura socket

ID evento = 14

Livello = 4 (informazioni)

Gli eventi Winsock seguenti sono tracciati per le operazioni di pulizia socket (Shutdown):

-   La funzione [**Shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) viene chiamata su un socket.
-   Il trasporto indica una disconnessione normale non riuscita.

I parametri seguenti vengono registrati per un evento di pulizia del socket (arresto) o di chiusura del socket:



| Parametro                                                                                            | Descrizione                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Processo<br/>     | Indirizzo della struttura EPROCESS del kernel per il processo.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint<br/> | Indirizzo del socket del kernel Winsock utilizzato come identificatore univoco per un socket.<br/> |
| <span id="Error"></span><span id="error"></span><span id="ERROR"></span>Errore<br/>             | Valore restituito per l'operazione di pulizia del socket (arresto).<br/>               |



 

## <a name="socket-accept"></a>Accettazione socket

ID evento = 15 (IPv4), ID evento = 16 (IPv6)

Livello = 4 (informazioni)

Gli eventi Winsock seguenti sono tracciati per una richiesta di funzione [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex)o [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) :

-   Richiesta di funzione [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex)o [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) su un handle di socket.

Per un evento Accept vengono registrati i parametri seguenti:



| Parametro                                                                                            | Descrizione                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Processo<br/>     | Indirizzo della struttura EPROCESS del kernel per il processo.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint<br/> | Indirizzo del socket del kernel Winsock utilizzato come identificatore univoco per un socket.<br/> |
| <span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Indirizzo<br/>     | Indirizzo IP remoto.<br/>                                                      |
| <span id="Port"></span><span id="port"></span><span id="PORT"></span>Porta<br/>                 | Numero di porta IP remoto.<br/>                                                  |
| <span id="Status"></span><span id="status"></span><span id="STATUS"></span>Stato<br/>         | Stato o codice di errore restituito per l'operazione Accept.<br/>                 |



 

## <a name="accept-failed"></a>Accettazione non riuscita

ID evento = 17

Livello = 4 (informazioni)

Gli eventi Winsock seguenti sono tracciati per un'operazione di accettazione non riuscita:

-   Richiesta [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex)o [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) su un handle di socket che ha esito negativo.

Per un evento Accept non riuscito vengono registrati i parametri seguenti:



| Parametro                                                                                            | Descrizione                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Processo<br/>     | Indirizzo della struttura EPROCESS del kernel per il processo.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint<br/> | Indirizzo del socket del kernel Winsock utilizzato come identificatore univoco per un socket.<br/> |
| <span id="Error"></span><span id="error"></span><span id="ERROR"></span>Errore<br/>             | Codice di errore restituito per l'operazione di accettazione non riuscita.<br/>                   |



 

## <a name="send-posted"></a>Invia inviato

ID evento = 18

Livello = 5 (dettagliato)

Per diagnosticare il danneggiamento del buffer dell'utente (ad esempio, quando un'applicazione riutilizza lo stesso buffer in un'altra chiamata Send o Receive mentre è ancora in uso), il buffer dei dati viene registrato quando viene inviato a Winsock e al completamento dal trasporto sottostante. Gli eventi Winsock seguenti sono tracciati per le operazioni post del buffer di invio e di ricezione del socket:

-   Un'applicazione invia un messaggio di invio.
-   Un'operazione di invio è stata completata in Winsock.

I parametri seguenti vengono registrati per le operazioni di invio del socket:



| Parametro                                                                                                            | Descrizione                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Processo<br/>                     | Indirizzo della struttura EPROCESS del kernel per il processo.<br/>                                                                          |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint<br/>                 | Indirizzo del socket del kernel Winsock utilizzato come identificatore univoco per un socket.<br/>                                                     |
| <span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath<br/>                 | Valore booleano che indica se è stato utilizzato il percorso di I/O veloce.<br/>                                                                       |
| <span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount<br/>     | Numero di buffer.<br/>                                                                                                               |
| <span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer<br/>                         | Indirizzo virtuale del buffer. Per i buffer concatenati, questo parametro è l'indirizzo virtuale del primo buffer nella catena.<br/> |
| <span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength<br/> | Lunghezza del buffer. Per i buffer concatenati, questo parametro è il numero totale di byte in tutti i buffer nella catena.<br/>  |



 

Quando FastPath è true, l'indirizzo usermode del primo buffer nella matrice di buffer viene registrato nel parametro buffer. Quando FastPath è false, l'indirizzo del buffer del kernel Winsock viene registrato nel parametro buffer.

## <a name="receive-posted"></a>Ricezione inviata

ID evento = 19

Livello = 5 (dettagliato)

Per diagnosticare il danneggiamento del buffer dell'utente (ad esempio, quando un'applicazione riutilizza lo stesso buffer in un'altra chiamata Send o Receive mentre è ancora in uso), il buffer dei dati viene registrato quando viene inviato a Winsock e al completamento dal trasporto sottostante. Gli eventi Winsock seguenti sono tracciati per le operazioni post del buffer di ricezione socket:

-   Un'applicazione invia una ricezione.
-   Un'operazione di ricezione viene completata in Winsock.

Per le operazioni di ricezione socket vengono registrati i parametri seguenti:



| Parametro                                                                                                            | Descrizione                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Processo<br/>                     | Indirizzo della struttura EPROCESS del kernel per il processo.<br/>                                                                          |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint<br/>                 | Indirizzo del socket del kernel Winsock utilizzato come identificatore univoco per un socket.<br/>                                                     |
| <span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath<br/>                 | Valore booleano che indica se è stato utilizzato il percorso di I/O veloce.<br/>                                                                       |
| <span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount<br/>     | Numero di buffer.<br/>                                                                                                               |
| <span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer<br/>                         | Indirizzo virtuale del buffer. Per i buffer concatenati, questo parametro è l'indirizzo virtuale del primo buffer nella catena.<br/> |
| <span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength<br/> | Lunghezza del buffer. Per i buffer concatenati, questo parametro è il numero totale di byte in tutti i buffer nella catena.<br/>  |



 

Quando FastPath è true, l'indirizzo usermode del primo buffer nella matrice di buffer viene registrato nel parametro buffer. Quando FastPath è false, l'indirizzo del buffer del kernel Winsock viene registrato nel parametro buffer.

## <a name="recvfrom-posted"></a>RecvFrom pubblicato

ID evento = 20

Livello = 5 (dettagliato)

Per diagnosticare il danneggiamento del buffer dell'utente (ad esempio, quando un'applicazione riutilizza lo stesso buffer in un'altra chiamata Send o Receive mentre è ancora in uso), il buffer dei dati viene registrato quando viene inviato a Winsock e al completamento dal trasporto sottostante. Gli eventi Winsock seguenti sono tracciati per un'operazione post del buffer [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) su un socket:

-   Un'applicazione invia un'operazione di ricezione da.

Per l'operazione recvfrom vengono registrati i parametri seguenti:



| Parametro                                                                                                            | Descrizione                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Processo<br/>                     | Indirizzo della struttura EPROCESS del kernel per il processo.<br/>                                                                          |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint<br/>                 | Indirizzo del socket del kernel Winsock utilizzato come identificatore univoco per un socket.<br/>                                                     |
| <span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath<br/>                 | Valore booleano che indica se è stato utilizzato il percorso di I/O veloce.<br/>                                                                       |
| <span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount<br/>     | Numero di buffer.<br/>                                                                                                               |
| <span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer<br/>                         | Indirizzo virtuale del buffer. Per i buffer concatenati, questo parametro è l'indirizzo virtuale del primo buffer nella catena.<br/> |
| <span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength<br/> | Lunghezza del buffer. Per i buffer concatenati, questo parametro è il numero totale di byte in tutti i buffer nella catena.<br/>  |



 

Quando FastPath è true, l'indirizzo usermode del primo buffer nella matrice di buffer viene registrato nel parametro buffer. Quando FastPath è false, l'indirizzo del buffer del kernel Winsock viene registrato nel parametro buffer.

## <a name="sendto-posted"></a>SendTo inviato

ID evento = 21 (IPv4), ID evento = 22 (IPv6)

Livello = 5 (dettagliato)

Per diagnosticare il danneggiamento del buffer dell'utente (ad esempio, quando un'applicazione riutilizza lo stesso buffer in un'altra chiamata Send o Receive mentre è ancora in uso), il buffer dei dati viene registrato quando viene inviato a Winsock e al completamento dal trasporto sottostante. Gli eventi Winsock seguenti sono tracciati per un'operazione post sul buffer [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto) su un socket:

-   Un'applicazione pubblica un invio da.

Per l'operazione [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto) vengono registrati i parametri seguenti:



| Parametro                                                                                                            | Descrizione                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Processo<br/>                     | Indirizzo della struttura EPROCESS del kernel per il processo.<br/>                                                                          |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint<br/>                 | Indirizzo del socket del kernel Winsock utilizzato come identificatore univoco per un socket.<br/>                                                     |
| <span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath<br/>                 | Valore booleano che indica se è stato utilizzato il percorso di I/O veloce.<br/>                                                                       |
| <span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount<br/>     | Numero di buffer.<br/>                                                                                                               |
| <span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer<br/>                         | Indirizzo virtuale del buffer. Per i buffer concatenati, questo parametro è l'indirizzo virtuale del primo buffer nella catena.<br/> |
| <span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength<br/> | Lunghezza del buffer. Per i buffer concatenati, questo parametro è il numero totale di byte in tutti i buffer nella catena.<br/>  |
| <span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Indirizzo<br/>                     | Indirizzo IP remoto del socket.<br/>                                                                                            |
| <span id="Port"></span><span id="port"></span><span id="PORT"></span>Porta<br/>                                 | Numero di porta IP remoto del socket.<br/>                                                                                        |



 

Quando FastPath è true, l'indirizzo usermode del primo buffer nella matrice di buffer viene registrato nel parametro buffer. Quando FastPath è false, l'indirizzo del buffer del kernel Winsock viene registrato nel parametro buffer.

## <a name="recv-completed"></a>Ricezione completato

ID evento = 23

Livello = 5 (dettagliato)

Per diagnosticare il danneggiamento del buffer dell'utente (ad esempio, quando un'applicazione riutilizza lo stesso buffer in un'altra chiamata Send o Receive mentre è ancora in uso), il buffer dei dati viene registrato quando viene inviato a Winsock e al completamento dal trasporto sottostante. Gli eventi Winsock seguenti sono tracciati per le operazioni di ricezione socket completate:

-   Un'operazione di invio viene completata al trasporto.
-   Un'operazione di ricezione viene completata al trasporto.

Vengono registrati i seguenti parametri per un invio completato o una ricezione completata:



| Parametro                                                                                                            | Descrizione                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Processo<br/>                     | Indirizzo della struttura EPROCESS del kernel per il processo.<br/>                                                                                   |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint<br/>                 | Indirizzo del socket del kernel Winsock utilizzato come identificatore univoco per un socket.<br/>                                                              |
| <span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer<br/>                         | Indirizzo virtuale del buffer. Per i buffer concatenati, questo parametro è l'indirizzo virtuale del primo buffer nella catena.<br/>          |
| <span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength<br/> | Lunghezza del buffer di byte ricevuti. Per i buffer concatenati, questo parametro è il numero totale di byte ricevuti in tutti i buffer della catena.<br/> |



 

## <a name="send-completed"></a>Invio completato

ID evento = 24

Livello = 5 (dettagliato)

Per diagnosticare il danneggiamento del buffer dell'utente (ad esempio, quando un'applicazione riutilizza lo stesso buffer in un'altra chiamata Send o Receive mentre è ancora in uso), il buffer dei dati viene registrato quando viene inviato a Winsock e al completamento dal trasporto sottostante. Gli eventi Winsock seguenti sono tracciati per le operazioni di invio socket completate:

-   Un'operazione di invio viene completata al trasporto.

Per un invio completato vengono registrati i parametri seguenti:



| Parametro                                                                                                            | Descrizione                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Processo<br/>                     | Indirizzo della struttura EPROCESS del kernel per il processo.<br/>                                                                             |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint<br/>                 | Indirizzo del socket del kernel Winsock utilizzato come identificatore univoco per un socket.<br/>                                                        |
| <span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer<br/>                         | Indirizzo virtuale del buffer. Per i buffer concatenati, questo parametro è l'indirizzo virtuale del primo buffer nella catena.<br/>    |
| <span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength<br/> | Lunghezza del buffer di byte inviati. Per i buffer concatenati, questo parametro è il numero totale di byte inviati da tutti i buffer nella catena.<br/> |



 

## <a name="sendmsg-completed"></a>SendMsg completato

ID evento = 25

Livello = 5 (dettagliato)

Per diagnosticare il danneggiamento del buffer dell'utente (ad esempio, quando un'applicazione riutilizza lo stesso buffer in un'altra chiamata Send o Receive mentre è ancora in uso), il buffer dei dati viene registrato quando viene inviato a Winsock e al completamento dal trasporto sottostante. Quando un'operazione post del buffer [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) viene completata in un socket, vengono tracciati gli eventi Winsock seguenti:

-   Un'applicazione completa un'operazione [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) .

Per il completamento [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) vengono registrati i parametri seguenti:



| Parametro                                                                                                            | Descrizione                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Processo<br/>                     | Indirizzo della struttura EPROCESS del kernel per il processo.<br/>                                                                             |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint<br/>                 | Indirizzo del socket del kernel Winsock utilizzato come identificatore univoco per un socket.<br/>                                                        |
| <span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount<br/>     | Numero di buffer.<br/>                                                                                                                  |
| <span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer<br/>                         | Indirizzo virtuale del buffer. Per i buffer concatenati, questo parametro è l'indirizzo virtuale del primo buffer nella catena.<br/>    |
| <span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength<br/> | Lunghezza del buffer di byte inviati. Per i buffer concatenati, questo parametro è il numero totale di byte inviati da tutti i buffer nella catena.<br/> |
| <span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Indirizzo<br/>                     | Indirizzo IP remoto del socket.<br/>                                                                                               |
| <span id="Port"></span><span id="port"></span><span id="PORT"></span>Porta<br/>                                 | Numero di porta IP remoto del socket.<br/>                                                                                           |



 

## <a name="recvfrom-completed"></a>RecvFrom completato

ID evento = 26 (IPv4), ID evento = 27 (IPv6)

Livello = 5 (dettagliato)

Per diagnosticare il danneggiamento del buffer dell'utente (ad esempio, quando un'applicazione riutilizza lo stesso buffer in un'altra chiamata Send o Receive mentre è ancora in uso), il buffer dei dati viene registrato quando viene inviato a Winsock e al completamento dal trasporto sottostante. Quando un'operazione post del buffer [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) viene completata in un socket, vengono tracciati gli eventi Winsock seguenti:

-   Un'applicazione completa un'operazione [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) .

Per il completamento [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) vengono registrati i parametri seguenti:



| Parametro                                                                                                            | Descrizione                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Processo<br/>                     | Indirizzo della struttura EPROCESS del kernel per il processo.<br/>                                                                                   |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint<br/>                 | Indirizzo del socket del kernel Winsock utilizzato come identificatore univoco per un socket.<br/>                                                              |
| <span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount<br/>     | Numero di buffer.<br/>                                                                                                                        |
| <span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer<br/>                         | Indirizzo virtuale del buffer. Per i buffer concatenati, questo parametro è l'indirizzo virtuale del primo buffer nella catena.<br/>          |
| <span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength<br/> | Lunghezza del buffer di byte ricevuti. Per i buffer concatenati, questo parametro è il numero totale di byte ricevuti in tutti i buffer della catena.<br/> |
| <span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Indirizzo<br/>                     | Indirizzo IP remoto del socket.<br/>                                                                                                     |
| <span id="Port"></span><span id="port"></span><span id="PORT"></span>Porta<br/>                                 | Numero di porta IP remoto del socket.<br/>                                                                                                 |



 

## <a name="sendto-completed"></a>SendTo completato

ID evento = 28

Livello = 5 (dettagliato)

Per diagnosticare il danneggiamento del buffer dell'utente (ad esempio, quando un'applicazione riutilizza lo stesso buffer in un'altra chiamata Send o Receive mentre è ancora in uso), il buffer dei dati viene registrato quando viene inviato a Winsock e al completamento dal trasporto sottostante. Gli eventi Winsock seguenti vengono tracciati quando un'operazione post del buffer [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto) viene completata in un socket:

-   Un'applicazione completa un'operazione [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto) .

Per il completamento del [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto) vengono registrati i parametri seguenti:



| Parametro                                                                                                            | Descrizione                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Processo<br/>                     | Indirizzo della struttura EPROCESS del kernel per il processo.<br/>                                                                             |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint<br/>                 | Indirizzo del socket del kernel Winsock utilizzato come identificatore univoco per un socket.<br/>                                                        |
| <span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount<br/>     | Numero di buffer.<br/>                                                                                                                  |
| <span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Buffer<br/>                         | Indirizzo virtuale del buffer. Per i buffer concatenati, questo parametro è l'indirizzo virtuale del primo buffer nella catena.<br/>    |
| <span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength<br/> | Lunghezza del buffer di byte inviati. Per i buffer concatenati, questo parametro è il numero totale di byte inviati da tutti i buffer nella catena.<br/> |
| <span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Indirizzo<br/>                     | Indirizzo IP remoto del socket.<br/>                                                                                               |
| <span id="Port"></span><span id="port"></span><span id="PORT"></span>Porta<br/>                                 | Numero di porta IP remoto del socket.<br/>                                                                                           |



 

## <a name="socket-option-set"></a>Set di opzioni socket

ID evento = 29

Livello = 5 (dettagliato)

Ogni volta che un'applicazione modifica determinati valori di opzioni socket e IOCTL, i nuovi valori verranno registrati. Le opzioni registrate possono essere usate per diagnosticare prestazioni insufficienti o comportamenti strani nelle applicazioni. Per alcune opzioni socket e IOCTL sono tracciati gli eventi Winsock seguenti:

-   QUINDI \_ sndbuf modifiche.
-   QUINDI \_ RCVBUF modifiche.
-   FIONBIO
-   SIO \_ Abilita \_ \_ Accodamento circolare
-   \_CONNRESET UDP \_ sio
-   \_OOBINLINE

Vengono registrati i seguenti parametri per le chiamate di funzione [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) e [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) che modificano uno dei valori precedenti:



| Parametro                                                                                            | Descrizione                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Processo<br/>     | Indirizzo della struttura EPROCESS del kernel per il processo.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint<br/> | Indirizzo del socket del kernel Winsock utilizzato come identificatore univoco per un socket.<br/> |
| <span id="Option"></span><span id="option"></span><span id="OPTION"></span>Opzione<br/>         | Opzione socket o IOCTL modificata. <br/>                                |
| <span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valore<br/>             | Nuovo valore per l'opzione socket o IOCTL. <br/>                              |



 

## <a name="selectpoll-posted"></a>Selezione/polling pubblicato

ID evento = 30

Livello = 5 (dettagliato)

Quando un'applicazione chiama la funzione [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) o [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) , vengono tracciati gli eventi Winsock seguenti:

-   L'applicazione invia una richiesta [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) o [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) .

Per gli eventi [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) o [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) vengono registrati i parametri seguenti:



| Parametro                                                                                                        | Descrizione                                                                                                    |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Processo<br/>                 | ID del processo proprietario.<br/>                                                                              |
| <span id="HandleCount"></span><span id="handlecount"></span><span id="HANDLECOUNT"></span>HandleCount<br/> | Il numero di handle passati dall'applicazione (valido solo nell'evento di avvio).<br/>            |
| <span id="Timeout"></span><span id="timeout"></span><span id="TIMEOUT"></span>Timeout<br/>                 | Tempo massimo di attesa per la funzione [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) o [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) .<br/> |



 

## <a name="selectpoll-completed"></a>Selezione/polling completato

ID evento = 31

Livello = 5 (dettagliato)

Quando un'applicazione chiama la funzione [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) o [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) , vengono tracciati gli eventi Winsock seguenti:

-   Winsock completa una chiamata [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) o [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) .

Quando viene completata un'operazione [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) o [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) , vengono registrati i parametri seguenti:



| Parametro                                                                                            | Descrizione                                                                                                    |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Processo<br/>     | Indirizzo della struttura EPROCESS del kernel per il processo.<br/>                                              |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint<br/> | Indirizzo del socket del kernel Winsock utilizzato come identificatore univoco per un socket.<br/>                         |
| <span id="Error"></span><span id="error"></span><span id="ERROR"></span>Errore<br/>             | Codice di errore restituito per l'operazione [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) o [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) .<br/> |



 

## <a name="wsaeventselect"></a>WSAEventSelect

ID evento = 32

Livello = 5 (dettagliato)

Quando un'applicazione chiama la funzione [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) , vengono tracciati gli eventi Winsock seguenti:

-   Registra la maschera eventi passata nella funzione [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) .

Per le chiamate di funzione [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) vengono registrati i parametri seguenti:



| Parametro                                                                                                | Descrizione                                                                            |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Processo<br/>         | Indirizzo della struttura EPROCESS del kernel per il processo.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint<br/>     | Indirizzo del socket del kernel Winsock utilizzato come identificatore univoco per un socket.<br/> |
| <span id="EventMask"></span><span id="eventmask"></span><span id="EVENTMASK"></span>EventMask<br/> | Valore per la maschera di evento. <br/>                                              |



 

## <a name="dropped-datagram"></a>Datagramma eliminato

ID evento = 33 (IPv4), ID evento = 34 (IPv6)

Livello = 5 (dettagliato)

Per semplificare la diagnosi dei problemi relativi alle applicazioni datagramma, vengono tracciati gli eventi Winsock seguenti:

-   Quando arriva un datagramma, questo viene eliminato allo spazio del buffer insufficiente.
-   In un datagramma connesso, se i dati arrivano da un'origine diversa dalla destinazione connessa.

Vengono registrati i seguenti parametri per i datagrammi eliminati:



| Parametro                                                                                                    | Descrizione                                                                            |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Processo<br/>             | Indirizzo della struttura EPROCESS del kernel per il processo.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint<br/>         | Indirizzo del socket del kernel Winsock utilizzato come identificatore univoco per un socket.<br/> |
| <span id="PacketSize"></span><span id="packetsize"></span><span id="PACKETSIZE"></span>PacketSize<br/> | Dimensioni del pacchetto che è stato eliminato. <br/>                                   |
| <span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Indirizzo<br/>             | Indirizzo IP dell'origine del pacchetto. <br/>                                |
| <span id="Port"></span><span id="port"></span><span id="PORT"></span>Porta<br/>                         | Numero di porta IP dell'origine del pacchetto.<br/>                             |
| <span id="Reason"></span><span id="reason"></span><span id="REASON"></span>Motivo<br/>                 | Il codice di errore o il motivo per cui il pacchetto è stato eliminato.<br/>                            |



 

## <a name="connection-indicated"></a>Connessione indicata

ID evento = 35 (IPv4), ID evento = 36 (IPv6)

Livello = 5 (dettagliato)

Gli eventi Winsock seguenti sono tracciati per le operazioni indicate per la connessione:

-   Un'applicazione riceve una richiesta di connessione.

Vengono registrati i seguenti parametri per le connessioni indicate dagli eventi di trasporto:



| Parametro                                                                                            | Descrizione                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Processo<br/>     | Indirizzo della struttura EPROCESS del kernel per il processo.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint<br/> | Indirizzo del socket del kernel Winsock utilizzato come identificatore univoco per un socket.<br/> |
| <span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Indirizzo<br/>     | Indirizzo IP remoto. <br/>                                                     |
| <span id="Port"></span><span id="port"></span><span id="PORT"></span>Porta<br/>                 | Numero di porta IP remoto.<br/>                                                  |



 

## <a name="data-indicated"></a>Dati indicati

ID evento = 37

Livello = 5 (dettagliato)

Gli eventi Winsock seguenti sono tracciati per le operazioni di dati indicate:

-   Un'applicazione riceve i dati su un socket connesso.

I parametri seguenti vengono registrati per i dati indicati dagli eventi di trasporto:



| Parametro                                                                                                                        | Descrizione                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Processo<br/>                                 | ID del processo proprietario.<br/>                                                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint<br/>                             | Indirizzo del socket del kernel Winsock utilizzato come identificatore univoco per un socket.<br/> |
| <span id="Bytes_Indicated"></span><span id="bytes_indicated"></span><span id="BYTES_INDICATED"></span>Byte indicati<br/> | Numero di byte ricevuti sul socket.<br/>                                 |



 

## <a name="data-indicated-from-transport"></a>Dati indicati dal trasporto

ID evento = 38 (IPv4), ID evento = 39 (IPv6)

Livello = 5 (dettagliato)

Gli eventi Winsock seguenti sono tracciati per i dati indicati dalle operazioni di trasporto:

-   Un'applicazione invia una richiesta di ricezione e riceve i dati.

I parametri seguenti vengono registrati per i dati indicati dagli eventi di trasporto:



| Parametro                                                                                                                        | Descrizione                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Processo<br/>                                 | Indirizzo della struttura EPROCESS del kernel per il processo.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint<br/>                             | Indirizzo del socket del kernel Winsock utilizzato come identificatore univoco per un socket.<br/> |
| <span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Indirizzo<br/>                                 | Indirizzo IP remoto. <br/>                                                     |
| <span id="Port"></span><span id="port"></span><span id="PORT"></span>Porta<br/>                                             | Numero di porta IP remoto.<br/>                                                  |
| <span id="Bytes_Indicated"></span><span id="bytes_indicated"></span><span id="BYTES_INDICATED"></span>Byte indicati<br/> | Numero di byte ricevuti sul socket.<br/>                                 |



 

## <a name="disconnect-indicated-from-transport"></a>Disconnessione indicata dal trasporto

ID evento = 41

Livello = 5 (dettagliato)

Gli eventi Winsock seguenti sono tracciati per le operazioni di disconnessione indicate:

-   Un'applicazione riceve un'indicazione di disconnessione.

I parametri seguenti vengono registrati per la disconnessione indicata dagli eventi di trasporto:



| Parametro                                                                                            | Descrizione                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>Processo<br/>     | Indirizzo della struttura EPROCESS del kernel per il processo.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Endpoint<br/> | Indirizzo del socket del kernel Winsock utilizzato come identificatore univoco per un socket.<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Controllo della traccia Winsock](control-of-winsock-tracing.md)
</dt> <dt>

[Traccia Winsock](winsock-tracing.md)
</dt> <dt>

[Dettagli della traccia delle modifiche del catalogo Winsock](winsock-layered-service-provider-tracing-event-details.md)
</dt> <dt>

[Livelli di traccia Winsock](winsock-tracing-levels.md)
</dt> </dl>

 

 
