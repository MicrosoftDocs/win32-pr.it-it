---
title: Messaggio DRV_DISABLE (mmsystem. h)
description: Disabilita il driver. Il driver deve inserire il dispositivo corrispondente, se presente, in uno stato inattivo e terminare eventuali funzioni di callback o thread.
ms.assetid: 83e99397-6f0e-4174-9f96-e10c1f17ef0b
keywords:
- DRV_DISABLE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- DRV_DISABLE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b512e90612a02681008474c7f1323f17304422d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964920"
---
# <a name="drv_disable-message"></a>\_Messaggio di disabilitazione DRV

Disabilita il driver. Il driver deve inserire il dispositivo corrispondente, se presente, in uno stato inattivo e terminare eventuali funzioni di callback o thread.

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

Dopo la disabilitazione del driver, il sistema invia in genere al driver un messaggio [**drv \_ libero**](drv-free.md) prima di rimuovere il driver dalla memoria.

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

 

 





