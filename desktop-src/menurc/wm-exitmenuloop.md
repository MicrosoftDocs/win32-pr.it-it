---
title: Messaggio WM_EXITMENULOOP (winuser. h)
description: Notifica alla routine della finestra principale di un'applicazione che un ciclo modale del menu è stato terminato.
ms.assetid: b2a9d537-af7c-4c8a-932a-95e45eb8deb5
keywords:
- Menu del messaggio WM_EXITMENULOOP e altre risorse
topic_type:
- apiref
api_name:
- WM_EXITMENULOOP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8440e1a255968eb3e1607b5d54375900f7b5de16
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741706"
---
# <a name="wm_exitmenuloop-message"></a>\_Messaggio EXITMENULOOP WM

Notifica alla routine della finestra principale di un'applicazione che un ciclo modale del menu è stato terminato.


```C++
#define WM_EXITMENULOOP                 0x0212
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica se il menu è un menu di scelta rapida. Il valore di questo parametro è **true** se si tratta di un menu di scelta rapida; in caso contrario, **false** .

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

[**\_ENTERMENULOOP WM**](wm-entermenuloop.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Menu](menus.md)
</dt> </dl>

 

