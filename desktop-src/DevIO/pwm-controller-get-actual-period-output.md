---
description: Contiene il periodo di segnale di output effettivo per un controller PWM (Pulse Width Modulation).
ms.assetid: 280F564F-FF7F-4121-B726-9F9AF9E98EB7
title: Struttura PWM_CONTROLLER_GET_ACTUAL_PERIOD_OUTPUT (PWM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PWM_CONTROLLER_GET_ACTUAL_PERIOD_OUTPUT
api_type:
- HeaderDef
api_location:
- Pwm.h
ms.openlocfilehash: f63057299a8ef37ed1b38151958d2e0061ad2727
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748343"
---
# <a name="pwm_controller_get_actual_period_output-structure"></a>Il \_ controller PWM \_ ottiene la struttura di \_ \_ output del periodo effettivo \_

\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Contiene il periodo di segnale di output effettivo per un controller PWM (Pulse Width Modulation).

## <a name="syntax"></a>Sintassi


```C++
typedef struct _PWM_CONTROLLER_GET_ACTUAL_PERIOD_OUTPUT {
  PWM_PERIOD ActualPeriod;
} PWM_CONTROLLER_GET_ACTUAL_PERIOD_OUTPUT;
```



## <a name="members"></a>Members

<dl> <dt>

**ActualPeriod**
</dt> <dd>

Il periodo effettivo del segnale di output viene misurato nei canali di output del controller.

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

[**\_controller IOCTL PWM \_ ottiene il \_ \_ \_ periodo effettivo**](https://www.bing.com/search?q=**IOCTL\_PWM\_CONTROLLER\_GET\_ACTUAL\_PERIOD**)
</dt> </dl>

 

 




