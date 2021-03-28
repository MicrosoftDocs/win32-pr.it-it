---
description: Questa classe è la classe padre per gli eventi di chiamata di procedura locale avanzati. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 5380fada-50e7-4eb2-8549-6d738a56d2cd
title: Classe ALPC
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ALPC
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2a4b09a8bab9280de8fb4c91368f5d6d93f7944a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977727"
---
# <a name="alpc-class"></a>Classe ALPC

Questa classe è la classe padre per gli eventi di chiamata di procedura locale avanzati.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Guid("{45d8cccd-539f-4b72-a8b7-5c683142609a}")]
class ALPC : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Members

La classe **ALPC** non definisce membri.

## <a name="remarks"></a>Commenti

Per abilitare gli eventi di chiamata della procedura locale avanzata in una sessione di registrazione del kernel NT, specificare il flag di **\_ traccia eventi \_ \_ ALPC** nel membro **EnableFlags** di una struttura di [**\_ \_ proprietà della traccia eventi**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) quando si chiama la funzione [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .

I consumer di traccia eventi possono implementare un'elaborazione speciale per gli eventi ALPC chiamando la funzione [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e specificando [**ALPCGuid**](nt-kernel-logger-constants.md) come parametro *pGuid* . Usare i tipi di evento seguenti per identificare l'evento ALPC effettivo quando si utilizzano gli eventi.



| Tipo di evento           | Descrizione                                                                                                                                         |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| Valore del tipo di evento, 33 | Evento Send Message. La classe MOF del [**\_ \_ messaggio Send ALPC**](alpc-send-message.md) definisce i dati dell'evento per questo evento.                           |
| Valore del tipo di evento, 34 | Evento Receive Message. La classe MOF del [**\_ \_ messaggio di ricezione ALPC**](alpc-receive-message.md) definisce i dati dell'evento per questo evento.                  |
| Valore del tipo di evento, 35 | Attendere l'evento di risposta. La classe [**ALPC \_ Wait \_ for \_ Reply**](alpc-wait-for-reply.md) MOF definisce i dati dell'evento per questo evento.                    |
| Valore del tipo di evento, 36 | Attendere l'evento nuovo messaggio. La classe [**ALPC \_ Wait \_ for \_ New \_ Message**](alpc-wait-for-new-message.md) MOF definisce i dati dell'evento per questo evento. |
| Valore del tipo di evento, 37 | Arresta l'evento in attesa. La classe [**ALPC \_ Unwait**](alpc-unwait.md) MOF definisce i dati dell'evento per questo evento.                                        |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

