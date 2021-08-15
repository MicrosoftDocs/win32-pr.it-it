---
title: WM_DPICHANGED_AFTERPARENT messaggio (Winuser.h)
description: Per le finestre di primo livello di Per Monitor v2, questo messaggio viene inviato a tutti gli HWND nell'albero HWDN figlio della finestra che sta subendo una modifica DPI. | WM_DPICHANGED_AFTERPARENT messaggio (Winuser.h)
ms.assetid: FEA1BF07-55B6-4584-ABD3-340515831E0A
keywords:
- WM_DPICHANGED_AFTERPARENT messaggio High DPI
topic_type:
- apiref
api_name:
- WM_DPICHANGED_AFTERPARENT
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d47f303db19438f1e7e2cd77df60ddace76bec791bb1789bed47e3f09d8a197c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118759364"
---
# <a name="wm_dpichanged_afterparent-message"></a>Messaggio WM \_ DPICHANGED \_ AFTERPARENT

Per le finestre di primo livello di [Per Monitor v2,](dpi-awareness-context.md) questo messaggio viene inviato a tutti gli HWND nell'albero HWDN figlio della finestra che sta subendo una modifica DPI. Questo messaggio si verifica dopo che la finestra di primo livello riceve [**WM \_ DPICHANGED**](wm-dpichanged.md)e attraversa l'albero figlio dall'alto verso il basso.


```C++
#define WM_DPICHANGED_AFTERPARENT       0x02E3
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo valore è inutilizzato e sarà zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo valore è inutilizzato e sarà zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo valore viene inutilizzato e ignorato dal sistema.

## <a name="remarks"></a>Commenti

Non esiste alcuna gestione predefinita di questo messaggio in [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).

Questo messaggio viene inviato solo quando la finestra di primo livello ha un contesto di riconoscimento DPI di PMv2.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, solo app desktop versione 1703 \[\]<br/>                            |
| Server minimo supportato<br/> | \[Windows Server 2016 solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Winuser</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**WM \_ DPICHANGED**](wm-dpichanged.md)
</dt> <dt>

[**WM \_ DPICHANGED \_ BEFOREPARENT**](wm-dpichanged-beforeparent.md)
</dt> </dl>

 

