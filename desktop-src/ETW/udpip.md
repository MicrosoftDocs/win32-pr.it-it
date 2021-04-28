---
description: 'Classe UdpIp: questa classe è la classe padre per gli eventi UDP/IP. La sintassi seguente è semplificata dal codice MOF.'
ms.assetid: 0fbecad2-0221-408e-9f43-859547efa803
title: Classe UdpIp
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UdpIp
api_type:
- NA
api_location: ''
ms.openlocfilehash: d76aeb00ece18b026d9e5515a74ce830eb14af32
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105389"
---
# <a name="udpip-class"></a>Classe UdpIp

Questa classe è la classe padre per gli eventi UDP/IP.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Guid("{bf3a50c5-a9c9-4988-a005-2df0b7c80f80}"), EventVersion(2)]
class UdpIp : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Members

La **classe UdpIp** non definisce membri.

## <a name="remarks"></a>Commenti

Per abilitare gli eventi UDP/IP in una sessione di registrazione del kernel NT, specificare il flag **EVENT TRACE FLAG NETWORK \_ \_ \_ \_ TCPIP** nel membro **EnableFlags** di una struttura [**EVENT TRACE \_ \_ PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) quando si chiama la [**funzione StartTrace.**](/windows/win32/api/evntrace/nf-evntrace-starttracea)

I consumer di traccia eventi possono implementare un'elaborazione speciale per gli eventi UDP/IP chiamando la [**funzione SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e specificando [**UdpIpGuid**](nt-kernel-logger-constants.md) come *parametro pGuid.* Usare i tipi di evento seguenti per identificare l'evento di rete effettivo (UDP/IP) quando si usano gli eventi.



| Tipo di evento                                                         | Descrizione                                                                                                                         |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| **EVENTO \_ TRACE \_ TYPE \_ RECEIVE**(il valore del tipo di evento è 11)<br/> | Evento di ricezione per il protocollo IPv4. La [**classe MOF \_ UdpIp TypeGroup1**](udpip-typegroup1.md) definisce i dati dell'evento per questo evento. |
| **EVENTO \_ TRACE \_ TYPE \_ SEND**(il valore del tipo di evento è 10)<br/>    | Evento di invio per il protocollo IPv4. La [**classe MOF \_ UdpIp TypeGroup1**](udpip-typegroup1.md) definisce i dati dell'evento per questo evento.    |
| Valore del tipo di evento, 17                                               | Evento Fail. La [**classe MOF UdpIp \_ Fail**](udpip-fail.md) definisce i dati dell'evento per questo evento.                                  |
| Valore del tipo di evento, 26                                               | Evento di invio per il protocollo IPv6. La [**classe \_ MOF UdpIp TypeGroup2**](udpip-typegroup2.md) definisce i dati dell'evento per questo evento.    |
| Valore del tipo di evento, 27                                               | Evento di ricezione per il protocollo IPv6. La [**classe \_ MOF UdpIp TypeGroup2**](udpip-typegroup2.md) definisce i dati dell'evento per questo evento. |



 

È possibile tracciare gli eventi di rete in un processo di origine e di destinazione usando la **proprietà ProcessId.** Poiché alcuni eventi di rete vengono registrati da thread separati, potrebbe non essere possibile usare i membri **ProcessId** e **ThreadId** di [**EVENT TRACE \_ \_ HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) per identificare il processo o il thread che ha originato le attività di rete.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows Vista \[\]<br/>       |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MSNT \_ SystemTrace**](msnt-systemtrace.md)
</dt> <dt>

[**UdpIp \_ Fail**](udpip-fail.md)
</dt> <dt>

[**UdpIp \_ TypeGroup1**](udpip-typegroup1.md)
</dt> <dt>

[**UdpIp \_ TypeGroup2**](udpip-typegroup2.md)
</dt> <dt>

[**UdpIp \_ V0**](udpip-v0.md)
</dt> <dt>

[**UdpIp \_ V1**](udpip-v1.md)
</dt> </dl>

 

 
