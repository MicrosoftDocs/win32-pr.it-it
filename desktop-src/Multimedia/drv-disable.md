---
title: DRV_DISABLE messaggio (Mmsystem.h)
description: Disabilita il driver. Il driver deve inserire il dispositivo corrispondente, se presente, in uno stato inattivo e terminare eventuali funzioni o thread di callback.
ms.assetid: 83e99397-6f0e-4174-9f96-e10c1f17ef0b
keywords:
- DRV_DISABLE di Windows multimediali
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
ms.openlocfilehash: 75d9c5a99414f0b755efbae005365d89665a2b2bc5a4673436101066ec740564
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144414"
---
# <a name="drv_disable-message"></a>Messaggio DRV \_ DISABLE

Disabilita il driver. Il driver deve inserire il dispositivo corrispondente, se presente, in uno stato inattivo e terminare eventuali funzioni o thread di callback.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*
</dt> <dd>

Handle dell'istanza del driver installabile.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

I *parametri dwDriverId*, *lParam1* e *lParam2* non vengono usati.

Dopo aver disabilitato il driver, il sistema in genere invia al driver un messaggio [**DRV \_ FREE**](drv-free.md) prima di rimuovere il driver dalla memoria.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Mmsystem.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Driver installabili](installable-drivers.md)
</dt> <dt>

[Messaggi di driver installabili](installable-driver-messages.md)
</dt> </dl>

 

 





