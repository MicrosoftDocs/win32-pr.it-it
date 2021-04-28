---
description: 'Classe TcpIp: questa classe è la classe padre per gli eventi TCP/IP. La sintassi seguente è semplificata dal codice MOF.'
ms.assetid: f9d6ea8f-c777-4747-89f4-f389c6eeac35
title: Classe TcpIp
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp
api_type:
- NA
api_location: ''
ms.openlocfilehash: abcd805b417451adf2122e7baf3310be101a35ff
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105729"
---
# <a name="tcpip-class"></a>Classe TcpIp

Questa classe è la classe padre per gli eventi TCP/IP.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Guid("{9a280ac0-c8e0-11d1-84e2-00c04fb998a2}"), EventVersion(2)]
class TcpIp : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Members

La **classe TcpIp** non definisce membri.

## <a name="remarks"></a>Commenti

Per abilitare gli eventi TCP/IP in una sessione di registrazione del kernel NT, specificare il flag **NETWORK \_ \_ \_ \_ TCPIP EVENT TRACE FLAG nel** membro **EnableFlags** di una struttura [**EVENT TRACE \_ \_ PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) quando si chiama la [**funzione StartTrace.**](/windows/win32/api/evntrace/nf-evntrace-starttracea)

I consumer di traccia eventi possono implementare un'elaborazione speciale per gli eventi TCP/IP chiamando la [**funzione SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e specificando [**TcpIpGuid**](nt-kernel-logger-constants.md) come *parametro pGuid.* Utilizzare i tipi di evento seguenti per identificare l'evento di rete effettivo (TCP/IP) quando si utilizzano gli eventi.



| Tipo di evento                                                            | Descrizione                                                                                                                                                                                   |
|-----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EVENTO \_ TRACE \_ TYPE \_ ACCEPT**(il valore del tipo di evento è 15)<br/>     | Accettare l'evento per il protocollo IPv4. La [**classe \_ MOF TypeGroup2 TcpIp**](tcpip-typegroup2.md) definisce i dati dell'evento per questo evento.                                                            |
| **EVENTO \_ TRACE \_ TYPE \_ CONNECT**(il valore del tipo di evento è 12)<br/>    | Evento Connect per il protocollo IPv4. La [**classe \_ MOF TypeGroup2 TcpIp**](tcpip-typegroup2.md) definisce i dati dell'evento per questo evento.                                                           |
| **EVENTO \_ TRACE \_ TYPE \_ DISCONNECT**(il valore del tipo di evento è 13)<br/> | Evento di disconnessione per il protocollo IPv4. La [**classe MOF \_ TypeGroup1 TcpIp**](tcpip-typegroup1.md) definisce i dati dell'evento per questo evento.                                                        |
| **EVENTO \_ TRACE \_ TYPE \_ RECEIVE**(il valore del tipo di evento è 11)<br/>    | Evento di ricezione per il protocollo IPv4. La [**classe MOF \_ TcpIp TypeGroup1**](tcpip-typegroup1.md) definisce i dati dell'evento.                                                           |
| **EVENTO \_ TRACE \_ TYPE \_ RECONNECT**(il valore del tipo di evento è 16)<br/>  | Evento di riconnessione per il protocollo IPv4. Un tentativo di connessione non è riuscito e viene eseguito un altro tentativo. La [**classe MOF \_ TcpIp TypeGroup1**](tcpip-typegroup1.md) definisce i dati dell'evento per questo evento. |
| **EVENTO \_ TRACE \_ TYPE \_ RETRANSMIT**(il valore del tipo di evento è 14)<br/> | Evento di ritrasmissione per il protocollo IPv4. La [**classe MOF \_ TcpIp TypeGroup1**](tcpip-typegroup1.md) definisce i dati dell'evento per questo evento.                                                        |
| **EVENTO \_ TRACE \_ TYPE \_ SEND**(il valore del tipo di evento è 10)<br/>       | Evento di invio per il protocollo IPv4. La [**classe MOF TcpIp \_ SendIPV4**](tcpip-sendipv4.md) definisce i dati dell'evento per questo evento.                                                                  |
| Valore del tipo di evento, 17                                                  | Evento Fail. La [**classe MOF TcpIp \_ Fail**](tcpip-fail.md) definisce i dati dell'evento per questo evento.                                                                                            |
| Valore del tipo di evento, 18                                                  | Evento di copia TCP per il protocollo IPv4. La [**classe MOF \_ TcpIp TypeGroup1**](tcpip-typegroup1.md) definisce i dati dell'evento per questo evento.                                                          |
| Valore del tipo di evento, 26                                                  | Evento di invio per il protocollo IPv6. La [**classe MOF TcpIp \_ SendIPV6**](tcpip-sendipv6.md) definisce i dati dell'evento per questo evento.                                                                  |
| Valore del tipo di evento, 27                                                  | Evento di ricezione per il protocollo IPv6. La [**classe \_ MOF TcpIp TypeGroup3**](tcpip-typegroup3.md) definisce i dati dell'evento per questo evento.                                                           |
| Valore del tipo di evento, 28                                                  | Evento Connect per il protocollo IPv6. La [**classe \_ MOF TypeGroup4 TcpIp**](tcpip-typegroup4.md) definisce i dati dell'evento.                                                           |
| Valore del tipo di evento, 29                                                  | Evento di disconnessione per il protocollo IPv6. La [**classe \_ MOF TcpIp TypeGroup3**](tcpip-typegroup3.md) definisce i dati dell'evento per questo evento.                                                        |
| Valore del tipo di evento, 30                                                  | Evento di ritrasmissione per il protocollo IPv6. La [**classe \_ MOF TcpIp TypeGroup3**](tcpip-typegroup3.md) definisce i dati dell'evento per questo evento.                                                        |
| Valore del tipo di evento, 31                                                  | Accettare l'evento per il protocollo IPv6. La [**classe \_ MOF TypeGroup4 TcpIp**](tcpip-typegroup4.md) definisce i dati dell'evento per questo evento.                                                            |
| Valore del tipo di evento, 32                                                  | Evento di riconnessione per il protocollo IPv6. Un tentativo di connessione non è riuscito e viene eseguito un altro tentativo. La [**classe \_ MOF TcpIp TypeGroup3**](tcpip-typegroup3.md) definisce i dati dell'evento per questo evento. |
| Valore del tipo di evento, 34                                                  | Evento di copia TCP per il protocollo IPv6. La [**classe MOF \_ TcpIp TypeGroup3**](tcpip-typegroup3.md) definisce i dati dell'evento.                                                          |



 

È possibile tracciare gli eventi di rete in un processo di origine e di destinazione usando la **proprietà ProcessId.** Poiché alcuni eventi di rete vengono registrati da thread separati, potrebbe non essere possibile usare i membri **ProcessId** e **ThreadId** di [**EVENT TRACE \_ \_ HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) per identificare il processo o il thread che ha originato le attività di rete.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows \[ Vista\]<br/>       |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MSNT \_ SystemTrace**](msnt-systemtrace.md)
</dt> <dt>

[**TcpIp \_ Fail**](tcpip-fail.md)
</dt> <dt>

[**TcpIp \_ SendIPV4**](tcpip-sendipv4.md)
</dt> <dt>

[**TcpIp \_ SendIPV6**](tcpip-sendipv6.md)
</dt> <dt>

[**TcpIp \_ TypeGroup1**](tcpip-typegroup1.md)
</dt> <dt>

[**TcpIp \_ TypeGroup2**](tcpip-typegroup2.md)
</dt> <dt>

[**TcpIp \_ TypeGroup3**](tcpip-typegroup3.md)
</dt> <dt>

[**TypeGroup \_ TcpIp4**](tcpip-typegroup4.md)
</dt> <dt>

[**TcpIp \_ V0**](tcpip-v0.md)
</dt> <dt>

[**TcpIp \_ V1**](tcpip-v1.md)
</dt> </dl>

 

 
