---
description: Il metodo onframes deve essere implementato dal monitoraggio. MCSVC chiama questo metodo quando il buffer di acquisizione è pieno o il tempo di aggiornamento è scaduto.
ms.assetid: 243bd35b-2527-463e-b3d2-4bd840fe9c3f
title: 'Metodo IMonitor:: onframes (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.OnFrames
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: c5b6ff3e9d5b97a228e6e1d865fe4d8f1b5bfc9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751087"
---
# <a name="imonitoronframes-method"></a>Metodo IMonitor:: onframes

Il metodo **Onframes** deve essere implementato dal monitoraggio. MCSVC chiama questo metodo quando il buffer di acquisizione è pieno o il tempo di aggiornamento è scaduto.

## <a name="syntax"></a>Sintassi


```C++
HRESULT OnFrames(
  [in] UPDATE_EVENT Event
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Evento* \[ in\]
</dt> <dd>

[Aggiornamento \_ di ](update-event.md) Struttura dell'evento che include le informazioni sul frame utilizzate per aggiornare gli eventi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, il valore restituito è \_ OK (che corrisponde a NOERROR). MCSVC passa di nuovo il valore restituito all'oggetto NPP per l'elaborazione.

Se il metodo ha esito negativo, il valore restituito è un codice di errore. MCSVC passa di nuovo il valore restituito all'oggetto NPP per l'elaborazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




