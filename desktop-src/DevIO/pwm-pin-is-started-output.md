---
description: Contiene lo stato di generazione del segnale corrente di un pin.
ms.assetid: 07D76F8D-C5B5-4500-BFA2-452989868027
title: PWM_PIN_IS_STARTED_OUTPUT (Pwm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PWM_PIN_IS_STARTED_OUTPUT
api_type:
- HeaderDef
api_location:
- Pwm.h
ms.openlocfilehash: 448b38e66b7cfb4bf7e24c5d3b7658d0e38ccb8a5ca8c95e1155129737087c68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076185"
---
# <a name="pwm_pin_is_started_output-structure"></a>STRUTTURA DI \_ OUTPUT AVVIATA DEL PIN PWM \_ \_ \_

\[Alcune informazioni riguardano un prodotto pre-rilasciato che può essere modificato sostanzialmente prima del rilascio in commercio. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Contiene lo stato di generazione del segnale corrente di un pin.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _PWM_PIN_IS_STARTED_OUTPUT {
  BOOLEAN IsStarted;
} PWM_PIN_IS_STARTED_OUTPUT;
```



## <a name="members"></a>Members

<dl> <dt>

**IsStarted**
</dt> <dd>

Stato di generazione del segnale corrente del pin. Il valore true indica che il pin viene avviato. Il valore false indica che il pin è arrestato.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                                      |
| Server minimo supportato<br/> | \[Windows Server 2016 solo app desktop\]<br/>                                             |
| Versione KMDF minima<br/>     | 1,19<br/>                                                                                  |
| Versione UMDF minima<br/>     | 2.19<br/>                                                                                  |
| Intestazione<br/>                   | <dl> <dt>Pwm.h (includere Pwm.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IL PIN PWM IOCTL \_ \_ È STATO \_ \_ AVVIATO**](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_IS\_STARTED**)
</dt> </dl>

 

 




