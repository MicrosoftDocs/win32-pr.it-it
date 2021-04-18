---
description: Nella tabella seguente sono riepilogate alcune delle opzioni del socket per Windows Sockets 2.
ms.assetid: 6731d27c-fb7d-421a-badf-0cad6a4712ea
title: Opzioni socket e IOCTL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 472d37bd8d2d97eead66d7c9d2319e57fc5dafde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315766"
---
# <a name="socket-options-and-ioctls"></a>Opzioni socket e IOCTL

Nella tabella seguente sono riepilogate alcune delle opzioni del socket per Windows Sockets 2. Informazioni più dettagliate sono disponibili nella sezione 4 in [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85)) e/o [**WSPSetSockOpt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)). Sono disponibili altre nuove opzioni di socket specifiche del protocollo, che è possibile trovare nell'allegato Protocol-Specific. Un elenco completo delle [**Opzioni di socket**](socket-options.md) per Windows Sockets è disponibile nella Guida di riferimento a Winsock.

Per un riepilogo di alcune delle IOCTL di Winsock, vedere [Riepilogo dei codici operativi IOCTL del socket](summary-of-socket-ioctl-opcodes-2.md). Un elenco completo di [**IOCTL Winsock**](winsock-ioctls.md) è disponibile nella Guida di riferimento a Winsock.

## <a name="summary-of-common-socket-options"></a>Riepilogo delle opzioni dei socket comuni

Un provider di servizi Winsock deve riconoscere tutte queste opzioni e (per [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85))) restituire valori plausibili per ogni. Il valore predefinito per ogni opzione è illustrato nella tabella seguente.

Valore

Type

Significato

Predefinito

Nota

<span id="SO_ACCEPTCONN"></span><span id="so_acceptconn"></span>\_ACCEPTCONN

BOOL

Il socket è in ascolto.

FALSE a meno che non sia stato eseguito un [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85)) .

<span id="SO_BROADCAST"></span><span id="so_broadcast"></span>\_trasmissione

BOOL

Il socket è configurato per la trasmissione e la ricezione di messaggi broadcast.

FALSE

<span id="SO_DEBUG"></span><span id="so_debug"></span>\_debug

BOOL

Il debug è abilitato.

FALSE

i

<span id="SO_DONTLINGER"></span><span id="so_dontlinger"></span>\_DONTLINGER

BOOL

Se true, l' \_ opzione so Linger è disabilitata.

true

<span id="SO_DONTROUTE"></span><span id="so_dontroute"></span>\_DONTROUTE

BOOL

Il routing è disabilitato. Ha esito positivo, ma viene ignorato nei \_ socket inet AF; non riesce nei \_ socket INET6 AF con [WSAENOPROTOOPT](windows-sockets-error-codes-2.md). Non supportato nei socket ATM (genera un errore).

FALSE

i

<span id="SO_ERROR"></span><span id="so_error"></span>\_errore

INT

Recupera lo stato di errore e Cancella.

0

<span id="SO_GROUP_ID"></span><span id="so_group_id"></span>\_ID gruppo \_

GROUP

Riservato.

NULL

Solo Get

<span id="SO_GROUP_PRIORITY"></span><span id="so_group_priority"></span>QUINDI \_ , \_ Priorità gruppo

INT

Riservato.

0

[**QUINDI \_ KeepAlive**](so-keepalive.md)

BOOL

È in corso l'invio di KeepAlive. Non supportato nei socket ATM (genera un errore).

FALSE

i

<span id="SO_LINGER"></span><span id="so_linger"></span>QUINDI, \_ indugio

Struttura Linger

Restituisce le opzioni Linger correnti.

l \_ OnOff è 0

<span id="SO_MAX_MSG_SIZE"></span><span id="so_max_msg_size"></span>\_dimensioni massime \_ messaggio \_

INT

Dimensioni massime in uscita di un messaggio per i tipi di socket del messaggio. Non è previsto alcun provisioning per determinare la dimensione massima del messaggio in ingresso. Non ha significato per i socket orientati al flusso.

Dipendente dall'implementazione

Solo Get

<span id="SO_OOBINLINE"></span><span id="so_oobinline"></span>\_OOBINLINE

BOOL

I dati di OOB vengono ricevuti nel flusso di dati normale.

FALSE

<span id="SO_PROTOCOL_INFOW"></span><span id="so_protocol_infow"></span>\_protocollo \_ INFOW

[ **\_ informazioni WSAPROTOCOL** struttura](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)

Descrizione delle informazioni sul protocollo associate al socket.

Dipendente dal protocollo

Solo Get

<span id="SO_RCVBUF"></span><span id="so_rcvbuf"></span>\_RCVBUF

INT

Spazio totale del buffer per socket riservato per le ricevute. Questa operazione non è correlata \_ alla \_ \_ dimensione massima dei messaggi e non corrisponde necessariamente alle dimensioni della finestra di ricezione TCP.

Dipendente dall'implementazione

i

<span id="SO_REUSEADDR"></span><span id="so_reuseaddr"></span>\_REUSEADDR

BOOL

L'indirizzo a cui è associato il socket può essere usato da altri utenti. Non applicabile nei socket ATM.

FALSE

<span id="SO_SNDBUF"></span><span id="so_sndbuf"></span>\_sndbuf

INT

Spazio totale del buffer per socket riservato per gli invii. Questa operazione non è correlata \_ alla \_ \_ dimensione massima dei messaggi e non corrisponde necessariamente alle dimensioni di una finestra di trasmissione TCP.

Dipendente dall'implementazione

i

<span id="SO_TYPE"></span><span id="so_type"></span>QUINDI, \_ digitare

INT

Tipo di socket (ad esempio, il flusso di SOCK \_ ).

Creato tramite socket.

<span id="PVD_CONFIG"></span><span id="pvd_config"></span>configurazione di PVD \_

caratteri lontani \*

Oggetto struttura di dati opaco contenente le informazioni di configurazione del provider di servizi.

Dipendente dall'implementazione

<span id="TCP_NODELAY"></span><span id="tcp_nodelay"></span>NoDelay TCP \_

BOOL

Disabilita l'algoritmo Nagle di unione dei pacchetti in invio.

Dipendente dall'implementazione

(i) un provider di servizi può ignorare l'opzione in modo invisibile all'utente in [**WSPSetSockOpt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)) e restituire un valore costante per [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85)), oppure può accettare un valore per **WSPSetSockOpt** e restituire il valore corrispondente in **WSPGetSockOpt** senza usare il valore in alcun modo.



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Opzioni socket**](socket-options.md)
</dt> <dt>

[**\_Opzioni Socket socket Sol**](sol-socket-socket-options.md)
</dt> <dt>

[**\_Opzioni socket TCP IPPROTO**](ipproto-tcp-socket-options.md)
</dt> <dt>

[**\_Opzioni socket UDP IPPROTO**](ipproto-udp-socket-options.md)
</dt> <dt>

[**IOCTL Winsock**](winsock-ioctls.md)
</dt> </dl>

 

 
