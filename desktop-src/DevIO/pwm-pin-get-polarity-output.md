---
description: Contiene un valore di polarità da restituire.
ms.assetid: 432C10EF-AC08-4781-9BCA-A31E0DF12704
title: Struttura PWM_PIN_GET_POLARITY_OUTPUT (PWM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PWM_PIN_GET_POLARITY_OUTPUT
api_type:
- HeaderDef
api_location:
- Pwm.h
ms.openlocfilehash: 81cf7b658a0024c3280db1523af34aaf2ef17262
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966085"
---
# <a name="pwm_pin_get_polarity_output-structure"></a>Struttura di output del pin PWM per \_ ottenere la \_ \_ polarità \_

\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Contiene un valore di polarità da restituire.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _PWM_PIN_GET_POLARITY_OUTPUT {
  PWM_POLARITY Polarity;
} PWM_PIN_GET_POLARITY_OUTPUT;
```



## <a name="members"></a>Members

<dl> <dt>

**Polarità**
</dt> <dd>

Polarità del PIN o del canale come valore di [**\_ polarità PWM**](/windows/desktop/api/Pwm/ne-pwm-pwm_polarity) . La polarità è attiva alta o attiva bassa.

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

[**\_ \_ \_ polarità pin IOCTL \_ PWM**](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_GET\_POLARITY**)
</dt> <dt>

[**\_polarità PWM**](/windows/win32/api/pwm/ne-pwm-pwm_polarity)
</dt> </dl>

 

