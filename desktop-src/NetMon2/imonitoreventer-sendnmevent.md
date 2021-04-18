---
description: Il metodo SendNMEvent invia eventi a Strumentazione gestione Windows (WMI).
ms.assetid: 85c33a71-72aa-4b0a-8e8b-3a220a080bb2
title: 'Metodo IMonitorEventer:: SendNMEvent (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitorEventer.SendNMEvent
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: 3286fca4d5b852d4562c13446699c1a6b40f3efe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308659"
---
# <a name="imonitoreventersendnmevent-method"></a>Metodo IMonitorEventer:: SendNMEvent

Il metodo **SendNMEvent** invia eventi a Strumentazione gestione Windows (WMI).

## <a name="syntax"></a>Sintassi


```C++
HRESULT SendNMEvent(
  [in] PNMEVENTDATA pNMEventData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pNMEventData* \[ in\]
</dt> <dd>

Puntatore all'evento inviato a WMI.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, il valore restituito è \_ OK.

Se il metodo ha esito negativo, il valore restituito è NMERR \_ \_ \_ memoria insufficiente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




