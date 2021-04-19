---
description: Argomento di navigazione per le IOCTL socket di Windows Sockets (Winsock).
ms.assetid: 6a63c2c9-4e09-4a62-b39f-3ccb26287da8
title: IOCTL Winsock (Winsock2.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de7094f802b815bfbd7511bd67eb4e6b1767cb94
ms.sourcegitcommit: 392c0a56f99f4d19686e734291abcac887fc5ba2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/22/2021
ms.locfileid: "106320080"
---
# <a name="winsock-ioctls"></a>IOCTL Winsock

Questa sezione descrive i controlli di input/output (IOCTL) del socket Winsock per varie edizioni dei sistemi operativi Windows. Utilizzare la funzione [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) o [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) per emettere un IOCTL Winsock per controllare la modalità di un socket, il protocollo di trasporto o il sottosistema di comunicazione.

Alcune IOCTL Winsock richiedono una spiegazione maggiore di quella concessa da questa tabella; tali opzioni contengono collegamenti ad argomenti aggiuntivi.

È possibile adottare uno schema di codifica che conserva i codici operativi [**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket) attualmente definiti, offrendo un modo pratico per partizionare lo spazio degli identificatori opcode in, in quanto il parametro *dwIoControlCode* è ora un'entità a 32 bit. Il parametro *dwIoControlCode* è progettato per consentire il protocollo e l'indipendenza del fornitore quando si aggiungono nuovi codici di controllo mantenendo la compatibilità con i codici di controllo Windows sockets 1,1 e UNIX. Il parametro *dwIoControlCode* ha il formato seguente.

| I  | O  | V  | T  | Gruppo fornitore/Indirizzo | Codice                   |
|-|-|-|-|-|-|
| 3  | 3  | 2  | 2 2 | 2 2 2 2 2 2 2 1 1 1 1 | 1 1 1 1 1 1              |
| 1  | 0  | 9  | 8 7 | 6 5 4 3 2 1 0 9 8 7 6 | 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0 |

> [!Note] 
> Il bit nel parametro *dwIoControlCode* visualizzato nella tabella deve essere letto verticalmente dall'alto verso il basso per colonna. Quindi, il bit più a sinistra è il bit 31, il bit successivo è il bit 30 e il bit più a destra è il bit 0.

Viene impostato se il buffer di input è valido per il codice, come per **IOC_IN**.

O viene impostato se il buffer di output è valido per il codice, come con **IOC_OUT**. I codici di controllo che usano I buffer di input e di output impostano sia I che O.

V viene impostato se non sono presenti parametri per il codice, come con **IOC_VOID**.

T è una quantità a 2 bit che definisce il tipo di IOCTL. Vengono definiti i valori seguenti:

0 il IOCTL è un codice IOCTL standard di UNIX, come con **FIONREAD** e **FIONBIO**.

1 il IOCTL è un codice IOCTL generico di Windows Sockets 2. I nuovi codici IOCTL definiti per Windows Sockets 2 avranno T = = 1.

2 il IOCTL si applica solo a una famiglia di indirizzi specifica.

3 il IOCTL si applica solo al provider di un fornitore specifico, come con **IOC_VENDOR**. Questo tipo consente alle aziende di essere assegnato un numero di fornitore visualizzato nel parametro della **famiglia di fornitori/indirizzi** . Quindi, il fornitore può definire nuovi IOCTL specifici del fornitore senza dover registrare il IOCTL con una compensazione, garantendo così la flessibilità e la privacy del fornitore.

**Gruppo fornitore/Indirizzo** Quantità a 11 bit che definisce il fornitore proprietario del codice (se T = = 3) o che contiene la famiglia di indirizzi a cui si applica il codice (se T = = 2). Se si tratta di un codice IOCTL UNIX (T = = 0), questo parametro ha lo stesso valore del codice in UNIX. Se si tratta di un comando IOCTL Windows Sockets 2 generico (T = = 1), questo parametro può essere utilizzato come estensione del parametro code per fornire valori di codice aggiuntivi.

**Codice** Quantità a 16 bit che contiene il codice IOCTL specifico per l'operazione.

## <a name="unix-ioctl-codes"></a>Codici IOCTL UNIX

Sono supportati i seguenti codici IOCTL UNIX (comandi).

### <a name="fionbio"></a>FIONBIO

Abilitare o disabilitare la modalità non di blocco nei socket *s*. Il parametro *lpvInBuffer* punta a un **unsigned long** (QoS), che è diverso da zero se è necessario abilitare la modalità non di blocco e zero se deve essere disabilitato. Quando un socket viene creato, viene eseguito in modalità di blocco, ovvero la modalità non di blocco è disabilitata. Questo è coerente con i socket BSD.

La routine [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) o [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) imposta automaticamente un socket in modalità non di blocco. Se **WSAAsyncSelect** o **WSAEventSelect** è stato emesso su un socket, qualsiasi tentativo di usare [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) per impostare il socket sulla modalità di blocco avrà esito negativo con WSAEINVAL. Per impostare di nuovo il socket sulla modalità di blocco, un'applicazione deve prima disabilitare **WSAAsyncSelect** chiamando **WSAAsyncSelect** con il parametro *Levent* uguale a zero oppure disabilitare **WSAEventSelect** chiamando **WSAEventSelect** con il parametro *lNetworkEvents* uguale a zero.

### <a name="fionread"></a>FIONREAD

Determinare la quantità di dati che possono essere letti in modo atomico da socket *s*. Il parametro *lpvOutBuffer* punta a un oggetto **Long senza segno** in cui [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) archivia il risultato.

Se il socket passato nel parametro *s* è orientato al flusso, ad esempio il tipo Sock \_ Stream, **FIONREAD** restituisce la quantità totale di dati che è possibile leggere in una singola operazione di ricezione. si tratta in genere dello stesso valore della quantità totale di dati accodati nel socket (poiché un flusso di dati è orientato ai byte, questa operazione non è garantita).

Se il socket passato nel parametro *s* è orientato ai messaggi (ad esempio, digitare Sock \_ DGRAM), **FIONREAD** restituisce il numero totale di byte disponibili per la lettura e non le dimensioni del primo datagramma (messaggio) accodato nel socket.

### <a name="siocatmark"></a>SIOCATMARK

Determinare se tutti i dati di OOB sono stati letti o meno. Si applica solo a un socket di tipo Stream, ad esempio il tipo SOCK \_ Stream, che è stato configurato per la ricezione inline di qualsiasi dato OOB ( \_ OOBINLINE). Se nessun dato OOB è in attesa di essere letto, l'operazione restituisce TRUE. In caso contrario, restituisce **false** e la successiva operazione di ricezione eseguita sul socket recupererà alcuni o tutti i dati che precedono il contrassegno; l'applicazione deve usare l'operazione **SIOCATMARK** per determinare se rimane. Se sono presenti dati normali che precedono i dati urgenti (fuori banda), verranno ricevuti in ordine. Si noti che le operazioni [**ricezione**](/windows/desktop/api/winsock/nf-winsock-recv) non mescoleranno mai OOB e i dati normali nella stessa chiamata. *lpvOutBuffer* punta a un bool in cui [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) archivia il risultato.

## <a name="windows-sockets-2-commands"></a>Comandi di Windows Sockets 2

Sono supportati i seguenti comandi di Windows Sockets 2.

### <a name="sio_acquire_port_reservation-opcode-setting-i-t3"></a>SIO_ACQUIRE_PORT_RESERVATION (impostazione opcode: I, T = = 3)

Richiedere una prenotazione di runtime per un blocco di porte TCP o UDP. Per le prenotazioni di porte di runtime, il pool di porte richiede che le prenotazioni vengano utilizzate dal processo sul cui socket è stata concessa la prenotazione. Le prenotazioni di porte di runtime durano solo fino a quando la durata del socket in cui è stata chiamata la [**\_ porta di acquisizione \_ \_ sio**](/previous-versions/windows/desktop/legacy/gg699720(v=vs.85)) è stata chiamata. Al contrario, le prenotazioni di porte permanenti create utilizzando la funzione [**CreatePersistentTcpPortReservation**](/windows/win32/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) o [**CreatePersistentUdpPortReservation**](/windows/win32/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) possono essere utilizzate da qualsiasi processo con la possibilità di ottenere prenotazioni permanenti.

Per informazioni più dettagliate, vedere le informazioni di riferimento sulla [**\_ prenotazione della \_ porta \_ sio Acquire**](/previous-versions/windows/desktop/legacy/gg699720(v=vs.85)) .

[**Sio \_ La \_ \_ prenotazione della porta di acquisizione**](/previous-versions/windows/desktop/legacy/gg699720(v=vs.85)) è supportata in Windows Vista e nelle versioni successive del sistema operativo.

### <a name="sio_address_list_change-opcode-setting-v-t1"></a>\_Modifica dell' \_ elenco di indirizzi sio \_ (impostazione opcode: V, T = = 1)

Per ricevere la notifica delle modifiche nell'elenco degli indirizzi di trasporto locali della famiglia di protocolli del socket a cui l'applicazione può eseguire il binding. Al completamento di questo IOCTL non verranno fornite informazioni di output; il completamento indica semplicemente che l'elenco di indirizzi locali disponibili è stato modificato ed è necessario eseguire di nuovo la query tramite la **\_ query dell' \_ elenco \_ di indirizzi sio**.

Viene presupposto (sebbene non necessario) che l'applicazione utilizzi l'I/O sovrapposto per ricevere una notifica di modifica tramite il completamento della richiesta di **\_ modifica dell' \_ elenco \_ di indirizzi sio** . In alternativa, se la **\_ modifica dell' \_ elenco \_ di indirizzi sio** viene eseguita su un socket non bloccante e senza parametri sovrapposti (*lpOverlapped* /  *il lpCompletionRoutine* sono impostati su **null**), il comando verrà completato immediatamente con l'errore [WSAEWOULDBLOCK](windows-sockets-error-codes-2.md). L'applicazione può quindi attendere gli eventi di modifica dell'elenco indirizzi tramite una chiamata a [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) o [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) con il \_ bit di \_ modifica elenco indirizzi FD \_ impostato nella maschera di bit dell'evento di rete.

### <a name="sio_address_list_query-opcode-setting-o-t1"></a>\_Query di \_ elenco indirizzi sio \_ (impostazione opcode: O, T = = 1)

Ottiene un elenco degli indirizzi di trasporto locali della famiglia di protocolli del socket a cui l'applicazione può eseguire il binding. L'elenco di indirizzi varia in base alla famiglia di indirizzi e alcuni indirizzi sono esclusi dall'elenco.

> [!Note] 
> Negli ambienti plug-n-Play di Windows gli indirizzi possono essere aggiunti e rimossi dinamicamente. Pertanto, le applicazioni non possono basarsi sulle informazioni restituite dalla **\_ query dell' \_ elenco \_ di indirizzi sio** per essere persistenti. Le applicazioni possono registrarsi per le notifiche di modifica degli indirizzi tramite l' **\_ elenco indirizzi sio \_ \_ modificare** IOCTL, che fornisce la notifica tramite l' \_ \_ evento di modifica elenco indirizzi I/o sovrapposto o FD \_ . La sequenza di azioni seguente può essere utilizzata per garantire che l'applicazione disponga sempre di informazioni sull'elenco di indirizzi correnti:

-  Rilascia IOCTL di **\_ \_ \_ modifica elenco indirizzi sio**
-  Errore **di \_ \_ \_ query elenco indirizzi sio**
-  Ogni volta che la **\_ \_ \_ modifica** dell'elenco di indirizzi sio invia una notifica all'applicazione della modifica dell'elenco di indirizzi (tramite i/o sovrapposti o segnalando \_ \_ l'evento di modifica dell'elenco di indirizzi FD \_ ), l'intera sequenza di azioni deve essere ripetuta.

Per informazioni più dettagliate, vedere il riferimento alla [**\_ \_ \_ query dell'elenco indirizzi sio**](/previous-versions/windows/desktop/legacy/dd877219(v=vs.85)) . **Sio \_ La \_ \_ query elenco indirizzi** è supportata in Windows 2000 e versioni successive.

### <a name="sio_apply_transport_setting-opcode-setting-i-t3"></a>\_Impostazione applica \_ trasporto sio \_ (impostazione opcode: I, T = = 3)

Applica un'impostazione di trasporto a un socket. L'impostazione di trasporto da applicare è basata sull' [**\_ \_ ID di impostazione del trasporto**](/windows/win32/api/transportsettingcommon/ns-transportsettingcommon-transport_setting_id) passato nel parametro *lpvInBuffer* .

L'unica impostazione del trasporto attualmente definita è per la funzionalità di **\_ notifica in tempo \_ \_ reale** in un socket TCP.

Se l' [**\_ \_ ID di impostazione del trasporto**](/windows/win32/api/transportsettingcommon/ns-transportsettingcommon-transport_setting_id) passato ha il membro **GUID** impostato sulla **\_ \_ \_ funzionalità di notifica in tempo reale**, si tratta di una richiesta per applicare le impostazioni di notifica in tempo reale per il socket TCP usato con [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) per ricevere notifiche di rete in background in un'app di Windows Store.

Per informazioni più dettagliate, vedere la Guida di riferimento per l' [**\_ impostazione del \_ trasporto \_ sio Apply**](/previous-versions/windows/desktop/legacy/jj553481(v=vs.85)) . **Sio \_ L' \_ \_ impostazione applica trasporto** è supportata in Windows 8, Windows Server 2012 e versioni successive.

### <a name="sio_associate_handle-opcode-setting-i-t1"></a>\_Handle di associazione sio \_ (impostazione opcode: I, T = = 1)

Associa il socket all'handle specificato di un'interfaccia correlata. Il buffer di input contiene il valore integer corrispondente alla costante del manifesto per l'interfaccia complementare, ad esempio \_ netdev e \_ TAPI., seguito da un valore che rappresenta un handle dell'interfaccia complementare specificata, insieme a qualsiasi altra informazione richiesta. Per informazioni dettagliate specifiche su una particolare interfaccia complementare, vedere la sezione appropriata negli [allegati di Winsock](winsock-annexes.md) . La dimensione totale viene riflessa nella lunghezza del buffer di input. Non è necessario alcun buffer di output. Il codice di errore [WSAENOPROTOOPT](windows-sockets-error-codes-2.md) è indicato per i provider di servizi che non supportano questo IOCTL. È possibile recuperare l'handle associato da questo IOCTL usando **l' \_ \_ handle di conversione sio**.

È possibile utilizzare un'interfaccia complementare, ad esempio, se un particolare provider fornisce (1) una grande quantità di controlli aggiuntivi sul comportamento di un socket e (2) i controlli sono sufficientemente specifici del provider e non eseguono il mapping alle funzioni socket Windows esistenti o a quelle che potrebbero essere definite in futuro. È consigliabile utilizzare il Component Object Model (COM) invece di questo IOCTL per individuare e rilevare altre interfacce che potrebbero essere supportate da un socket. Questo IOCTL è presente per la compatibilità (inversa) con i sistemi in cui COM non è disponibile o non può essere usato per altri motivi.

### <a name="sio_associate_port_reservation-opcode-setting-i-t3"></a>\_Prenotazione porta di associazione sio \_ \_ (impostazione opcode: I, T = = 3)

Associare un socket a una prenotazione di runtime o permanente per un blocco di porte TCP o UDP identificato dal token di prenotazione della porta. Prima di associare il socket, è necessario emettere l'IOCTL di [**\_ prenotazione della \_ porta \_ di associazione sio**](/previous-versions/windows/desktop/legacy/gg699721(v=vs.85)) . Se e quando il socket è associato, la porta assegnata verrà selezionata dalla prenotazione della porta identificata dal token specificato. Se non è disponibile alcuna porta dalla prenotazione specificata, la chiamata della funzione [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) avrà esito negativo.

Per informazioni più dettagliate, vedere il riferimento alla [**\_ prenotazione della \_ porta \_ di associazione sio**](/previous-versions/windows/desktop/legacy/gg699721(v=vs.85)) .

[**Sio \_ La \_ \_ prenotazione delle porte associate**](/previous-versions/windows/desktop/legacy/gg699721(v=vs.85)) è supportata in Windows Vista e nelle versioni successive del sistema operativo.

### <a name="sio_base_handle-opcode-setting-o-t1"></a>\_ \_ Handle di base SIO (impostazione opcode: O, T = = 1)

Recupera l'handle del provider di servizi di base per un socket specificato. Il valore restituito è un **socket**.

Un provider di servizi su più livelli non intercetta mai questo IOCTL poiché il valore restituito deve essere l'handle del socket del provider di servizi di base.

Se il buffer di output non è sufficientemente grande per un handle di socket (il valore di *cbOutBuffer* è inferiore alla dimensione di un **socket**) o il parametro *lpvOutBuffer* è un puntatore **null** , viene restituito un **\_ errore socket** come risultato di questo IOCTL e [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) restituisce [WSAEFAULT](windows-sockets-error-codes-2.md).

**Sio \_ L' \_ handle di base** è definito nel file di intestazione *mswsock. h* e supportato in Windows Vista e versioni successive.

### <a name="sio_bsp_handle-opcode-setting-o-t1"></a>\_Handle BSP sio \_ (impostazione opcode: O, T = = 1)

Recupera l'handle del provider di servizi di base per un socket usato dalla funzione [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) . Il valore restituito è un **socket**.

Questo IOCTL viene usato da un provider di servizi su più livelli per assicurarsi che il provider intercetta la funzione [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) .

Se il buffer di output non è sufficientemente grande per un handle di socket (il valore di *cbOutBuffer* è inferiore alla dimensione di un **socket**) o il parametro *lpvOutBuffer* è un puntatore **null** , viene restituito un **\_ errore socket** come risultato di questo IOCTL e [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) restituisce [WSAEFAULT](windows-sockets-error-codes-2.md).

**Sio \_ L' \_ handle BSP** è definito nel file di intestazione *mswsock. h* e supportato in Windows Vista e versioni successive.

### <a name="sio_bsp_handle_select-opcode-setting-o-t1"></a>\_ \_ Selezione handle BSP sio \_ (impostazione opcode: O, T = = 1)

Recupera l'handle del provider di servizi di base per un socket utilizzato dalla funzione [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) . Il valore restituito è un **socket**.

Questo IOCTL viene usato da un provider di servizi su più livelli per assicurarsi che il provider intercetta la funzione [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) .

Se il buffer di output non è sufficientemente grande per un handle di socket (il valore di *cbOutBuffer* è inferiore alla dimensione di un **socket**) o il parametro *lpvOutBuffer* è un puntatore **null** , viene restituito un **\_ errore socket** come risultato di questo IOCTL e [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) restituisce [WSAEFAULT](windows-sockets-error-codes-2.md).

**Sio \_ La \_ \_ selezione dell'handle BSP** viene definita nel file di intestazione *mswsock. h* e supportata in Windows Vista e versioni successive.

### <a name="sio_bsp_handle_poll-opcode-setting-o-t1"></a>\_ \_ Polling dell'handle di sio BSP \_ (impostazione opcode: O, T = = 1)

Recupera l'handle del provider di servizi di base per un socket usato dalla funzione [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) . Il parametro *lpOverlapped* deve essere un puntatore **null** . Il valore restituito è un **socket**.

Questo IOCTL viene usato da un provider di servizi su più livelli per assicurarsi che il provider intercetta la funzione [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) .

Se il buffer di output non è sufficientemente grande per un handle di socket (il valore di *cbOutBuffer* è inferiore alle dimensioni di un **socket**), il parametro *lpvOutBuffer* è un puntatore **null** o il parametro *lpOverlapped* non è un puntatore **null** , viene restituito un **\_ errore socket** come risultato di questo IOCTL e [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) restituisce [WSAEFAULT](windows-sockets-error-codes-2.md).

**Sio \_ Il \_ \_ polling dell'handle BSP** è definito nel file di intestazione *mswsock. h* e supportato in Windows Vista e versioni successive.

### <a name="sio_chk_qos-opcode-setting-i-o-t3"></a>\_QoS sio chk \_ (impostazione opcode: I, O, T = = 3)

Recupera informazioni sulle caratteristiche del traffico QoS. Durante la fase di transizione sul sistema di invio tra la configurazione del flusso e la ricezione di un messaggio RESV (vedere [come il servizio RSVP richiama TC](/previous-versions/windows/desktop/qos/how-the-rsvp-service-invokes-tc) per ulteriori informazioni sulla fase di transizione), il traffico associato a un flusso di RSVP viene modellato in base al tipo di servizio ([massimo sforzo](/previous-versions/windows/desktop/qos/best-effort), [carico controllato](/previous-versions/windows/desktop/qos/controlled-load)o [garantito](/previous-versions/windows/desktop/qos/guaranteed)). Per altre informazioni, vedere [uso di sio \_ chk \_ QoS](/previous-versions/windows/desktop/qos/using-sio-chk-qos) nella sezione relativa alla [qualità del servizio](/previous-versions/windows/desktop/qos/qos-start-page) di Platform SDK.

### <a name="sio_cpu_affinity-opcode-setting-i-t3"></a>SIO_CPU_AFFINITY (impostazione opcode: I, T = = 3)

Consente la condivisione delle porte e la ricezione della parallelizzazione delle indicazioni. Quando l'applicazione utilizza questa opzione socket per associare i socket a processori diversi e quindi associa i socket allo stesso indirizzo, le indicazioni di ricezione verranno distribuite tra i socket basati sull'hash di Receive-Side Scaling (RSS). Le impostazioni RSS non cambiano, quindi qualsiasi flusso specificato (endpoint locale, coppia di endpoint remoti) sarà sempre indicato nello stesso processore. Di conseguenza, tutti i pacchetti che appartengono a un determinato flusso verranno indicati nello stesso socket. Questo IOCTL deve essere chiamato prima dell'associazione; in caso contrario, verrà restituito WSAEINVAL. Il buffer di input è un indice del processore (in base zero) di tipo USHORT. IOCTL è incompatibile con SO_REUSEADDR e SO_REUSE_MULTICASTPORT. Supportato solo per i socket UDP.

> [!NOTE]
> Se la destinazione è la versione 10.0.19041.0 (Windows 10, versione 2004) del Windows SDK, usare il valore `0x98000015` anziché il nome **SIO_CPU_AFFINITY**.

### <a name="sio_enable_circular_queueing-opcode-setting-v-t1"></a>SIO \_ Abilita \_ \_ Accodamento circolare (impostazione opcode: V, T = = 1)

Indica al provider di servizi sottostante orientato ai messaggi che un messaggio appena raggiunto non deve mai essere eliminato a causa di un overflow della coda del buffer. Al contrario, il messaggio meno recente nella coda deve essere eliminato per poter contenere il messaggio appena arrivato. Non sono necessari buffer di input e di output. Si noti che questo IOCTL è valido solo per i socket associati a protocolli non affidabili e orientati ai messaggi. Il codice di errore [WSAENOPROTOOPT](windows-sockets-error-codes-2.md) è indicato per i provider di servizi che non supportano questo IOCTL.

### <a name="sio_find_route-opcode-setting-o-t1"></a>\_ \_ Route di ricerca SIO (impostazione opcode: O, T = = 1)

Quando viene emesso, questo IOCTL richiede che venga individuata la route per l'indirizzo remoto specificato come [**sockaddr**](sockaddr-2.md) nel buffer di input. Se l'indirizzo è già presente nella cache locale, la relativa voce viene invalidata. Nel caso di IPX di Novell, questa chiamata avvia un GetLocalTarget IPX (GLT), che esegue una query sulla rete per l'indirizzo remoto specificato.

### <a name="sio_flush-opcode-setting-v-t1"></a>\_Scaricamento SIO (impostazione opcode: V, T = = 1)

Elimina il contenuto corrente della coda di invio associata al socket. Non sono necessari buffer di input e di output. Il codice di errore [WSAENOPROTOOPT](windows-sockets-error-codes-2.md) è indicato per i provider di servizi che non supportano questo IOCTL.

### <a name="sio_get_broadcast_address-opcode-setting-o-t1"></a>\_ \_ Indirizzo di trasmissione sio Get \_ (impostazione opcode: O, T = = 1)

Questo IOCTL riempie il buffer di output con una struttura [sockaddr](sockaddr-2.md) contenente un indirizzo di broadcast adatto da usare con [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto) /  [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto). Questo IOCTL non è supportato per i socket IPv6 e restituisce il codice di errore [WSAENOPROTOOPT](windows-sockets-error-codes-2.md) .

### <a name="sio_get_extension_function_pointer-opcode-setting-o-i-t1"></a>\_Puntatore alla funzione di estensione sio Get \_ \_ \_ (impostazione opcode: O, I, T = = 1)

Recuperare un puntatore alla funzione di estensione specificata supportata dal provider di servizi associato. Il buffer di input contiene un identificatore univoco globale (**GUID**) il cui valore identifica la funzione di estensione in questione. Il puntatore alla funzione desiderata viene restituito nel buffer di output. Gli identificatori delle funzioni di estensione sono stabiliti dai fornitori di provider di servizi e devono essere inclusi nella documentazione del fornitore che descrive le funzionalità e la semantica delle funzioni di estensione.

I valori GUID per le funzioni di estensione supportate dal provider di servizi TCP/IP di Windows sono definiti nel file di intestazione *mswsock. h* . Il valore possibile per questi GUID è il seguente:

| Termine                                                                                                                | Descrizione                                                                               |
|-|-|
| <span id="WSAID_ACCEPTEX"></span><span id="wsaid_acceptex"></span>\_ACCEPTEX WSAID<br/>                                     | Funzione di estensione [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex) .<br/>                         |
| <span id="WSAID_CONNECTEX"></span><span id="wsaid_connectex"></span>\_CONNECTEX WSAID<br/>                                  | Funzione di estensione [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex) . <br/>                      |
| <span id="WSAID_DISCONNECTEX"></span><span id="wsaid_disconnectex"></span>\_DISCONNECTEX WSAID<br/>                         | Funzione di estensione [**DisconnectEx**](/previous-versions/windows/desktop/legacy/ms737757(v=vs.85)) . <br/>                |
| <span id="WSAID_GETACCEPTEXSOCKADDRS"></span><span id="wsaid_getacceptexsockaddrs"></span>\_GETACCEPTEXSOCKADDRS WSAID<br/> | Funzione di estensione [**GetAcceptExSockaddrs**](/windows/win32/api/mswsock/nf-mswsock-getacceptexsockaddrs) .<br/> |
| <span id="WSAID_TRANSMITFILE"></span><span id="wsaid_transmitfile"></span>\_TRANSMITFILE WSAID<br/>                         | Funzione di estensione [**TransmitFile**](/windows/win32/api/mswsock/nf-mswsock-transmitfile) .<br/>                 |
| <span id="WSAID_TRANSMITPACKETS"></span><span id="wsaid_transmitpackets"></span>\_TRANSMITPACKETS WSAID<br/>                | Funzione di estensione [**TransmitPackets**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_transmitpackets) . <br/>          |
| <span id="WSAID_WSARECVMSG"></span><span id="wsaid_wsarecvmsg"></span>\_WSARECVMSG WSAID<br/>                               | Funzione di estensione [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) .<br/>                     |
| <span id="WSAID_WSASENDMSG"></span><span id="wsaid_wsasendmsg"></span>\_WSASENDMSG WSAID<br/>                               | Funzione di estensione [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) . <br/>                      |

### <a name="sio_get_group_qos-opcode-setting-o-i-t1"></a>\_QoS del gruppo sio Get \_ \_ (impostazione opcode: O, I, T = = 1)

Riservato per un utilizzo futuro con i socket.

Recuperare la struttura [**QoS**](/windows/win32/api/winsock2/ns-winsock2-qos) associata al gruppo di socket a cui appartiene il socket. Il buffer di input è facoltativo. Alcuni protocolli (ad esempio, RSVP) consentono di usare il buffer di input per qualificare una richiesta di qualità del servizio. La struttura **QoS** verrà copiata nel buffer di output. Se il socket non appartiene a un gruppo di socket appropriato, i membri **SendingFlowspec** e **ReceivingFlowspec** della struttura **QoS** restituita vengono impostati su **null**. Il codice di errore [WSAENOPROTOOPT](windows-sockets-error-codes-2.md) è indicato per i provider di servizi che non supportano la qualità del servizio.

### <a name="sio_get_interface_list-opcode-setting-o-t0"></a>\_ \_ Elenco di interfaccia sio Get \_ (impostazione opcode: O, T = = 0)

Restituisce un elenco di interfacce IP configurate e dei relativi parametri come una matrice di strutture di [**\_ informazioni di interfaccia**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-interface_info) .

> [!Note]  
> Il supporto di questo comando è obbligatorio per i provider di servizi TCP/IP conformi a Windows Sockets 2.

Il parametro *lpvOutBuffer* punta al buffer in cui archiviare le informazioni sulle interfacce come una matrice di strutture di [**\_ informazioni di interfaccia**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-interface_info) per gli indirizzi IP unicast sulle interfacce. Il parametro *cbOutBuffer* specifica la lunghezza del buffer di output. Il numero di interfacce restituite (numero di strutture restituite nel buffer a cui punta il parametro *lpvOutBuffer* ) può essere determinato in base alla lunghezza effettiva del buffer di output restituito nel parametro *lpcbBytesReturned* .

Se la funzione [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) viene chiamata con **l' \_ \_ \_ elenco di interfacce sio Get** e il membro level del parametro socket *s* non è definito **come \_ IP IPPROTO**, viene restituito **WSAEINVAL** . Una chiamata alla funzione **WSAIoctl** con l' **\_ elenco di \_ interfaccia \_ sio Get** restituisce **WSAEFAULT** se il parametro *cbOutBuffer* che specifica la lunghezza del buffer di output è troppo piccolo per ricevere l'elenco delle interfacce configurate.

**Sio \_ GET \_ Interface \_ List** è supportato in Windows Me/98 e Windows NT 4,0 con SP4 e versioni successive.

### <a name="sio_get_interface_list_ex-opcode-setting-o-t0"></a>\_Esempio sio Get \_ Interface \_ List \_ (impostazione opcode: O, T = = 0)

Riservato per un utilizzo futuro con i socket.

Restituisce un elenco di interfacce IP configurate e dei relativi parametri come matrice di strutture di [**\_ \_ informazioni di interfaccia**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-interface_info_ex) .

Il parametro *lpvOutBuffer* punta al buffer in cui archiviare le informazioni sulle interfacce come una matrice di strutture delle [**\_ informazioni di \_ interfaccia**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-interface_info_ex) per gli indirizzi IP unicast sull'interfaccia. Il parametro *cbOutBuffer* specifica la lunghezza del buffer di output. Il numero di interfacce restituite (numero di strutture restituite in *lpvOutBuffer*) può essere determinato in base alla lunghezza effettiva del buffer di output restituito nel parametro *lpcbBytesReturned* .

**Sio \_ Il GET \_ Interface list, ad \_ \_ esempio** , non è attualmente supportato in Windows.

### <a name="sio_get_qos-opcode-setting-o-t1"></a>\_QoS Get \_ QoS (impostazione opcode: O, T = = 1)

Riservato per un utilizzo futuro con i socket. Recuperare la struttura [**QoS**](/windows/win32/api/winsock2/ns-winsock2-qos) associata al socket. Il buffer di input è facoltativo. Alcuni protocolli (ad esempio, RSVP) consentono di usare il buffer di input per qualificare una richiesta di qualità del servizio. La struttura **QoS** verrà copiata nel buffer di output. Il buffer di output deve avere dimensioni sufficientemente grandi per poter contenere la struttura **QoS** completa. Il codice di errore [WSAENOPROTOOPT](windows-sockets-error-codes-2.md) è indicato per i provider di servizi che non supportano la qualità del servizio.

Un mittente non è in grado di chiamare **sio \_ get \_ QoS** finché il socket non è connesso.

Un ricevitore può chiamare **sio \_ get \_ QoS** non appena viene associato.

### <a name="sio_ideal_send_backlog_change-opcode-setting-v-t0"></a>\_Modifica backlog di invio ideale per sio \_ \_ \_ (impostazione opcode: V, T = = 0)

Notifica a un'applicazione quando viene modificato il valore di backlog di invio ideale per la connessione sottostante.

Quando si inviano dati tramite una connessione TCP mediante Windows Sockets, è importante garantire una quantità sufficiente di dati in attesa (inviati ma non ancora riconosciuti) in TCP per ottenere la massima velocità effettiva. Il valore ideale per la quantità di dati in attesa di ottenere la migliore velocità effettiva per la connessione TCP è denominato dimensione del backlog di invio ideale. Il valore ISB è una funzione del prodotto di ritardo della larghezza di banda della connessione TCP e della finestra di ricezione annunciata del ricevitore (e parzialmente la quantità di congestione nella rete).

Il valore ISB per connessione è disponibile nell'implementazione del protocollo TCP in Windows Server 2008, Windows Vista con SP1 e versioni successive del sistema operativo. La **\_ modifica del \_ \_ backlog di \_ invio ideale di sio** può essere usata da un'applicazione per ricevere una notifica quando il valore di ISB cambia in modo dinamico per una connessione.

Per informazioni più dettagliate, vedere il riferimento alla [**\_ modifica del \_ \_ backlog \_ di invio ideale per sio**](/previous-versions/windows/desktop/legacy/bb736548(v=vs.85)) .

[**Sio \_ La \_ \_ \_ modifica del backlog di invio ideale**](/previous-versions/windows/desktop/legacy/bb736548(v=vs.85)) è supportata in Windows Server 2008, Windows Vista con SP1 e versioni successive del sistema operativo.

### <a name="sio_ideal_send_backlog_query-opcode-setting-o-t0"></a>\_Query del backlog di invio ideale per sio \_ \_ \_ (impostazione opcode: O, T = = 0)

Recupera il valore di backlog di invio ideale per la connessione sottostante.

Quando si inviano dati tramite una connessione TCP mediante Windows Sockets, è importante garantire una quantità sufficiente di dati in attesa (inviati ma non ancora riconosciuti) in TCP per ottenere la massima velocità effettiva. Il valore ideale per la quantità di dati in attesa di ottenere la migliore velocità effettiva per la connessione TCP è denominato dimensione del backlog di invio ideale. Il valore ISB è una funzione del prodotto di ritardo della larghezza di banda della connessione TCP e della finestra di ricezione annunciata del ricevitore (e parzialmente la quantità di congestione nella rete).

Il valore ISB per connessione è disponibile nell'implementazione del protocollo TCP in Windows Server 2008 e versioni successive. La **\_ query del \_ \_ backlog di \_ invio ideale di sio** può essere usata da un'applicazione per eseguire una query sul valore ISB per una connessione.

Per informazioni più dettagliate, vedere il riferimento alla [**\_ query del \_ \_ backlog \_ di invio ideale di sio**](/previous-versions/windows/desktop/legacy/bb736549(v=vs.85)) .

[**Sio \_ La \_ \_ \_ query del backlog di invio ideale**](/previous-versions/windows/desktop/legacy/bb736549(v=vs.85)) è supportata in Windows Server 2008, Windows Vista con SP1 e versioni successive del sistema operativo.

### <a name="sio_keepalive_vals-opcode-setting-i-t3"></a>SIO \_ KeepAlive \_ Vals (impostazione opcode: I, T = = 3)

Abilita o Disabilita l'impostazione per connessione dell'opzione **Keep-Alive** TCP che specifica il timeout e l'intervallo keep-alive TCP. Per ulteriori informazioni sull'opzione Keep-Alive, vedere la sezione 4.2.3.6 in *requisiti per gli host Internet-livelli di comunicazione* specificati in RFC 1122 disponibili sul [sito Web IETF](https://www.ietf.org/rfc/rfc1122.txt). Questa risorsa può essere disponibile solo in inglese.

**Sio \_ KEEPALIVE \_ Vals** può essere usato per abilitare o disabilitare i probe Keep-Alive e impostare il timeout e l'intervallo keep-alive. Il timeout Keep-Alive specifica il timeout, in millisecondi, senza alcuna attività fino a quando non viene inviato il primo pacchetto keep-alive. L'intervallo keep-Alive specifica l'intervallo in millisecondi tra l'invio di pacchetti keep-alive successivi se non viene ricevuto alcun riconoscimento.

Per abilitare o disabilitare il keep-alive TCP in una connessione, è possibile usare l'opzione [**so \_**](so-keepalive.md) Keep-Alive, che è una delle opzioni del [ \_ socket di socket Sol](sol-socket-socket-options.md), ed eseguire una query sullo stato corrente di questa opzione. Per eseguire una query sul fatto che il keep-alive TCP sia abilitato in un socket, è possibile chiamare la funzione [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) con l'opzione **so \_ KeepAlive** . Per abilitare o disabilitare il keep-alive TCP, è possibile chiamare la funzione [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) con l'opzione [**\_ Keep**](so-keepalive.md) -Alive. Se l'opzione keep-alive TCP è abilitata con, **\_ KeepAlive**, le impostazioni TCP predefinite vengono usate per il timeout e l'intervallo keep-alive a meno che tali valori non siano stati modificati usando **sio \_ KeepAlive \_ Vals**.

Per informazioni più dettagliate, vedere la Guida di riferimento a [**sio \_ KeepAlive \_**](/previous-versions/windows/desktop/legacy/dd877220(v=vs.85)) . **Sio \_ KEEPALIVE \_ Vals** è supportato in Windows 2000 e versioni successive.

### <a name="sio_loopback_fast_path-opcode-setting-i-t3"></a>\_Percorso rapido di loopback sio \_ \_ (impostazione opcode: I, T = = 3)

Configura un socket TCP per una latenza più bassa e operazioni più veloci sull'interfaccia di loopback. Questo IOCTL richiede che lo stack TCP/IP usi un percorso veloce speciale per le operazioni di loopback in questo socket. Il [**\_ \_ \_ percorso veloce del loopback sio**](/previous-versions/windows/desktop/legacy/jj841212(v=vs.85)) può essere usato solo con i socket TCP. Questo IOCTL deve essere utilizzato su entrambi i lati della sessione di loopback. Il percorso veloce di loopback TCP è supportato tramite l'interfaccia di loopback IPv4 o IPv6. Per impostazione predefinita, il **\_ \_ \_ percorso rapido di loopback sio** è disabilitato.

Per informazioni più dettagliate, vedere il riferimento al [**\_ \_ \_ percorso rapido di loopback sio**](/previous-versions/windows/desktop/legacy/jj841212(v=vs.85)) . **Sio \_ Il \_ \_ percorso rapido di loopback** è supportato in Windows 8, Windows Server 2012 e versioni successive.

### <a name="sio_multipoint_loopback-opcode-setting-v-t1"></a>\_Loopback multipoint \_ di sio (impostazione opcode: V, T = = 1)

Controlla se i dati inviati da un'applicazione nel computer locale (non necessariamente dallo stesso socket) in una sessione multicast saranno ricevuti da un socket aggiunto al gruppo di destinazione multicast sull'interfaccia di loopback. Se il valore è **true** , i dati multicast inviati da un'applicazione nel computer locale vengono recapitati a un socket in ascolto sull'interfaccia di loopback. Il valore **false** impedisce che i dati multicast inviati da un'applicazione nel computer locale vengano recapitati a un socket in ascolto sull'interfaccia di loopback. Per impostazione predefinita, il **\_ \_ loopback di sio multipoint** è abilitato.

### <a name="sio_multicast_scope-opcode-setting-i-t1"></a>\_Ambito multicast sio \_ (impostazione opcode: I, T = = 1)

Specifica l'ambito in cui si verificheranno le trasmissioni multicast. L'ambito è definito come il numero di segmenti di rete indirizzati da coprire. Un ambito pari a zero indicherà che la trasmissione multicast non verrà distribuita in transito, ma potrebbe essere divulgata tra i socket all'interno dell'host locale. Un valore di ambito pari a uno (impostazione predefinita) indica che la trasmissione verrà posizionata in transito, ma non incrocierà alcun router. I valori di ambito più elevati determinano il numero di router che possono essere superati. Si noti che corrisponde al parametro time-to-Live (TTL) in multicast IP. Per impostazione predefinita, scope è 1.

### <a name="sio_query_rss_processor_info-opcode-setting-o-t1"></a>\_Informazioni sul \_ processore RSS della query sio \_ \_ (impostazione opcode: O, T = = 1)

Esegue una query sull'associazione tra un socket e un core del processore RSS e un nodo NUMA.

Le [**\_ informazioni sul \_ \_ processore RSS \_ della query sio**](/previous-versions/windows/desktop/legacy/jj553482(v=vs.85)) restituiscono una struttura di [**\_ \_ affinità del processore socket**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) che contiene il [**\_ numero di processore**](/windows/win32/api/winnt/ns-winnt-processor_number) e l'ID del nodo NUMA. La struttura **del \_ numero di processore** restituito contiene un numero di gruppo e un numero di processore relativo all'interno del gruppo.

Per informazioni più dettagliate, vedere le informazioni di riferimento sul [**\_ \_ \_ \_ processore RSS di query sio**](/previous-versions/windows/desktop/legacy/jj553482(v=vs.85)) . **Sio \_ Le \_ \_ \_ informazioni sul processore RSS di query** sono supportate in Windows 8, Windows Server 2012 e versioni successive.

### <a name="sio_query_rss_scalability_info-opcode-setting-o-t3"></a>\_Informazioni sulla \_ scalabilità RSS per query sio \_ \_ (impostazione opcode: O, T = = 3)

Query offload interfacce per la funzionalità Receive-Side Scaling (RSS). La struttura di argomenti restituita per le **\_ \_ \_ \_ informazioni di scalabilità RSS della query sio** è specificata nella struttura delle **\_ \_ informazioni di scalabilità RSS** definita nel file di intestazione *MSTCPIP. h* . Questa struttura viene definita nel modo seguente:

```cpp
// Scalability info for the transport
typedef struct _RSS_SCALABILITY_INFO {
   BOOLEAN RssEnabled;
} RSS_SCALABILITY_INFO, *PRSS_SCALABILITY_INFO;
```

Il valore restituito nel membro **RssEnabled** indica se RSS è abilitato in almeno un'interfaccia.

Se il buffer di output non è sufficientemente grande per la struttura delle **\_ \_ informazioni di scalabilità RSS** (il valore di *cbOutBuffer* è inferiore alla dimensione di un' **\_ \_ informazione di scalabilità RSS**) o il parametro *lpvOutBuffer* è un puntatore **null** , viene restituito un **\_ errore socket** come risultato di questo IOCTL e [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) restituisce [WSAEINVAL](windows-sockets-error-codes-2.md).

In una rete ad alta velocità in cui più CPU si trovano all'interno di un singolo sistema, la possibilità di scalare correttamente lo stack del protocollo di rete in un sistema con più CPU viene inibita perché l'architettura di NDIS 5,1 e versioni precedenti limita l'elaborazione del protocollo di ricezione a una singola CPU. Receive-Side Scaling (RSS) risolve questo problema consentendo il bilanciamento del carico di rete da una scheda di rete su più CPU.

**Sio \_ Le \_ \_ \_ informazioni sulla scalabilità RSS di query** sono supportate in Windows Vista e versioni successive.

### <a name="sio_query_transport_setting-opcode-setting-i-t3"></a>\_Impostazione del trasporto di query sio \_ \_ (impostazione opcode: I, T = = 3)

Esegue una query sulle impostazioni di trasporto in un socket. L'impostazione di trasporto sottoposta a query è basata sull' [**\_ \_ ID di impostazione del trasporto**](/windows/win32/api/transportsettingcommon/ns-transportsettingcommon-transport_setting_id) passato nel parametro *lpvInBuffer* .

L'unica impostazione del trasporto attualmente definita è per la funzionalità di **\_ notifica in tempo \_ \_ reale** in un socket TCP.

Se l' [**\_ \_ ID dell'impostazione di trasporto**](/windows/win32/api/transportsettingcommon/ns-transportsettingcommon-transport_setting_id) dispone del membro **GUID** impostato sulla **\_ \_ \_ funzionalità di notifica in tempo reale**, si tratta di una richiesta per eseguire una query sulle impostazioni di notifica in tempo reale per il socket TCP usato con [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) per ricevere notifiche di rete in background in un'app di Windows Store. Se la chiamata a [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) o [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) ha esito positivo, questo IOCTL restituisce una struttura di [**output dell'impostazione di \_ notifica in tempo \_ \_ \_ reale**](/windows/desktop/api/Mstcpip/ns-mstcpip-real_time_notification_setting_input) con lo stato corrente.

Per informazioni più dettagliate, vedere le informazioni di riferimento sull' [**\_ impostazione del \_ trasporto \_ di query sio**](/previous-versions/windows/desktop/legacy/jj553483(v=vs.85)) . **Sio \_ L' \_ \_ impostazione del trasporto query** è supportata in Windows 8, Windows Server 2012 e versioni successive.

### <a name="sio_query_wfp_ale_endpoint_handle-opcode-setting-o-t3"></a>HANDLE dell'endpoint della query SIO per la \_ query sio \_ \_ \_ \_ (impostazione opcode: O, T = = 3)

Esegue una query sull'handle dell'endpoint di Application Level Enforcement (ALE).

Windows Filtering Platform (WFP) supporta l'ispezione e la modifica del traffico di rete. In Windows Vista, Pam si concentra sugli scenari in cui il computer host è l'endpoint di comunicazione. In Windows Server 2008, tuttavia, sono presenti implementazioni del firewall perimetrali che desiderano sfruttare la piattaforma WFP per esaminare e il traffico pass-through del proxy. Il server ISA (Internet Security and Acceleration) è un esempio di tale dispositivo perimetrale.

Esistono alcuni scenari firewall che possono richiedere la possibilità di inserire un pacchetto in ingresso nel percorso di trasmissione associato a un endpoint esistente. È necessario disporre di un meccanismo per individuare l'handle dell'endpoint del livello di trasporto associato all'endpoint di destinazione. L'applicazione che ha creato l'endpoint possiede questi endpoint del livello di trasporto. Questo IOCTL viene usato per fornire handle del socket al mapping dell'handle dell'endpoint del livello di trasporto.

Se il buffer di output non è sufficientemente grande per l'handle dell'endpoint *(cbOutBuffer* è minore delle dimensioni di un **UInt64**) o il parametro *lpvOutBuffer* è un puntatore **null** , viene restituito un **\_ errore socket** come risultato di questo IOCTL e [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) restituisce [WSAEINVAL](windows-sockets-error-codes-2.md).

**Sio \_ L' \_ \_ handle dell' \_ endpoint \_ di query PAM ale** è supportato in Windows Vista e versioni successive.

### <a name="sio_query_wfp_connection_redirect_context-opcode-setting-i-t3"></a>\_ \_ \_ Contesto di reindirizzamento della connessione del WFP di query sio \_ \_ (impostazione opcode: I, T = = 3)

Esegue una query sul contesto di reindirizzamento per un record di reindirizzamento utilizzato da un servizio di reindirizzamento di Windows Filtering Platform (WFP).

L'IOCTL del [**\_ contesto di \_ \_ \_ Reindirizzamento \_ della connessione per la query sio**](/previous-versions/windows/desktop/legacy/hh859712(v=vs.85)) viene usato per fornire il rilevamento delle connessioni con proxy sulle connessioni socket reindirizzate. Questa funzionalità WFP facilita il rilevamento dei record di reindirizzamento dal reindirizzamento iniziale di una connessione alla connessione finale alla destinazione.

Per informazioni più dettagliate, vedere la pagina relativa al riferimento al [**\_ contesto di \_ \_ \_ Reindirizzamento \_ della connessione WFP della query sio**](/previous-versions/windows/desktop/legacy/hh859712(v=vs.85)) . **Sio \_ Il \_ \_ contesto di \_ Reindirizzamento \_ della connessione di query WFP** è supportato in windows 8, Windows Server 2012 e versioni successive.

### <a name="sio_query_wfp_connection_redirect_records-opcode-setting-i-t3"></a>\_ \_ I record di reindirizzamento della connessione WFP della query sio \_ \_ \_ (impostazione opcode: I, T = = 3)

Esegue una query sul record di reindirizzamento per la connessione TCP/IP accettata per l'utilizzo da parte di un servizio di reindirizzamento della piattaforma filtro Windows (WFP).

I [**\_ record di \_ \_ \_ Reindirizzamento \_ della connessione di query sio**](/previous-versions/windows/desktop/legacy/hh859713(v=vs.85)) vengono usati per fornire il rilevamento delle connessioni con proxy sulle connessioni socket reindirizzate. Questa funzionalità WFP facilita il rilevamento dei record di reindirizzamento dal reindirizzamento iniziale di una connessione alla connessione finale alla destinazione.

Per informazioni più dettagliate, vedere la pagina relativa al riferimento ai [**record di reindirizzamento della connessione del \_ WFP della query \_ \_ \_ \_ sio**](/previous-versions/windows/desktop/legacy/hh859713(v=vs.85)) . **Sio \_ I \_ \_ record di \_ Reindirizzamento \_ della connessione di query WFP** sono supportati in windows 8, Windows Server 2012 e versioni successive.

### <a name="sio_rcvall-opcode-setting-i-t3"></a>SIO \_ RCVALL (impostazione opcode: I, T = = 3)

Consente a un socket di ricevere tutti i pacchetti IPv4 o IPv6 passando throuigh un'interfaccia di rete. L'handle del socket passato alla funzione [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) deve essere uno dei seguenti:

-   Un socket IPv4 creato con la famiglia di indirizzi impostata su AF \_ inet, il tipo di socket impostato su Sock \_ RAW e il protocollo impostato su IPPROTO \_ IP.
-   Socket IPv6 creato con la famiglia di indirizzi impostata su AF \_ INET6, il tipo di socket impostato su Sock \_ RAW e il protocollo impostato su IPPROTO \_ IPv6.

Il socket deve anche essere associato a un'interfaccia IPv4 o IPv6 locale esplicita, il che significa che non è possibile eseguire l'associazione a **inaddr \_ any** o **in6addr \_ any**.

In Windows Server 2008 e versioni precedenti, l'impostazione IOCTL [**\_ RCVALL di sio**](/previous-versions/windows/desktop/legacy/ee309610(v=vs.85)) non acquisisce i pacchetti locali inviati da un'interfaccia di rete. Sono stati inclusi i pacchetti ricevuti su un'altra interfaccia ed è stata inoltrata l'interfaccia di rete specificata per l'IOCTL **\_ RCVALL sio** .

In Windows 7 e Windows Server 2008 R2 questa operazione è stata modificata in modo da acquisire anche i pacchetti locali inviati da un'interfaccia di rete. Sono inclusi i pacchetti ricevuti su un'altra interfaccia e quindi l'interfaccia di rete associata al socket con IOCTL [**\_ RCVALL di sio**](/previous-versions/windows/desktop/legacy/ee309610(v=vs.85)) .

Per impostare questo IOCTL è necessario disporre dei privilegi di amministratore nel computer locale.

Questa funzionalità viene talvolta definita modalità promiscua.

I valori possibili per l'opzione IOCTL **\_ RCVALL di sio** sono specificati nell'enumerazione del **\_ valore RCVALL** definito nel file di intestazione *MSTCPIP. h* . I valori possibili per SIO \_ RCVALL sono i seguenti:

| Termine                                                                                                                 | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-|-|
| <span id="RCVALL_OFF"></span><span id="rcvall_off"></span>RCVALL \_ disattivato<br/>                                     | Disabilitare questa opzione in modo che un socket non riceva tutti i pacchetti IPv4 o IPv6 sulla rete. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="RCVALL_ON"></span><span id="rcvall_on"></span>RCVALL \_<br/>                                        | Abilitare questa opzione per consentire a un socket di ricevere tutti i pacchetti IPv4 o IPv6 sulla rete. Questa opzione Abilita la modalità promiscua sulla scheda di interfaccia di rete (NIC) se la scheda di interfaccia di rete supporta la modalità promiscua. In un segmento LAN con un hub di rete, una scheda di interfaccia di rete che supporta la modalità promiscua acquisisce tutto il traffico IPv4 o IPv6 sulla LAN, incluso il traffico tra altri computer nello stesso segmento LAN. Tutti i pacchetti acquisiti (IPv4 o IPv6, a seconda del socket) verranno recapitati al socket non elaborato. <br/> Questa opzione non consente di acquisire altri pacchetti (ad esempio, i pacchetti ARP, IPX e NetBEUI) nell'interfaccia.<br/> Netmon usa la stessa modalità per l'interfaccia di rete, ma non usa questa opzione per acquisire il traffico.<br/> |
| <span id="RCVALL_SOCKETLEVELONLY"></span><span id="rcvall_socketlevelonly"></span>\_SOCKETLEVELONLY RCVALL<br/> | Questa funzionalità non è attualmente implementata, pertanto l'impostazione di questa opzione non ha alcun effetto.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="RCVALL_IPLEVEL"></span><span id="rcvall_iplevel"></span>\_IPLEVEL RCVALL<br/>                         | Abilitare questa opzione in modo che un socket IPv4 o IPv6 riceva tutti i pacchetti a livello di IP sulla rete. Questa opzione non Abilita la modalità promiscua nella scheda di interfaccia di rete. Questa opzione influiscono solo sull'elaborazione dei pacchetti a livello IP. La scheda di interfaccia di rete riceve ancora solo i pacchetti indirizzati agli indirizzi unicast e multicast configurati. Tuttavia, un socket con questa opzione abilitata riceverà non solo i pacchetti diretti a indirizzi IP specifici, ma riceverà tutti i pacchetti IPv4 o IPv6 ricevuti dalla scheda di interfaccia di rete.<br/> Questa opzione non consente di acquisire altri pacchetti (ad esempio, i pacchetti ARP, IPX e NetBEUI) ricevuti sull'interfaccia.<br/>                                                                                             |



 

Per informazioni più dettagliate, vedere la Guida di riferimento per [**sio \_ RCVALL**](/previous-versions/windows/desktop/legacy/ee309610(v=vs.85)) .

**Sio \_ RCVALL** è supportato in Windows 2000 e versioni successive.

### <a name="sio_rcvall_igmpmcast-opcode-setting-i-t3"></a>SIO \_ RCVALL \_ IGMPMCAST (impostazione opcode: I, T = = 3)

Consente a un socket di ricevere tutto il traffico IP multicast IGMP sulla rete, senza ricevere altro traffico IP multicast. L'handle del socket passato alla funzione [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) deve essere una \_ famiglia di indirizzi AF inet, un tipo di \_ socket raw Sock e un \_ protocollo IGMP IPPROTO. Il socket deve anche essere associato a un'interfaccia locale esplicita, il che significa che non è possibile eseguire l'associazione a inaddr \_ any.

Una volta associato il socket e il set IOCTL, le chiamate alle funzioni [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) o [**ricezione**](/windows/desktop/api/winsock/nf-winsock-recv) restituiscono i datagrammi IP multicast che passano attraverso l'interfaccia specificata. Si noti che è necessario fornire un buffer sufficientemente grande. Per impostare questo IOCTL è necessario disporre dei privilegi di amministratore nel computer locale.

**Sio \_ RCVALL \_ IGMPMCAST** è supportato in Windows 2000 e versioni successive.

### <a name="sio_rcvall_mcast-opcode-setting-i-t3"></a>SIO \_ RCVALL \_ mcast (impostazione opcode: I, T = = 3)

Consente a un socket di ricevere tutto il traffico IP multicast sulla rete, ovvero tutti i pacchetti IP destinati agli indirizzi IP nell'intervallo tra 224.0.0.0 e 239.255.255.255. L'handle del socket passato alla funzione [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) deve essere una \_ famiglia di indirizzi AF inet, un tipo di \_ socket raw Sock e un \_ protocollo UDP IPPROTO. Il socket deve anche essere associato a un'interfaccia locale esplicita, il che significa che non è possibile eseguire l'associazione a inaddr \_ any. Il socket deve essere associato alla porta zero.

Una volta associato il socket e il set IOCTL, le chiamate alle funzioni [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) o [**ricezione**](/windows/desktop/api/winsock/nf-winsock-recv) restituiscono i datagrammi IP multicast che passano attraverso l'interfaccia specificata. Si noti che è necessario fornire un buffer sufficientemente grande. Per impostare questo IOCTL è necessario disporre dei privilegi di amministratore nel computer locale.

**Sio \_ RCVALL \_ mcast** è supportato in Windows 2000 e versioni successive.

### <a name="sio_release_port_reservation-opcode-setting-i-t3"></a>\_Prenotazione della porta di rilascio sio \_ \_ (impostazione opcode: I, T = = 3)

Rilascia una prenotazione di runtime per un blocco di porte TCP o UDP. È necessario che la prenotazione di runtime da rilasciare sia stata ottenuta dal processo di emissione usando il comando di [**\_ prenotazione della \_ porta \_ sio Acquire**](/previous-versions/windows/desktop/legacy/gg699720(v=vs.85)) .

Per informazioni più dettagliate, vedere le informazioni di riferimento sulla [**\_ prenotazione della \_ porta \_ di versione sio**](/previous-versions/windows/desktop/legacy/gg699722(v=vs.85)) .

[**Sio \_ La \_ \_ prenotazione della porta di rilascio**](/previous-versions/windows/desktop/legacy/gg699722(v=vs.85)) è supportata in Windows Vista e nelle versioni successive del sistema operativo.

### <a name="sio_routing_interface_change-opcode-setting-i-t1"></a>\_Modifica dell' \_ interfaccia di routing sio \_ (impostazione opcode: I, T = = 1)

Per ricevere la notifica di una modifica dell'interfaccia di routing da usare per raggiungere l'indirizzo remoto nel buffer di input (specificato come struttura [**sockaddr**](sockaddr-2.md) ). Al completamento di questo IOCTL non verranno fornite informazioni di output sulla nuova interfaccia di routing; il completamento indica semplicemente che l'interfaccia di routing per una determinata destinazione è cambiata e deve essere sottoposta a query utilizzando l' **\_ interfaccia di routing sio \_ \_ query** IOCTL.

Si presuppone, sebbene non sia necessario, che l'applicazione utilizzi l'I/O sovrapposto per ricevere una notifica della modifica dell'interfaccia di routing tramite il completamento della richiesta di **\_ modifica dell' \_ interfaccia \_ di routing sio** . In alternativa, se la **\_ modifica dell' \_ interfaccia \_ di routing sio** viene eseguita su un socket non bloccante con i parametri *lpOverlapped* e *il lpCompletionRoutine* impostati su **null**, viene completata immediatamente la restituzione e la [WSAEWOULDBLOCK](windows-sockets-error-codes-2.md) come errore e l'applicazione può quindi attendere il routing degli eventi di modifica tramite la chiamata a [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) o [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) con il bit di modifica dell'interfaccia di \_ routing FD \_ \_ impostato nella maschera di bit dell'evento di rete.

È stato rilevato che le informazioni di routing rimangono stabili nella maggior parte dei casi, in modo che la richiesta all'applicazione di mantenere più IOCTL in attesa per ricevere notifiche relative a tutte le destinazioni a cui è interessato e che il provider di servizi tenga traccia delle richieste di notifica utilizzerà una quantità significativa di risorse di sistema. Questa situazione può essere evitata estendendo il significato dei parametri di input e rilassando i requisiti del provider di servizi, come indicato di seguito:

-   L'applicazione può specificare un indirizzo jolly specifico per la famiglia di protocolli (uguale a quello usato nella chiamata di [**Binding**](/windows/desktop/api/winsock/nf-winsock-bind) quando viene richiesta l'associazione a qualsiasi indirizzo disponibile) per richiedere notifiche di eventuali modifiche del routing. Ciò consente all'applicazione di mantenerne solo una modifica in attesa di un' **\_ interfaccia di routing \_ \_ sio** per tutti i socket e le destinazioni che possiede, quindi usa la **query dell' \_ \_ interfaccia \_ di routing sio** per ottenere le informazioni di routing effettive.
-   Un provider di servizi ha la possibilità di ignorare le informazioni specificate dall'applicazione nel buffer di input della **modifica dell' \_ \_ interfaccia di \_ routing sio** (come se l'applicazione avesse specificato un indirizzo con caratteri jolly) e di completare l'evento di modifica dell'interfaccia di **\_ routing \_ \_ sio** o Signal FD \_ routing \_ Interface \_ Change in caso di modifica delle informazioni di routing (non solo la route alla destinazione specificata nel buffer di input).

### <a name="sio_routing_interface_query-opcode-setting-i-o-t1"></a>\_Query di interfaccia di routing sio \_ \_ (impostazione opcode: I, O, T = = 1)

Per ottenere l'indirizzo dell'interfaccia locale (rappresentato come struttura [**sockaddr**](sockaddr-2.md) ) da utilizzare per l'invio all'indirizzo remoto specificato nel buffer di input (come **sockaddr**). Gli indirizzi multicast remoti possono essere inviati nel buffer di input per ottenere l'indirizzo dell'interfaccia preferita per la trasmissione multicast. In ogni caso, l'indirizzo di interfaccia restituito può essere usato dall'applicazione in una richiesta BIND () successiva.

Si noti che le route sono soggette a modifiche. Pertanto, le applicazioni non possono basarsi sulle informazioni restituite dalla **\_ query dell' \_ interfaccia \_ di routing sio** per essere persistenti. Le applicazioni possono registrarsi per il routing delle notifiche di modifica tramite l' **\_ interfaccia di routing sio \_ \_ Change** IOCTL che fornisce la notifica tramite i/o sovrapposto o un \_ evento di modifica dell'interfaccia di routing FD \_ \_ . La sequenza di azioni seguente può essere utilizzata per garantire che l'applicazione disponga sempre di informazioni sull'interfaccia di routing correnti per una determinata destinazione:

-   Rilascia **l' \_ interfaccia di routing sio \_ \_ modificare** IOCTL
-   Invia **\_ query sull' \_ interfaccia \_ di routing sio**
-   Ogni volta che la **\_ modifica dell' \_ interfaccia \_ di routing sio** invia una notifica all'applicazione della modifica del routing (tramite i/o sovrapposti o segnalando \_ \_ un evento di modifica dell'interfaccia di routing FD \_ ), l'intera sequenza di azioni deve essere ripetuta.

Se il buffer di output non è sufficientemente grande da contenere l'indirizzo di interfaccia, \_ viene restituito un errore socket come risultato di questo IOCTL e [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) restituisce [WSAEFAULT](windows-sockets-error-codes-2.md). In questo caso, la dimensione richiesta del buffer di output verrà restituita in *lpcbBytesReturned* . Si noti che il codice di errore WSAEFAULT viene restituito anche se il parametro *lpvInBuffer*, *lpvOutBuffer* o *lpcbBytesReturned* non è interamente contenuto in una parte valida dello spazio degli indirizzi utente.

Se non è possibile raggiungere l'indirizzo di destinazione specificato nel buffer di input tramite una delle interfacce disponibili, \_ viene restituito un errore socket come risultato di questo IOCTL e [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) restituisce [WSAENETUNREACH](windows-sockets-error-codes-2.md) o anche [WSAENETDOWN](windows-sockets-error-codes-2.md) se tutta la connettività di rete va persa.

### <a name="sio_set_compatibility_mode-opcode-setting-i-t3"></a>\_Modalità di \_ compatibilità set sio \_ (impostazione opcode: I, T = = 3)

Richiede il modo in cui lo stack di rete deve gestire determinati comportamenti per i quali la modalità predefinita di gestione del comportamento può essere diversa nelle versioni di Windows. La struttura degli argomenti per la **\_ \_ \_ modalità di compatibilità set sio** è specificata nella struttura della **\_ \_ modalità di compatibilità WSA** definita nel file di intestazione *Mswsockdef. h* . Questa struttura viene definita nel modo seguente:

```cpp
/* Argument structure for SIO_SET_COMPATIBILITY_MODE */
typedef struct _WSA_COMPATIBILITY_MODE {
    WSA_COMPATIBILITY_BEHAVIOR_ID BehaviorId;
    ULONG TargetOsVersion;
} WSA_COMPATIBILITY_MODE, *PWSA_COMPATIBILITY_MODE;
```

Il valore specificato nel membro **BehaviorId** indica il comportamento richiesto. Il valore specificato nel membro **TargetOSVersion** indica la versione di Windows richiesta per il comportamento.

Il membro **BehaviorId** può essere uno dei valori del tipo di **enumerazione \_ \_ \_ ID del comportamento di compatibilità WSA** definito nel file di intestazione *Mswsockdef. h* . I valori possibili per il membro **BehaviorId** sono i seguenti.

| Termine                                                                                                                                                                             | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-|-|
| <span id="WsaBehaviorAll"></span><span id="wsabehaviorall"></span><span id="WSABEHAVIORALL"></span>WsaBehaviorAll<br/>                                                     | Questa operazione equivale a richiedere tutti i possibili comportamenti compatibili definiti per l'ID del **\_ comportamento di \_ \_ compatibilità WSA**.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="WsaBehaviorReceiveBuffering"></span><span id="wsabehaviorreceivebuffering"></span><span id="WSABEHAVIORRECEIVEBUFFERING"></span>WsaBehaviorReceiveBuffering<br/> | Quando il membro **TargetOSVersion** è impostato su un valore per Windows Vista o versione successiva, le riduzioni delle dimensioni del buffer di ricezione TCP in questo socket con l'opzione socket **\_ RCVBUF** sono consentite anche dopo la creazione di una connessione TCP. <br/> Quando il membro **TargetOSVersion** è impostato su un valore precedente a Windows Vista, le riduzioni delle dimensioni del buffer di ricezione TCP in questo socket con l'opzione socket **\_ RCVBUF** non sono consentite dopo lo stabilimento della connessione. <br/>                                                                                                                                                                                  |
| <span id="WsaBehaviorAutoTuning"></span><span id="wsabehaviorautotuning"></span><span id="WSABEHAVIORAUTOTUNING"></span>WsaBehaviorAutoTuning<br/>                         | Quando il membro **TargetOSVersion** è impostato su un valore per Windows Vista o versione successiva, l'ottimizzazione automatica della finestra di ricezione è abilitata e il fattore di scala della finestra TCP viene ridotto a 2 rispetto al valore predefinito di 8.<br/> Quando **TargetOSVersion** è impostato su un valore precedente a Windows Vista, l'ottimizzazione automatica della finestra di ricezione è disabilitata. Anche l'opzione di scalabilità della finestra TCP è disabilitata e le dimensioni massime della finestra di ricezione true sono limitate a 65.535 byte. Non è possibile negoziare l'opzione di scalabilità della finestra TCP sulla connessione anche se per questo socket è stata chiamata l'opzione **\_ RCVBUF** socket, che specifica un valore maggiore di 65.535 byte prima che sia stata stabilita la connessione.<br/> |



 

Per informazioni più dettagliate, vedere il riferimento alla [**\_ \_ \_ modalità di compatibilità set sio**](/previous-versions/windows/desktop/legacy/cc136103(v=vs.85)) .

**Sio \_ La \_ \_ modalità di compatibilità set** è supportata in Windows Vista e versioni successive.

### <a name="sio_set_group_qos-opcode-setting-i-t1"></a>\_ \_ QoS gruppo set sio \_ (impostazione opcode: I, T = = 1)

Riservato.

### <a name="sio_set_priority_hint-opcode-setting-i-t3"></a>SIO_SET_PRIORITY_HINT (impostazione opcode: I, T = = 3)

Fornisce un suggerimento al protocollo di trasporto sottostante per trattare il traffico su questo socket con una priorità specifica. *LpvInBuffer* deve puntare a una variabile di tipo **PRIORITY_HINT** con *cbInBuffer* impostato su sizeof (PRIORITY_HINT). I parametri *lpvOutBuffer* e *cbOutBuffer* devono essere rispettivamente **null** e 0. L'implementazione TCP di Microsoft Windows supporta questo IOCTL a partire da Windows 10, versione 1809 (10,0; Build 17763) e versioni successive come indicato di seguito: quando il valore di priorità richiesto è impostato su **IoPriorityHintVeryLow**, TCP usa una versione modificata dell'algoritmo LEDBAT (definito in RFC 6817) per controllare la velocità del traffico in uscita sul socket. Il traffico in ingresso non è influenzato da questo IOCTL. LEDBAT è un algoritmo di scavenging e il suo obiettivo è quello di ridurre la latenza e prevenire qualsiasi effetto negativo sul traffico con priorità normale uscendo dal modo in cui è presente il traffico con priorità normale.

Vedere anche [RFC 6817](https://tools.ietf.org/html/rfc6817).

**SIO_SET_PRIORITY_HINT** è supportato in Windows 10, versione 1809 (10,0; Build 17763) e versioni successive.

### <a name="sio_set_qos-opcode-setting-i-t1"></a>\_QoS set sio \_ (impostazione opcode: I, T = = 1)

Associare la struttura [**QoS**](/windows/win32/api/winsock2/ns-winsock2-qos) specificata al socket. Non è necessario alcun buffer di output, la struttura **QoS** sarà ottenuta dal buffer di input. Il codice di errore [WSAENOPROTOOPT](windows-sockets-error-codes-2.md) è indicato per i provider di servizi che non supportano la qualità del servizio.

### <a name="sio_tcp_initial_rto-opcode-setting-i-t3"></a>SIO_TCP_INITIAL_RTO (impostazione opcode: I, T = = 3)

Controlla le caratteristiche di ritrasmissione iniziali (SYN/SYN + ACK) di un socket TCP configurando i parametri del timeout di ritrasmissione iniziale (RTO). I parametri di configurazione sono specificati in una struttura di [**\_ \_ \_ parametri RTO iniziali TCP**](/windows/desktop/api/mswsock/ns-mswsock-transmit_file_buffers) .

Per informazioni più dettagliate, vedere il riferimento [**SIO_TCP_INITIAL_RTO**](./sio-tcp-initial-rto.md) . [**SIO_TCP_INITIAL_RTO**](./sio-tcp-initial-rto.md) è supportato in Windows 8, windows Server 2012 e versioni successive.

### <a name="sio_translate_handle-opcode-setting-i-o-t1"></a>\_ \_ Handle di conversione SIO (impostazione opcode: I, O, T = = 1)

Per ottenere un handle corrispondente per i *socket che* è valido nel contesto di un'interfaccia complementare, ad esempio \_ netdev e \_ TAPI. Una costante manifesto che identifica l'interfaccia complementare insieme a tutti gli altri parametri necessari viene specificata nel buffer di input. Il punto di controllo corrispondente sarà disponibile nel buffer di output al completamento della funzione. Per informazioni dettagliate specifiche su una particolare interfaccia complementare, vedere la sezione appropriata negli [allegati di Winsock](winsock-annexes.md) . Il codice di errore [WSAENOPROTOOPT](windows-sockets-error-codes-2.md) è indicato per i provider di servizi che non supportano questo IOCTL per l'interfaccia complementare specificata. Questo IOCTL recupera l'handle associato usando **l' \_ \_ handle di conversione sio**.

È consigliabile utilizzare il Component Object Model (COM) invece di questo IOCTL per individuare e rilevare altre interfacce che potrebbero essere supportate da un socket. Questo IOCTL è presente per la compatibilità con le versioni precedenti dei sistemi in cui COM non è disponibile o non può essere usato per altri motivi.

### <a name="sio_udp_connreset-opcode-setting-i-t3"></a>\_CONNRESET UDP sio \_ (impostazione opcode: I, T = = 3)

**Windows XP:** Controlla se i messaggi di porta UDP non \_ raggiungibili vengono segnalati. Impostare su **true** per abilitare la creazione di report. Impostare su **false** per disabilitare la creazione di report.

### <a name="sio_set_wfp_connection_redirect_records-opcode-setting-i-t3"></a>SIO \_ imposta \_ i \_ record di reindirizzamento della connessione WFP \_ \_ (impostazione opcode: I, T = = 3)

Imposta il record di reindirizzamento sul nuovo socket TCP usato per la connessione alla destinazione finale per l'uso da parte di un servizio di reindirizzamento della piattaforma filtro Windows (WFP).

Il [**\_ set di \_ dati di \_ \_ Reindirizzamento \_ della connessione di sio set WFP**](/previous-versions/windows/desktop/legacy/hh859714(v=vs.85)) viene usato come parte del rilevamento delle connessioni con proxy per le connessioni socket reindirizzate. Questa funzionalità WFP facilita il rilevamento dei record di reindirizzamento dal reindirizzamento iniziale di una connessione alla connessione finale alla destinazione.

Per informazioni più dettagliate, vedere il riferimento per i [**record di reindirizzamento della connessione di sio \_ set \_ WFP \_ \_ \_**](/previous-versions/windows/desktop/legacy/hh859714(v=vs.85)) . **Sio \_ IMPOSTARE \_ i \_ \_ \_ record di reindirizzamento della connessione WFP** è supportato in windows 8, Windows Server 2012 e versioni successive.

### <a name="sio_tcp_info-opcode-setting-i-o-t3"></a>\_Informazioni TCP sio \_ (impostazione opcode: I, O, T = = 3)

Recupera le statistiche TCP per un socket. Le statistiche TCP sono disponibili in una struttura [**TCP \_ info \_ V0**](/windows/desktop/api/Mstcpip/ns-mstcpip-tcp_info_v0) .

A differenza del recupero delle statistiche TCP con la funzione [**GetPerTcpConnectionEStats**](/windows/win32/api/iphlpapi/nf-iphlpapi-getpertcpconnectionestats) , il recupero delle statistiche TCP con questo codice di controllo non richiede il caricamento, l'archiviazione e il filtro della tabella di connessione TCP da parte del codice utente e non richiede privilegi elevati per l'utilizzo di.

Per altre informazioni, vedere [**sio \_ TCP \_ info**](/previous-versions/windows/desktop/legacy/mt823415(v=vs.85)). **Sio \_ Le \_ informazioni TCP** sono supportate in Windows 10, versione 1703, windows server 2016 e versioni successive.

## <a name="remarks"></a>Commenti

Le IOCTL Winsock sono definite in una serie di diversi file di intestazione. Sono inclusi il file di intestazione *Winsock2. h*, *mswsock. h* e *MSTCPIP. h* .

In Microsoft Windows Software Development Kit (SDK) rilasciata per Windows Vista e versioni successive, l'organizzazione dei file di intestazione è stata modificata e in *Ws2def.* h, *Ws2ipdef. h* e *Mswsockdef.* h i file di intestazione. h, viene definito anche un numero di IOCTL Winsock. Il file di intestazione *Ws2def. h* viene incluso automaticamente nel file di intestazione *Winsock2. h* . Il file di intestazione *Ws2ipdef. h* viene incluso automaticamente nel file di intestazione *Ws2tcpip. h* . Il file di intestazione *Mswsockdef. h* viene incluso automaticamente nel file di intestazione *Mswsockdef. h* .

## <a name="requirements"></a>Requisiti

|||
|-|-|
| Intestazione<br/> | <dl> <dt>Winsock2. h; </dt> <dt>MSTCPIP. h; </dt> <dt>Mswsock. h; </dt> <dt>Mswsockdef. h in Windows Vista, Windows Server 2008 e Windows 7 (includere mswsock. h); </dt> <dt>Ws2def. h in Windows Vista, Windows Server 2008 e Windows 7 (includere Winsock2. h); </dt> <dt>Ws2ipdef. h in Windows Vista, Windows Server 2008 e Windows 7 (includere Ws2tcpip. h)</dt> </dl> |
