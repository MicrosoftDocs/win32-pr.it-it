---
description: Il \_ messaggio WM PRINTCLIENT viene inviato a una finestra per richiedere che disegni la propria area client nel contesto di dispositivo specificato, in genere in un contesto di dispositivo stampante.
ms.assetid: 8703ee74-812a-4ca2-8ee3-a3b8779739e7
title: Messaggio WM_PRINTCLIENT (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52aca68695964a35ab9a2c4e309cd71c2e9f7eca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980279"
---
# <a name="wm_printclient-message"></a>\_Messaggio PRINTCLIENT WM

Il messaggio **WM \_ PRINTCLIENT** viene inviato a una finestra per richiedere che disegni la propria area client nel contesto di dispositivo specificato, in genere in un contesto di dispositivo stampante.

A differenza di [**WM \_ Print**](wm-print.md), **WM \_ PRINTCLIENT** non viene elaborato da [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca). Una finestra deve elaborare il messaggio **WM \_ PRINTCLIENT** tramite una funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) definita dall'applicazione affinché venga utilizzata correttamente.


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

Handle per il contesto di dispositivo da creare.

</dd> <dt>

*lParam* 
</dt> <dd>

Opzioni di disegno. Il parametro può essere costituito da uno o più dei valori seguenti.



| Valore                                                                                                                                                                  | Significato                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="PRF_CHECKVISIBLE"></span><span id="prf_checkvisible"></span><dl> <dt>**\_CHECKVISIBLE PRF**</dt> </dl> | Disegna la finestra solo se è visibile.<br/>          |
| <span id="PRF_CHILDREN"></span><span id="prf_children"></span><dl> <dt>**\_elementi figlio PRF**</dt> </dl>             | Disegna tutte le finestre figlio visibili.<br/>              |
| <span id="PRF_CLIENT"></span><span id="prf_client"></span><dl> <dt>**\_client PRF**</dt> </dl>                   | Disegna l'area client della finestra.<br/>             |
| <span id="PRF_ERASEBKGND"></span><span id="prf_erasebkgnd"></span><dl> <dt>**\_ERASEBKGND PRF**</dt> </dl>       | Cancella lo sfondo prima di disegnare la finestra.<br/> |
| <span id="PRF_NONCLIENT"></span><span id="prf_nonclient"></span><dl> <dt>**non \_ client PRF**</dt> </dl>          | Disegna l'area non client della finestra.<br/>          |
| <span id="PRF_OWNED"></span><span id="prf_owned"></span><dl> <dt>**\_Proprietà PRF**</dt> </dl>                      | Disegna tutte le finestre di proprietà.<br/>                         |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Una finestra può elaborare questo messaggio in modo molto simile a [**WM \_ Paint**](./wm-paint.md), ad eccezione del fatto che non è necessario chiamare [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) e [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) (viene fornito un contesto di dispositivo) e la finestra deve disegnare l'intera area client anziché solo l'area non valida.

Windows che può essere utilizzato in qualsiasi punto del sistema, ad esempio i controlli, deve elaborare questo messaggio. È probabilmente utile per altre finestre elaborare anche questo messaggio perché è relativamente semplice da implementare.

La funzione [AnimateWindow](/windows/desktop/api/winuser/nf-winuser-animatewindow) richiede che la finestra animata implementi il messaggio **WM \_ PRINTCLIENT** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Cenni preliminari su disegno e disegno](painting-and-drawing.md)
</dt> <dt>

[Disegno e creazione di messaggi](painting-and-drawing-messages.md)
</dt> <dt>

[**AnimateWindow**](/windows/win32/api/winuser/nf-winuser-animatewindow)
</dt> <dt>

[**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint)
</dt> <dt>

[**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint)
</dt> <dt>

[**\_disegno WM**](wm-paint.md)
</dt> </dl>

 

 
