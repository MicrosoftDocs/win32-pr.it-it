---
title: Messaggio DRV_OPEN (mmsystem. h)
description: Indica al driver di aprire una nuova istanza.
ms.assetid: 6b5e21e3-dc29-4f0f-84cb-bd2d2e3c54e9
keywords:
- DRV_OPEN messaggi multimediali di Windows
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
ms.openlocfilehash: 53c56e62cb85f09a3846c6d95d723b9fa05d95a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121466"
---
# <a name="drv_open-message"></a>\_Messaggio aperto DRV

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

Indirizzo di una stringa di caratteri wide con terminazione null che specifica le informazioni di configurazione utilizzate per aprire l'istanza. Se non sono disponibili informazioni di configurazione, la stringa è vuota o il parametro è **null**.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

dati specifici del driver a 32 bit.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero se ha esito positivo o zero in caso contrario.

## <a name="remarks"></a>Commenti

Se il driver restituisce un valore diverso da zero, il sistema utilizza tale valore come identificatore del driver (il parametro *dwDriverId* ) nei messaggi inviati successivamente all'istanza del driver. Il driver può restituire qualsiasi tipo di valore come identificatore. Alcuni driver, ad esempio, restituiscono indirizzi di memoria che puntano a informazioni specifiche dell'istanza. L'utilizzo di questo metodo per specificare gli identificatori per un'istanza di driver consente ai driver di accedere alle informazioni durante l'elaborazione dei messaggi.

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

 

 





