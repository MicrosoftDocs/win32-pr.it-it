---
title: DRV_OPEN messaggio (Mmsystem.h)
description: Indica al driver di aprire una nuova istanza.
ms.assetid: 6b5e21e3-dc29-4f0f-84cb-bd2d2e3c54e9
keywords:
- DRV_OPEN messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- DRV_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 537d3067c85cf3f92eaf2fae81cd392490ff9fa728ed8377d8241c7204cf64e1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691581"
---
# <a name="drv_open-message"></a>Messaggio DRV \_ OPEN

Indica al driver di aprire una nuova istanza.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*
</dt> <dd>

Identificatore del driver installabile.

</dd> <dt>

<span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*
</dt> <dd>

Handle dell'istanza del driver installabile.

</dd> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Indirizzo di una stringa di caratteri wide con terminazione Null che specifica le informazioni di configurazione usate per aprire l'istanza. Se non sono disponibili informazioni di configurazione, questa stringa è vuota o il parametro è **NULL.**

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Dati specifici del driver a 32 bit.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero in caso di esito positivo o zero in caso contrario.

## <a name="remarks"></a>Commenti

Se il driver restituisce un valore diverso da zero, il sistema usa tale valore come identificatore del driver (il *parametro dwDriverId)* nei messaggi inviati successivamente all'istanza del driver. Il driver può restituire qualsiasi tipo di valore come identificatore. Ad esempio, alcuni driver restituiscono indirizzi di memoria che puntano a informazioni specifiche dell'istanza. L'uso di questo metodo per specificare gli identificatori per un'istanza del driver consente ai driver di accedere prontamente alle informazioni durante l'elaborazione dei messaggi.

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

[Messaggi del driver installabili](installable-driver-messages.md)
</dt> </dl>

 

 





