---
title: EN_ALIGN_RTL_EC di notifica (Winuser.h)
description: Inviato quando l'utente ha modificato la direzione del controllo di modifica da destra a sinistra. La finestra padre del controllo di modifica riceve questo codice di notifica tramite un messaggio WM \_ COMMAND.
ms.assetid: c53bc808-48c6-4a8f-ae5d-af2164fe419a
keywords:
- EN_ALIGN_RTL_EC del codice di notifica Windows controlli
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
ms.openlocfilehash: d16b44ecd143715eb5c1bc895ca5c20fa066b17b71ab31ee667e2d6b2b6a0852
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119437091"
---
# <a name="en_align_rtl_ec-notification-code"></a>Codice di notifica EN \_ ALIGN \_ RTL \_ EC

Inviato quando l'utente ha modificato la direzione del controllo di modifica da destra a sinistra. La finestra padre del controllo di modifica riceve questo codice di notifica tramite un [**messaggio WM \_ COMMAND.**](/windows/desktop/menurc/wm-command)


```C++
EN_ALIGN_RTL_EC

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

La [**parola chiave LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore del controllo di modifica. HiWORD [**specifica**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) il codice di notifica.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per il controllo di modifica che invia il codice di notifica.

</dd> </dl>

## <a name="remarks"></a>Commenti

Se nel sistema è installata una lingua bidirezionale, ad esempio arabo o ebraico, è possibile modificare la direzione del controllo di modifica usando CTRL+LSHIFT (da sinistra a destra) e CTRL+RSHIFT (per da destra a sinistra).

**Rich Edit:** Questo codice di notifica non è supportato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**COMANDO \_ WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

