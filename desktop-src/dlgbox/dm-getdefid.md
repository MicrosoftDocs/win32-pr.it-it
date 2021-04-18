---
title: Messaggio DM_GETDEFID (winuser. h)
description: Recupera l'identificatore del controllo pulsante di comando predefinito per una finestra di dialogo.
ms.assetid: 9f00a494-f5a2-4c4e-a9fc-2220d9326eb9
keywords:
- Finestre di dialogo DM_GETDEFID messaggio
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
ms.openlocfilehash: 7fdcdfc2cd278ab452d48ecb1c254bdb00ffbb7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518880"
---
# <a name="dm_getdefid-message"></a>\_Messaggio DM GETDEFID

Recupera l'identificatore del controllo pulsante di comando predefinito per una finestra di dialogo.


```C++
#define WM_USER              0x0400
#define DM_GETDEFID         (WM_USER+0)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene utilizzato e deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene utilizzato e deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se esiste un pulsante di push predefinito, la parola più significativa del valore restituito contiene il valore **DC \_ HASDEFID** e la parola di basso livello contiene l'identificatore del controllo. In caso contrario, il valore restituito è zero.

## <a name="remarks"></a>Commenti

La funzione [**DefDlgProc**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw) elabora questo messaggio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**DefDlgProc**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw)
</dt> <dt>

[**\_SETDEFID DM**](dm-setdefid.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Finestre di dialogo](dialog-boxes.md)
</dt> </dl>

 

 





