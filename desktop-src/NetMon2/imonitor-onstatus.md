---
description: Il metodo MCSVC chiama il metodo OnStatus per notificare al monitoraggio che si è verificata l'esistenza di un evento di stato NPP. Questo metodo deve essere implementato dal monitoraggio.
ms.assetid: 771852b1-77d8-4d7d-b3fb-03eb3ea593b8
title: 'Metodo IMonitor:: onStatus (Netmon. h)'
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
ms.openlocfilehash: fc2716a10673cc1178591b14a335b1d8559aa35a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130262"
---
# <a name="imonitoronstatus-method"></a>Metodo IMonitor:: OnStatus

Il metodo MCSVC chiama il metodo **OnStatus** per notificare al monitoraggio che si è verificata l'esistenza di un evento di stato NPP. Questo metodo deve essere implementato dal monitoraggio.

## <a name="syntax"></a>Sintassi


```C++
HRESULT OnStatus(
  [in] UPDATE_EVENT Event
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Evento* \[ in\]
</dt> <dd>

Struttura [di \_ eventi di aggiornamento](update-event.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, il valore restituito è \_ OK (che corrisponde a NOERROR) e MCSVC passa il valore restituito all'oggetto NPP per l'elaborazione.

Se il metodo ha esito negativo, restituire un codice di errore. In errore, MCSVC passa il valore restituito all'oggetto NPP per l'elaborazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




