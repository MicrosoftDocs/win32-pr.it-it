---
description: Il \_ \_ \_ tipo di enumerazione dei valori di stato con correzione del colore WPD \_ descrive lo stato di correzione dei colori di un'immagine o un file video.
ms.assetid: af129a1b-7760-4339-adf7-3f3c17cebde2
title: Enumerazione WPD_COLOR_CORRECTED_STATUS_VALUES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COLOR_CORRECTED_STATUS_VALUES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: ec6bfcaa3933bb70c3064f829e701509e3ff32f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330581"
---
# <a name="wpd_color_corrected_status_values-enumeration"></a>\_ \_ \_ Enumerazione dei valori di stato con correzione del colore WPD \_

Il tipo di enumerazione dei **valori di stato con \_ correzione del colore \_ \_ \_ WPD** descrive lo stato di correzione dei colori di un'immagine o un file video.

## <a name="syntax"></a>Sintassi


```C++
typedef enum WPD_COLOR_CORRECTED_STATUS_VALUES { 
  WPD_COLOR_CORRECTED_STATUS_NOT_CORRECTED            = 0,
  WPD_COLOR_CORRECTED_STATUS_CORRECTED                = 1,
  WPD_COLOR_CORRECTED_STATUS_SHOULD_NOT_BE_CORRECTED  = 2
} ;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="WPD_COLOR_CORRECTED_STATUS_NOT_CORRECTED"></span><span id="wpd_color_corrected_status_not_corrected"></span>**\_stato correzione colore WPD \_ \_ \_ non \_ corretto**
</dt> <dd>

Colore non corretto per l'immagine.

</dd> <dt>

<span id="WPD_COLOR_CORRECTED_STATUS_CORRECTED"></span><span id="wpd_color_corrected_status_corrected"></span>**\_ \_ \_ correzione stato correzione colore \_ WPD**
</dt> <dd>

Il colore dell'immagine è stato corretto.

</dd> <dt>

<span id="WPD_COLOR_CORRECTED_STATUS_SHOULD_NOT_BE_CORRECTED"></span><span id="wpd_color_corrected_status_should_not_be_corrected"></span>**\_ \_ lo stato corretto del colore WPD \_ \_ \_ non deve \_ essere \_ corretto**
</dt> <dd>

L'immagine non è stata e non deve essere con correzione del colore.

</dd> </dl>

## <a name="remarks"></a>Commenti

Indica lo stato corretto del colore di un'immagine. Questa enumerazione viene utilizzata dalla proprietà [ \_ \_ \_ \_ dello stato WPD image correct color](image-properties.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Strutture e tipi di enumerazione**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




