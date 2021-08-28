---
title: DRV_REMOVE messaggio (Mmsystem.h)
description: Notifica al driver che sta per essere rimosso dal sistema. Quando un driver riceve questo messaggio, deve rimuovere tutte le sezioni create nel Registro di sistema.
ms.assetid: e4f6ce7c-29e5-4256-b08a-13571256207c
keywords:
- DRV_REMOVE di messaggi Windows multimediali
topic_type:
- apiref
api_name:
- DRV_REMOVE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c08302d69e934ec77908b247f3c8f6368de8de4eab36809b6102b74858adde5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119496421"
---
# <a name="drv_remove-message"></a>Messaggio DRV \_ REMOVE

Notifica al driver che sta per essere rimosso dal sistema. Quando un driver riceve questo messaggio, deve rimuovere tutte le sezioni create nel Registro di sistema.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*
</dt> <dd>

Identificatore del driver installabile. Si tratta dello stesso valore restituito in precedenza dal driver dal [**messaggio DRV \_ OPEN.**](drv-open.md)

</dd> <dt>

<span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*
</dt> <dd>

Handle dell'istanza del driver installabile.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

I *parametri lParam1* *e lParam2* non vengono usati.

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

 

 





