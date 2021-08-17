---
description: Il messaggio WM PRINT viene inviato a una finestra per richiedere il disegno nel contesto di dispositivo specificato, in genere in un \_ contesto di dispositivo della stampante.
ms.assetid: e6be2ecd-603a-405f-8a48-68d971e1f6de
title: WM_PRINT messaggio (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45a09d3cb7dbb3b4a4fca7a2af4272f1b4175aa26e911d1def909c97ba35f3d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119964851"
---
# <a name="wm_print-message"></a>Messaggio \_ PRINT WM

Il **messaggio WM \_ PRINT** viene inviato a una finestra per richiedere il disegno nel contesto di dispositivo specificato, in genere in un contesto di dispositivo della stampante.

Una finestra riceve questo messaggio tramite la [**relativa funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


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

La [**funzione DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) elabora questo messaggio in base all'opzione di disegno specificata: se si specifica PRF CHECKVISIBLE e la finestra non è visibile, Non eseguire alcuna operazione. Se si specifica PRF NONCLIENT, disegnare l'area non client nel contesto di dispositivo specificato. Se si \_ specifica PRF ERASEBKGND, inviare alla finestra un messaggio \_ \_ WM [**\_ ERASEBKGND.**](../winmsg/wm-erasebkgnd.md) Se si specifica PRF CLIENT, inviare alla finestra un messaggio \_ [**\_ PRINTCLIENT WM.**](wm-printclient.md) \_ **\_** \_ **\_** Se è impostato PRF CHILDREN, inviare a ogni finestra figlio visibile un messaggio WM PRINT, se PRF OWNED è impostato, inviare a ogni finestra di proprietà visibile un messaggio WM PRINT.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Cenni preliminari sul disegno e sul disegno](painting-and-drawing.md)
</dt> <dt>

[Disegnare e disegnare messaggi](painting-and-drawing-messages.md)
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md)
</dt> <dt>

[**WM \_ PRINTCLIENT**](wm-printclient.md)
</dt> </dl>

 

 
