---
description: Questa classe è la classe padre per gli eventi di I/O suddivisi. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: d65c5180-6f1a-45cc-bca8-eac13857d383
title: Classe SplitIo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SplitIo
api_type:
- NA
api_location: ''
ms.openlocfilehash: 0268c3dfa778eb8694a81f57b9212b68bd6674e6c7de6324cdc297550745b2a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069721"
---
# <a name="splitio-class"></a>Classe SplitIo

Questa classe è la classe padre per gli eventi di I/O suddivisi.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Guid("{d837ca92-12b9-44a5-ad6a-3a65b3578aa8}")]
class SplitIo : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Members

La **classe SplitIo** non definisce membri.

## <a name="remarks"></a>Commenti

Per abilitare gli eventi di I/O suddivisi in una sessione di registrazione del kernel NT, specificare il flag **EVENT TRACE FLAG SPLIT \_ \_ \_ \_ IO** nel membro **EnableFlags** di una struttura [**EVENT TRACE \_ \_ PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) quando si chiama la [**funzione StartTrace.**](/windows/win32/api/evntrace/nf-evntrace-starttracea)

I consumer di traccia eventi possono implementare un'elaborazione speciale per gli eventi di I/O suddivisi chiamando la [**funzione SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e specificando [**SplitIoGuid**](nt-kernel-logger-constants.md) come *parametro pGuid.* Usare il tipo di evento seguente per identificare l'evento effettivo quando si utilizzano gli eventi.



| Tipo di evento           | Descrizione                                                                                                |
|----------------------|------------------------------------------------------------------------------------------------------------|
| Valore del tipo di evento, 32 | Evento Dividi I/O. La [**classe MOF SplitIo \_ Info**](splitio-info.md) definisce i dati dell'evento. |



 

Gli eventi Dividi I/O indicano che le richieste di I/O sono state suddivise in più richieste di I/O su disco a causa dell'hardware del disco di mirroring sottostante.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



 

 
