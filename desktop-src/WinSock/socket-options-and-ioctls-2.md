---
description: Nella tabella seguente sono riepilogate Windows socket 2.
ms.assetid: 6731d27c-fb7d-421a-badf-0cad6a4712ea
title: Opzioni socket e IOCTL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 020495cca9f0c4ec412f0a4d3dd29ae7235e22e52f4beda4372cf9fb50409ece
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993411"
---
# <a name="socket-options-and-ioctls"></a>Opzioni socket e IOCTL

Nella tabella seguente sono riepilogate Windows socket 2. Informazioni più dettagliate sono disponibili nella sezione 4 in [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85)) e/o [**WSPSetSockOpt.**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)) Sono disponibili altre nuove opzioni socket specifiche del protocollo, disponibili nell'Protocol-Specific Annex. Un elenco completo delle [**opzioni socket**](socket-options.md) per Windows socket è disponibile nelle informazioni di riferimento su Winsock.

Per un riepilogo di alcuni ioctls di Winsock, vedere [Summary of Socket Ioctl Opcodes (Riepilogo degli opcode Ioctl socket).](summary-of-socket-ioctl-opcodes-2.md) Un elenco completo degli [**IOCL di Winsock**](winsock-ioctls.md) è disponibile nelle informazioni di riferimento su Winsock.

## <a name="summary-of-common-socket-options"></a>Riepilogo delle opzioni socket comuni

Un provider di servizi Winsock deve riconoscere tutte queste opzioni e (per [**WSPGetSockOpt)**](/previous-versions/windows/hardware/network/ff566292(v=vs.85))restituisce valori plausibili per ognuna. Il valore predefinito per ogni opzione è illustrato nella tabella seguente.

Valore

Type

Significato

Predefinito

Nota

<span id="SO_ACCEPTCONN"></span><span id="so_acceptconn"></span>SO \_ ACCEPTCONN

BOOL

Il socket è in ascolto.

FALSE a meno che non sia stato eseguito un [**WSPListen.**](/previous-versions/windows/hardware/network/ff566297(v=vs.85))

<span id="SO_BROADCAST"></span><span id="so_broadcast"></span>SO \_ BROADCAST

BOOL

Il socket è configurato per la trasmissione e la ricezione di messaggi trasmessi.

FALSE

<span id="SO_DEBUG"></span><span id="so_debug"></span>QUINDI \_ DEBUG

BOOL

Il debug è abilitato.

FALSE

(i)

<span id="SO_DONTLINGER"></span><span id="so_dontlinger"></span>QUINDI \_ DONTLINGER

BOOL

Se true, l'opzione SO \_ LINGER è disabilitata.

true

<span id="SO_DONTROUTE"></span><span id="so_dontroute"></span>QUINDI \_ DONTROUTE

BOOL

Il routing è disabilitato. Ha esito positivo ma viene ignorato nei socket INET di Af; ha esito negativo nei \_ \_ socket AF INET6 [con WSAENOPROTOOPT.](windows-sockets-error-codes-2.md) Non supportato nei socket ATM (si verifica un errore).

FALSE

(i)

<span id="SO_ERROR"></span><span id="so_error"></span>SO \_ ERROR

int

Recupera lo stato dell'errore e cancella.

0

<span id="SO_GROUP_ID"></span><span id="so_group_id"></span>SO \_ GROUP \_ ID

GROUP

Riservato.

NULL

Ottieni solo

<span id="SO_GROUP_PRIORITY"></span><span id="so_group_priority"></span>SO \_ GROUP \_ PRIORITY

int

Riservato.

0

[**SO \_ KEEPALIVE**](so-keepalive.md)

BOOL

I keep-alias vengono inviati. Non supportato nei socket ATM (si verifica un errore).

FALSE

(i)

<span id="SO_LINGER"></span><span id="so_linger"></span>SO \_ LINGER

Residuo della struttura

Restituisce le opzioni residue correnti.

l \_ onoff è 0

<span id="SO_MAX_MSG_SIZE"></span><span id="so_max_msg_size"></span>DIMENSIONI \_ \_ MASSIME \_ MSG

int

Dimensione massima in uscita di un messaggio per i tipi di socket dei messaggi. Non è disponibile alcun provisioning per determinare le dimensioni massime dei messaggi in ingresso. Non ha alcun significato per i socket orientati al flusso.

Dipendente dall'implementazione

Ottieni solo

<span id="SO_OOBINLINE"></span><span id="so_oobinline"></span>SO \_ OOBINLINE

BOOL

I dati OOB vengono ricevuti nel flusso di dati normale.

FALSE

<span id="SO_PROTOCOL_INFOW"></span><span id="so_protocol_infow"></span>SO \_ PROTOCOL \_ INFOW

struttura [ **WSAPROTOCOL \_ INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)

Descrizione delle informazioni sul protocollo associato a questo socket.

Dipendente dal protocollo

Ottieni solo

<span id="SO_RCVBUF"></span><span id="so_rcvbuf"></span>SO \_ RCVBUF

int

Spazio totale del buffer per socket riservato per le ricevute. Ciò non è correlato a SO MAX MSG SIZE e non corrisponde necessariamente alle \_ dimensioni della finestra di ricezione \_ \_ TCP.

Dipendente dall'implementazione

(i)

<span id="SO_REUSEADDR"></span><span id="so_reuseaddr"></span>\_RIUTILIZZOADDR

BOOL

L'indirizzo a cui è associato questo socket può essere usato da altri. Non applicabile nei socket ATM.

FALSE

<span id="SO_SNDBUF"></span><span id="so_sndbuf"></span>SO \_ SNDBUF

int

Spazio totale del buffer per socket riservato per gli invii. Ciò non è correlato a SO MAX MSG SIZE e non corrisponde necessariamente alle dimensioni di \_ una finestra di invio \_ \_ TCP.

Dipendente dall'implementazione

(i)

<span id="SO_TYPE"></span><span id="so_type"></span>SO \_ TYPE

int

Tipo di socket (ad esempio, SOCK \_ STREAM).

Come creato tramite socket.

<span id="PVD_CONFIG"></span><span id="pvd_config"></span>CONFIGURAZIONE \_ PVD

char FAR \*

Oggetto struttura di dati opaco contenente le informazioni di configurazione del provider di servizi.

Dipendente dall'implementazione

<span id="TCP_NODELAY"></span><span id="tcp_nodelay"></span>TCP \_ NODELAY

BOOL

Disabilita l'algoritmo Nagle di unione dei pacchetti in invio.

Dipendente dall'implementazione

(i) Un provider di servizi può ignorare in modo invisibile all'utente questa opzione in [**WSPSetSockOpt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)) e restituire un valore costante per [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85))oppure può accettare un valore per **WSPSetSockOpt** e restituire il valore corrispondente in **WSPGetSockOpt** senza usare il valore in alcun modo.



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Opzioni socket**](socket-options.md)
</dt> <dt>

[**Opzioni socket SOCKET SOL \_**](sol-socket-socket-options.md)
</dt> <dt>

[**Opzioni socket \_ TCP IPPROTO**](ipproto-tcp-socket-options.md)
</dt> <dt>

[**Opzioni socket \_ UDP IPPROTO**](ipproto-udp-socket-options.md)
</dt> <dt>

[**Winsock IOCTLs**](winsock-ioctls.md)
</dt> </dl>

 

 
