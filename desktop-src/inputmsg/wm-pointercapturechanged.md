---
title: WM_POINTERCAPTURECHANGED messaggio
description: Inviato a una finestra che sta perdendo l'acquisizione di un puntatore di input.
ms.assetid: 6eec37da-227c-4be1-bf0b-98704caa1322
keywords:
- WM_POINTERCAPTURECHANGED messaggi di input e notifiche
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
ms.openlocfilehash: 5bdea552bdde46fc075965d83d614fd9208cca818de71d97506aa18d816f07d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117695612"
---
# <a name="wm_pointercapturechanged-message"></a>WM_POINTERCAPTURECHANGED messaggio

Inviato a una finestra che sta perdendo l'acquisizione di un puntatore di input.

Una finestra riceve questo messaggio tramite la relativa [**funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_POINTERCAPTURECHANGED           0x024C
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Contiene informazioni sul puntatore di input che viene perso. Usare [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api) per ottenere l'ID puntatore.

</dd> <dt>

*lParam* 
</dt> <dd>

Contiene un handle per la finestra che acquisisce il puntatore di input. Questo valore può essere NULL se il puntatore non viene più acquisito dalla finestra.

Se questo messaggio viene generato dall'elaborazione interna, il valore può essere l'handle della finestra che riceve il messaggio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora questo messaggio, deve restituire zero.

Se l'applicazione non elabora questo messaggio, deve chiamare [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).

## <a name="remarks"></a>Commenti

Una finestra deve usare questa notifica per arrestare l'elaborazione dei messaggi successivi e avviare qualsiasi pulizia necessaria per la perdita del puntatore. Anche l'elaborazione dei movimenti associati al puntatore deve terminare (ad esempio, chiamando [**StopInteractionContext)**](/windows/win32/api/interactioncontext/nf-interactioncontext-stopinteractioncontext)e i contatti rimanenti devono essere nuovamente associati alla finestra.

In genere, se una finestra riceve la notifica **WM_POINTERCAPTURECHANGED,** non vengono ricevute notifiche successive correlate al puntatore di input. Per questo scopo, non dipendere dalle notifiche abbinate, ad esempio WM_POINTERENTER [**e**](wm-pointerenter.md) [**WM_POINTERLEAVE**](wm-pointerleave.md).

**WM_POINTERCAPTURECHANGED** non include [**dati**](/previous-versions/windows/desktop/api) POINTER_INFO dati. Oltre al flag [**POINTER_FLAG_CAPTURECHANGED**](pointer-flags-contants.md) impostato, i dati restituiti da [**GetPointerInfo**](/previous-versions/windows/desktop/api) (o da qualsiasi variante) sono identici a quelli restituiti prima della notifica.

Se l'applicazione non elabora questa notifica, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) può generare uno o più messaggi [**WM_GESTURE**](../wintouch/wm-gesture.md) o, se un movimento non viene riconosciuto, **DefWindowProc** può generare l'input del mouse.

Se un'applicazione utilizza in modo selettivo un input del puntatore e passa il resto a [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca), il comportamento risultante non è definito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                               |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Messaggi](messages.md)
</dt> </dl>

 

