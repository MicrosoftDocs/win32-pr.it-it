---
description: Il metodo MCSVC chiama il metodo OnStatus per notificare al monitoraggio che esiste un evento di stato NPP. Questo metodo deve essere implementato dal monitoraggio.
ms.assetid: 771852b1-77d8-4d7d-b3fb-03eb3ea593b8
title: Metodo IMonitor::OnStatus (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.OnStatus
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: 2a82594400bebc8a529290e0e0e881603172aa45c111d2d4d83ebcbd5ebfbeb6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779041"
---
# <a name="imonitoronstatus-method"></a>Metodo IMonitor::OnStatus

Il metodo MCSVC chiama il **metodo OnStatus** per notificare al monitoraggio che esiste un evento di stato NPP. Questo metodo deve essere implementato dal monitoraggio.

## <a name="syntax"></a>Sintassi


```C++
HRESULT OnStatus(
  [in] UPDATE_EVENT Event
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Evento* \[ Pollici\]
</dt> <dd>

Struttura [UPDATE \_ EVENT.](update-event.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, il valore restituito è S OK (che corrisponde a NOERROR) e MCSVC passa il valore restituito all'NPP per \_ l'elaborazione.

Se il metodo ha esito negativo, restituire un codice di errore. In caso di errore, MCSVC passa il valore restituito all'NPP per l'elaborazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




