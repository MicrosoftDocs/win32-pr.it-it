---
title: DRV_ENABLE messaggio (Mmsystem.h)
description: Abilita il driver. Il driver deve inizializzare le variabili e individuare i dispositivi con l'interfaccia di input e output (I/O).
ms.assetid: 8aa36f3d-b36c-4460-859c-108a7a450ae5
keywords:
- DRV_ENABLE messaggio Windows Multimediali
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
ms.openlocfilehash: e7ab74abf08380db97a15da22fa99d58d72b6aba124a430cad665f65bc94e26c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526281"
---
# <a name="drv_enable-message"></a>Messaggio DRV \_ ENABLE

Abilita il driver. Il driver deve inizializzare le variabili e individuare i dispositivi con l'interfaccia di input e output (I/O).

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

I driver vengono considerati abilitati dal momento in cui ricevono questo messaggio fino a quando non vengono disabilitati usando [**il messaggio DRV \_ DISABLE.**](drv-disable.md)

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

 

 





