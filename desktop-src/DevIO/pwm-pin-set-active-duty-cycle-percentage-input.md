---
description: Contiene una percentuale del ciclo di lavoro desiderata per un PIN o un canale in un controller PWM (Pulse Width Modulation).
ms.assetid: CA699703-2D9B-4841-99AD-9C27FF428394
title: Struttura PWM_PIN_SET_ACTIVE_DUTY_CYCLE_PERCENTAGE_INPUT (PWM. h)
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
ms.openlocfilehash: 98811ace7ce8fce760e10757b8bf012cc2b9b27d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401366"
---
# <a name="pwm_pin_set_active_duty_cycle_percentage_input-structure"></a>\_Struttura di \_ \_ \_ \_ \_ input percentuale del ciclo di lavoro attivo \_ per il pin PWM

\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Contiene una percentuale del ciclo di lavoro desiderata per un PIN o un canale in un controller PWM (Pulse Width Modulation).

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

Il ciclo di servizio del segnale PWM desiderato, come \_ percentuale di PWM, che è un valore ULONGLONG.

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

[**\_percentuale del \_ \_ ciclo di \_ \_ dazio attivo \_ set \_ di pin IOCTL**](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_SET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE**)
</dt> </dl>

 

 




