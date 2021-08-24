---
description: Il messaggio WM PRINTCLIENT viene inviato a una finestra per richiedere di disegnare la relativa area client nel contesto di dispositivo specificato, in genere \_ in un contesto di dispositivo della stampante.
ms.assetid: 8703ee74-812a-4ca2-8ee3-a3b8779739e7
title: WM_PRINTCLIENT messaggio (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 807c12ca4d0a5fe5f1e2a12aecd3b3148d936119f72771e811fe85d5b0af3abf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119717661"
---
# <a name="wm_printclient-message"></a>Messaggio \_ WM PRINTCLIENT

Il **messaggio WM \_ PRINTCLIENT** viene inviato a una finestra per richiedere di disegnare la relativa area client nel contesto di dispositivo specificato, in genere in un contesto di dispositivo della stampante.

A [**differenza di WM \_ PRINT,**](wm-print.md) **WM \_ PRINTCLIENT** non viene elaborato [**da DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca). Una finestra deve elaborare il **messaggio WM \_ PRINTCLIENT** tramite una funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) definita dall'applicazione per poterlo usare correttamente.


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per il contesto di dispositivo in cui disegnare.

</dd> <dt>

*lParam* 
</dt> <dd>

Opzioni di disegno. Questo parametro può essere uno o più dei valori seguenti.



| Valore                                                                                                                                                                  | Significato                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="PRF_CHECKVISIBLE"></span><span id="prf_checkvisible"></span><dl> <dt>**PRF \_ CHECKVISIBLE**</dt> </dl> | Disegna la finestra solo se è visibile.<br/>          |
| <span id="PRF_CHILDREN"></span><span id="prf_children"></span><dl> <dt>**PRF \_ CHILDREN**</dt> </dl>             | Disegna tutte le finestre figlio visibili.<br/>              |
| <span id="PRF_CLIENT"></span><span id="prf_client"></span><dl> <dt>**PRF \_ CLIENT**</dt> </dl>                   | Disegna l'area client della finestra.<br/>             |
| <span id="PRF_ERASEBKGND"></span><span id="prf_erasebkgnd"></span><dl> <dt>**PRF \_ ERASEBKGND**</dt> </dl>       | Cancella lo sfondo prima di disegnare la finestra.<br/> |
| <span id="PRF_NONCLIENT"></span><span id="prf_nonclient"></span><dl> <dt>**PRF \_ NONCLIENT**</dt> </dl>          | Disegna l'area non client della finestra.<br/>          |
| <span id="PRF_OWNED"></span><span id="prf_owned"></span><dl> <dt>**PROPRIETÀ \_ PRF**</dt> </dl>                      | Disegna tutte le finestre di proprietà.<br/>                         |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Una finestra può elaborare questo messaggio in modo molto simile a [**WM \_ PAINT,**](./wm-paint.md)ad eccezione del fatto che non è necessario chiamare [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) ed [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) (viene fornito un contesto di dispositivo) e la finestra deve disegnare l'intera area client anziché solo l'area non valida.

Windows questo messaggio deve essere usato in qualsiasi punto del sistema, ad esempio i controlli. È probabilmente utile che anche altre finestre elavano questo messaggio perché è relativamente semplice da implementare.

La [funzione AnimateWindow](/windows/desktop/api/winuser/nf-winuser-animatewindow) richiede che la finestra animata implementi il **messaggio WM \_ PRINTCLIENT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica di disegno e disegno](painting-and-drawing.md)
</dt> <dt>

[Disegno e disegno di messaggi](painting-and-drawing-messages.md)
</dt> <dt>

[**AnimateWindow**](/windows/win32/api/winuser/nf-winuser-animatewindow)
</dt> <dt>

[**Beginpaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint)
</dt> <dt>

[**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint)
</dt> <dt>

[**WM \_ PAINT**](wm-paint.md)
</dt> </dl>

 

 
