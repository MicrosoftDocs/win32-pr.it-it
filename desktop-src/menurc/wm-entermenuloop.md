---
title: Messaggio WM_ENTERMENULOOP (winuser. h)
description: Notifica alla routine della finestra principale di un'applicazione che è stato immesso un ciclo modale di menu.
ms.assetid: 0a018b6f-fe4b-4e90-bbb6-9b5719253dc1
keywords:
- Menu del messaggio WM_ENTERMENULOOP e altre risorse
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
ms.openlocfilehash: 3a7b325719c428dc7310503320b53f3a5f96182e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301192"
---
# <a name="wm_entermenuloop-message"></a>\_Messaggio ENTERMENULOOP WM

Notifica alla routine della finestra principale di un'applicazione che è stato immesso un ciclo modale di menu.


```C++
#define WM_ENTERMENULOOP                0x0211
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica se il menu finestra è stato immesso utilizzando la funzione [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) . Il valore di questo parametro è **true** se il menu finestra è stato immesso utilizzando **TrackPopupMenu** e **false** in caso contrario.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Un'applicazione deve restituire zero se elabora questo messaggio.

## <a name="remarks"></a>Commenti

La funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) restituisce zero.

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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**\_EXITMENULOOP WM**](wm-exitmenuloop.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Menu](menus.md)
</dt> </dl>

 

