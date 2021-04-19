---
title: Codice di notifica NM_NCHITTEST (COMmctrl. h)
description: Inviato da un controllo Rebar quando il controllo riceve un \_ messaggio WM NCHITTEST. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 0e088b14-b912-4f60-9d25-cd0a0ba264c3
keywords:
- Controlli di Windows per il codice di notifica NM_NCHITTEST
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
ms.openlocfilehash: f8af39fd792ecb9aeb463957f49f5722737e6ee5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301704"
---
# <a name="nm_nchittest-notification-code"></a>\_Codice di notifica NCHITTEST Nm

Inviato da un controllo Rebar quando il controllo riceve un messaggio [**WM \_ NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) . Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
NM_NCHITTEST
        
    lpnmmouse = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) che contiene informazioni sul codice di notifica. Il membro *PT* contiene le coordinate del mouse del messaggio di hit test.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se non diversamente specificato, restituire zero per consentire al controllo di eseguire l'elaborazione predefinita del messaggio di hit test oppure restituire uno dei valori HT \* documentati in [**WM \_ NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) per eseguire l'override dell'elaborazione dell'hit test predefinito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

