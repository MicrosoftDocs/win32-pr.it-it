---
description: Il \_ \_ \_ tipo di enumerazione delle impostazioni di bilanciamento del bianco WPD descrive il modo in cui un dispositivo video o immagine pondera i canali di colore per ottenere un giusto equilibrio bianco.
ms.assetid: 7bc173dd-4fdd-4b03-994e-f0711c910618
title: Enumerazione WPD_WHITE_BALANCE_SETTINGS (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_WHITE_BALANCE_SETTINGS
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 06e607acc06ed00cc9fe91670650caee44c30430
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327258"
---
# <a name="wpd_white_balance_settings-enumeration"></a>\_ \_ Enumerazione impostazioni bilanciamento bianco WPD \_

Il tipo di enumerazione **\_ \_ \_ delle impostazioni di bilanciamento del bianco WPD** descrive il modo in cui un dispositivo video o immagine pondera i canali di colore per ottenere un giusto equilibrio bianco.

## <a name="syntax"></a>Sintassi


```C++
typedef enum WPD_WHITE_BALANCE_SETTINGS { 
  WPD_WHITE_BALANCE_UNDEFINED           = 0,
  WPD_WHITE_BALANCE_MANUAL              = 1,
  WPD_WHITE_BALANCE_AUTOMATIC           = 2,
  WPD_WHITE_BALANCE_ONE_PUSH_AUTOMATIC  = 3,
  WPD_WHITE_BALANCE_DAYLIGHT            = 4,
  WPD_WHITE_BALANCE_TUNGSTEN            = 5,
  WPD_WHITE_BALANCE_FLASH               = 6
} ;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="WPD_WHITE_BALANCE_UNDEFINED"></span><span id="wpd_white_balance_undefined"></span>**\_bilanciamento bianco WPD non \_ \_ definito**
</dt> <dd>

Questo valore non è stato definito.

</dd> <dt>

<span id="WPD_WHITE_BALANCE_MANUAL"></span><span id="wpd_white_balance_manual"></span>**\_Manuale di \_ bilanciamento del bianco WPD \_**
</dt> <dd>

Il bilanciamento bianco viene impostato in modo esplicito tramite la proprietà [WPD \_ still \_ Image \_ RGB \_ Gain](still-image-properties.md) e non verrà modificato da solo.

</dd> <dt>

<span id="WPD_WHITE_BALANCE_AUTOMATIC"></span><span id="wpd_white_balance_automatic"></span>**\_bilanciamento del bianco WPD \_ \_ automatico**
</dt> <dd>

Il dispositivo imposterà il saldo bianco.

</dd> <dt>

<span id="WPD_WHITE_BALANCE_ONE_PUSH_AUTOMATIC"></span><span id="wpd_white_balance_one_push_automatic"></span>**\_bilanciamento del bianco WPD \_ \_ One \_ push \_ automatico**
</dt> <dd>

Il dispositivo imposterà il saldo bianco, ma solo quando l'utente preme il pulsante di acquisizione del dispositivo puntando al dispositivo in un campo bianco.

</dd> <dt>

<span id="WPD_WHITE_BALANCE_DAYLIGHT"></span><span id="wpd_white_balance_daylight"></span>**WPD \_ di \_ bilanciamento del bianco \_**
</dt> <dd>

Il dispositivo utilizzerà i numeri di bilancia bianca appropriati per l'uso nella maggior parte delle impostazioni dell'ora legale.

</dd> <dt>

<span id="WPD_WHITE_BALANCE_TUNGSTEN"></span><span id="wpd_white_balance_tungsten"></span>**WPD \_ bilanciamento del bianco di \_ \_ tungsteno**
</dt> <dd>

Il dispositivo utilizzerà i numeri di bilancia bianca appropriati per l'uso nella maggior parte delle impostazioni di illuminazione incandescenza interna.

</dd> <dt>

<span id="WPD_WHITE_BALANCE_FLASH"></span><span id="wpd_white_balance_flash"></span>**\_ \_ Flash Bilanciamento bianco \_ WPD**
</dt> <dd>

Il dispositivo utilizzerà i numeri di bilancia bianca appropriati per l'uso con Flash.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa enumerazione viene utilizzata dalla proprietà [di \_ \_ bilanciamento del \_ bianco \_ WPD Still Image](still-image-properties.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Strutture e tipi di enumerazione**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




