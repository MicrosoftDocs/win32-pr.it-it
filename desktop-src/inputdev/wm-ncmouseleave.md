---
title: WM_NCMOUSELEAVE messaggio (Winuser.h)
description: Inviato a una finestra quando il cursore esce dall'area non client della finestra specificata in una chiamata precedente a TrackMouseEvent.
ms.assetid: b3ada6db-93ce-45d7-b408-d08692328aeb
keywords:
- WM_NCMOUSELEAVE messaggio Input da tastiera e mouse
topic_type:
- apiref
api_name:
- WM_NCMOUSELEAVE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 141c4f1f2483e1cbd725a70454b1df1be12c46ec1970c052938181fb511ed248
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778451"
---
# <a name="wm_ncmouseleave-message"></a>Messaggio \_ WM NCMOUSELEAVE

Inviato a una finestra quando il cursore esce dall'area non client della finestra specificata in una chiamata precedente a [**TrackMouseEvent.**](/windows/win32/api/winuser/nf-winuser-trackmouseevent)

Una finestra riceve questo messaggio tramite la [**relativa funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_NCMOUSELEAVE                 0x02A2
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

Se un'applicazione elabora questo messaggio, deve restituire zero.

## <a name="remarks"></a>Commenti

Tutto il rilevamento richiesto [**da TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) viene annullato quando viene generato questo messaggio. L'applicazione deve chiamare **TrackMouseEvent** quando il mouse consente di reimerire la finestra se richiede un ulteriore rilevamento del comportamento del passaggio del mouse.

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

[**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent)
</dt> <dt>

[**TRACKMOUSEEVENT**](/windows/win32/api/winuser/ns-winuser-trackmouseevent)
</dt> <dt>

[**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

[**WM \_ MOUSELEAVE**](wm-mouseleave.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Mouse Input](mouse-input.md)
</dt> </dl>

 

