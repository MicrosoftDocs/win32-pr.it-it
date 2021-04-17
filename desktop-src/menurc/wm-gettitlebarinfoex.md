---
title: Messaggio WM_GETTITLEBARINFOEX (winuser. h)
description: Inviato per richiedere informazioni estese sulla barra del titolo. Una finestra riceve questo messaggio tramite la funzione WindowProc.
ms.assetid: 0760dbf1-5b20-471c-bfd9-b8d28b52074b
keywords:
- Menu del messaggio WM_GETTITLEBARINFOEX e altre risorse
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
ms.openlocfilehash: fea31326faf5953df0facf34b58b06d7766c2e7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400364"
---
# <a name="wm_gettitlebarinfoex-message"></a>\_Messaggio GETTITLEBARINFOEX WM

Inviato per richiedere informazioni estese sulla barra del titolo. Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_GETTITLEBARINFOEX            0x033F
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene utilizzato e deve essere 0.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**TITLEBARINFOEX**](/windows/win32/api/winuser/ns-winuser-titlebarinfoex) . Il mittente del messaggio è responsabile dell'allocazione della memoria per questa struttura. Impostare il membro **cbSize** della struttura su `sizeof(TITLEBARINFOEX)` prima di passare questa struttura con il messaggio.

</dd> </dl>

## <a name="remarks"></a>Commenti

Nell'esempio seguente viene illustrato come il ricevitore del messaggio esegue il cast di un valore **lParam** per recuperare la struttura [**TITLEBARINFOEX**](/windows/win32/api/winuser/ns-winuser-titlebarinfoex) .

`TITLEBARINFOEX *ptinfo = (TITLEBARINFOEX *)lParam;`

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica sui menu](menus.md)
</dt> </dl>

 

