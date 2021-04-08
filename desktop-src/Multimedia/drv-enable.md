---
title: Messaggio DRV_ENABLE (mmsystem. h)
description: Consente di abilitare il driver. Il driver deve inizializzare qualsiasi variabile e individuare i dispositivi con l'interfaccia di input e output (I/O).
ms.assetid: 8aa36f3d-b36c-4460-859c-108a7a450ae5
keywords:
- DRV_ENABLE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- DRV_ENABLE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 569b4ca5f3d0dc5f439b1e2b0e25887ffd1da4ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964922"
---
# <a name="drv_enable-message"></a>\_Messaggio di abilitazione DRV

Consente di abilitare il driver. Il driver deve inizializzare qualsiasi variabile e individuare i dispositivi con l'interfaccia di input e output (I/O).

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

I driver vengono considerati abilitati dal momento in cui ricevono questo messaggio finché non vengono disabilitati usando il messaggio di [**\_ disabilitazione DRV**](drv-disable.md) .

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

 

 





