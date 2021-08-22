---
title: WM_DPICHANGED_BEFOREPARENT messaggio (Winuser.h)
description: Per le finestre di primo livello per Monitor v2, questo messaggio viene inviato a tutti gli HWND nell'albero HWDN figlio della finestra che sta subendo una modifica DPI. | WM_DPICHANGED_BEFOREPARENT messaggio (Winuser.h)
ms.assetid: EC8CC313-565F-451F-AE18-66F3B63303CE
keywords:
- WM_DPICHANGED_BEFOREPARENT messaggio High DPI (DPI elevato)
topic_type:
- apiref
api_name:
- WM_DPICHANGED_BEFOREPARENT
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a1a52216052f597ce26e5be476a970ff78f0297c08124c9b1ca89453b6fca76
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119557671"
---
# <a name="wm_dpichanged_beforeparent-message"></a>MESSAGGIO WM \_ DPICHANGED \_ BEFOREPARENT

Per le finestre di primo livello per Monitor [v2,](dpi-awareness-context.md) questo messaggio viene inviato a tutti gli HWND nell'albero HWDN figlio della finestra che sta subendo una modifica DPI. Questo messaggio viene visualizzato prima che la finestra di primo livello riceva [**WM \_ DPICHANGED**](wm-dpichanged.md)e attraversa l'albero figlio dal basso verso l'alto.


```C++
#define WM_DPICHANGED_BEFOREPARENT       0x02E2
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

Non esiste alcuna gestione predefinita di questo messaggio in [DefWindowProc.](/windows/win32/api/winuser/nf-winuser-defwindowproca)

Questo messaggio viene inviato solo quando la finestra di primo livello ha un contesto di riconoscimento DPI PMv2.

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

[**WM \_ DPICHANGED \_ AFTERPARENT**](wm-dpichanged-afterparent.md)
</dt> </dl>

 

