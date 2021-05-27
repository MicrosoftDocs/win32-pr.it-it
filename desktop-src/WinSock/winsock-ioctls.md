---
description: Argomento di navigazione per gli IOCTL socket di Windows Sockets (Winsock).
ms.assetid: 6a63c2c9-4e09-4a62-b39f-3ccb26287da8
title: IOCTL Winsock (Winsock2.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eadf4a0e2799d6123bf81069fe65ea16313af444
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550256"
---
# <a name="winsock-ioctls"></a>IOCTL winsock

Questa sezione descrive i controlli di input/output (IOCTL) di Winsock Socket per diverse edizioni dei sistemi operativi Windows. Usare la [**funzione WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) o [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) per eseguire un ioCTL Winsock per controllare la modalità di un socket, il protocollo di trasporto o il sottosistema delle comunicazioni.

Alcuni IOCL Winsock richiedono una spiegazione maggiore di quanto possa comunicare questa tabella. tali opzioni contengono collegamenti ad argomenti aggiuntivi.

È possibile adottare uno schema di codifica che manteni gli opcode [**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket) attualmente definiti, offrendo al tempo stesso un modo pratico per partizionare lo spazio dell'identificatore del codice operativo in quanto il *parametro dwIoControlCode* è ora un'entità a 32 bit. Il *parametro dwIoControlCode* viene compilato per consentire l'indipendenza del protocollo e del fornitore quando si aggiungono nuovi codici di controllo mantenendo la compatibilità con le versioni precedenti con i codici di controllo di Windows Sockets 1.1 e Unix. Il *formato del parametro dwIoControlCode* è il seguente.

| I  | O  | V  | T  | Famiglia di fornitori/indirizzi | Codice                   |
|-|-|-|-|-|-|
| 3  | 3  | 2  | 2 2 | 2 2 2 2 2 2 2 1 1 1 1 | 1 1 1 1 1 1              |
| 1  | 0  | 9  | 8 7 | 6 5 4 3 2 1 0 9 8 7 6 | 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0 |

> [!Note] 
> I bit nel *parametro dwIoControlCode* visualizzato nella tabella devono essere letti verticalmente dall'alto verso il basso in base alla colonna. Il bit più a sinistra è il bit 31, il bit successivo è il bit 30 e il bit più a destra è il bit 0.

Viene impostato se il buffer di input è valido per il codice, come **con IOC_IN**.

O viene impostato se il buffer di output è valido per il codice, come **IOC_OUT**. I codici di controllo che usano buffer di input e output impostano sia I che O.

V viene impostato se non sono presenti parametri per il codice, come con **IOC_VOID**.

T è una quantità a 2 bit che definisce il tipo di IOCTL. Vengono definiti i valori seguenti:

0 IoCTL è un codice IOCTL Unix standard, come con **FIONREAD** e **FIONBIO.**

1 IoCTL è un codice IOCTL generico di Windows Sockets 2. I nuovi codici IOCTL definiti per Windows Sockets 2 avranno T == 1.

2 L'ioCTL si applica solo a una famiglia di indirizzi specifica.

3 L'IOCTL si applica solo al provider di un fornitore specifico, come **IOC_VENDOR**. Questo tipo consente alle società di essere assegnate a un numero di fornitore visualizzato nel **parametro vendor/address family.** Il fornitore può quindi definire nuovi IOCTL specifici per il fornitore senza dover registrare l'IOCTL con un'istanza di clearinghouse, garantendo in tal modo flessibilità e privacy al fornitore.

**Famiglia di fornitori/indirizzi** Quantità a 11 bit che definisce il fornitore proprietario del codice (se T == 3) o che contiene la famiglia di indirizzi a cui si applica il codice (se T == 2). Se si tratta di un codice IOCTL Unix (T == 0), questo parametro ha lo stesso valore del codice in Unix. Se si tratta di un IOCTL di Windows Sockets 2 generico (T == 1), questo parametro può essere usato come estensione del parametro di codice per fornire valori di codice aggiuntivi.

**Codice** Quantità a 16 bit che contiene il codice IOCTL specifico per l'operazione.

## <a name="unix-ioctl-codes"></a>Codici IOCTL Unix

Sono supportati i codici (comandi) IOCTL Unix seguenti.

### <a name="fionbio"></a>FIONBIO

Abilitare o disabilitare la modalità non bloccante nel socket *.* Il *parametro lpvInBuffer* punta a un valore **unsigned long** (QoS), che è diverso da zero se deve essere abilitata la modalità non bloccante e zero se deve essere disabilitato. Quando viene creato, un socket opera in modalità di blocco, ovvero la modalità non di blocco è disabilitata. Questo è coerente con i socket BSD.

La routine [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) o [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) imposta automaticamente un socket in modalità non di blocco. Se **WSAAsyncSelect** o **WSAEventSelect** è stato rilasciato in un socket, qualsiasi tentativo di usare [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) per impostare il socket sulla modalità di blocco avrà esito negativo con WSAEINVAL. Per impostare nuovamente il socket sulla modalità di blocco, un'applicazione deve prima disabilitare **WSAAsyncSelect** chiamando **WSAAsyncSelect** con il parametro *lEvent* uguale a zero oppure disabilitare **WSAEventSelect** chiamando **WSAEventSelect** con il parametro *lNetworkEvents* uguale a zero.

### <a name="fionread"></a>FIONREAD

Determinare la quantità di dati che possono essere letti atomicamente da socket *s*. Il *parametro lpvOutBuffer* punta a **un valore long senza** segno in cui [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) archivia il risultato.

Se il socket passato nel parametro *s* è orientato al flusso (ad esempio, il tipo SOCK \_ STREAM), **FIONREAD** restituisce la quantità totale di dati che possono essere letti in una singola operazione di ricezione. Questo è in genere lo stesso della quantità totale di dati accodati nel socket (poiché un flusso di dati è orientato ai byte, questo non è garantito).

Se il socket passato nel parametro *s* è orientato ai messaggi (ad esempio, tipo SOCK \_ DGRAM), **FIONREAD** restituisce il numero totale di byte disponibili per la lettura, non le dimensioni del primo datagramma (messaggio) accodato sul socket.

### <a name="siocatmark"></a>SIOCATMARK

Determinare se tutti i dati OOB sono stati letti. Ciò si applica solo a un socket di tipo flusso (ad esempio, sock STREAM) configurato per la ricezione inline di tutti i dati \_ OOB (SO \_ OOBINLINE). Se nessun dato OOB è in attesa di essere letto, l'operazione restituisce TRUE. In caso contrario, restituisce **FALSE** e l'operazione di ricezione successiva eseguita sul socket recupererà alcuni o tutti i dati che precedono il contrassegno. l'applicazione deve usare **l'operazione SIOCATMARK** per determinare se rimane. Se sono presenti dati normali che precedono i dati urgenti (fuori banda), verranno ricevuti nell'ordine indicato. Si noti che [**le operazioni recv**](/windows/desktop/api/winsock/nf-winsock-recv) non combinano mai dati OOB e normali nella stessa chiamata. *lpvOutBuffer* punta a un oggetto BOOL in [**cui WSAIoctl archivia**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) il risultato.

## <a name="windows-sockets-2-commands"></a>Comandi di Windows Sockets 2

Sono supportati i comandi di Windows Sockets 2 seguenti.

### <a name="sio_acquire_port_reservation-opcode-setting-i-t3"></a>SIO_ACQUIRE_PORT_RESERVATION (impostazione del codice operativo: I, T==3)

Richiedere una prenotazione di runtime per un blocco di porte TCP o UDP. Per le prenotazioni di porte di runtime, il pool di porte richiede che le prenotazioni siano utilizzate dal processo sul cui socket è stata concessa la prenotazione. Le prenotazioni di porte di runtime durano solo fino alla durata del socket in cui è stato chiamato [**SIO \_ ACQUIRE PORT \_ \_ RESERVATION**](/previous-versions/windows/desktop/legacy/gg699720(v=vs.85)) IOCTL. Al contrario, le prenotazioni di porte persistenti create usando la [**funzione CreatePersistentTcpPortReservation**](/windows/win32/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) o [**CreatePersistentUdpPortReservation**](/windows/win32/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) possono essere utilizzate da qualsiasi processo con la possibilità di ottenere prenotazioni permanenti.

Per informazioni più dettagliate, vedere le informazioni di [**riferimento su SIO \_ ACQUIRE PORT \_ \_ RESERVATION.**](/previous-versions/windows/desktop/legacy/gg699720(v=vs.85))

[**SIO \_ ACQUIRE \_ PORT \_ RESERVATION**](/previous-versions/windows/desktop/legacy/gg699720(v=vs.85)) è supportato in Windows Vista e versioni successive del sistema operativo.

### <a name="sio_address_list_change-opcode-setting-v-t1"></a>SIO \_ ADDRESS LIST CHANGE \_ \_ (impostazione del codice operativo: V, T==1)

Per ricevere una notifica delle modifiche nell'elenco degli indirizzi di trasporto locali della famiglia di protocolli del socket a cui l'applicazione può eseguire l'associazione. Non verranno fornite informazioni di output al completamento di questo IOCTL. il completamento indica semplicemente che l'elenco di indirizzi locali disponibili è stato modificato e deve essere nuovamente sottoposto a query tramite **SIO \_ ADDRESS LIST \_ \_ QUERY**.

Si presuppone (anche se non obbligatorio) che l'applicazione usi operazioni di I/O sovrapposte per ricevere una notifica della modifica completando la richiesta **SIO \_ ADDRESS LIST \_ \_ CHANGE.** In alternativa, se **SIO \_ ADDRESS LIST \_ \_ CHANGE** IOCTL viene generato in un socket non bloccante e senza parametri sovrapposti (*lpOverlapped* lpCompletionRoutine è impostato su NULL), verrà completato immediatamente con l'errore /   [WSAEWOULDBLOCK](windows-sockets-error-codes-2.md).  L'applicazione può quindi attendere gli eventi di modifica dell'elenco indirizzi tramite una chiamata a [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) o [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) con bit CHANGE FD ADDRESS LIST impostato nella maschera di bit dell'evento \_ di \_ \_ rete.

### <a name="sio_address_list_query-opcode-setting-o-t1"></a>SIO \_ ADDRESS LIST QUERY \_ \_ (impostazione del codice operativo: O, T==1)

Ottiene un elenco di indirizzi di trasporto locali della famiglia di protocolli del socket a cui l'applicazione può eseguire l'associazione. L'elenco di indirizzi varia in base alla famiglia di indirizzi e alcuni indirizzi vengono esclusi dall'elenco.

> [!Note] 
> Negli ambienti Plug-n-Play Windows gli indirizzi possono essere aggiunti e rimossi dinamicamente. Pertanto, le applicazioni non possono basarsi sulle informazioni restituite da **SIO \_ ADDRESS LIST \_ \_ QUERY** per essere persistenti. Le applicazioni possono registrarsi per le notifiche di modifica degli indirizzi tramite **SIO \_ ADDRESS LIST \_ \_ CHANGE** IOCTL, che fornisce la notifica tramite un evento DI I/O sovrapposto o FD \_ ADDRESS LIST \_ \_ CHANGE. La sequenza di azioni seguente può essere usata per garantire che l'applicazione abbia sempre informazioni aggiornate sull'elenco di indirizzi:

-  Problema **SIO \_ ADDRESS LIST \_ \_ CHANGE** IOCTL
-  Problema **SIO \_ ADDRESS LIST \_ \_ QUERY** IOCTL
-  Ogni **volta che SIO ADDRESS LIST \_ \_ \_ CHANGE** IOCTL notifica all'applicazione la modifica dell'elenco di indirizzi (tramite I/O sovrapposto o segnalando l'evento FD ADDRESS LIST CHANGE), l'intera sequenza di azioni deve essere \_ ripetuta. \_ \_

Per informazioni più dettagliate, vedere le informazioni di [**riferimento su SIO \_ ADDRESS LIST \_ \_ QUERY.**](/previous-versions/windows/desktop/legacy/dd877219(v=vs.85)) **SIO \_ ADDRESS \_ LIST \_ QUERY** è supportato in Windows 2000 e versioni successive.

### <a name="sio_apply_transport_setting-opcode-setting-i-t3"></a>SIO \_ APPLY TRANSPORT SETTING \_ \_ (impostazione del codice operativo: I, T==3)

Applica un'impostazione di trasporto a un socket. L'impostazione di trasporto applicata si basa [**\_ \_ sull'ID TRANSPORT SETTING**](/windows/win32/api/transportsettingcommon/ns-transportsettingcommon-transport_setting_id) passato nel parametro *lpvInBuffer.*

L'unica impostazione di trasporto attualmente definita è per la funzionalità **\_ \_ DI \_** NOTIFICA IN TEMPO REALE su un socket TCP.

Se  [**\_ \_ l'ID**](/windows/win32/api/transportsettingcommon/ns-transportsettingcommon-transport_setting_id) IMPOSTAZIONE TRASPORTO passato ha il membro GUID impostato su **REAL TIME NOTIFICATION \_ \_ \_ CAPABILITY,** si tratta di una richiesta per applicare le impostazioni di notifica in tempo reale per il socket TCP usato con [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) per ricevere notifiche di rete in background in un'app di Windows Store.

Per informazioni più dettagliate, vedere le informazioni di [**riferimento su SIO \_ APPLY TRANSPORT \_ \_ SETTING.**](/previous-versions/windows/desktop/legacy/jj553481(v=vs.85)) **SIO \_ APPLY \_ TRANSPORT \_ SETTING** è supportato in Windows 8, Windows Server 2012 e versioni successive.

### <a name="sio_associate_handle-opcode-setting-i-t1"></a>SIO \_ ASSOCIATE \_ HANDLE (impostazione del codice operativo: I, T==1)

Associa il socket all'handle specificato di un'interfaccia correlata. Il buffer di input contiene il valore intero corrispondente alla costante manifesto per l'interfaccia complementare (ad esempio, TH NETDEV e \_ TH TAPI), seguito da un valore che è un handle dell'interfaccia complementare specificata, insieme a qualsiasi altra informazione \_ richiesta. Fare riferimento alla sezione appropriata in [Winsock Annexes per](winsock-annexes.md) informazioni dettagliate specifiche di una particolare interfaccia complementare. La dimensione totale viene riflessa nella lunghezza del buffer di input. Non è necessario alcun buffer di output. Il [codice di errore WSAENOPROTOOPT](windows-sockets-error-codes-2.md) è indicato per i provider di servizi che non supportano questo IOCTL. L'handle associato a questo IOCTL può essere recuperato usando **SIO \_ TRANSLATE \_ HANDLE**.

È possibile usare un'interfaccia complementare, ad esempio, se un provider specifico fornisce (1) una grande quantità di controlli aggiuntivi sul comportamento di un socket e (2) i controlli sono specifici del provider in modo tale che non esemplino il mapping alle funzioni esistenti di Windows Socket o a quelle che probabilmente verranno definite in futuro. È consigliabile usare Component Object Model (COM) anziché questo IOCTL per individuare e tenere traccia di altre interfacce che potrebbero essere supportate da un socket. Questo IOCTL è presente per la compatibilità (inversa) con i sistemi in cui COM non è disponibile o non può essere usato per altri motivi.

### <a name="sio_associate_port_reservation-opcode-setting-i-t3"></a>SIO \_ ASSOCIATE PORT RESERVATION \_ \_ (impostazione del codice operativo: I, T==3)

Associare un socket a una prenotazione di runtime o permanente per un blocco di porte TCP o UDP identificate dal token di prenotazione della porta. [**L'IOCTL SIO \_ ASSOCIATE \_ PORT \_ RESERVATION**](/previous-versions/windows/desktop/legacy/gg699721(v=vs.85)) deve essere emesso prima dell'associazione del socket. Se e quando il socket è associato, la porta assegnata verrà selezionata dalla prenotazione di porte identificata dal token specificato. Se non sono disponibili porte dalla prenotazione specificata, la [**chiamata di**](/windows/desktop/api/winsock/nf-winsock-bind) funzione bind avrà esito negativo.

Per informazioni più dettagliate, vedere le informazioni di [**riferimento su SIO \_ ASSOCIATE PORT \_ \_ RESERVATION.**](/previous-versions/windows/desktop/legacy/gg699721(v=vs.85))

[**SIO \_ ASSOCIATE \_ PORT \_ RESERVATION**](/previous-versions/windows/desktop/legacy/gg699721(v=vs.85)) è supportato in Windows Vista e versioni successive del sistema operativo.

### <a name="sio_base_handle-opcode-setting-o-t1"></a>SIO \_ BASE \_ HANDLE (impostazione del codice operativo: O, T==1)

Recupera l'handle del provider di servizi di base per un socket specificato. Il valore restituito è un **socket**.

Un provider di servizi a più livelli non intercetterebbe mai questo IOCTL perché il valore restituito deve essere l'handle socket dal provider di servizi di base.

Se il buffer di output non è sufficientemente grande per un handle socket *(cbOutBuffer* è minore delle dimensioni di un **SOCKET**) o il *parametro lpvOutBuffer* è un **puntatore NULL,** **socket \_ ERROR** viene restituito come risultato di questo IOCTL e [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) restituisce [WSAEFAULT](windows-sockets-error-codes-2.md).

**SIO \_ BASE \_ HANDLE** è definito nel file *di intestazione Mswsock.h* e supportato in Windows Vista e versioni successive.

### <a name="sio_bsp_handle-opcode-setting-o-t1"></a>SIO \_ BSP \_ HANDLE (impostazione del codice operativo: O, T==1)

Recupera l'handle del provider di servizi di base per un socket utilizzato dalla [**funzione WSASendMsg.**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) Il valore restituito è un **socket**.

Questo Ioctl viene usato da un provider di servizi a più livelli per garantire che intercetti la [**funzione WSASendMsg.**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg)

Se il buffer di output non è sufficientemente grande per un handle socket *(cbOutBuffer* è minore delle dimensioni di un **SOCKET**) o il *parametro lpvOutBuffer* è un **puntatore NULL,** **socket \_ ERROR** viene restituito come risultato di questo IOCTL e [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) restituisce [WSAEFAULT](windows-sockets-error-codes-2.md).

**SIO \_ BSP \_ HANDLE** è definito nel file *di intestazione Mswsock.h* e supportato in Windows Vista e versioni successive.

### <a name="sio_bsp_handle_select-opcode-setting-o-t1"></a>SIO \_ BSP \_ HANDLE SELECT \_ (impostazione del codice operativo: O, T==1)

Recupera l'handle del provider di servizi di base per un socket utilizzato dalla [**funzione select.**](/windows/desktop/api/Winsock2/nf-winsock2-select) Il valore restituito è un **socket**.

Questo Ioctl viene usato da un provider di servizi a più livelli per garantire che intercetti la [**funzione select.**](/windows/desktop/api/Winsock2/nf-winsock2-select)

Se il buffer di output non è sufficientemente grande per un handle socket *(cbOutBuffer* è minore delle dimensioni di un **SOCKET**) o il *parametro lpvOutBuffer* è un **puntatore NULL,** **socket \_ ERROR** viene restituito come risultato di questo IOCTL e [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) restituisce [WSAEFAULT](windows-sockets-error-codes-2.md).

**SIO \_ BSP \_ HANDLE \_ SELECT** è definito nel file *di intestazione Mswsock.h* e supportato in Windows Vista e versioni successive.

### <a name="sio_bsp_handle_poll-opcode-setting-o-t1"></a>SIO \_ BSP \_ HANDLE POLL \_ (impostazione del codice operativo: O, T==1)

Recupera l'handle del provider di servizi di base per un socket utilizzato dalla [**funzione WSAPoll.**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) Il *parametro lpOverlapped* deve essere un **puntatore NULL.** Il valore restituito è un **socket**.

Questo Ioctl viene usato da un provider di servizi a più livelli per garantire che intercetti la [**funzione WSAPoll.**](/windows/win32/api/winsock2/nf-winsock2-wsapoll)

Se le dimensioni del buffer di output non sono sufficienti per un handle di socket *(cbOutBuffer* è minore delle dimensioni di un **SOCKET),** il *parametro lpvOutBuffer* è **un puntatore NULL** o il parametro *lpOverlapped* non è un puntatore **NULL,** socket **\_ ERROR** viene restituito come risultato di questo IOCTL e [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) restituisce [WSAEFAULT](windows-sockets-error-codes-2.md).

**SIO \_ BSP \_ HANDLE \_ POLL** è definito nel file di intestazione *Mswsock.h* ed è supportato in Windows Vista e versioni successive.

### <a name="sio_chk_qos-opcode-setting-i-o-t3"></a>SIO \_ CHK \_ QOS (impostazione del codice operativo: I, O, T==3)

Recupera informazioni sulle caratteristiche del traffico QoS. Durante la fase di transizione nel sistema di invio tra la configurazione del flusso e la ricezione di un messaggio RESV (vedere How [the RSVP Service Invokes TC](/previous-versions/windows/desktop/qos/how-the-rsvp-service-invokes-tc) (Come il servizio RSVP richiama TC per altre informazioni sulla fase di transizione), il traffico associato a un flusso RSVP viene modellato in base al tipo di servizio[(BEST EFFORT,](/previous-versions/windows/desktop/qos/best-effort) [CONTROLLED LOAD](/previous-versions/windows/desktop/qos/controlled-load)o [GUARANTEED).](/previous-versions/windows/desktop/qos/guaranteed) Per altre informazioni, vedere Using SIO CHK QOS (Uso di [SIO \_ CHK \_ QOS)](/previous-versions/windows/desktop/qos/using-sio-chk-qos) nella [sezione Quality of Service](/previous-versions/windows/desktop/qos/qos-start-page) (Qualità del servizio) di Platform SDK.

### <a name="sio_cpu_affinity-opcode-setting-i-t3"></a>SIO_CPU_AFFINITY (impostazione del codice operativo: I, T==3)

Abilita la parallelizzazione delle indicazioni di ricezione e condivisione delle porte. Quando l'applicazione usa questa opzione socket per associare i socket a processori diversi e quindi associa i socket allo stesso indirizzo, le indicazioni di ricezione verranno distribuite tra i socket in base all'hash RSS (Receive Side Scaling). Le impostazioni RSS non cambiano, quindi qualsiasi flusso (endpoint locale, coppia di endpoint remoti) verrà sempre indicato nello stesso processore. Di conseguenza, tutti i pacchetti appartenenti a un determinato flusso verranno indicati allo stesso socket. Questo ioCTL deve essere chiamato prima dell'associazione. In caso contrario, verrà restituito WSAEINVAL. Il buffer di input è un indice del processore (in base 0) di tipo USHORT. IOCTL non è compatibile con SO_REUSEADDR e SO_REUSE_MULTICASTPORT. Supportato solo per i socket UDP.

> [!NOTE]
> Se si usa la versione 10.0.19041.0 (Windows 10, versione 2004) del Windows SDK, usare il valore anziché il nome `0x98000015` **SIO_CPU_AFFINITY**.

### <a name="sio_enable_circular_queueing-opcode-setting-v-t1"></a>SIO \_ ENABLE \_ CIRCULAR \_ QUEUEING (impostazione del codice operativo: V, T==1)

Indica al provider di servizi orientato ai messaggi sottostante che un messaggio appena arrivato non deve mai essere eliminato a causa di un overflow della coda del buffer. Al contrario, il messaggio meno recente nella coda deve essere eliminato per contenere il messaggio appena arrivato. Non sono necessari buffer di input e output. Si noti che questo IOCTL è valido solo per i socket associati a protocolli inaffidabili orientati ai messaggi. Il [codice di errore WSAENOPROTOOPT](windows-sockets-error-codes-2.md) è indicato per i provider di servizi che non supportano questo IOCTL.

### <a name="sio_find_route-opcode-setting-o-t1"></a>SIO \_ FIND \_ ROUTE (impostazione del codice operativo: O, T==1)

Quando viene emesso, questo IOCTL richiede che la route all'indirizzo remoto specificato come [**sockaddr**](sockaddr-2.md) nel buffer di input sia individuata. Se l'indirizzo esiste già nella cache locale, la relativa voce viene invalidata. Nel caso di IPX di Novell, questa chiamata avvia un oggetto IPX GetLocalTarget (GLT), che esegue una query sulla rete per l'indirizzo remoto specificato.

### <a name="sio_flush-opcode-setting-v-t1"></a>SIO \_ FLUSH (impostazione del codice operativo: V, T==1)

Rimuove il contenuto corrente della coda di invio associata a questo socket. Non sono necessari buffer di input e output. Il [codice di errore WSAENOPROTOOPT](windows-sockets-error-codes-2.md) è indicato per i provider di servizi che non supportano questo IOCTL.

### <a name="sio_get_broadcast_address-opcode-setting-o-t1"></a>SIO \_ GET BROADCAST ADDRESS \_ \_ (impostazione del codice operativo: O, T==1)

Questo IOCTL riempie il buffer di output con una struttura [sockaddr](sockaddr-2.md) contenente un indirizzo broadcast adatto per l'uso con [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) /  [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto). Questo IOCTL non è supportato per i socket IPv6 e restituisce il codice di errore [WSAENOPROTOOPT.](windows-sockets-error-codes-2.md)

### <a name="sio_get_extension_function_pointer-opcode-setting-o-i-t1"></a>SIO \_ GET EXTENSION FUNCTION POINTER \_ \_ \_ (impostazione del codice operativo: O, I, T===1)

Recuperare un puntatore alla funzione di estensione specificata supportata dal provider di servizi associato. Il buffer di input contiene un identificatore univoco globale (**GUID**) il cui valore identifica la funzione di estensione in questione. Il puntatore alla funzione desiderata viene restituito nel buffer di output. Gli identificatori di funzione di estensione vengono stabiliti dai fornitori di provider di servizi e devono essere inclusi nella documentazione del fornitore che descrive le funzionalità e la semantica delle funzioni di estensione.

I valori GUID per le funzioni di estensione supportate dal provider di servizi TCP/IP di Windows sono definiti nel file di intestazione *Mswsock.h.* Il valore possibile per questi GUID è il seguente:

| Termine                                                                                                                | Descrizione                                                                               |
|-|-|
| <span id="WSAID_ACCEPTEX"></span><span id="wsaid_acceptex"></span>WSAID \_ ACCEPTEX<br/>                                     | Funzione [**di estensione AcceptEx.**](/windows/win32/api/mswsock/nf-mswsock-acceptex)<br/>                         |
| <span id="WSAID_CONNECTEX"></span><span id="wsaid_connectex"></span>WSAID \_ CONNECTEX<br/>                                  | Funzione [**di estensione ConnectEx.**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex) <br/>                      |
| <span id="WSAID_DISCONNECTEX"></span><span id="wsaid_disconnectex"></span>WSAID \_ DISCONNECTEX<br/>                         | Funzione [**di estensione DisconnectEx.**](/previous-versions/windows/desktop/legacy/ms737757(v=vs.85)) <br/>                |
| <span id="WSAID_GETACCEPTEXSOCKADDRS"></span><span id="wsaid_getacceptexsockaddrs"></span>WSAID \_ GETACCEPTEXSOCKADDRS<br/> | Funzione [**di estensione GetAcceptExSockaddrs.**](/windows/win32/api/mswsock/nf-mswsock-getacceptexsockaddrs)<br/> |
| <span id="WSAID_TRANSMITFILE"></span><span id="wsaid_transmitfile"></span>FILE DI TRASMISSIONE WSAID \_<br/>                         | Funzione [**di estensione TransmitFile.**](/windows/win32/api/mswsock/nf-mswsock-transmitfile)<br/>                 |
| <span id="WSAID_TRANSMITPACKETS"></span><span id="wsaid_transmitpackets"></span>TRASMETTITORI WSAID \_<br/>                | Funzione [**di estensione TransmitPackets.**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_transmitpackets) <br/>          |
| <span id="WSAID_WSARECVMSG"></span><span id="wsaid_wsarecvmsg"></span>WSAID \_ WSARECVMSG<br/>                               | Funzione [**di estensione LPFN_WSARECVMSG (WSARecvMsg).**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)<br/>                     |
| <span id="WSAID_WSASENDMSG"></span><span id="wsaid_wsasendmsg"></span>WSAID \_ WSASENDMSG<br/>                               | Funzione [**di estensione WSASendMsg.**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) <br/>                      |

### <a name="sio_get_group_qos-opcode-setting-o-i-t1"></a>SIO \_ GET \_ GROUP \_ QOS (impostazione del codice operativo: O, I, T==1)

Riservato per un uso futuro con i socket.

Recuperare la [**struttura QOS**](/windows/win32/api/winsock2/ns-winsock2-qos) associata al gruppo di socket a cui appartiene questo socket. Il buffer di input è facoltativo. Alcuni protocolli, ad esempio RSVP, consentono l'uso del buffer di input per qualificare una richiesta di qualità del servizio. La **struttura QOS** verrà copiata nel buffer di output. Se questo socket non appartiene a un gruppo di socket appropriato, i membri **SendingFlowspec** e **ReceivingFlowspec** della struttura **QOS** restituita vengono impostati su **NULL.** Il [codice di errore WSAENOPROTOOPT](windows-sockets-error-codes-2.md) è indicato per i provider di servizi che non supportano la qualità del servizio.

### <a name="sio_get_interface_list-opcode-setting-o-t0"></a>SIO \_ GET INTERFACE LIST \_ \_ (impostazione del codice operativo: O, T==0)

Restituisce un elenco di interfacce IP configurate e dei relativi parametri come matrice di [**strutture INTERFACE \_ INFO.**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-interface_info)

> [!Note]  
> Il supporto di questo comando è obbligatorio per i provider di servizi TCP/IP conformi a Windows Sockets 2.

Il *parametro lpvOutBuffer* punta al buffer in cui archiviare le informazioni sulle interfacce come matrice di strutture [**INTERFACE \_ INFO**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-interface_info) per gli indirizzi IP unicast nelle interfacce. Il *parametro cbOutBuffer* specifica la lunghezza del buffer di output. Il numero di interfacce restituite (numero di strutture restituite nel buffer a cui punta il parametro *lpvOutBuffer)* può essere determinato in base alla lunghezza effettiva del buffer di output restituito nel parametro *lpcbBytesReturned.*

Se la [**funzione WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) viene chiamata con **SIO \_ GET INTERFACE \_ \_ LIST** e il membro di livello del parametro *s* del socket non è definito come **IPPROTO \_ IP,** viene restituito **WSAEINVAL.** Una chiamata alla funzione **WSAIoctl** con **SIO \_ GET INTERFACE \_ \_ LIST** restituisce **WSAEFAULT** se il parametro *cbOutBuffer* che specifica la lunghezza del buffer di output è troppo piccolo e riceve l'elenco di interfacce configurate.

**SIO \_ GET \_ INTERFACE \_ LIST** è supportato in Windows Me/98 e Windows NT 4.0 con SP4 e versioni successive.

### <a name="sio_get_interface_list_ex-opcode-setting-o-t0"></a>SIO \_ GET INTERFACE LIST EX \_ \_ \_ (impostazione del codice operativo: O, T==0)

Riservato per un uso futuro con i socket.

Restituisce un elenco di interfacce IP configurate e dei relativi parametri come matrice di [**strutture INTERFACE \_ INFO \_ EX.**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-interface_info_ex)

Il *parametro lpvOutBuffer* punta al buffer in cui archiviare le informazioni sulle interfacce come matrice di [**strutture INTERFACE INFO \_ \_ EX**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-interface_info_ex) per gli indirizzi IP unicast nell'interfaccia. Il *parametro cbOutBuffer* specifica la lunghezza del buffer di output. Il numero di interfacce restituite (numero di strutture restituite in *lpvOutBuffer*) può essere determinato in base alla lunghezza effettiva del buffer di output restituito nel *parametro lpcbBytesReturned.*

**SIO \_ GET \_ INTERFACE \_ LIST \_ EX** non è attualmente supportato in Windows.

### <a name="sio_get_qos-opcode-setting-o-t1"></a>SIO \_ GET \_ QOS (impostazione del codice operativo: O, T==1)

Riservato per un uso futuro con i socket. Recuperare la [**struttura QOS**](/windows/win32/api/winsock2/ns-winsock2-qos) associata al socket. Il buffer di input è facoltativo. Alcuni protocolli (ad esempio, RSVP) consentono l'uso del buffer di input per qualificare una richiesta di qualità del servizio. La **struttura QOS** verrà copiata nel buffer di output. Le dimensioni del buffer di output devono essere sufficientemente grandi da poter contenere la struttura **QOS** completa. Il [codice di errore WSAENOPROTOOPT](windows-sockets-error-codes-2.md) è indicato per i provider di servizi che non supportano la qualità del servizio.

Un mittente non può chiamare **SIO \_ GET \_ QOS** fino a quando il socket non è connesso.

Un ricevitore può chiamare **SIO \_ GET \_ QOS** non appena è associato.

### <a name="sio_get_tx_timestamp"></a>SIO_GET_TX_TIMESTAMP

IoCTL socket usato per ottenere i timestamp per i pacchetti trasmessi (TX). Valido solo per i socket di datagramma.

Il **SIO_GET_TX_TIMESTAMP** del controllo di trasmissione rimuove un timestamp di trasmissione dalla coda di timestamp di trasmissione di un socket. Abilitare prima la ricezione di timestamp usando il [**SIO_TIMESTAMPING**](#sio_timestamping) IOCTL del socket. Recuperare quindi i timestamp tx in base all'ID chiamando la [**funzione WSAIoctl**](/windows/win32/api/winsock2/nf-winsock2-wsaioctl) (o [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85))) con i parametri seguenti.

Per **SIO_GET_TX_TIMESTAMP**, l'input è un ID timestamp **UINT32** e l'output è un valore di timestamp **UINT64.** In caso di esito positivo, il timestamp tx è disponibile e viene restituito . Se non sono disponibili timestamp di trasmissione, [**WSAGetLastError**](/windows/win32/api/winsock/nf-winsock-wsagetlasterror) restituisce **WSAEWOULDBLOCK**.

> [!NOTE]
> I timestamp TX non sono supportati quando si esegue un invio coalesced **tramite UDP_SEND_MSG_SIZE**.

Vedere anche [Timestamping di Winsock.](/windows/win32/winsock/winsock-timestamping)

### <a name="sio_ideal_send_backlog_change-opcode-setting-v-t0"></a>SIO \_ IDEAL \_ SEND \_ BACKLOG CHANGE \_ (impostazione del codice operativo: V, T==0)

Notifica a un'applicazione quando il valore del backlog di invio ideale (ISB) cambia per la connessione sottostante.

Quando si inviano dati tramite una connessione TCP tramite Windows sockets, è importante mantenere una quantità sufficiente di dati in sospeso (inviati ma non ancora riconosciuti) in TCP per ottenere la velocità effettiva massima. Il valore ideale per la quantità di dati in sospeso per ottenere la velocità effettiva migliore per la connessione TCP è detto dimensione ideale del backlog di invio (ISB). Il valore ISB è una funzione del prodotto con ritardo della larghezza di banda della connessione TCP e della finestra di ricezione annunciata del ricevitore (e in parte della congestione nella rete).

Il valore ISB per ogni connessione è disponibile dall'implementazione del protocollo TCP in Windows Server 2008, Windows Vista con SP1 e versioni successive del sistema operativo. **SIO \_ IDEAL SEND \_ \_ BACKLOG \_ CHANGE** IOCTL può essere usato da un'applicazione per ricevere una notifica quando il valore ISB cambia in modo dinamico per una connessione.

Per informazioni più dettagliate, vedere le informazioni di [**riferimento su SIO \_ IDEAL SEND \_ \_ BACKLOG \_ CHANGE.**](/previous-versions/windows/desktop/legacy/bb736548(v=vs.85))

[**SIO \_ IDEAL \_ SEND \_ BACKLOG \_ CHANGE**](/previous-versions/windows/desktop/legacy/bb736548(v=vs.85)) è supportato in Windows Server 2008, Windows Vista con SP1 e versioni successive del sistema operativo.

### <a name="sio_ideal_send_backlog_query-opcode-setting-o-t0"></a>SIO \_ IDEAL \_ SEND \_ BACKLOG QUERY \_ (impostazione del codice operativo: O, T==0)

Recupera il valore isb (Ideal Send Backlog) per la connessione sottostante.

Quando si inviano dati tramite una connessione TCP usando Windows sockets, è importante mantenere una quantità sufficiente di dati in sospeso (inviati ma non ancora riconosciuti) in TCP per ottenere la velocità effettiva più elevata. Il valore ideale per la quantità di dati in sospeso per ottenere la velocità effettiva migliore per la connessione TCP è detto dimensione isb (Ideal Send Backlog). Il valore ISB è una funzione del prodotto con ritardo della larghezza di banda della connessione TCP e della finestra di ricezione annunciata del ricevitore (e in parte della quantità di congestione nella rete).

Il valore ISB per ogni connessione è disponibile dall'implementazione del protocollo TCP in Windows Server 2008 e versioni successive. **SIO \_ IDEAL \_ SEND \_ BACKLOG \_ QUERY** IOCTL può essere usato da un'applicazione per eseguire query sul valore ISB per una connessione.

Per informazioni più dettagliate, vedere le informazioni di [**riferimento su SIO \_ IDEAL SEND \_ \_ BACKLOG \_ QUERY.**](/previous-versions/windows/desktop/legacy/bb736549(v=vs.85))

[**SIO \_ IDEAL \_ SEND \_ BACKLOG \_ QUERY**](/previous-versions/windows/desktop/legacy/bb736549(v=vs.85)) è supportato in Windows Server 2008, Windows Vista con SP1 e versioni successive del sistema operativo.

### <a name="sio_keepalive_vals-opcode-setting-i-t3"></a>SIO \_ KEEPALIVE \_ VALS (impostazione del codice operativo: I, T==3)

Abilita o disabilita l'impostazione per connessione dell'opzione **keep-alive** TCP che specifica il timeout e l'intervallo keep-alive TCP. Per altre informazioni sull'opzione keep-alive, vedere la sezione 4.2.3.6 in Requisiti per gli host *Internet -* Livelli di comunicazione specificati in RFC 1122 disponibile nel sito Web [IETF](https://www.ietf.org/rfc/rfc1122.txt). Questa risorsa può essere disponibile solo in inglese.

**SIO \_ KEEPALIVE \_ VALS può essere** usato per abilitare o disabilitare i probe keep-alive e impostare il timeout e l'intervallo keep-alive. Il timeout keep-alive specifica il timeout, in millisecondi, senza attività fino all'invio del primo pacchetto keep-alive. L'intervallo keep-alive specifica l'intervallo, in millisecondi, tra l'invio di pacchetti keep-alive successivi se non viene ricevuto alcun acknowledgement.

L'opzione [**SO \_ KEEPALIVE,**](so-keepalive.md) che è una delle opzioni socket [SOCKET SOL, \_](sol-socket-socket-options.md)può essere usata anche per abilitare o disabilitare il keep-alive TCP in una connessione, nonché per eseguire query sullo stato corrente di questa opzione. Per verificare se il keep-alive TCP è abilitato in un socket, è possibile chiamare la funzione [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) con **l'opzione SO \_ KEEPALIVE.** Per abilitare o disabilitare il keep-alive TCP, è possibile chiamare la funzione [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) con [**l'opzione SO \_ KEEPALIVE.**](so-keepalive.md) Se il keep-alive TCP è abilitato con **SO \_ KEEPALIVE,** le impostazioni TCP predefinite vengono usate per il timeout e l'intervallo keep-alive, a meno che questi valori non siano stati modificati usando **SIO \_ KEEPALIVE \_ VALS.**

Per informazioni più dettagliate, vedere le informazioni [**di riferimento su SIO \_ KEEPALIVE \_ VALS.**](/previous-versions/windows/desktop/legacy/dd877220(v=vs.85)) **SIO \_ KEEPALIVE \_ VALS** è supportato in Windows 2000 e versioni successive.

### <a name="sio_loopback_fast_path-opcode-setting-i-t3"></a>SIO \_ LOOPBACK \_ FAST PATH \_ (impostazione del codice operativo: I, T==3)

Configura un socket TCP per una latenza inferiore e operazioni più veloci sull'interfaccia di loopback. Questo ioCTL richiede che lo stack TCP/IP usi un percorso rapido speciale per le operazioni di loopback su questo socket. [**L'IOCTL \_ SIO LOOPBACK \_ FAST \_ PATH**](/previous-versions/windows/desktop/legacy/jj841212(v=vs.85)) può essere usato solo con socket TCP. Questo IOCTL deve essere usato su entrambi i lati della sessione di loopback. Il percorso rapido di loopback TCP è supportato tramite l'interfaccia di loopback IPv4 o IPv6. Per impostazione predefinita, **SIO \_ LOOPBACK \_ FAST PATH \_ è** disabilitato.

Per informazioni più dettagliate, vedere le informazioni [**di riferimento su SIO \_ LOOPBACK FAST \_ \_ PATH.**](/previous-versions/windows/desktop/legacy/jj841212(v=vs.85)) **SIO \_ LOOPBACK \_ FAST \_ PATH** è supportato in Windows 8, Windows Server 2012 e versioni successive.

### <a name="sio_multipoint_loopback-opcode-setting-v-t1"></a>SIO \_ MULTIPOINT \_ LOOPBACK (impostazione del codice operativo: V, T==1)

Controlla se i dati inviati da un'applicazione nel computer locale (non necessariamente dallo stesso socket) in una sessione multicast verranno ricevuti da un socket aggiunto al gruppo di destinazione multicast nell'interfaccia di loopback. Il valore **TRUE** fa sì che i dati multicast inviati da un'applicazione nel computer locale siano recapitati a un socket di ascolto nell'interfaccia di loopback. Il valore **FALSE impedisce** che i dati multicast inviati da un'applicazione nel computer locale vengano recapitati a un socket di ascolto nell'interfaccia di loopback. Per impostazione predefinita, **SIO \_ MULTIPOINT \_ LOOPBACK** è abilitato.

### <a name="sio_multicast_scope-opcode-setting-i-t1"></a>SIO \_ MULTICAST \_ SCOPE (impostazione del codice operativo: I, T==1)

Specifica l'ambito su cui verranno eseguite le trasmissioni multicast. L'ambito è definito come numero di segmenti di rete indirizzati da coprire. Un ambito pari a zero indica che la trasmissione multicast non verrebbe posizionata in transito, ma potrebbe essere diffusa tra socket all'interno dell'host locale. Un valore di ambito pari a uno (impostazione predefinita) indica che la trasmissione verrà posizionata in transito, ma non attraverserà alcun router. I valori di ambito più elevati determinano il numero di router che è possibile attraversare. Si noti che corrisponde al parametro time-to-live (TTL) nel multicast IP. Per impostazione predefinita, l'ambito è 1.

### <a name="sio_query_rss_processor_info-opcode-setting-o-t1"></a>SIO \_ QUERY RSS PROCESSOR INFO \_ \_ \_ (impostazione del codice operativo: O, T==1)

Esegue una query sull'associazione tra un socket e un core del processore RSS e un nodo NUMA.

[**L'ELEMENTO SIO \_ QUERY \_ RSS PROCESSOR \_ \_ INFO**](/previous-versions/windows/desktop/legacy/jj553482(v=vs.85)) IOCTL restituisce una struttura DI AFFINITÀ PROCESSORE SOCKET contenente il NUMERO PROCESSORE e l'ID nodo NUMA. [**\_ \_**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) [**\_**](/windows/win32/api/winnt/ns-winnt-processor_number) La struttura **PROCESSOR \_ NUMBER** restituita contiene un numero di gruppo e un numero di processore relativo all'interno del gruppo.

Per informazioni più dettagliate, vedere informazioni di riferimento [**su SIO \_ QUERY RSS \_ PROCESSOR \_ \_ INFO.**](/previous-versions/windows/desktop/legacy/jj553482(v=vs.85)) **SIO \_ QUERY \_ RSS \_ PROCESSOR \_ INFO** è supportato in Windows 8, Windows Server 2012 e versioni successive.

### <a name="sio_query_rss_scalability_info-opcode-setting-o-t3"></a>SIO \_ QUERY \_ RSS \_ SCALABILITY INFO \_ (impostazione del codice operativo: O, T==3)

Esegue l'offload delle interfacce per la funzionalità receive-side scaling (RSS). La struttura dell'argomento restituita per **SIO \_ QUERY RSS \_ \_ SCALABILITY \_ INFO** è specificata nella struttura **RSS \_ SCALABILITY \_ INFO** definita nel file di intestazione *Mstcpip.h.* Questa struttura è definita come segue:

```cpp
// Scalability info for the transport
typedef struct _RSS_SCALABILITY_INFO {
   BOOLEAN RssEnabled;
} RSS_SCALABILITY_INFO, *PRSS_SCALABILITY_INFO;
```

Il valore restituito nel **membro RssEnabled** indica se RSS è abilitato in almeno un'interfaccia.

Se le dimensioni del buffer di output non sono sufficienti per la struttura **RSS \_ SCALABILITY \_ INFO** *(cbOutBuffer* è minore delle dimensioni di **RSS \_ SCALABILITY \_ INFO)** o *il parametro lpvOutBuffer* è un **puntatore NULL,** viene restituito **SOCKET \_ ERROR** come risultato di questo IOCTL e [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) restituisce [WSAEINVAL](windows-sockets-error-codes-2.md).

Nelle reti ad alta velocità in cui più CPU risiedono all'interno di un singolo sistema, la capacità dello stack di protocolli di rete di scalare bene in un sistema con più CPU non è più adatta perché l'architettura di NDIS 5.1 e versioni precedenti limita l'elaborazione del protocollo a una singola CPU. Receive-Side Scaling (RSS) risolve questo problema consentendo il bilanciamento del carico di rete da una scheda di rete tra più CPU.

**SIO \_ QUERY \_ RSS \_ SCALABILITY \_ INFO** è supportato in Windows Vista e versioni successive.

### <a name="sio_query_transport_setting-opcode-setting-i-t3"></a>SIO \_ QUERY TRANSPORT SETTING \_ \_ (impostazione del codice operativo: I, T==3)

Esegue una query sulle impostazioni di trasporto su un socket. L'impostazione di trasporto su cui viene eseguita la query si basa [**\_ \_ sull'ID TRANSPORT SETTING**](/windows/win32/api/transportsettingcommon/ns-transportsettingcommon-transport_setting_id) passato nel parametro *lpvInBuffer.*

L'unica impostazione di trasporto attualmente definita è per la funzionalità DI NOTIFICA **\_ \_ \_ IN** TEMPO REALE in un socket TCP.

Se [**\_ l'ID \_**](/windows/win32/api/transportsettingcommon/ns-transportsettingcommon-transport_setting_id) IMPOSTAZIONE TRASPORTO ha il **membro GUID** impostato su REAL TIME **NOTIFICATION \_ \_ \_ CAPABILITY,** si tratta di una richiesta per eseguire una query delle impostazioni di notifica in tempo reale per il socket TCP usato con [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) per ricevere notifiche di rete in background in un'app di Windows Store. Se la [**chiamata WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) o [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) ha esito positivo, questo IOCTL restituisce una struttura [**OUTPUT DI \_ \_ IMPOSTAZIONE \_ \_**](/windows/desktop/api/Mstcpip/ns-mstcpip-real_time_notification_setting_input) DELLE NOTIFICHE IN TEMPO REALE con lo stato corrente.

Per informazioni più dettagliate, vedere le informazioni di [**riferimento su SIO \_ QUERY TRANSPORT \_ \_ SETTING.**](/previous-versions/windows/desktop/legacy/jj553483(v=vs.85)) **SIO \_ QUERY \_ TRANSPORT \_ SETTING** è supportato in Windows 8, Windows Server 2012 e versioni successive.

### <a name="sio_query_wfp_ale_endpoint_handle-opcode-setting-o-t3"></a>\_SIO QUERY \_ WFP \_ ALE \_ ENDPOINT HANDLE \_ (impostazione del codice operativo: O, T===3)

Esegue una query sull'handle dell'endpoint application layer enforcement (ALE).

Windows Filtering Platform (WFP) supporta l'ispezione e la modifica del traffico di rete. In Windows Vista, WFP si concentra sugli scenari in cui il computer host è l'endpoint di comunicazione. In Windows Server 2008, tuttavia, esistono implementazioni del firewall perimetrale che desiderano sfruttare la piattaforma WFP per ispezionare e proxy il traffico pass-through. Il server ISA (Internet Security and Acceleration) è un esempio di dispositivo perimetrale di questo tipo.

Esistono alcuni scenari firewall che possono richiedere la possibilità di inserire un pacchetto in ingresso nel percorso di invio associato a un endpoint esistente. Deve essere presente un meccanismo per individuare l'handle dell'endpoint del livello di trasporto associato all'endpoint di destinazione. L'applicazione che ha creato l'endpoint è proprietaria di questi endpoint del livello di trasporto. Questo ioCTL viene usato per fornire l'handle del socket al mapping dell'handle dell'endpoint del livello di trasporto.

Se le dimensioni del buffer di output non sono sufficienti per l'handle dell'endpoint *(cbOutBuffer* è inferiore alla dimensione di **un UINT64)** o se il *parametro lpvOutBuffer* è **un puntatore NULL,** socket **\_ ERROR** viene restituito come risultato di questo IOCTL e [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) restituisce [WSAEINVAL.](windows-sockets-error-codes-2.md)

**SIO \_ QUERY \_ WFP \_ ALE ENDPOINT \_ \_ HANDLE** è supportato in Windows Vista e versioni successive.

### <a name="sio_query_wfp_connection_redirect_context-opcode-setting-i-t3"></a>SIO QUERY WFP CONNECTION REDIRECT CONTEXT (contesto di reindirizzamento della connessione SIO \_ \_ PAM) \_ \_ \_ (impostazione del codice operativo: I, T==3)

Esegue una query sul contesto di reindirizzamento per un record di reindirizzamento usato da un servizio di reindirizzamento windows filtering platform (WFP).

SIO [**QUERY WFP CONNECTION REDIRECT \_ \_ \_ \_ \_ CONTEXT**](/previous-versions/windows/desktop/legacy/hh859712(v=vs.85)) IOCTL viene usato per fornire il rilevamento delle connessioni proxy sulle connessioni socket reindirizzate. Questa funzionalità WFP facilita il rilevamento dei record di reindirizzamento dal reindirizzamento iniziale di una connessione alla connessione finale alla destinazione.

Per informazioni più dettagliate, vedere informazioni di riferimento [**sul CONTESTO DI REINDIRIZZAMENTO DELLA CONNESSIONE SIO \_ QUERY \_ WFP. \_ \_ \_**](/previous-versions/windows/desktop/legacy/hh859712(v=vs.85)) **SIO \_ QUERY \_ WFP CONNECTION REDIRECT \_ \_ \_ CONTEXT** è supportato in Windows 8, Windows Server 2012 e versioni successive.

### <a name="sio_query_wfp_connection_redirect_records-opcode-setting-i-t3"></a>SIO \_ QUERY \_ WFP \_ CONNECTION \_ REDIRECT \_ RECORDS (opcode setting: I, T==3)

Esegue una query sul record di reindirizzamento per la connessione TCP/IP accettata per l'uso da parte di un servizio di reindirizzamento windows filtering platform (WFP).

SIO [**QUERY WFP CONNECTION REDIRECT \_ \_ \_ \_ \_ RECORDS**](/previous-versions/windows/desktop/legacy/hh859713(v=vs.85)) IOCTL viene usato per fornire il rilevamento delle connessioni proxy sulle connessioni socket reindirizzate. Questa funzionalità WFP facilita il rilevamento dei record di reindirizzamento dal reindirizzamento iniziale di una connessione alla connessione finale alla destinazione.

Per informazioni più dettagliate, vedere le informazioni di riferimento sui RECORD DI REINDIRIZZAMENTO DELLE CONNESSIONI [**\_ SIO QUERY \_ WFP. \_ \_ \_**](/previous-versions/windows/desktop/legacy/hh859713(v=vs.85)) **SIO \_ QUERY \_ WFP CONNECTION REDIRECT \_ \_ \_ RECORDS** è supportato in Windows 8, Windows Server 2012 e versioni successive.

### <a name="sio_rcvall-opcode-setting-i-t3"></a>SIO \_ RCVALL (impostazione del codice operativo: I, T==3)

Consente a un socket di ricevere tutti i pacchetti IPv4 o IPv6 che passano attraverso un'interfaccia di rete. L'handle socket passato alla [**funzione WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) deve essere uno dei seguenti:

-   Un socket IPv4 creato con la famiglia di indirizzi impostata su AF INET, il tipo di socket impostato su SOCK RAW e il protocollo impostato \_ \_ su IPPROTO \_ IP.
-   Un socket IPv6 creato con la famiglia di indirizzi impostata su AF INET6, il tipo di socket impostato su SOCK RAW e il protocollo impostato \_ \_ su IPPROTO \_ IPV6.

Il socket deve anche essere associato a un'interfaccia IPv4 o IPv6 locale esplicita, il che significa che non è possibile eseguire l'associazione a **INADDR \_ ANY** o **in6addr \_ any**.

In Windows Server 2008 e versioni precedenti, l'impostazione [**SIO \_ RCVALL**](/previous-versions/windows/desktop/legacy/ee309610(v=vs.85)) IOCTL non acquisisce i pacchetti locali inviati da un'interfaccia di rete. Sono inclusi i pacchetti ricevuti in un'altra interfaccia e inoltrati all'interfaccia di rete specificata per **SIO \_ RCVALL** IOCTL.

In Windows 7 e Windows Server 2008 R2 questa operazione è stata modificata in modo da acquisire anche i pacchetti locali inviati da un'interfaccia di rete. Sono inclusi i pacchetti ricevuti in un'altra interfaccia e quindi inoltrati all'interfaccia di rete associata al socket con [**SIO \_ RCVALL**](/previous-versions/windows/desktop/legacy/ee309610(v=vs.85)) IOCTL.

L'impostazione di questo IOCTL richiede privilegi di amministratore nel computer locale.

Questa funzionalità viene talvolta definita modalità promiscua.

I valori possibili per l'opzione **SIO \_ RCVALL** IOCTL sono specificati nell'enumerazione **RCVALL \_ VALUE** definita nel file di intestazione *Mstcpip.h.* I valori possibili per SIO \_ RCVALL sono i seguenti:

| Termine                                                                                                                 | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-|-|
| <span id="RCVALL_OFF"></span><span id="rcvall_off"></span>RCVALL \_ OFF<br/>                                     | Disabilitare questa opzione in modo che un socket non riceva tutti i pacchetti IPv4 o IPv6 nella rete. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="RCVALL_ON"></span><span id="rcvall_on"></span>RC RPC \_ ON<br/>                                        | Abilitare questa opzione in modo che un socket riceva tutti i pacchetti IPv4 o IPv6 nella rete. Questa opzione abilita la modalità promiscua nella scheda di interfaccia di rete (NIC), se la scheda di interfaccia di rete supporta la modalità promiscua. In un segmento LAN con un hub di rete, una scheda di interfaccia di rete che supporta la modalità promiscua acquisisce tutto il traffico IPv4 o IPv6 sulla LAN, incluso il traffico tra altri computer nello stesso segmento LAN. Tutti i pacchetti acquisiti (IPv4 o IPv6, a seconda del socket) verranno recapitati al socket non elaborato. <br/> Questa opzione non acquisisce altri pacchetti (ad esempio pacchetti ARP, IPX e NetBEUI) nell'interfaccia.<br/> Netmon usa la stessa modalità per l'interfaccia di rete, ma non usa questa opzione per acquisire il traffico.<br/> |
| <span id="RCVALL_SOCKETLEVELONLY"></span><span id="rcvall_socketlevelonly"></span>RC \_ SOCKETLEVELONLY<br/> | Questa funzionalità non è attualmente implementata, quindi l'impostazione di questa opzione non ha alcun effetto.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="RCVALL_IPLEVEL"></span><span id="rcvall_iplevel"></span>RCLEVEL \_ IPLEVEL<br/>                         | Abilitare questa opzione in modo che un socket IPv4 o IPv6 riceva tutti i pacchetti a livello ip nella rete. Questa opzione non abilita la modalità promiscua nella scheda di interfaccia di rete. Questa opzione influisce solo sull'elaborazione dei pacchetti a livello di IP. La scheda di interfaccia di rete riceve comunque solo i pacchetti indirizzati agli indirizzi unicast e multicast configurati. Tuttavia, un socket con questa opzione abilitata riceverà non solo i pacchetti indirizzati a indirizzi IP specifici, ma riceverà tutti i pacchetti IPv4 o IPv6 ricevuti dalla scheda di interfaccia di rete.<br/> Questa opzione non acquisisce altri pacchetti (ad esempio ARP, IPX e NetBEUI) ricevuti sull'interfaccia.<br/>                                                                                             |



 

Per informazioni più dettagliate, vedere le informazioni [**di riferimento su SIO \_ RCACCI.**](/previous-versions/windows/desktop/legacy/ee309610(v=vs.85))

**SIO \_ RC RPC** è supportato in Windows 2000 e versioni successive.

### <a name="sio_rcvall_igmpmcast-opcode-setting-i-t3"></a>SIO \_ RCGM \_ IGMPMCAST (impostazione del codice operativo: I, T==3)

Consente a un socket di ricevere tutto il traffico IP multicast IGMP sulla rete, senza ricevere altro traffico IP multicast. L'handle socket passato alla [**funzione WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) deve essere della famiglia di indirizzi AF INET, del tipo di socket SOCK RAW e del protocollo \_ \_ \_ IPPROTO IGMP. Il socket deve anche essere associato a un'interfaccia locale esplicita, il che significa che non è possibile eseguire l'associazione a INADDR \_ ANY.

Dopo che il socket è stato associato e il set IOCTL, le chiamate alle funzioni [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) o [**recv recv**](/windows/desktop/api/winsock/nf-winsock-recv) restituiscono datagrammi IP multicast che passano attraverso l'interfaccia specificata. Si noti che è necessario fornire un buffer sufficientemente grande. L'impostazione di questo IOCTL richiede privilegi di amministratore nel computer locale.

**SIO \_ RCVALL \_ IGMPMCAST** è supportato in Windows 2000 e versioni successive.

### <a name="sio_rcvall_mcast-opcode-setting-i-t3"></a>SIO \_ RCVALL \_ MCAST (impostazione del codice operativo: I, T==3)

Consente a un socket di ricevere tutto il traffico IP multicast sulla rete, ovvero tutti i pacchetti IP destinati agli indirizzi IP nell'intervallo da 224.0.0.0 a 239.255.255.255. L'handle socket passato alla [**funzione WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) deve essere della famiglia di indirizzi AF INET, del tipo di socket SOCK RAW e del protocollo \_ UDP \_ IPPROTO. \_ Il socket deve anche essere associato a un'interfaccia locale esplicita, il che significa che non è possibile eseguire l'associazione a INADDR \_ ANY. Il socket deve essere associato alla porta zero.

Dopo che il socket è stato associato e il set IOCTL, le chiamate alle funzioni [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) o [**recv recv**](/windows/desktop/api/winsock/nf-winsock-recv) restituiscono datagrammi IP multicast che passano attraverso l'interfaccia specificata. Si noti che è necessario fornire un buffer sufficientemente grande. L'impostazione di questo IOCTL richiede privilegi di amministratore nel computer locale.

**SIO \_ RCVALL \_ MCAST** è supportato in Windows 2000 e versioni successive.

### <a name="sio_release_port_reservation-opcode-setting-i-t3"></a>SIO \_ RELEASE PORT RESERVATION \_ \_ (impostazione del codice operativo: I, T==3)

Rilascia una prenotazione di runtime per un blocco di porte TCP o UDP. La prenotazione di runtime da rilasciare deve essere stata ottenuta dal processo di emissione usando [**SIO \_ ACQUIRE PORT \_ \_ RESERVATION**](/previous-versions/windows/desktop/legacy/gg699720(v=vs.85)) IOCTL.

Per informazioni più dettagliate, vedere le informazioni di [**riferimento su SIO \_ RELEASE PORT \_ \_ RESERVATION.**](/previous-versions/windows/desktop/legacy/gg699722(v=vs.85))

[**SIO \_ RELEASE \_ PORT \_ RESERVATION**](/previous-versions/windows/desktop/legacy/gg699722(v=vs.85)) è supportato in Windows Vista e versioni successive del sistema operativo.

### <a name="sio_routing_interface_change-opcode-setting-i-t1"></a>SIO \_ ROUTING INTERFACE CHANGE \_ \_ (impostazione del codice operativo: I, T==1)

Per ricevere la notifica di una modifica dell'interfaccia di routing che deve essere usata per raggiungere l'indirizzo remoto nel buffer di input (specificato come [**struttura sockaddr).**](sockaddr-2.md) Al termine di questo IOCTL non verranno fornite informazioni di output sulla nuova interfaccia di routing. il completamento indica semplicemente che l'interfaccia di routing per una determinata destinazione è stata modificata e deve essere eseguita una query usando **SIO \_ ROUTING INTERFACE \_ \_ QUERY** IOCTL.

Si presuppone, anche se non obbligatorio, che l'applicazione usi I/O sovrapposto per ricevere una notifica della modifica dell'interfaccia di routing tramite il completamento della richiesta **SIO \_ ROUTING INTERFACE \_ \_ CHANGE.** In alternativa, se l'INTERFACCIA DI **ROUTING SIO \_ \_ \_ CHANGE** IOCTL viene emessa in un socket non bloccante con i parametri *lpOverlapped* e *lpCompletionRoutine* impostati su **NULL**, verrà completata immediatamente la restituzione e [WSAEWOULDBLOCK](windows-sockets-error-codes-2.md) come errore e l'applicazione può quindi attendere il routing degli eventi di modifica tramite chiamata a [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) o [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) con bit FD ROUTING INTERFACE CHANGE impostato nella maschera di bit dell'evento di \_ \_ \_ rete.

È riconosciuto che le informazioni di routing rimangono stabili nella maggior parte dei casi in modo che la richiesta all'applicazione di mantenere più IOCL in sospeso per ottenere notifiche su tutte le destinazioni a cui è interessata, nonché che il provider di servizi tenga traccia di queste richieste di notifica userà una quantità significativa di risorse di sistema. Questa situazione può essere evitata estendendo il significato dei parametri di input e dilatando i requisiti del provider di servizi come indicato di seguito:

-   L'applicazione può specificare un indirizzo jolly specifico della famiglia di protocolli (uguale a quello usato nella chiamata [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) quando richiede di eseguire l'associazione a qualsiasi indirizzo disponibile) per richiedere notifiche di eventuali modifiche di routing. In questo modo l'applicazione può mantenere solo una MODIFICA dell'INTERFACCIA DI **\_ ROUTING \_ \_ SIO** in sospeso per tutti i socket e le destinazioni di cui dispone e quindi usare **SIO \_ ROUTING INTERFACE \_ \_ QUERY** per ottenere le informazioni di routing effettive.
-   Un provider di servizi può ignorare le informazioni specificate dall'applicazione nel buffer di input di **SIO \_ ROUTING INTERFACE \_ \_ CHANGE** (come se l'applicazione specifica un indirizzo jolly) e completare l'evento **SIO ROUTING INTERFACE \_ \_ \_ CHANGE** IOCTL o segnale FD ROUTING INTERFACE CHANGE in caso di modifica delle informazioni di routing (non solo la route alla destinazione specificata nel \_ buffer di \_ \_ input).

### <a name="sio_routing_interface_query-opcode-setting-i-o-t1"></a>SIO \_ ROUTING INTERFACE QUERY \_ \_ (impostazione del codice operativo: I, O, T===1)

Per ottenere l'indirizzo dell'interfaccia locale (rappresentata come struttura [**sockaddr)**](sockaddr-2.md) da usare per inviare all'indirizzo remoto specificato nel buffer di input (come **sockaddr**). Gli indirizzi multicast remoti possono essere inviati nel buffer di input per ottenere l'indirizzo dell'interfaccia preferita per la trasmissione multicast. In ogni caso, l'indirizzo dell'interfaccia restituito può essere usato dall'applicazione in una richiesta bind() successiva.

Si noti che le route sono soggette a modifiche. Pertanto, le applicazioni non possono basarsi sulle informazioni restituite da **SIO \_ ROUTING INTERFACE \_ \_ QUERY** per essere persistenti. Le applicazioni possono registrarsi per il routing delle notifiche di modifica tramite l'IOCTL **SIO \_ ROUTING INTERFACE \_ \_ CHANGE,** che fornisce la notifica tramite I/O sovrapposto o un evento FD \_ ROUTING INTERFACE \_ \_ CHANGE. La sequenza di azioni seguente può essere usata per garantire che l'applicazione abbia sempre informazioni sull'interfaccia di routing corrente per una determinata destinazione:

-   Problema **SIO \_ ROUTING INTERFACE \_ \_ CHANGE** IOCTL
-   Problema **SIO \_ ROUTING INTERFACE \_ \_ QUERY** IOCTL
-   Ogni volta che **SIO \_ ROUTING INTERFACE \_ \_ CHANGE** IOCTL notifica all'applicazione la modifica del routing (tramite I/O sovrapposto o segnalando l'evento FD ROUTING INTERFACE CHANGE), l'intera sequenza di azioni deve essere \_ ripetuta. \_ \_

Se le dimensioni del buffer di output non sono sufficienti per contenere l'indirizzo dell'interfaccia, viene restituito SOCKET ERROR come risultato di \_ questo IOCTL e [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) restituisce [WSAEFAULT](windows-sockets-error-codes-2.md). In questo caso, le dimensioni richieste del buffer di output verranno restituite in *lpcbBytesReturned.* Si noti che il codice di errore WSAEFAULT viene restituito anche se il parametro *lpvInBuffer*, *lpvOutBuffer* o *lpcbBytesReturned* non è completamente contenuto in una parte valida dello spazio degli indirizzi utente.

Se l'indirizzo di destinazione specificato nel buffer di input non può essere raggiunto tramite nessuna delle interfacce disponibili, viene restituito SOCKET ERROR come risultato di \_ questo IOCTL e [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) restituisce [WSAENETUNREACH](windows-sockets-error-codes-2.md) o [anche WSAENETDOWN](windows-sockets-error-codes-2.md) se tutta la connettività di rete viene persa.

### <a name="sio_set_compatibility_mode-opcode-setting-i-t3"></a>SIO \_ SET COMPATIBILITY MODE \_ \_ (impostazione del codice operativo: I, T==3)

Richiede il modo in cui lo stack di rete deve gestire determinati comportamenti per i quali il modo predefinito di gestione del comportamento può variare tra le versioni di Windows. La struttura dell'argomento **per SIO \_ SET COMPATIBILITY \_ \_ MODE** è specificata nella struttura **WSA \_ COMPATIBILITY \_ MODE** definita nel file di intestazione *Mswsockdef.h.* Questa struttura è definita nel modo seguente:

```cpp
/* Argument structure for SIO_SET_COMPATIBILITY_MODE */
typedef struct _WSA_COMPATIBILITY_MODE {
    WSA_COMPATIBILITY_BEHAVIOR_ID BehaviorId;
    ULONG TargetOsVersion;
} WSA_COMPATIBILITY_MODE, *PWSA_COMPATIBILITY_MODE;
```

Il valore specificato nel **membro BehaviorId** indica il comportamento richiesto. Il valore specificato nel **membro TargetOsVersion** indica la versione di Windows richiesta per il comportamento.

Il **membro BehaviorId** può essere uno dei valori del tipo di enumerazione **WSA \_ COMPATIBILITY BEHAVIOR \_ \_ ID** definito nel file di intestazione *Mswsockdef.h.* I valori possibili per il **membro BehaviorId** sono i seguenti.

| Termine                                                                                                                                                                             | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-|-|
| <span id="WsaBehaviorAll"></span><span id="wsabehaviorall"></span><span id="WSABEHAVIORALL"></span>WsaBehaviorAll<br/>                                                     | Equivale a richiedere tutti i possibili comportamenti compatibili definiti per **\_ \_ \_ L'ID COMPORTAMENTO DI COMPATIBILITÀ WSA**.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="WsaBehaviorReceiveBuffering"></span><span id="wsabehaviorreceivebuffering"></span><span id="WSABEHAVIORRECEIVEBUFFERING"></span>WsaBehaviorReceiveBuffering<br/> | Quando il membro **TargetOsVersion** è impostato su un valore per Windows Vista o versioni successive, le riduzioni alle dimensioni del buffer di ricezione TCP su questo socket usando l'opzione socket **\_ SO RCVBUF** sono consentite anche dopo che è stata stabilita una connessione TCP. <br/> Quando il membro **TargetOsVersion** è impostato su un valore precedente a Windows Vista, le riduzioni alle dimensioni del buffer di ricezione TCP in questo socket tramite l'opzione socket **\_ SO RCVBUF** non sono consentite dopo la creazione della connessione. <br/>                                                                                                                                                                                  |
| <span id="WsaBehaviorAutoTuning"></span><span id="wsabehaviorautotuning"></span><span id="WSABEHAVIORAUTOTUNING"></span>WsaBehaviorAutoTuning<br/>                         | Quando il membro **TargetOsVersion** è impostato su un valore per Windows Vista o versioni successive, l'ottimizzazione automatica della finestra di ricezione è abilitata e il fattore di scala della finestra TCP viene ridotto a 2 dal valore predefinito 8.<br/> Quando **TargetOsVersion** è impostato su un valore precedente a Windows Vista, l'ottimizzazione automatica della finestra di ricezione è disabilitata. Anche l'opzione di ridimensionamento della finestra TCP è disabilitata e le dimensioni massime della finestra di ricezione reale sono limitate a 65.535 byte. L'opzione di ridimensionamento della finestra TCP non può essere negoziata sulla connessione anche se l'opzione socket **\_ SO RCVBUF** è stata chiamata su questo socket specificando un valore maggiore di 65.535 byte prima che la connessione venga stabilita.<br/> |



 

Per informazioni più dettagliate, vedere le informazioni di [**riferimento su SIO \_ SET COMPATIBILITY \_ \_ MODE.**](/previous-versions/windows/desktop/legacy/cc136103(v=vs.85))

**SIO \_ SET \_ COMPATIBILITY \_ MODE è** supportato in Windows Vista e versioni successive.

### <a name="sio_set_group_qos-opcode-setting-i-t1"></a>SIO \_ SET \_ GROUP \_ QOS (impostazione del codice operativo: I, T==1)

Riservato.

### <a name="sio_set_priority_hint-opcode-setting-i-t3"></a>SIO_SET_PRIORITY_HINT (impostazione del codice operativo: I, T==3)

Fornisce un hint al protocollo di trasporto sottostante per trattare il traffico su questo socket con una priorità specifica. *LpvInBuffer* deve puntare a una variabile di tipo **PRIORITY_HINT** con *cbInBuffer* impostato su sizeof(PRIORITY_HINT). I *parametri lpvOutBuffer* *e cbOutBuffer* devono essere **rispettivamente NULL** e 0. L'implementazione TCP di Microsoft Windows supporta questo IOCTL a partire da Windows 10, versione 1809 (10.0; Build 17763) e successive come indicato di seguito: quando il valore di priorità richiesto è impostato su **IoPriorityHintVeryLow,** TCP usa una versione modificata dell'algoritmo LEDBAT (definito in RFC 6817) per controllare la velocità del traffico in uscita sul socket. Il traffico in ingresso non è interessato da questo IOCTL. LEDBAT è un algoritmo di scavenger e l'obiettivo è quello di mantenere bassa la latenza e impedire qualsiasi effetto negativo sul traffico con priorità normale, usurando dal modo in cui è presente il traffico con priorità normale.

Vedere anche [RFC 6817.](https://tools.ietf.org/html/rfc6817)

**SIO_SET_PRIORITY_HINT** è supportato in Windows 10, versione 1809 (10.0; Build 17763) e versioni successive.

### <a name="sio_set_qos-opcode-setting-i-t1"></a>SIO \_ SET \_ QOS (impostazione del codice operativo: I, T==1)

Associare la [**struttura QOS**](/windows/win32/api/winsock2/ns-winsock2-qos) specificata al socket. Non è necessario alcun buffer di output, la struttura **QOS** verrà ottenuta dal buffer di input. Il [codice di errore WSAENOPROTOOPT](windows-sockets-error-codes-2.md) è indicato per i provider di servizi che non supportano la qualità del servizio.

### <a name="sio_tcp_initial_rto-opcode-setting-i-t3"></a>SIO_TCP_INITIAL_RTO (impostazione del codice operativo: I, T==3)

Controlla le caratteristiche di ritrasmissione iniziali (SYN/SYN+ACK) di un socket TCP configurando i parametri di timeout di ritrasmissione iniziale (RTO). I parametri di configurazione vengono specificati in una [**struttura TCP \_ INITIAL \_ RTO \_ PARAMETERS.**](/windows/desktop/api/mswsock/ns-mswsock-transmit_file_buffers)

Per informazioni più dettagliate, vedere le informazioni di [**SIO_TCP_INITIAL_RTO**](./sio-tcp-initial-rto.md) riferimento. [**SIO_TCP_INITIAL_RTO**](./sio-tcp-initial-rto.md) è supportato in Windows 8, Windows Server 2012 e versioni successive.

### <a name="sio_timestamping"></a>SIO_TIMESTAMPING

IoCTL del socket usato per configurare la ricezione dei timestamp di trasmissione/ricezione del socket. Valido solo per i socket di datagramma. Il tipo di input **per SIO_TIMESTAMPING** è la [**TIMESTAMPING_CONFIG**](/windows/win32/api/mstcpip/ns-mstcpip-timestamping_config) di dati.

Vedere anche [Timestamping di Winsock.](/windows/win32/winsock/winsock-timestamping)

### <a name="sio_translate_handle-opcode-setting-i-o-t1"></a>SIO \_ TRANSLATE \_ HANDLE (impostazione del codice operativo: I, O, T==1)

Per ottenere un handle corrispondente per socket *s* valido nel contesto di un'interfaccia complementare, ad esempio TH \_ NETDEV e TH \_ TAPI. Nel buffer di input viene specificata una costante manifesto che identifica l'interfaccia complementare insieme agli altri parametri necessari. L'handle corrispondente sarà disponibile nel buffer di output al completamento di questa funzione. Per informazioni dettagliate specifiche di una particolare interfaccia complementare, vedere la sezione appropriata in [Winsock Annexes.](winsock-annexes.md) Il codice di errore [WSAENOPROTOOPT](windows-sockets-error-codes-2.md) è indicato per i provider di servizi che non supportano questo IOCTL per l'interfaccia complementare specificata. Questo IOCTL recupera l'handle associato tramite **SIO \_ TRANSLATE \_ HANDLE**.

È consigliabile usare Component Object Model (COM) anziché questo IOCTL per individuare e tenere traccia di altre interfacce che potrebbero essere supportate da un socket. Questo IOCTL è presente per la compatibilità con le versioni precedenti con sistemi in cui COM non è disponibile o non può essere usato per altri motivi.

### <a name="sio_udp_connreset-opcode-setting-i-t3"></a>SIO \_ UDP \_ CONNRESET (impostazione del codice operativo: I, T==3)

**Windows XP:** Controlla se vengono segnalati messaggi UDP PORT \_ UNREACHABLE. Impostare su **TRUE per** abilitare la creazione di report. Impostare su **FALSE per** disabilitare la creazione di report.

### <a name="sio_set_wfp_connection_redirect_records-opcode-setting-i-t3"></a>SIO \_ SET \_ WFP \_ CONNECTION \_ REDIRECT \_ RECORDS (opcode setting: I, T==3)

Imposta il record di reindirizzamento sul nuovo socket TCP usato per la connessione alla destinazione finale per l'uso da parte di un servizio di reindirizzamento windows filtering platform (WFP).

SIO [**SET WFP CONNECTION REDIRECT \_ \_ \_ \_ \_ RECORDS**](/previous-versions/windows/desktop/legacy/hh859714(v=vs.85)) IOCTL viene usato come parte del rilevamento delle connessioni proxy nelle connessioni socket reindirizzate. Questa funzionalità WFP facilita il rilevamento dei record di reindirizzamento dal reindirizzamento iniziale di una connessione alla connessione finale alla destinazione.

Per informazioni più dettagliate, vedere le informazioni di [**riferimento sui RECORD DI REINDIRIZZAMENTO DELLA CONNESSIONE SIO SET \_ \_ WFP. \_ \_ \_**](/previous-versions/windows/desktop/legacy/hh859714(v=vs.85)) **SIO \_ SET \_ WFP CONNECTION REDIRECT \_ \_ \_ RECORDS** è supportato in Windows 8, Windows Server 2012 e versioni successive.

### <a name="sio_tcp_info-opcode-setting-i-o-t3"></a>SIO \_ TCP \_ INFO (impostazione del codice operativo: I, O, T==3)

Recupera le statistiche TCP per un socket. Le statistiche TCP vengono fornite in una [**struttura TCP \_ INFO \_ v0.**](/windows/desktop/api/Mstcpip/ns-mstcpip-tcp_info_v0)

A differenza del recupero di statistiche TCP con la funzione [**GetPerTcpConnectionEStats,**](/windows/win32/api/iphlpapi/nf-iphlpapi-getpertcpconnectionestats) il recupero delle statistiche TCP con questo codice di controllo non richiede che il codice utente carichi, archivi e filtri la tabella di connessione TCP e non richieda privilegi elevati per l'uso.

Per altre informazioni, vedere [**SIO \_ TCP \_ INFO.**](/previous-versions/windows/desktop/legacy/mt823415(v=vs.85)) **SIO \_ TCP \_ INFO** è supportato in Windows 10 versione 1703, Windows Server 2016 e versioni successive.

## <a name="remarks"></a>Commenti

Gli ioctls winsock sono definiti in diversi file di intestazione. Sono inclusi i file *di intestazione Winsock2.h,* *Mswsock.h* e *Mstcpip.h.*

In Microsoft Windows Software Development Kit (Windows SDK) (SDK) rilasciato per Windows Vista e versioni successive, l'organizzazione dei file di intestazione è stata modificata e diversi Ioctls Winsock sono definiti anche nei file di intestazione *Ws2def.h,* *Ws2ipdef.h* e *Mswsockdef.h.* Il file *di intestazione Ws2def.h* viene incluso automaticamente dal file *di intestazione Winsock2.h.* Il file *di intestazione Ws2ipdef.h* viene incluso automaticamente dal file di intestazione *Ws2tcpip.h.* Il file *di intestazione Mswsockdef.h* viene incluso automaticamente nel file di intestazione *Mswsockdef.h.*

## <a name="requirements"></a>Requisiti

|Requisito|Valore|
|-|-|
| Intestazione<br/> | <dl> <dt>Winsock2.h; </dt> <dt>Mstcpip.h; </dt> <dt>Mswsock.h; </dt> <dt>Mswsockdef.h in Windows Vista, Windows Server 2008 e Windows 7 (incluso Mswsock.h); </dt> <dt>Ws2def.h in Windows Vista, Windows Server 2008 e Windows 7 (include Winsock2.h); </dt> <dt>Ws2ipdef.h in Windows Vista, Windows Server 2008 e Windows 7 (includere Ws2tcpip.h)</dt> </dl> |
