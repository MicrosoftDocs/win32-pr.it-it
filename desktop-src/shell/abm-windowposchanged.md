---
description: Notifica al sistema quando la posizione di un'appbar è stata modificata. Un'appbar deve chiamare questo messaggio in risposta al messaggio WM \_ WINDOWPOSCHANGED.
ms.assetid: 8ca51f5f-b6cf-4f2c-98f4-69c992679320
title: ABM_WINDOWPOSCHANGED messaggio (Shellapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d770d50629342095308376856b98e6250adc1f9a1f2559da8509d685995428ac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057811"
---
# <a name="abm_windowposchanged-message"></a>Messaggio ABM \_ WINDOWPOSCHANGED

Notifica al sistema quando la posizione di un'appbar è stata modificata. Un'appbar deve chiamare questo messaggio in risposta al [**messaggio WM \_ WINDOWPOSCHANGED.**](/windows/desktop/winmsg/wm-windowposchanged)


```C++
SHAppBarMessage(ABM_WINDOWPOSCHANGED, pabd); 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pabd* 
</dt> <dd>

Puntatore a una [**struttura APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) che identifica la barra dell'app da attivare. È necessario specificare i **membri cbSize** **e hWnd** quando si invia questo messaggio. tutti gli altri membri vengono ignorati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce sempre **TRUE.**

## <a name="remarks"></a>Commenti

Questo messaggio viene ignorato se il **membro hWnd** della struttura a cui punta *pabd* identifica una barra dell'app con rilevamento automatico.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Shellapi.h</dt> </dl> |



 

