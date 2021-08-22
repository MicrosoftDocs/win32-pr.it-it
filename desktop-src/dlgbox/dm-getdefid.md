---
title: DM_GETDEFID messaggio (Winuser.h)
description: Recupera l'identificatore del controllo pulsante di push predefinito per una finestra di dialogo.
ms.assetid: 9f00a494-f5a2-4c4e-a9fc-2220d9326eb9
keywords:
- DM_GETDEFID finestre di dialogo del messaggio
topic_type:
- apiref
api_name:
- DM_GETDEFID
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6898ed6484a66e1c0d5fa498b0352498c0a57fbe91a74f738e2c6438511aef21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118785823"
---
# <a name="dm_getdefid-message"></a>Messaggio \_ DM GETDEFID

Recupera l'identificatore del controllo pulsante di push predefinito per una finestra di dialogo.


```C++
#define WM_USER              0x0400
#define DM_GETDEFID         (WM_USER+0)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato e deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato e deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se esiste un pulsante di push predefinito, la parola di ordine superiore del valore restituito contiene il valore **DC \_ HASDEFID** e la parola di ordine basso contiene l'identificatore di controllo. In caso contrario, il valore restituito è zero.

## <a name="remarks"></a>Commenti

La [**funzione DefDlgProc**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw) elabora questo messaggio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**DefDlgProc**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw)
</dt> <dt>

[**DM \_ SETDEFID**](dm-setdefid.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Finestre di dialogo](dialog-boxes.md)
</dt> </dl>

 

 





