---
title: WM_ENTERMENULOOP messaggio (Winuser.h)
description: Notifica alla routine della finestra principale di un'applicazione che è stato immesso un ciclo modale di menu.
ms.assetid: 0a018b6f-fe4b-4e90-bbb6-9b5719253dc1
keywords:
- WM_ENTERMENULOOP menu e altre risorse del messaggio
topic_type:
- apiref
api_name:
- WM_ENTERMENULOOP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb5851109e44100d558603fb268a4668c1f138fff97e5e87db50a28445e70adb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939611"
---
# <a name="wm_entermenuloop-message"></a>Messaggio WM \_ ENTERMENULOOP

Notifica alla routine della finestra principale di un'applicazione che è stato immesso un ciclo modale di menu.


```C++
#define WM_ENTERMENULOOP                0x0211
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica se il menu della finestra è stato immesso usando la [**funzione TrackPopupMenu.**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) Questo parametro ha valore **TRUE se** il menu della finestra è stato immesso usando **TrackPopupMenu** e **FALSE** in caso contrario.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Un'applicazione deve restituire zero se elabora questo messaggio.

## <a name="remarks"></a>Commenti

La [**funzione DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) restituisce zero.

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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**WM \_ EXITMENULOOP**](wm-exitmenuloop.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Menu](menus.md)
</dt> </dl>

 

