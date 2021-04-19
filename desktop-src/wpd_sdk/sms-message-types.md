---
description: Il \_ \_ tipo di enumerazione dei tipi di messaggio SMS descrive il tipo di contenuto di un messaggio SMS (Short Message Service).
ms.assetid: 882886a6-ecce-443f-a7e9-2e4e367ad804
title: Enumerazione SMS_MESSAGE_TYPES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SMS_MESSAGE_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: a2e1ccfd074ff1f5287af22c5a8ebb3c6b3c661d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326596"
---
# <a name="sms_message_types-enumeration"></a>\_Enumerazione tipi di messaggio SMS \_

Il tipo di enumerazione dei **\_ \_ tipi di messaggio SMS** descrive il tipo di contenuto di un messaggio SMS (Short Message Service).

## <a name="syntax"></a>Sintassi


```C++
typedef enum SMS_MESSAGE_TYPES { 
  SMS_TEXT_MESSAGE    = 0,
  SMS_BINARY_MESSAGE  = 1
} ;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="SMS_TEXT_MESSAGE"></span><span id="sms_text_message"></span>**SMS \_ \_**
</dt> <dd>

Messaggio di testo.

</dd> <dt>

<span id="SMS_BINARY_MESSAGE"></span><span id="sms_binary_message"></span>**\_messaggio binario \_ SMS**
</dt> <dd>

Messaggio binario.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa enumerazione viene utilizzata dal comando [**WPD \_ \_ SMS \_ Send**](wpd-command-sms-send-command.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Strutture e tipi di enumerazione**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




