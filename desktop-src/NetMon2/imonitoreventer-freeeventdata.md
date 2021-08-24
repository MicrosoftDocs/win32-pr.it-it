---
description: Il metodo FreeEventData libera lo spazio allocato per la struttura NMEVENTDATA.
ms.assetid: f86dcfd8-5a3b-4ce3-9d45-04545b030a89
title: Metodo IMonitorEventer::FreeEventData (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitorEventer.FreeEventData
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: f2bf462ef63045c8c4e5822e3d28fc21b44dfeed5848da3ac89c8232dfacc062
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037441"
---
# <a name="imonitoreventerfreeeventdata-method"></a>Metodo IMonitorEventer::FreeEventData

Il **metodo FreeEventData** libera lo spazio allocato per [**la struttura NMEVENTDATA.**](nmeventdata.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT FreeEventData(
  [in] PNMEVENTDATA pNMEventData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pNMEventData* \[ Pollici\]
</dt> <dd>

Indirizzo della [**struttura NMEVENTDATA,**](nmeventdata.md) la cui memoria viene liberata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce S \_ OK.

## <a name="remarks"></a>Commenti

I monitoraggi chiamano questo metodo per liberare la memoria allocata per la struttura dei dati dell'evento. Tenere presente che mentre il monitoraggio ha ancora un puntatore alle stringhe in una struttura [**NMEVENTDATA**](nmeventdata.md) allocata, la memoria per queste stringhe deve essere liberata prima che venga chiamato il **metodo FreeEventData.**

Per altre informazioni su come allocare memoria per una [**struttura NMEVENTDATA,**](nmeventdata.md) vedere [**IMonitorEventer::GetEventData**](imonitoreventer-geteventdata.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMonitorEventer**](imonitoreventer.md)
</dt> <dt>

[**IMonitorEventer::GetEventData**](imonitoreventer-geteventdata.md)
</dt> <dt>

[**NMEVENTDATA**](nmeventdata.md)
</dt> </dl>

 

 




