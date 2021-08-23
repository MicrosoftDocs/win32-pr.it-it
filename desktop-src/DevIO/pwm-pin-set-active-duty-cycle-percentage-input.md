---
description: Contiene una percentuale di ciclo di lavoro desiderata per un pin o un canale in un controller PWM (Pulse Width Modulation).
ms.assetid: CA699703-2D9B-4841-99AD-9C27FF428394
title: PWM_PIN_SET_ACTIVE_DUTY_CYCLE_PERCENTAGE_INPUT (Pwm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PWM_PIN_SET_ACTIVE_DUTY_CYCLE_PERCENTAGE_INPUT
api_type:
- HeaderDef
api_location:
- Pwm.h
ms.openlocfilehash: ca6b2ee6aa4d4d2da3f94aa7cc471de12c1f8040b597edf568bf061c8e392aa1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758851"
---
# <a name="pwm_pin_set_active_duty_cycle_percentage_input-structure"></a>PWM \_ PIN SET ACTIVE DUTY CYCLE PERCENTAGE INPUT \_ \_ \_ \_ \_ \_ structure

\[Alcune informazioni riguardano un prodotto pre-rilasciato che può essere modificato sostanzialmente prima del rilascio in commercio. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Contiene una percentuale di ciclo di lavoro desiderata per un pin o un canale in un controller PWM (Pulse Width Modulation).

## <a name="syntax"></a>Sintassi


```C++
typedef struct _PWM_PIN_SET_ACTIVE_DUTY_CYCLE_PERCENTAGE_INPUT {
  PWM_PERCENTAGE Percentage;
} PWM_PIN_SET_ACTIVE_DUTY_CYCLE_PERCENTAGE_INPUT;
```



## <a name="members"></a>Members

<dl> <dt>

**Percentuale**
</dt> <dd>

Ciclo di lavoro del segnale PWM desiderato, come percentuale PWM, \_ che è un valore ULONGLONG.

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

[**IOCTL PWM PIN SET ACTIVE DUTY CYCLE PERCENTAGE (PERCENTUALE CICLO DI LAVORO ATTIVO IMPOSTATO \_ \_ SU PWM \_ \_ \_ \_ \_ IOCTL)**](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_SET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE**)
</dt> </dl>

 

 




