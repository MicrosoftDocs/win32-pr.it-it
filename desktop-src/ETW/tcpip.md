---
description: Questa classe è la classe padre per gli eventi TCP/IP. La sintassi seguente è semplificata dal codice MOF.
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
ms.openlocfilehash: 6488ece2fd8df0670455ceea25560835c352b83e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978226"
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

La classe **Tcpip** non definisce membri.

## <a name="remarks"></a>Commenti

Per abilitare gli eventi TCP/IP in una sessione di registrazione del kernel NT, specificare il flag **tcpip di rete del flag di \_ traccia \_ \_ \_ eventi** nel membro **EnableFlags** di una struttura di [**\_ \_ proprietà della traccia eventi**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) quando si chiama la funzione [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .

I consumer di traccia degli eventi possono implementare un'elaborazione speciale per gli eventi TCP/IP chiamando la funzione [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e specificando [**TcpIpGuid**](nt-kernel-logger-constants.md) come parametro *pGuid* . Usare i tipi di eventi seguenti per identificare l'evento di rete (TCP/IP) effettivo quando si utilizzano gli eventi.



| Tipo di evento                                                            | Descrizione                                                                                                                                                                                   |
|-----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Evento \_ Tipo di traccia \_ \_ Accept**(il valore del tipo di evento è 15)<br/>     | Evento Accept per il protocollo IPv4. La classe [**TCPIP \_ TypeGroup2**](tcpip-typegroup2.md) MOF definisce i dati dell'evento per questo evento.                                                            |
| **Evento \_ Tipo di traccia \_ \_ Connect**(il valore del tipo di evento è 12)<br/>    | Evento Connect per il protocollo IPv4. La classe [**TCPIP \_ TypeGroup2**](tcpip-typegroup2.md) MOF definisce i dati dell'evento per questo evento.                                                           |
| **Evento \_ \_Disconnessione \_ tipo di traccia**(il valore del tipo di evento è 13)<br/> | Evento di disconnessione per il protocollo IPv4. La classe [**TCPIP \_ TypeGroup1**](tcpip-typegroup1.md) MOF definisce i dati dell'evento per questo evento.                                                        |
| **Evento \_ Tipo di traccia \_ \_ Receive**(il valore del tipo di evento è 11)<br/>    | Evento di ricezione per il protocollo IPv4. La classe [**TCPIP \_ TypeGroup1**](tcpip-typegroup1.md) MOF definisce i dati dell'evento per questo evento.                                                           |
| **Evento \_ Tipo di traccia \_ \_ riconnessione**(il valore del tipo di evento è 16)<br/>  | Riconnetti l'evento per il protocollo IPv4. Un tentativo di connessione non è riuscito e viene effettuato un altro tentativo. La classe [**TCPIP \_ TypeGroup1**](tcpip-typegroup1.md) MOF definisce i dati dell'evento per questo evento. |
| **Evento \_ \_RItrasmissione \_ del tipo di traccia**(il valore del tipo di evento è 14)<br/> | Ritrasmissione dell'evento per il protocollo IPv4. La classe [**TCPIP \_ TypeGroup1**](tcpip-typegroup1.md) MOF definisce i dati dell'evento per questo evento.                                                        |
| **Evento \_ Tipo di traccia \_ \_ Send**(il valore del tipo di evento è 10)<br/>       | Inviare un evento per il protocollo IPv4. La classe [**TCPIP \_ SendIPV4**](tcpip-sendipv4.md) MOF definisce i dati dell'evento per questo evento.                                                                  |
| Valore del tipo di evento, 17                                                  | Evento fail. La classe MOF [**\_ Fail di Tcpip**](tcpip-fail.md) definisce i dati dell'evento per questo evento.                                                                                            |
| Valore del tipo di evento, 18                                                  | Evento di copia TCP per il protocollo IPv4. La classe [**TCPIP \_ TypeGroup1**](tcpip-typegroup1.md) MOF definisce i dati dell'evento per questo evento.                                                          |
| Valore del tipo di evento, 26                                                  | Inviare un evento per il protocollo IPv6. La classe [**TCPIP \_ SendIPV6**](tcpip-sendipv6.md) MOF definisce i dati dell'evento per questo evento.                                                                  |
| Valore del tipo di evento, 27                                                  | Evento di ricezione per il protocollo IPv6. La classe [**TCPIP \_ TypeGroup3**](tcpip-typegroup3.md) MOF definisce i dati dell'evento per questo evento.                                                           |
| Valore del tipo di evento, 28                                                  | Evento Connect per il protocollo IPv6. La classe [**TCPIP \_ TypeGroup4**](tcpip-typegroup4.md) MOF definisce i dati dell'evento per questo evento.                                                           |
| Valore del tipo di evento, 29                                                  | Evento Disconnect per protocollo IPv6. La classe [**TCPIP \_ TypeGroup3**](tcpip-typegroup3.md) MOF definisce i dati dell'evento per questo evento.                                                        |
| Valore del tipo di evento, 30                                                  | Ritrasmissione dell'evento per il protocollo IPv6. La classe [**TCPIP \_ TypeGroup3**](tcpip-typegroup3.md) MOF definisce i dati dell'evento per questo evento.                                                        |
| Valore del tipo di evento, 31                                                  | Evento Accept per il protocollo IPv6. La classe [**TCPIP \_ TypeGroup4**](tcpip-typegroup4.md) MOF definisce i dati dell'evento per questo evento.                                                            |
| Valore del tipo di evento, 32                                                  | Riconnetti evento per protocollo IPv6. Un tentativo di connessione non è riuscito e viene effettuato un altro tentativo. La classe [**TCPIP \_ TypeGroup3**](tcpip-typegroup3.md) MOF definisce i dati dell'evento per questo evento. |
| Valore del tipo di evento, 34                                                  | Evento di copia TCP per il protocollo IPv6. La classe [**TCPIP \_ TypeGroup3**](tcpip-typegroup3.md) MOF definisce i dati dell'evento per questo evento.                                                          |



 

È possibile tracciare gli eventi di rete in un processo di origine e di destinazione usando la proprietà **ProcessID** . Poiché alcuni eventi di rete vengono registrati da thread distinti, potrebbe non essere possibile usare i membri **ProcessID** e **ThreadID** dell' [**\_ \_ intestazione della traccia eventi**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) per identificare il processo o il thread che ha originato le attività di rete.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_SYSTEMTRACE MSNT**](msnt-systemtrace.md)
</dt> <dt>

[**\_Errore Tcpip**](tcpip-fail.md)
</dt> <dt>

[**\_SendIPV4 Tcpip**](tcpip-sendipv4.md)
</dt> <dt>

[**\_SendIPV6 Tcpip**](tcpip-sendipv6.md)
</dt> <dt>

[**\_TypeGroup1 Tcpip**](tcpip-typegroup1.md)
</dt> <dt>

[**\_TypeGroup2 Tcpip**](tcpip-typegroup2.md)
</dt> <dt>

[**\_TypeGroup3 Tcpip**](tcpip-typegroup3.md)
</dt> <dt>

[**\_TypeGroup4 Tcpip**](tcpip-typegroup4.md)
</dt> <dt>

[**TcpIp \_ V0**](tcpip-v0.md)
</dt> <dt>

[**TcpIp \_ V1**](tcpip-v1.md)
</dt> </dl>

 

 
