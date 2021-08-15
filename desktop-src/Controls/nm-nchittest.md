---
title: NM_NCHITTEST di notifica (Commctrl.h)
description: 'NM_NCHITTEST di notifica: inviato da un controllo Rebar quando il controllo riceve un messaggio \_ WM NCHITTEST. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.'
ms.assetid: 0e088b14-b912-4f60-9d25-cd0a0ba264c3
keywords:
- NM_NCHITTEST del codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- NM_NCHITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab16a835e5e321b916f27b6c79141495f3c05cd4ca8e979e77fef50f84e2ca83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118410692"
---
# <a name="nm_nchittest-notification-code"></a>Codice \_ di notifica NM NCHITTEST

Inviato da un controllo Rebar quando il controllo riceve un [**messaggio \_ WM NCHITTEST.**](/windows/desktop/inputdev/wm-nchittest) Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_NCHITTEST
        
    lpnmmouse = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) che contiene informazioni sul codice di notifica. Il *membro pt* contiene le coordinate del mouse del messaggio di hit test.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se non diversamente specificato, restituire zero per consentire al controllo di eseguire l'elaborazione predefinita del messaggio di hit test o restituire uno dei valori HT documentati in \* [**WM \_ NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) per eseguire l'override dell'elaborazione dell'hit test predefinita.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

