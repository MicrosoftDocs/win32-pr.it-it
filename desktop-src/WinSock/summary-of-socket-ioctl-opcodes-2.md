---
description: Alcuni dei codici operativo IOCTL del socket per Windows Sockets 2 sono riepilogati nella tabella seguente.
ms.assetid: fb6447b4-28f5-4ab7-bbdc-5a57ed38a994
title: Riepilogo degli opcode Ioctl del socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88f0d6163e4ef36598dad56dd4d81201bdda3c2a3b1bb0473a0ef9ffb4675b2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118559661"
---
# <a name="summary-of-socket-ioctl-opcodes"></a>Riepilogo degli opcode Ioctl del socket

Alcuni dei codici operativo IOCTL del socket per Windows Sockets 2 sono riepilogati nella tabella seguente. Informazioni più dettagliate sono disponibili nelle informazioni di riferimento di [**Winsock sugli IOCL di Winsock**](winsock-ioctls.md) e [**sulla funzione WSPIoctl.**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) Nell'allegato specifico del protocollo sono disponibili altri nuovi codici operativo IOCTL specifici del protocollo.

Un elenco completo degli [**IOCL di Winsock**](winsock-ioctls.md) è disponibile nelle informazioni di riferimento su Winsock.



| Opcode                                                      | Tipo di input                               | Tipo di output                                 | Significato                                                                                                                                                                                                            |
|-------------------------------------------------------------|------------------------------------------|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| FIONBIO                                                     | Unsigned long                            | <Not used>                            | Abilita o disabilita la modalità non di blocco nel socket.                                                                                                                                                                |
| FIONREAD                                                    | <Not used>                         | Unsigned long                               | Determina la quantità di dati che possono essere letti atomicamente dal socket.                                                                                                                                         |
| SIOCATMARK                                                  | <Not used>                         | BOOL                                        | Determina se tutti i dati OOB sono stati letti.                                                                                                                                                              |
| HANDLE DI ASSOCIAZIONE SIO \_ \_                                      | Dipendente dall'API complementare                  | <Not used>                            | Associa il socket all'handle specificato di un'interfaccia complementare.                                                                                                                                          |
| SIO \_ ENABLE \_ CIRCULAR \_ QUEUEING                             | <Not used>                         | <Not used>                            | Abilita l'accodamento circolare.                                                                                                                                                                                          |
| SIO \_ FIND \_ ROUTE                                            | [**Struttura sockaddr**](sockaddr-2.md) | <Not used>                            | Richiede l'individuare la route all'indirizzo specificato.                                                                                                                                                      |
| SCARICAMENTO SIO \_                                                  | <Not used>                         | <Not used>                            | Rimuove il contenuto corrente della coda di invio.                                                                                                                                                                    |
| SIO \_ GET \_ BROADCAST \_ ADDRESS                                | <Not used>                         | [**Struttura sockaddr**](sockaddr-2.md)    | Recupera l'indirizzo broadcast specifico del protocollo da utilizzare in [**WSPSendTo.**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85))                                                                                                                  |
| SIO \_ GET \_ QOS                                               | <Not used>                         | [**Qos**](/windows/win32/api/winsock2/ns-winsock2-qos)                          | Recupera le specifiche correnti del flusso per il socket.                                                                                                                                                              |
| SIO \_ GET \_ GROUP \_ QOS                                        | <Not used>                         | [**Qos**](/windows/win32/api/winsock2/ns-winsock2-qos)                          | Riservato.                                                                                                                                                                                                          |
| SIO \_ MULTIPOINT \_ LOOPBACK                                   | BOOL                                     | <Not used>                            | Controlla se anche i dati inviati in una sessione multipoint verranno ricevuti dallo stesso socket nell'host locale.                                                                                                     |
| AMBITO \_ MULTICAST SIO \_                                       | int                                      | <Not used>                            | Specifica l'ambito su cui verranno eseguite le trasmissioni multicast.                                                                                                                                                 |
| SIO \_ SET \_ QOS                                               | [**Qos**](/windows/win32/api/winsock2/ns-winsock2-qos)                       | <Not used>                            | Stabilisce nuove specifiche di flusso per il socket.                                                                                                                                                                |
| QOS \_ DEL GRUPPO SET \_ \_ SIO                                        | [**Qos**](/windows/win32/api/winsock2/ns-winsock2-qos)                       | <Not used>                            | Riservato.                                                                                                                                                                                                          |
| HANDLE DI CONVERSIONE SIO \_ \_                                      | int                                      | Dipendente dall'API complementare                     | Ottiene un handle corrispondente per *i* socket validi nel contesto di un'interfaccia complementare.                                                                                                               |
| QUERY DELL'INTERFACCIA DI ROUTING SIO \_ \_ \_                              | [**sockaddr**](sockaddr-2.md)           | [**sockaddr**](sockaddr-2.md)              | Ottiene l'indirizzo dell'interfaccia locale che deve essere utilizzata per inviare all'indirizzo specificato.                                                                                                                   |
| MODIFICA DELL'INTERFACCIA DI ROUTING SIO \_ \_ \_                             | [**sockaddr**](sockaddr-2.md)           | <Not used>                            | Richiede la notifica delle modifiche alle informazioni segnalate tramite SIO \_ ROUTING INTERFACE QUERY per \_ \_ l'indirizzo specificato.                                                                                         |
| [**QUERY ELENCO INDIRIZZI SIO \_ \_ \_**](/previous-versions/windows/desktop/legacy/dd877219(v=vs.85)) | <Not used>                         | [**INDIRIZZO \_ SOCKET**](/windows/desktop/api/Ws2def/ns-ws2def-socket_address) | Ottiene un elenco di indirizzi di trasporto locali della famiglia di protocolli del socket a cui l'applicazione può eseguire l'associazione. L'elenco di indirizzi varia in base alla famiglia di indirizzi e alcuni indirizzi vengono esclusi dall'elenco. |
| MODIFICA \_ DELL'ELENCO INDIRIZZI SIO \_ \_                                  | <Not used>                         | <Not used>                            | Richiede la notifica delle modifiche alle informazioni segnalate tramite SIO \_ ADDRESS \_ LIST \_ QUERY                                                                                                                         |
| HANDLE DI DESTINAZIONE \_ \_ PNP DI QUERY \_ SIO \_                             | <Not used>                         | Socket                                      | Ottiene il descrittore del socket del provider successivo nella catena da cui dipende il socket corrente in relazione a PnP.                                                                                                     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Winsock IOCTLs**](winsock-ioctls.md)
</dt> <dt>

[**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85))
</dt> </dl>

 

 
