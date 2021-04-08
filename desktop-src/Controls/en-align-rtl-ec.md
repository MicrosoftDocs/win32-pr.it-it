---
title: Codice di notifica EN_ALIGN_RTL_EC (winuser. h)
description: Inviato quando l'utente ha modificato la direzione del controllo di modifica da destra a sinistra. La finestra padre del controllo di modifica riceve questo codice di notifica tramite un \_ messaggio di comando WM.
ms.assetid: c53bc808-48c6-4a8f-ae5d-af2164fe419a
keywords:
- Controlli di Windows per il codice di notifica EN_ALIGN_RTL_EC
topic_type:
- apiref
api_name:
- EN_ALIGN_RTL_EC
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eca94073b86ea44b192360e593f4b76d4227cf82
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873586"
---
# <a name="en_align_rtl_ec-notification-code"></a>\_Allinea il \_ codice di \_ notifica RTL EC

Inviato quando l'utente ha modificato la direzione del controllo di modifica da destra a sinistra. La finestra padre del controllo di modifica riceve questo codice di notifica tramite un messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) .


```C++
EN_ALIGN_RTL_EC

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore del controllo di modifica. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica il codice di notifica.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per il controllo di modifica che invia il codice di notifica.

</dd> </dl>

## <a name="remarks"></a>Commenti

Se nel sistema è installata una lingua bidirezionale, ad esempio l'arabo o l'ebraico, è possibile modificare la direzione del controllo di modifica usando CTRL + LSHIFT (da sinistra a destra) e CTRL + RSHIFT (da destra a sinistra).

**Modifica avanzata:** Questo codice di notifica non è supportato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_comando WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

