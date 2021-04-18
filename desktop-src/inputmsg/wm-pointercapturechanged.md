---
title: Messaggio WM_POINTERCAPTURECHANGED
description: Inviato a una finestra che sta perdendo l'acquisizione di un puntatore di input.
ms.assetid: 6eec37da-227c-4be1-bf0b-98704caa1322
keywords:
- Messaggi e notifiche di input del messaggio WM_POINTERCAPTURECHANGED
topic_type:
- apiref
api_name:
- WM_POINTERCAPTURECHANGED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 768dc81be57bb61a23acab7ebea450dba577d60a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302385"
---
# <a name="wm_pointercapturechanged-message"></a>Messaggio WM_POINTERCAPTURECHANGED

Inviato a una finestra che sta perdendo l'acquisizione di un puntatore di input.

Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_POINTERCAPTURECHANGED           0x024C
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Contiene informazioni sul puntatore di input che viene perso. Usare [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api) per ottenere l'ID del puntatore.

</dd> <dt>

*lParam* 
</dt> <dd>

Contiene un handle per la finestra che sta acquisendo il puntatore di input. Questo valore può essere NULL se il puntatore non viene più acquisito dalla finestra.

Se questo messaggio viene generato dall'elaborazione interna, il valore può essere l'handle della finestra che riceve il messaggio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora il messaggio, deve restituire zero.

Se l'applicazione non elabora questo messaggio, deve chiamare [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).

## <a name="remarks"></a>Commenti

Una finestra deve usare questa notifica per arrestare l'elaborazione dei messaggi successivi e per avviare le operazioni di pulizia necessarie per la perdita del puntatore. Anche l'elaborazione dei movimenti associati al puntatore deve essere terminata (ad esempio chiamando [**StopInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-stopinteractioncontext)) e i contatti rimanenti vengono nuovamente associati alla finestra.

In genere, se una finestra riceve la notifica **WM_POINTERCAPTURECHANGED** , non vengono ricevute notifiche successive relative al puntatore di input. Per questo motivo, non dipendere da notifiche associate, ad esempio [**WM_POINTERENTER**](wm-pointerenter.md) e [**WM_POINTERLEAVE**](wm-pointerleave.md).

**WM_POINTERCAPTURECHANGED** non include i dati [**POINTER_INFO**](/previous-versions/windows/desktop/api) . Oltre al flag di [**POINTER_FLAG_CAPTURECHANGED**](pointer-flags-contants.md) impostato, i dati restituiti da [**GetPointerInfo**](/previous-versions/windows/desktop/api) (o qualsiasi variante) sono identici a quelli restituiti prima della notifica.

Se l'applicazione non elabora questa notifica, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) può generare uno o più messaggi di [**WM_GESTURE**](../wintouch/wm-gesture.md) o, se non viene riconosciuto un movimento, **DefWindowProc** può generare un input del mouse.

Se un'applicazione usa selettivamente un input del puntatore e passa il resto a [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca), il comportamento risultante non è definito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                               |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Messaggi](messages.md)
</dt> </dl>

 

