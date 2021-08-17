---
title: WM_GETTITLEBARINFOEX messaggio (Winuser.h)
description: Inviato per richiedere informazioni estese sulla barra del titolo. Una finestra riceve questo messaggio tramite la relativa funzione WindowProc.
ms.assetid: 0760dbf1-5b20-471c-bfd9-b8d28b52074b
keywords:
- WM_GETTITLEBARINFOEX menu e altre risorse del messaggio
topic_type:
- apiref
api_name:
- WM_GETTITLEBARINFOEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1acbe85afa1871caf796c70a9535f5646d2511317a0e9ee0564db55101a16449
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117869667"
---
# <a name="wm_gettitlebarinfoex-message"></a>Messaggio \_ WM GETTITLEBARINFOEX

Inviato per richiedere informazioni estese sulla barra del titolo. Una finestra riceve questo messaggio tramite la [**relativa funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_GETTITLEBARINFOEX            0x033F
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato e deve essere 0.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura TITLEBARINFOEX.**](/windows/win32/api/winuser/ns-winuser-titlebarinfoex) Il mittente del messaggio è responsabile dell'allocazione della memoria per questa struttura. Impostare il **membro cbSize** di questa struttura su `sizeof(TITLEBARINFOEX)` prima di passare questa struttura con il messaggio.

</dd> </dl>

## <a name="remarks"></a>Commenti

Nell'esempio seguente viene illustrato come il ricevitore del messaggio esegue il cast di un **valore LPARAM** per recuperare la [**struttura TITLEBARINFOEX.**](/windows/win32/api/winuser/ns-winuser-titlebarinfoex)

`TITLEBARINFOEX *ptinfo = (TITLEBARINFOEX *)lParam;`

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Cenni preliminari sui menu](menus.md)
</dt> </dl>

 

