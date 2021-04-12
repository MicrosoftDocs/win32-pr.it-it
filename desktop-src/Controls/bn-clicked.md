---
title: Codice di notifica BN_CLICKED (winuser. h)
description: Inviato quando l'utente fa clic su un pulsante. La finestra padre del pulsante riceve questo codice di notifica tramite il \_ messaggio di comando WM.
ms.assetid: 74847549-b92f-4981-a979-d0b2a8a5539a
keywords:
- Controlli di Windows per il codice di notifica BN_CLICKED
topic_type:
- apiref
api_name:
- BN_CLICKED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 894837c9a930c6a5f6d124b6b9e983465ef3beac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119339"
---
# <a name="bn_clicked-notification-code"></a>\_Codice di notifica fatto clic su BN

Inviato quando l'utente fa clic su un pulsante.

La finestra padre del pulsante riceve questo codice di notifica tramite il messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) .


```C++
BN_CLICKED

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore di controllo del pulsante. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica il codice di notifica.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per il pulsante.

</dd> </dl>

## <a name="remarks"></a>Commenti

Un pulsante disabilitato non invia un \_ codice di notifica fatto clic su BN alla finestra padre.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Altre risorse**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**\_comando WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

