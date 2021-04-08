---
title: Messaggio DRV_FREE (mmsystem. h)
description: Notifica al driver che è stata rimossa dalla memoria. Il driver deve liberare memoria e altre risorse di sistema allocate.
ms.assetid: 0447f8e9-4c4d-4be5-ab1f-ecd3e8cd2e67
keywords:
- DRV_FREE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- DRV_FREE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abb9d70d269cb84e0d6ef0881618b67cfef11068
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964919"
---
# <a name="drv_free-message"></a>\_Messaggio privo di DRV

Notifica al driver che è stata rimossa dalla memoria. Il driver deve liberare memoria e altre risorse di sistema allocate.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*
</dt> <dd>

Handle dell'istanza del driver installabile.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

I parametri *dwDriverId*, *lParam1* e *lParam2* non vengono usati.

Il messaggio **drv \_ Free** è sempre l'ultimo messaggio ricevuto da un driver di dispositivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Mmsystem. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Driver installabili](installable-drivers.md)
</dt> <dt>

[Messaggi di driver installabili](installable-driver-messages.md)
</dt> </dl>

 

 





