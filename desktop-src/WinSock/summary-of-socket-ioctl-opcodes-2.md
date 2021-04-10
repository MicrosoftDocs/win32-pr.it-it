---
description: Alcuni dei codici operativi IOCTL del socket per Windows Sockets 2 sono riepilogati nella tabella seguente.
ms.assetid: fb6447b4-28f5-4ab7-bbdc-5a57ed38a994
title: Riepilogo dei codici operativi IOCTL del socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2243457ddbb7e0bb59f14357cf61d2e771c6a7d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131163"
---
# <a name="summary-of-socket-ioctl-opcodes"></a>Riepilogo dei codici operativi IOCTL del socket

Alcuni dei codici operativi IOCTL del socket per Windows Sockets 2 sono riepilogati nella tabella seguente. Per informazioni più dettagliate, fare riferimento a Winsock per le [**IOCTL Winsock**](winsock-ioctls.md) e la funzione [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) . Sono disponibili altri nuovi codici operativi IOCTL specifici del protocollo che è possibile trovare nell'allegato specifico del protocollo.

Un elenco completo di [**IOCTL Winsock**](winsock-ioctls.md) è disponibile nella Guida di riferimento a Winsock.



| Opcode                                                      | Tipo di input                               | Tipo di output                                 | Significato                                                                                                                                                                                                            |
|-------------------------------------------------------------|------------------------------------------|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| FIONBIO                                                     | Long senza segno                            | <Not used>                            | Abilita o Disabilita la modalità di non blocco sul socket.                                                                                                                                                                |
| FIONREAD                                                    | <Not used>                         | Long senza segno                               | Determina la quantità di dati che possono essere letti atomicamente dal socket.                                                                                                                                         |
| SIOCATMARK                                                  | <Not used>                         | BOOL                                        | Determina se tutti i dati OOB sono stati letti o meno.                                                                                                                                                              |
| \_handle associato \_ sio                                      | Dipendenza dall'API complementare                  | <Not used>                            | Associa il socket all'handle specificato di un'interfaccia complementare.                                                                                                                                          |
| SIO \_ Abilita \_ \_ Accodamento circolare                             | <Not used>                         | <Not used>                            | Abilita l'accodamento circolare.                                                                                                                                                                                          |
| \_Route di ricerca sio \_                                            | struttura [**sockaddr**](sockaddr-2.md) | <Not used>                            | Richiede che la route venga individuata all'indirizzo specificato.                                                                                                                                                      |
| \_scaricamento sio                                                  | <Not used>                         | <Not used>                            | Elimina il contenuto corrente della coda di invio.                                                                                                                                                                    |
| \_indirizzo di \_ trasmissione sio Get \_                                | <Not used>                         | struttura [**sockaddr**](sockaddr-2.md)    | Recupera l'indirizzo di trasmissione specifico del protocollo da utilizzare in [**WSPSendTo**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85)).                                                                                                                  |
| \_QoS Get \_ QoS                                               | <Not used>                         | [**QOS**](/windows/win32/api/winsock2/ns-winsock2-qos)                          | Recupera le specifiche del flusso corrente per il socket.                                                                                                                                                              |
| \_QoS del \_ gruppo sio Get \_                                        | <Not used>                         | [**QOS**](/windows/win32/api/winsock2/ns-winsock2-qos)                          | Riservato.                                                                                                                                                                                                          |
| \_loopback MultiPoint di sio \_                                   | BOOL                                     | <Not used>                            | Controlla se i dati inviati in una sessione multipoint verranno ricevuti anche dallo stesso socket nell'host locale.                                                                                                     |
| \_ambito multicast \_ sio                                       | INT                                      | <Not used>                            | Specifica l'ambito in cui si verificheranno le trasmissioni multicast.                                                                                                                                                 |
| \_QoS set \_ sio                                               | [**QOS**](/windows/win32/api/winsock2/ns-winsock2-qos)                       | <Not used>                            | Stabilisce nuove specifiche del flusso per il socket.                                                                                                                                                                |
| \_ \_ QoS gruppo set \_ sio                                        | [**QOS**](/windows/win32/api/winsock2/ns-winsock2-qos)                       | <Not used>                            | Riservato.                                                                                                                                                                                                          |
| \_handle di conversione sio \_                                      | INT                                      | Complementare-API dipendente                     | Ottiene un handle corrispondente per *i socket che* è valido nel contesto di un'interfaccia complementare.                                                                                                               |
| \_query sull' \_ interfaccia di routing sio \_                              | [**sockaddr**](sockaddr-2.md)           | [**sockaddr**](sockaddr-2.md)              | Ottiene l'indirizzo dell'interfaccia locale che deve essere utilizzato per inviare all'indirizzo specificato.                                                                                                                   |
| \_modifica dell' \_ interfaccia di routing sio \_                             | [**sockaddr**](sockaddr-2.md)           | <Not used>                            | Richiede la notifica delle modifiche alle informazioni segnalate \_ tramite \_ la query dell'interfaccia di routing sio \_ per l'indirizzo specificato.                                                                                         |
| [**\_ \_ query elenco indirizzi \_ sio**](/previous-versions/windows/desktop/legacy/dd877219(v=vs.85)) | <Not used>                         | [**\_indirizzo socket**](/windows/desktop/api/Ws2def/ns-ws2def-socket_address) | Ottiene un elenco degli indirizzi di trasporto locali della famiglia di protocolli del socket a cui l'applicazione può eseguire il binding. L'elenco di indirizzi varia in base alla famiglia di indirizzi e alcuni indirizzi sono esclusi dall'elenco. |
| \_ \_ modifica elenco indirizzi \_ sio                                  | <Not used>                         | <Not used>                            | Richiede la notifica delle modifiche alle informazioni segnalate tramite la \_ \_ query dell'elenco indirizzi sio \_                                                                                                                         |
| \_handle di \_ \_ destinazione PNP della query \_ sio                             | <Not used>                         | PRESA                                      | Ottiene il descrittore del socket del provider successivo nella catena da cui dipende il socket corrente rispetto a PnP.                                                                                                     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IOCTL Winsock**](winsock-ioctls.md)
</dt> <dt>

[**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85))
</dt> </dl>

 

 
