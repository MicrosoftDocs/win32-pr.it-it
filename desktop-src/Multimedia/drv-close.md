---
title: DRV_CLOSE messaggio (Mmsystem.h)
description: Indica al driver di chiudere l'istanza specificata. Se non sono aperte altre istanze, il driver deve prepararsi per il rilascio successivo dalla memoria.
ms.assetid: 98d7fe47-5194-4912-a9d6-3af3d1fa4e60
keywords:
- DRV_CLOSE messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- DRV_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d89be1821b03e43fbe05b5ed2efc90e40db03e36538cf0412201baa7273e596
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118622668"
---
# <a name="drv_close-message"></a>Messaggio CLOSE di \_ DRV

Indica al driver di chiudere l'istanza specificata. Se non sono aperte altre istanze, il driver deve prepararsi per il rilascio successivo dalla memoria.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*
</dt> <dd>

Identificatore del driver installabile. Si tratta dello stesso valore restituito in precedenza dal driver dal [**messaggio DRV \_ OPEN.**](drv-open.md)

</dd> <dt>

<span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*
</dt> <dd>

Handle dell'istanza del driver installabile.

</dd> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Valore a 32 bit specificato come parametro *lParam1* in una chiamata alla **funzione DriverClose.**

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Valore a 32 bit specificato come *parametro lParam2* in una chiamata alla **funzione DriverClose.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero se ha esito positivo o zero in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Mmsystem.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Driver installabili](installable-drivers.md)
</dt> <dt>

[Messaggi del driver installabili](installable-driver-messages.md)
</dt> </dl>

 

 





