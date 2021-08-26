---
description: Contiene la percentuale corrente del ciclo di lavoro per un pin o un canale in un controller PWM (Pulse Width Modulation).
ms.assetid: 09C0232A-DF5C-4A1C-8138-D3D65E45731B
title: PWM_PIN_GET_ACTIVE_DUTY_CYCLE_PERCENTAGE_OUTPUT struttura (Pwm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PWM_PIN_GET_ACTIVE_DUTY_CYCLE_PERCENTAGE_OUTPUT
api_type:
- HeaderDef
api_location:
- Pwm.h
ms.openlocfilehash: dda05c06ee8c53968647bc29da2febee14abf758d4ad228c16178703c2d1da08
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053321"
---
# <a name="pwm_pin_get_active_duty_cycle_percentage_output-structure"></a>PWM \_ PIN GET ACTIVE DUTY CYCLE PERCENTAGE OUTPUT \_ \_ \_ \_ \_ \_ structure

\[Alcune informazioni riguardano prodotti pre-rilasciati che possono essere modificati in modo sostanziale prima che venga rilasciato commercialmente. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Contiene la percentuale corrente del ciclo di lavoro per un pin o un canale in un controller PWM (Pulse Width Modulation).

## <a name="syntax"></a>Sintassi


```C++
typedef struct _PWM_PIN_GET_ACTIVE_DUTY_CYCLE_PERCENTAGE_OUTPUT {
  PWM_PERCENTAGE Percentage;
} PWM_PIN_GET_ACTIVE_DUTY_CYCLE_PERCENTAGE_OUTPUT;
```



## <a name="members"></a>Members

<dl> <dt>

**Percentuale**
</dt> <dd>

Ciclo di servizio del segnale PWM corrente, come PWM \_ PERCENTAGE, che è un valore ULONGLONG.

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

[**IOCTL \_ PWM \_ PIN \_ GET \_ ACTIVE \_ DUTY \_ CYCLE \_ PERCENTAGE**](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_GET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE**)
</dt> </dl>

 

 




