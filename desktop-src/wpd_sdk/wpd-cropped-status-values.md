---
description: Il \_ \_ tipo di enumerazione dei valori di stato ritagliati WPD \_ descrive lo stato di ritaglio di un'immagine.
ms.assetid: 7ee87fb7-1d17-4e89-aee7-e7abacbd790d
title: Enumerazione WPD_CROPPED_STATUS_VALUES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_CROPPED_STATUS_VALUES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 3f324fd90e58e486a12bffebde9f844d96c3ed83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324214"
---
# <a name="wpd_cropped_status_values-enumeration"></a>\_ \_ Enumerazione dei valori di stato ritagliati WPD \_

Il tipo di enumerazione dei **\_ \_ \_ valori di stato ritagliati WPD** descrive lo stato di ritaglio di un'immagine.

## <a name="syntax"></a>Sintassi


```C++
typedef enum WPD_CROPPED_STATUS_VALUES { 
  WPD_CROPPED_STATUS_NOT_CROPPED            = 0,
  WPD_CROPPED_STATUS_CROPPED                = 1,
  WPD_CROPPED_STATUS_SHOULD_NOT_BE_CROPPED  = 2
} ;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="WPD_CROPPED_STATUS_NOT_CROPPED"></span><span id="wpd_cropped_status_not_cropped"></span>**\_stato ritagliato WPD \_ \_ non \_ ritagliato**
</dt> <dd>

L'immagine non è stata ritagliata.

</dd> <dt>

<span id="WPD_CROPPED_STATUS_CROPPED"></span><span id="wpd_cropped_status_cropped"></span>**stato ritagliato WPD \_ \_ \_**
</dt> <dd>

L'immagine è stata ritagliata.

</dd> <dt>

<span id="WPD_CROPPED_STATUS_SHOULD_NOT_BE_CROPPED"></span><span id="wpd_cropped_status_should_not_be_cropped"></span>**\_lo stato ritagliato WPD \_ \_ \_ non deve \_ essere \_ ritagliato**
</dt> <dd>

L'immagine non è stata e non deve essere ritagliata.

</dd> </dl>

## <a name="remarks"></a>Commenti

Indica lo stato ritagliato di un'immagine. Questa enumerazione viene utilizzata dalla proprietà [di \_ \_ \_ stato ritagliata immagine WPD](image-properties.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Strutture e tipi di enumerazione**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




