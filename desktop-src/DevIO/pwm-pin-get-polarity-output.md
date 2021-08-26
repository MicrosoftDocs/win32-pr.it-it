---
description: Contiene un valore di polarità da restituire.
ms.assetid: 432C10EF-AC08-4781-9BCA-A31E0DF12704
title: PWM_PIN_GET_POLARITY_OUTPUT (Pwm.h)
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
ms.openlocfilehash: 7d4c3103663ceac65deff7744b0cf45a21a787959cc6e866bde5ac8673f7f64a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984431"
---
# <a name="pwm_pin_get_polarity_output-structure"></a>Struttura DI \_ OUTPUT \_ GET \_ POLARITY DEL PIN PWM \_

\[Alcune informazioni riguardano un prodotto pre-rilasciato che può essere modificato sostanzialmente prima del rilascio in commercio. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

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

Polarità del pin o del canale come valore [**\_ POLARITY PWM.**](/windows/desktop/api/Pwm/ne-pwm-pwm_polarity) La polarità è Active High o Active Low.

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

[**IOCTL \_ PWM \_ PIN \_ GET \_ POLARITY**](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_GET\_POLARITY**)
</dt> <dt>

[**POLARITÀ \_ PWM**](/windows/win32/api/pwm/ne-pwm-pwm_polarity)
</dt> </dl>

 

