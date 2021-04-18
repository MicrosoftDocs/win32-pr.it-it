---
description: Il \_ \_ \_ tipo di enumerazione WPD SMS Encoding types descrive il tipo di codifica di un messaggio SMS (Short Message Service).
ms.assetid: 5a9752e5-4e09-42a4-8fed-b4ea551fa36f
title: Enumerazione WPD_SMS_ENCODING_TYPES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_SMS_ENCODING_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: f7deae3cdc560e27e19b5ff7664e5566cff6d7e1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331721"
---
# <a name="wpd_sms_encoding_types-enumeration"></a>\_ \_ Enumerazione tipi di codifica SMS di WPD \_

Il tipo di enumerazione **WPD \_ SMS \_ Encoding \_ types** descrive il tipo di codifica di un messaggio SMS (Short Message Service).

## <a name="syntax"></a>Sintassi


```C++
typedef enum WPD_SMS_ENCODING_TYPES { 
  SMS_ENCODING_7_BIT   = 0,
  SMS_ENCODING_8_BIT   = 1,
  SMS_ENCODING_UTF_16  = 2
} ;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="SMS_ENCODING_7_BIT"></span><span id="sms_encoding_7_bit"></span>**\_Codifica SMS \_ 7 \_ bit**
</dt> <dd>

Codifica a sette bit.

</dd> <dt>

<span id="SMS_ENCODING_8_BIT"></span><span id="sms_encoding_8_bit"></span>**\_Codifica SMS \_ 8 \_ bit**
</dt> <dd>

Codifica a 8 bit.

</dd> <dt>

<span id="SMS_ENCODING_UTF_16"></span><span id="sms_encoding_utf_16"></span>**\_Codifica SMS \_ UTF \_ 16**
</dt> <dd>

Codifica a 16 bit (UTF).

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa enumerazione viene utilizzata dalla proprietà [di \_ \_ codifica SMS di WPD](sms-properties.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Strutture e tipi di enumerazione**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




