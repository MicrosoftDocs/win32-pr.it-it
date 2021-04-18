---
title: Messaggio WM_NCMOUSELEAVE (winuser. h)
description: Inserito in una finestra quando il cursore esce dall'area non client della finestra specificata in una chiamata precedente a TrackMouseEvent.
ms.assetid: b3ada6db-93ce-45d7-b408-d08692328aeb
keywords:
- Input della tastiera e del mouse WM_NCMOUSELEAVE messaggio
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
ms.openlocfilehash: 5cf7f9d0931c2623d2e92010abfca96f391107b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301418"
---
# <a name="wm_ncmouseleave-message"></a>\_Messaggio NCMOUSELEAVE WM

Inserito in una finestra quando il cursore esce dall'area non client della finestra specificata in una chiamata precedente a [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent).

Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_NCMOUSELEAVE                 0x02A2
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

Se un'applicazione elabora il messaggio, deve restituire zero.

## <a name="remarks"></a>Commenti

Tutti i tracciati richiesti da [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) vengono annullati quando viene generato questo messaggio. L'applicazione deve chiamare **TrackMouseEvent** quando il mouse riimmette la finestra se è necessario un ulteriore rilevamento del comportamento del passaggio del mouse.

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

[**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent)
</dt> <dt>

[**TRACKMOUSEEVENT**](/windows/win32/api/winuser/ns-winuser-trackmouseevent)
</dt> <dt>

[**\_SYSCOMMAND WM**](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

[**MOUSELEAVE di WM \_**](wm-mouseleave.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Input del mouse](mouse-input.md)
</dt> </dl>

 

