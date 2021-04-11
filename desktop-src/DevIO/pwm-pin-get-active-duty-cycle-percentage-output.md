---
description: Contiene la percentuale del ciclo di lavoro corrente per un PIN o un canale in un controller PWM (Pulse Width Modulation).
ms.assetid: 09C0232A-DF5C-4A1C-8138-D3D65E45731B
title: Struttura PWM_PIN_GET_ACTIVE_DUTY_CYCLE_PERCENTAGE_OUTPUT (PWM. h)
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
ms.openlocfilehash: 607fcb1ab429e7cbe9aee593f75d48f0f9d308bd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126771"
---
# <a name="pwm_pin_get_active_duty_cycle_percentage_output-structure"></a>\_Struttura di \_ \_ \_ \_ \_ output percentuale del ciclo di dazio attivo \_ per pin PWM

\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Contiene la percentuale del ciclo di lavoro corrente per un PIN o un canale in un controller PWM (Pulse Width Modulation).

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

Il ciclo del dazio del segnale PWM corrente, come \_ percentuale di PWM, che è un valore ULONGLONG.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                                      |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2016\]<br/>                                             |
| Versione KMDF minima<br/>     | 1,19<br/>                                                                                  |
| Versione UMDF minima<br/>     | 2.19<br/>                                                                                  |
| Intestazione<br/>                   | <dl> <dt>PWM. h (incluso PWM. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_percentuale del \_ ciclo di lavoro per pin PWM \_ get \_ attivo \_ \_ \_**](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_GET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE**)
</dt> </dl>

 

 




