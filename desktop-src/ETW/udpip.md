---
description: Questa classe è la classe padre per gli eventi UDP/IP. La sintassi seguente è semplificata dal codice MOF.
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
ms.openlocfilehash: 5116b5f97a4aa7e3bafa9da1c1208ce7ee9d5794
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527288"
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

La classe **UdpIp** non definisce membri.

## <a name="remarks"></a>Commenti

Per abilitare gli eventi UDP/IP in una sessione di registrazione del kernel NT, specificare il flag **tcpip di rete del flag di \_ traccia \_ \_ \_ eventi** nel membro **EnableFlags** di una struttura di [**\_ \_ proprietà della traccia eventi**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) quando si chiama la funzione [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .

I consumer di traccia eventi possono implementare un'elaborazione speciale per gli eventi UDP/IP chiamando la funzione [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e specificando [**UdpIpGuid**](nt-kernel-logger-constants.md) come parametro *pGuid* . Usare i tipi di eventi seguenti per identificare l'evento di rete (UDP/IP) effettivo quando si utilizzano gli eventi.



| Tipo di evento                                                         | Descrizione                                                                                                                         |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| **Evento \_ Tipo di traccia \_ \_ Receive**(il valore del tipo di evento è 11)<br/> | Evento di ricezione per il protocollo IPv4. La classe MOF [**UdpIp \_ TypeGroup1**](udpip-typegroup1.md) definisce i dati dell'evento per questo evento. |
| **Evento \_ Tipo di traccia \_ \_ Send**(il valore del tipo di evento è 10)<br/>    | Inviare un evento per il protocollo IPv4. La classe MOF [**UdpIp \_ TypeGroup1**](udpip-typegroup1.md) definisce i dati dell'evento per questo evento.    |
| Valore del tipo di evento, 17                                               | Evento fail. La classe MOF [**UdpIp \_ Fail**](udpip-fail.md) definisce i dati dell'evento per questo evento.                                  |
| Valore del tipo di evento, 26                                               | Inviare un evento per il protocollo IPv6. La classe MOF [**UdpIp \_ TypeGroup2**](udpip-typegroup2.md) definisce i dati dell'evento per questo evento.    |
| Valore del tipo di evento, 27                                               | Evento di ricezione per il protocollo IPv6. La classe MOF [**UdpIp \_ TypeGroup2**](udpip-typegroup2.md) definisce i dati dell'evento per questo evento. |



 

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

[**UdpIp \_ non riuscito**](udpip-fail.md)
</dt> <dt>

[**\_TypeGroup1 UdpIp**](udpip-typegroup1.md)
</dt> <dt>

[**\_TypeGroup2 UdpIp**](udpip-typegroup2.md)
</dt> <dt>

[**UdpIp \_ V0**](udpip-v0.md)
</dt> <dt>

[**UdpIp \_ V1**](udpip-v1.md)
</dt> </dl>

 

 
