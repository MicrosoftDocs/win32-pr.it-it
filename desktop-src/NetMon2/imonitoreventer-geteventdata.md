---
description: Il metodo GetEventData alloca spazio per le strutture NMEVENTDATA e NMCOLUMNINFO.
ms.assetid: b24a2a30-4543-4311-87ec-66872463aed7
title: Metodo IMonitorEventer::GetEventData (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitorEventer.GetEventData
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: 3a089e57ac5f66187f97dfa6ae7533aeda620632bdbf35c7b5bf3a34d4654b0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037371"
---
# <a name="imonitoreventergeteventdata-method"></a>Metodo IMonitorEventer::GetEventData

Il **metodo GetEventData** alloca spazio per le [strutture NMEVENTDATA](nmeventdata.md) e [NMCOLUMNINFO.](nmcolumninfo.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetEventData(
  [in]  BYTE         bNumColumns,
  [out] PNMEVENTDATA *ppNMEventData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bNumColumns* \[ Pollici\]
</dt> <dd>

Numero di **strutture NMCOLUMNINFO** necessarie.

</dd> <dt>

*ppNMEventData* \[ Cambio\]
</dt> <dd>

Indirizzo della **struttura NMEVENTDATA** restituita.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, il valore restituito è S \_ OK.

Se il metodo ha esito negativo, il valore restituito è NMERR \_ OUT \_ OF \_ MEMORY.

## <a name="remarks"></a>Commenti

I monitoraggi chiamano questo metodo per allocare memoria per i dati degli eventi e le strutture di informazioni sulle colonne. Per liberare memoria allocata per **una struttura NMEVENTDATA,** vedere [IMonitorEventer::FreeEventData](imonitoreventer-freeeventdata.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IMonitorEventer](imonitoreventer.md)
</dt> <dt>

[IMonitorEventer::FreeEventData](imonitoreventer-freeeventdata.md)
</dt> <dt>

[NMEVENTDATA](nmeventdata.md)
</dt> <dt>

[NMCOLUMNINFO](nmcolumninfo.md)
</dt> </dl>

 

 




