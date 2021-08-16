---
description: Il tipo di enumerazione WPD WHITE BALANCE SETTINGS descrive in che modo un dispositivo video o immagine pondera i canali di colore \_ \_ per ottenere un \_ bilanciamento del bianco appropriato.
ms.assetid: 7bc173dd-4fdd-4b03-994e-f0711c910618
title: WPD_WHITE_BALANCE_SETTINGS enumerazione (PortableDevice.h)
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
ms.openlocfilehash: 1b596dd6d8fbcc2b2a875b70d80e8eb4040c966590642a004c551ec159c9f5d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117842048"
---
# <a name="wpd_white_balance_settings-enumeration"></a>Enumerazione WPD \_ WHITE \_ BALANCE \_ SETTINGS

Il **tipo di enumerazione WPD WHITE BALANCE \_ \_ \_ SETTINGS** descrive in che modo un dispositivo video o immagine pondera i canali di colore per ottenere un bilanciamento del bianco appropriato.

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

<span id="WPD_WHITE_BALANCE_UNDEFINED"></span><span id="wpd_white_balance_undefined"></span>**BILANCIAMENTO DEL \_ BIANCO WPD \_ NON \_ DEFINITO**
</dt> <dd>

Questo valore non è stato definito.

</dd> <dt>

<span id="WPD_WHITE_BALANCE_MANUAL"></span><span id="wpd_white_balance_manual"></span>**MANUALE PER IL \_ BILANCIAMENTO DEL \_ BIANCO WPD \_**
</dt> <dd>

Il bilanciamento del bianco viene impostato in modo esplicito usando la proprietà [WPD \_ STILL \_ IMAGE \_ RGB \_ GAIN](still-image-properties.md) e non cambia da solo.

</dd> <dt>

<span id="WPD_WHITE_BALANCE_AUTOMATIC"></span><span id="wpd_white_balance_automatic"></span>**BILANCIAMENTO DEL \_ BIANCO WPD \_ \_ AUTOMATICO**
</dt> <dd>

Il dispositivo imposta il bilanciamento del bianco.

</dd> <dt>

<span id="WPD_WHITE_BALANCE_ONE_PUSH_AUTOMATIC"></span><span id="wpd_white_balance_one_push_automatic"></span>**WPD \_ WHITE \_ BALANCE \_ ONE \_ PUSH \_ AUTOMATIC**
</dt> <dd>

Il dispositivo imposterà il bilanciamento del bianco, ma solo quando l'utente preme il pulsante di acquisizione del dispositivo mentre punta il dispositivo a un campo bianco.

</dd> <dt>

<span id="WPD_WHITE_BALANCE_DAYLIGHT"></span><span id="wpd_white_balance_daylight"></span>**WPD \_ WHITE \_ BALANCE \_ DAYLIGHT**
</dt> <dd>

Il dispositivo userà i numeri di bilanciamento del bianco appropriati per l'uso nella maggior parte delle impostazioni di ora legale.

</dd> <dt>

<span id="WPD_WHITE_BALANCE_TUNGSTEN"></span><span id="wpd_white_balance_tungsten"></span>**WPD \_ WHITE \_ BALANCE \_ TUNGSTEN**
</dt> <dd>

Il dispositivo userà numeri di bilanciamento del bianco appropriati per l'uso nella maggior parte delle impostazioni di illuminazione interna e incandescente.

</dd> <dt>

<span id="WPD_WHITE_BALANCE_FLASH"></span><span id="wpd_white_balance_flash"></span>**WPD \_ WHITE \_ BALANCE \_ FLASH**
</dt> <dd>

Il dispositivo userà i numeri di bilanciamento del bianco appropriati per l'uso con un flash.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa enumerazione viene usata dalla [proprietà \_ WPD STILL IMAGE WHITE \_ \_ \_ BALANCE.](still-image-properties.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Strutture e tipi di enumerazione**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




