---
title: DRV_QUERYCONFIGURE messaggio (Mmsystem.h)
description: Indica al driver di specificare se supporta la configurazione personalizzata.
ms.assetid: fb2e36a7-8d6b-4b08-b2d7-e128ca7082dc
keywords:
- DRV_QUERYCONFIGURE messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- DRV_QUERYCONFIGURE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22c49ec54d1822bbc9ddc4d2606f8905a21c5193322a12df335549074dacdea3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691571"
---
# <a name="drv_queryconfigure-message"></a>Messaggio \_ DRV QUERYCONFIGURE

Indica al driver di specificare se supporta la configurazione personalizzata.

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

Restituisce un valore diverso da zero se il driver può visualizzare una finestra di dialogo di configurazione oppure zero in caso contrario.

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

 

 





