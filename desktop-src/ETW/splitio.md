---
description: Questa classe è la classe padre per gli eventi i/o divisi. La sintassi seguente è semplificata dal codice MOF.
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
ms.openlocfilehash: f2efc14ce8804852f983ebe9dcb852c8c0669899
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978842"
---
# <a name="splitio-class"></a>Classe SplitIo

Questa classe è la classe padre per gli eventi i/o divisi.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Guid("{d837ca92-12b9-44a5-ad6a-3a65b3578aa8}")]
class SplitIo : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Members

La classe **SplitIo** non definisce membri.

## <a name="remarks"></a>Commenti

Per abilitare gli eventi di i/o suddivisi in una sessione di registrazione del kernel NT, specificare il flag di traccia di i/o **\_ \_ \_ \_ Split** nel membro **EnableFlags** di una struttura di [**\_ \_ proprietà della traccia eventi**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) quando si chiama la funzione [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .

I consumer di traccia eventi possono implementare un'elaborazione speciale per gli eventi di i/o suddivisi chiamando la funzione [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e specificando [**SplitIoGuid**](nt-kernel-logger-constants.md) come parametro *pGuid* . Usare il tipo di evento seguente per identificare l'evento effettivo quando si utilizzano gli eventi.



| Tipo di evento           | Descrizione                                                                                                |
|----------------------|------------------------------------------------------------------------------------------------------------|
| Valore del tipo di evento, 32 | Evento Split IO. La classe [**SplitIo \_ info**](splitio-info.md) MOF definisce i dati dell'evento per questo evento. |



 

Gli eventi di i/o suddivisi indicano che le richieste di i/o sono state suddivise in più richieste IO disco a causa dell'hardware sottostante del disco di mirroring.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 
