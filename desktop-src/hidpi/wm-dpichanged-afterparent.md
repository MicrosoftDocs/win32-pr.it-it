---
title: Messaggio WM_DPICHANGED_AFTERPARENT (winuser. h)
description: Per le finestre di primo livello di per monitor V2, questo messaggio viene inviato a tutti gli HWND nell'albero HWDN figlio della finestra in cui è in corso una modifica del valore DPI. | Messaggio WM_DPICHANGED_AFTERPARENT (winuser. h)
ms.assetid: FEA1BF07-55B6-4584-ABD3-340515831E0A
keywords:
- Messaggio WM_DPICHANGED_AFTERPARENT alto DPI
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
ms.openlocfilehash: 10cc76602662cefba42f62bd3ed85913ade40f15
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321921"
---
# <a name="wm_dpichanged_afterparent-message"></a>\_ \_ Messaggio AFTERPARENT di WM DPICHANGED

Per le finestre di primo livello di per [Monitor V2](dpi-awareness-context.md) , questo messaggio viene inviato a tutti gli HWND nell'albero HWDN figlio della finestra in cui è in corso una modifica del valore dpi. Questo messaggio si verifica dopo che la finestra di primo livello riceve [**WM \_ DPICHANGED**](wm-dpichanged.md)e attraversa l'albero figlio dall'alto verso il basso.


```C++
#define WM_DPICHANGED_AFTERPARENT       0x02E3
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo valore non è utilizzato e sarà zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo valore non è utilizzato e sarà zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo valore non è utilizzato e viene ignorato dal sistema.

## <a name="remarks"></a>Commenti

Non esiste alcuna gestione predefinita del messaggio in [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).

Questo messaggio viene inviato solo quando la finestra di primo livello ha un contesto di riconoscimento DPI di PMv2.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1703 \[\]<br/>                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2016\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Winuser. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_DPICHANGED WM**](wm-dpichanged.md)
</dt> <dt>

[**\_BEFOREPARENT DPICHANGED \_ WM**](wm-dpichanged-beforeparent.md)
</dt> </dl>

 

