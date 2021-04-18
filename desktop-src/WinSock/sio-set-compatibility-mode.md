---
description: Richiede il modo in cui lo stack di rete deve gestire determinati comportamenti per i quali la modalità predefinita di gestione del comportamento può essere diversa nelle versioni di Windows.
ms.assetid: 9574e21f-5ac4-4210-8031-2f3b07416813
title: Codice di controllo SIO_SET_COMPATIBILITY_MODE
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 58972595adb71a30728cb4817a80814cd987a6de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306902"
---
# <a name="sio_set_compatibility_mode-control-code"></a>Codice di controllo SIO_SET_COMPATIBILITY_MODE

## <a name="description"></a>Descrizione

Il codice di controllo della **\_ \_ \_ modalità di compatibilità set sio** richiede il modo in cui lo stack di rete deve gestire determinati comportamenti per i quali la modalità predefinita di gestione del comportamento può essere diversa nelle versioni di Windows.

Per eseguire questa operazione, chiamare la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con i parametri seguenti.

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_SET_COMPATIBILITY_MODE, // dwIoControlCode
  (LPVOID) lpvInBuffer,    // pointer to WSA_COMPATIBILITY_MODE struct
  (DWORD) cbInBuffer,      // length of input buffer
  NULL,         // output buffer
  0,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_SET_COMPATIBILITY_MODE, // dwIoControlCode
  (LPVOID) lpvInBuffer,    // pointer to WSA_COMPATIBILITY_MODE struct
  (DWORD) cbInBuffer,      // length of input buffer
  NULL,         // output buffer
  0,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a>Parametri

### <a name="s"></a>s

Descrittore che identifica un socket.

### <a name="dwiocontrolcode"></a>dwIoControlCode

Codice di controllo per l'operazione.
Usare **la \_ \_ \_ modalità di compatibilità set sio** per questa operazione.

### <a name="lpvinbuffer"></a>lpvInBuffer

Puntatore al buffer di input.
Questo parametro deve puntare a una struttura della **\_ \_ modalità di compatibilità WSA** .

### <a name="cbinbuffer"></a>cbInBuffer

Dimensione, in byte, del buffer di input.
Questo parametro deve essere maggiore o uguale alla dimensione della struttura della **\_ \_ modalità di compatibilità WSA** a cui punta il parametro *lpvInBuffer* .

### <a name="lpvoutbuffer"></a>lpvOutBuffer

Puntatore al buffer di output.
Questo parametro non è utilizzato per questa operazione.

### <a name="cboutbuffer"></a>cbOutBuffer

Dimensione, in byte, del buffer di output.
Questo parametro deve essere impostato su zero.

### <a name="lpcbbytesreturned"></a>lpcbBytesReturned

Puntatore a una variabile che riceve le dimensioni, in byte, dei dati archiviati nel buffer di output.
Il parametro restituito punta a un valore **DWORD** pari a zero per questa operazione, poiché non è presente alcun output.

### <a name="lpvoverlapped"></a>lpvOverlapped

Puntatore a una struttura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .

Se il socket *s* è stato creato senza l'attributo Overlapped, il parametro *lpOverlapped* viene ignorato.

Se *s* è stato aperto con l'attributo Overlapped e il parametro *LpOverlapped* non è **null**, l'operazione viene eseguita come operazione sovrapposta (asincrona).
In questo caso, il parametro *lpOverlapped* deve puntare a una struttura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) valida.

Per le operazioni sovrapposte, la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** restituisce immediatamente un risultato e il metodo di completamento appropriato viene segnalato al completamento dell'operazione.
In caso contrario, la funzione non restituisce alcun risultato fino a quando l'operazione non viene completata o si verifica un errore.

### <a name="lpcompletionroutine"></a>Il lpCompletionRoutine

Tipo: \_ in_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)

Puntatore alla routine di completamento chiamata quando l'operazione è stata completata (ignorata per i socket non sovrapposti).

### <a name="lpthreadid"></a>lpThreadId

Puntatore a una struttura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) che deve essere usata dal provider in una chiamata successiva a [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc).
Il provider deve archiviare la struttura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a cui si fa riferimento (non il puntatore alla stessa) finché non viene restituito il risultato della funzione [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) .

**Nota**  Questo parametro è valido solo per la funzione **WSPIoctl** .

### <a name="lperrno"></a>lpErrno

Puntatore al codice di errore.

**Nota**  Questo parametro è valido solo per la funzione **WSPIoctl** .

## <a name="return-value"></a>Valore restituito

Se l'operazione viene completata correttamente, la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** restituisce zero.

Se l'operazione ha esito negativo o è in sospeso, la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** restituisce un **\_ errore socket**.
Per ottenere informazioni estese sull'errore, chiamare [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).

| Codice di errore | Significato |
|------------|---------|
| **\_io WSA \_ in sospeso** | Un'operazione sovrapposta è stata avviata correttamente e il completamento verrà indicato in un secondo momento. |
| **\_operazione WSA \_ interrotta** | Un'operazione sovrapposta è stata annullata a causa della chiusura del socket o dell'esecuzione del comando IOCTL **\_ Flush sio** . |
| **WSAEFAULT** | Il parametro *lpOverlapped* o *il lpCompletionRoutine* non è interamente contenuto in una parte valida dello spazio degli indirizzi utente. |
| **WSAEINPROGRESS** | La funzione viene richiamata quando è in corso un callback. |
| **WSAEINTR** | Un'operazione di blocco è stata interrotta. |
| **WSAEINVAL** | Il parametro *dwIoControlCode* non è un comando valido oppure un parametro di input specificato non è accettabile oppure il comando non è applicabile al tipo di socket specificato. Questo errore viene restituito se il parametro *cbInBuffer* è minore di sizeof la struttura **della \_ \_ modalità di compatibilità WSA** .
| **WSAENETDOWN** | Il sottosistema di rete non è riuscito. |
| **WSAENOPROTOOPT** | L'opzione socket non è supportata nel protocollo specificato. |
| **WSAENOTCONN** | Il Socket s non è connesso. |
| **WSAENOTSOCK** | Il descrittore *s* non è un socket. |
| **ILWSAEOPNOTSUPP** | Il comando IOCTL specificato non è supportato. Questo errore viene restituito se la **\_ modalità di \_ compatibilità \_ del set sio** non è supportata dal provider di trasporto. Questo errore viene restituito anche quando un tentativo di usare la **\_ modalità di \_ compatibilità \_ set sio** viene eseguito su un socket di datagramma. |

## <a name="remarks"></a>Commenti

la **\_ modalità di \_ compatibilità \_ set sio** richiede il modo in cui lo stack di rete deve gestire determinati comportamenti per i quali la modalità predefinita di gestione del comportamento può essere diversa nelle versioni di Windows.
La struttura degli argomenti di input per la **\_ \_ \_ modalità di compatibilità set sio** è specificata nella struttura della **\_ \_ modalità di compatibilità WSA** definita nel file di intestazione *Mswsockdef. h* .
Un puntatore alla struttura **della \_ \_ modalità di compatibilità WSA** viene passato nel parametro *cbInBuffer* .
Questa struttura viene definita nel modo seguente:

```cpp
// Need to #include <mswsock.h>

/* Argument structure for SIO_SET_COMPATIBILITY_MODE */
typedef struct _WSA_COMPATIBILITY_MODE {
    WSA_COMPATIBILITY_BEHAVIOR_ID BehaviorId;
    ULONG TargetOsVersion;
} WSA_COMPATIBILITY_MODE, *PWSA_COMPATIBILITY_MODE;
```

Il valore specificato nel membro **BehaviorId** indica il comportamento richiesto.
Il valore specificato nel membro **TargetOSVersion** indica la versione di Windows richiesta per il comportamento.

Il membro **BehaviorId** può essere uno dei valori del tipo di **enumerazione \_ \_ \_ ID del comportamento di compatibilità WSA** definito nel file di intestazione *Mswsockdef. h* .
I valori possibili per il membro **BehaviorId** sono i seguenti:

| Termine | Descrizione |
|------|-------------|
| WsaBehaviorAll | Questa operazione equivale a richiedere tutti i possibili comportamenti compatibili definiti per l'ID del **\_ comportamento di \_ \_ compatibilità WSA**. |
| WsaBehaviorReceiveBuffering | Quando il membro **TargetOSVersion** è impostato su un valore per Windows Vista o versione successiva, le riduzioni delle dimensioni del buffer di ricezione TCP in questo socket con l'opzione socket **\_ RCVBUF** sono consentite anche dopo la creazione di una connessione TCP. Quando il membro **TargetOSVersion** è impostato su un valore precedente a Windows Vista, le riduzioni delle dimensioni del buffer di ricezione TCP in questo socket con l'opzione socket **\_ RCVBUF** non sono consentite dopo lo stabilimento della connessione. |
| WsaBehaviorAutoTuning | Quando il membro **TargetOSVersion** è impostato su un valore per Windows Vista o versione successiva, l'ottimizzazione automatica della finestra di ricezione è abilitata e il fattore di scala della finestra TCP viene ridotto a 2 rispetto al valore predefinito di 8. Quando **TargetOSVersion** è impostato su un valore precedente a Windows Vista, l'ottimizzazione automatica della finestra di ricezione è disabilitata. Anche l'opzione di scalabilità della finestra TCP è disabilitata e le dimensioni massime della finestra di ricezione true sono limitate a 65.535 byte. Non è possibile negoziare l'opzione di scalabilità della finestra TCP sulla connessione anche se per questo socket è stata chiamata l'opzione **\_ RCVBUF** socket, che specifica un valore maggiore di 65.535 byte prima che sia stata stabilita la connessione. |

Il membro **TargetOSVersion** può essere una delle costanti di versione NTDDI definite nel file di intestazione *Sdkddkver. h* .
Alcuni dei valori possibili per il membro **TargetOSVersion** sono i seguenti:

| Termine | Descrizione |
|------|-------------|
| NTDDI \_ Longhorn | Il comportamento di destinazione è l'impostazione predefinita per Windows Vista. |
| \_WS03 NTDDI | Il comportamento di destinazione è l'impostazione predefinita per Windows Server 2003. |
| NTDDI \_ WinXP | Il comportamento di destinazione è l'impostazione predefinita per Windows XP. |
| \_Win2k NTDDI | Il comportamento di destinazione è l'impostazione predefinita per Windows 2000. |

L'effetto principale del membro **TargetOSVersion** è se il membro è impostato su un valore uguale o maggiore di **NTDDI \_ Longhorn**.

Le prestazioni TCP dipendono non solo dalla velocità di trasferimento, bensì dal prodotto della velocità di trasferimento e dal tempo di ritardo del round trip.
Questo prodotto a ritardo della larghezza di banda misura la quantità di dati che "riempiono la pipe".
Questo prodotto con ritardo della larghezza di banda è lo spazio del buffer necessario al mittente e al destinatario per ottenere la velocità effettiva massima sulla connessione TCP sul percorso.
Questo spazio buffer rappresenta la quantità di dati non riconosciuti che TCP deve gestire per garantire la completa pipeline.
Si verificano problemi di prestazioni TCP quando il prodotto con ritardo della larghezza di banda è elevato.
Un percorso di rete che opera in queste condizioni è spesso definito "pipe lungo e FAT".
Gli esempi includono collegamenti satellitari per pacchetti ad alta capacità, collegamenti wireless ad alta velocità e collegamenti fibre ottici terrestri su lunghe distanze.

L'intestazione TCP utilizza un campo dati a 16 bit (il campo finestra nell'intestazione del pacchetto TCP) per segnalare le dimensioni della finestra di ricezione al mittente.
Pertanto, la finestra più grande che può essere utilizzata è 65.535 byte.
Per ovviare a questa limitazione, è stata aggiunta un'opzione di estensione TCP per il protocollo TCP a prestazioni elevate per consentire la distribuzione di Windows con dimensioni maggiori di 65.535 byte.
L'opzione di scalabilità della finestra TCP (WSopt) è definita nella RFC 1323 disponibile sul [sito Web IETF](https://www.ietf.org/rfc/rfc1122.txt).
L'estensione WSopt espande la definizione della finestra TCP a 32 bit usando un fattore di scala logaritmico a un byte per estendere il campo della finestra a 16 bit nell'intestazione TCP.
L'estensione WSopt definisce un fattore di scala implicito (2 a una potenza), che viene usato per moltiplicare il valore delle dimensioni della finestra trovato in un'intestazione TCP per ottenere le dimensioni della finestra vera e propria.
Pertanto, un fattore di scala della finestra pari a 8 comporterebbe una vera dimensione della finestra uguale al valore nel campo della finestra nell'intestazione TCP moltiplicato per 2 ^ 8 o 256.
Quindi, se il campo finestra nell'intestazione TCP è stato impostato sul valore massimo di 65.535 byte e il fattore di scala WSopt è stato negoziato con un valore pari a 8, le dimensioni della finestra true sarebbero 16.776.960 byte.

La dimensione effettiva della finestra di ricezione e pertanto il fattore di scala è determinata dallo spazio massimo del buffer di ricezione.
Questo spazio di buffer massimo corrisponde alla quantità di dati che un ricevitore TCP consente a un mittente TCP di inviare prima di dover attendere il riconoscimento.
Una volta stabilita la connessione, la dimensione della finestra di ricezione viene annunciata in ogni segmento TCP, ovvero il campo della finestra nell'intestazione TCP.
L'annuncio della quantità massima di dati che il mittente può inviare è un meccanismo di controllo del flusso lato ricevitore che impedisce al mittente di inviare i dati che il ricevitore non può archiviare.
Un host di invio può inviare solo la quantità massima di dati annunciata dal ricevitore prima di attendere un riconoscimento e l'aggiornamento delle dimensioni della finestra di ricezione.

In Windows Server 2003 e Windows XP, lo spazio massimo del buffer di ricezione che rappresenta le dimensioni della finestra di ricezione per lo stack TCP/IP ha un valore predefinito basato sulla velocità di collegamento dell'interfaccia di invio.
Il valore effettivo si adatta automaticamente a incrementi delle dimensioni massime del segmento (MSS) negoziate durante lo stabilimento di connessione TCP.
Quindi, per un collegamento di 10 Mbit/sec, le dimensioni predefinite della finestra di ricezione vengono normalmente impostate su 16K bytes, mentre in un collegamento 100 MBit/sec la dimensione della finestra di ricezione predefinita viene impostata su 65.535 byte.

In Windows Server 2003 e Windows XP, le dimensioni massime della finestra di ricezione per lo stack TCP/IP possono essere configurate manualmente utilizzando i seguenti valori del registro di sistema in un'interfaccia specifica o per l'intero sistema:

`HKEY_LOCAL_MACHINE\SYSTEM\Current Control Set\Services\Tcpip\Parameters\TCPWindowSize`

`HKEY_LOCAL_MACHINE\SYSTEM\Current Control Set\Services\Tcpip\Parameters\Interface\TCPWindowSize`

Il valore del registro di sistema per **TcpWindowSize** può essere impostato su un massimo di 65.535 byte quando non si usa l'estensione wsopt o un massimo di 1.073.741.823 byte quando viene usata l'estensione wsopt (è supportato un fattore di scala massimo 4).
Senza il ridimensionamento delle finestre, un'applicazione può ottenere solo una velocità effettiva di circa 5 megabit al secondo (Mbps) in un percorso con un tempo di round trip di 100 millisecondi (RTT), indipendentemente dalla larghezza di banda del percorso.
Questa velocità effettiva può essere ridotta a più di un gigabit al secondo (Gbps) con la scalabilità della finestra, che consente a TCP di negoziare il fattore di scala per le dimensioni della finestra durante lo stabilimento della connessione.

In Windows Server 2003 e Windows XP è possibile abilitare l'estensione WSopt impostando il valore del registro di sistema seguente.

`HKEY_LOCAL_MACHINE\SYSTEM\Current Control Set\Services\Tcpip\Parameters\Tcp1323Opts`

Il valore del registro di sistema **TCP1323Opts** è un **DWORD** codificato in modo che, quando è impostato il bit 0, è abilitata l'estensione TCP wsopt.
Quando è impostato il bit 1, è abilitata l'opzione TCP timestamp (TSopt) definita in RFC 1323.
Quindi, un valore pari a 1 o 3 consentirà di abilitare l'estensione WSopt.

In Windows Server 2003 e Windows XP, il valore predefinito è che i valori del registro di sistema TCPWindowSize e Tcp1323Opts non vengono creati.
Per impostazione predefinita, l'estensione WSopt è disabilitata e le dimensioni della finestra di ricezione TCP sono impostate dal sistema su un valore massimo di 65.535 byte in base alla velocità del collegamento.
Quando il ridimensionamento delle finestre è abilitato in Windows Server 2003 e Windows XP impostando il valore del registro di sistema Tcp1323Opts, la scalabilità della finestra in una connessione TCP viene comunque usata solo quando il mittente e il destinatario includono un'opzione di scalabilità della finestra TCP nel segmento Synchronize (SYN) inviato tra loro per negoziare un fattore di scala della finestra.
Quando si usa la scalabilità della finestra in una connessione, il campo della finestra nell'intestazione TCP viene impostato su 65.535 byte e il fattore di scala della finestra viene usato per regolare la dimensione della finestra di ricezione reale verso l'alto in base al fattore di scala della finestra negoziato quando viene stabilita la connessione.

Un'applicazione può specificare le dimensioni della finestra di ricezione TCP per una connessione utilizzando l'opzione **\_ RCVBUF** socket.
Le dimensioni della finestra di ricezione TCP per un socket possono essere aumentate in qualsiasi momento usando **\_ RCVBUF**, ma è possibile ridurle solo prima di stabilire una connessione.
Per usare il ridimensionamento delle finestre, un'applicazione deve specificare una dimensione della finestra maggiore di 65.535 byte quando si usa l'opzione **\_ RCVBUF** socket, prima che venga stabilita la connessione.

Il valore ideale per le dimensioni della finestra di ricezione TCP è spesso difficile da determinare.
Per riempire la capacità della rete tra il mittente e il destinatario, le dimensioni della finestra di ricezione devono essere impostate sul prodotto con ritardo della larghezza di banda per la connessione, ovvero la larghezza di banda moltiplicata per il tempo di round trip.
Anche se un'applicazione è in grado di determinare correttamente il prodotto con ritardo della larghezza di banda, non è ancora noto quanto velocemente l'applicazione ricevente recupererà i dati dal buffer dei dati in ingresso (la velocità di recupero dell'applicazione).
Nonostante il supporto per il ridimensionamento delle finestre TCP, le dimensioni massime della finestra di ricezione in Windows Server 2003 e Windows XP possono comunque limitare la velocità effettiva perché si tratta di una dimensione massima fissa per tutte le connessioni TCP (a meno che non sia specificata per ogni applicazione che usa **\_ RCVBUF**), che può migliorare la velocità effettiva per alcune connessioni e ridurre la velocità effettiva per altri
Inoltre, le dimensioni massime della finestra di ricezione fisse per una connessione TCP non variano in base alle condizioni di rete mutevoli.

Per risolvere il problema della corretta determinazione del valore delle dimensioni massime della finestra di ricezione per una connessione TCP in base alle condizioni correnti della rete, lo stack TCP/IP in Windows Vista supporta una funzionalità di ottimizzazione automatica della finestra di ricezione.
Quando questa funzionalità è abilitata, l'ottimizzazione automatica della finestra di ricezione determina continuamente le dimensioni ottimali della finestra di ricezione misurando il prodotto con ritardo della larghezza di banda e la velocità di recupero dell'applicazione e regola le dimensioni massime massime della finestra di ricezione in base alle mutevoli condizioni della rete.
L'ottimizzazione automatica della finestra di ricezione Abilita l'estensione TCP WSopt per impostazione predefinita, consentendo fino a 16.776.960 byte per le dimensioni della finestra vera e propria.
Quando i dati passano attraverso la connessione, lo stack TCP/IP monitora la connessione, misura il prodotto con ritardo della larghezza di banda corrente per la connessione e la velocità di ricezione dell'applicazione e regola le dimensioni effettive della finestra di ricezione per ottimizzare la velocità effettiva.
Lo stack TCP/IP modifica il valore del campo finestra nell'intestazione TCP in base alle condizioni della rete, perché il fattore di scala WSopt viene corretto quando la connessione viene stabilita per la prima volta.

Lo stack TCP/IP in Windows Vista non utilizza più i valori del registro di sistema **TcpWindowSize** .
Con una migliore velocità effettiva tra i peer TCP, l'utilizzo della larghezza di banda di rete aumenta durante il trasferimento dei dati.
Se tutte le applicazioni sono ottimizzate per la ricezione di dati TCP, l'utilizzo complessivo della rete può aumentare in modo sostanziale, rendendo l'utilizzo di QoS (Quality of Service) più importante nelle reti che operano alla capacità o quasi in prossimità.

Il comportamento predefinito in Windows Vista per il buffer di ricezione quando la **\_ \_ \_ modalità di compatibilità set sio** non viene specificato con **WsaBehaviorReceiveBuffering** è che non sono consentite riduzioni delle dimensioni della finestra di ricezione che utilizzano l'opzione di socket **\_ RCVBUF** , dopo che è stata stabilita una connessione.

Il comportamento predefinito in Windows Vista per l'ottimizzazione automatica quando **la \_ \_ \_ modalità di compatibilità set sio** non viene specificato con **WsaBehaviorAutoTuning** è che lo stack effettuerà l'ottimizzazione automatica della finestra di ricezione usando un fattore di scala della finestra pari a 8.
Si noti che se un'applicazione imposta una dimensione della finestra di ricezione valida con l'opzione **\_ RCVBUF** socket, lo stack utilizzerà la dimensione specificata e l'ottimizzazione automatica della ricezione della finestra sarà disabilitata.
L'ottimizzazione automatica di Windows può anche essere disabilitata completamente usando il comando seguente, `netsh interface tcp set global autotuninglevel=disabled` , nel qual caso la specifica di **WsaBehaviorAutoTuning** non avrà alcun effetto.
L'ottimizzazione automatica della ricezione della finestra può anche essere disabilitata in base a criteri di gruppo impostati in Windows Server 2008.

L'opzione **WsaBehaviorAutoTuning** è necessaria in Windows Vista per alcuni dispositivi gateway Internet e firewall che non supportano correttamente i flussi di dati per le connessioni TCP che usano l'estensione wsopt e un fattore di scala Windows.
In Windows Vista, per impostazione predefinita, un ricevitore negozia un fattore di scala della finestra pari a 8 per una dimensione massima effettiva della finestra di 16.776.960 byte.
Quando i dati iniziano a propagarsi su un collegamento rapido, Windows inizia inizialmente con una dimensione della finestra vera 64 kilobyte impostando il campo finestra dell'intestazione TCP su 256 e impostando il fattore di scala della finestra su 8 nelle opzioni TCP (256 * 2 ^ 8 = 64KB).
Alcuni dispositivi e firewall del gateway Internet ignorano il fattore di scalabilità della finestra e esaminano solo il campo finestra annunciata nell'intestazione TCP specificata come 256 e rilasciano i pacchetti in ingresso per la connessione che contiene più di 256 byte di dati TCP.
Per supportare la scalabilità della finestra di ricezione TCP, un dispositivo o un firewall gateway deve monitorare l'handshake TCP e tenere traccia del fattore di scala della finestra negoziato come parte dei dati di connessione TCP.
Inoltre, alcune applicazioni e implementazioni di stack TCP su altre piattaforme ignorano l'estensione TCP WSopt e il fattore di scala della finestra.
Quindi, l'host remoto che invia i dati può inviare i dati alla tariffa annunciata nel campo finestra dell'intestazione TCP (256 byte).
Ciò può comportare la ricezione di dati molto lentamente dal ricevitore.

Impostando il membro **BehaviorId** su **WsaBehaviorAutoTuning** e **TargetOSVersion** su Windows Vista, il fattore di scala della finestra viene ridotto a 2, in modo che il campo finestra nell'intestazione TCP venga inizialmente impostato su 16.384 byte e il fattore di scala della finestra sia impostato su 2 per una dimensione di ricezione della finestra true iniziale di 64K byte.
La funzionalità di ottimizzazione automatica della finestra può quindi aumentare le dimensioni di ricezione della finestra true fino a 262.140 byte impostando il campo finestra nell'intestazione TCP su 65.535 byte.
Un'applicazione deve impostare la **\_ modalità di \_ compatibilità \_ del set sio** non appena viene creato un socket, perché questa opzione non ha senso o si applica dopo l'invio di un SYN.
L'impostazione di questa opzione ha lo stesso effetto del comando seguente: `netsh interface tcp set global autotuninglevel=highlyrestricted`

Si noti che il file di intestazione *Mswsockdef. h* viene incluso automaticamente in *mswsock. h* o *Netiodef. h* e non deve essere utilizzato direttamente.

## <a name="see-also"></a>Vedi anche

[**presa**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
