---
description: Il metodo FreeEventData libera lo spazio allocato per la struttura NMEVENTDATA.
ms.assetid: f86dcfd8-5a3b-4ce3-9d45-04545b030a89
title: 'Metodo IMonitorEventer:: FreeEventData (Netmon. h)'
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
ms.openlocfilehash: c71b7563e00bfceb220ce1c2bf109339267fbabf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305870"
---
# <a name="imonitoreventerfreeeventdata-method"></a>Metodo IMonitorEventer:: FreeEventData

Il metodo **FreeEventData** libera lo spazio allocato per la struttura [**NMEVENTDATA**](nmeventdata.md) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT FreeEventData(
  [in] PNMEVENTDATA pNMEventData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pNMEventData* \[ in\]
</dt> <dd>

Indirizzo della struttura [**NMEVENTDATA**](nmeventdata.md) , la cui memoria viene liberata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce \_ OK.

## <a name="remarks"></a>Commenti

I monitoraggi chiamano questo metodo per liberare la memoria allocata per la struttura dei dati dell'evento. Tenere presente che, mentre il monitoraggio dispone ancora di un puntatore alle stringhe in una struttura [**NMEVENTDATA**](nmeventdata.md) allocata, è necessario liberare la memoria per queste stringhe prima di chiamare il metodo **FreeEventData** .

Per ulteriori informazioni su come allocare memoria per una struttura [**NMEVENTDATA**](nmeventdata.md) , vedere [**IMonitorEventer:: GetEventData**](imonitoreventer-geteventdata.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMonitorEventer**](imonitoreventer.md)
</dt> <dt>

[**IMonitorEventer::GetEventData**](imonitoreventer-geteventdata.md)
</dt> <dt>

[**NMEVENTDATA**](nmeventdata.md)
</dt> </dl>

 

 




