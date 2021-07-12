---
description: Si invia il **WM_SETREDRAW** a una finestra per consentire il ridisegno delle modifiche in tale finestra o per impedire il ridisegno delle modifiche in tale finestra.
ms.assetid: 0085a55e-7bf6-4eb6-a649-832b685db1cc
title: WM_SETREDRAW messaggio (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1232833fc4465e2341541a0036af47fdd3b53393
ms.sourcegitcommit: e5d6fb49928cc8cea4ec77dce03b740d40076348
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/10/2021
ms.locfileid: "113593457"
---
# <a name="wm_setredraw-message"></a>WM_SETREDRAW messaggio

Si invia il **messaggio WM \_ SETREDRAW** a una finestra per consentire il ridisegno delle modifiche in tale finestra o per impedire il ridisegno delle modifiche in tale finestra.

Per inviare questo messaggio, chiamare la [**funzione SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) con i parametri seguenti.

```C++
SendMessage(
  (HWND) hWnd,
  WM_SETREDRAW,
  (WPARAM) wParam,
  (LPARAM) lParam
);
```

## <a name="parameters"></a>Parametri

`wParam`

Stato di ridisegno. Se questo parametro è **TRUE,** il contenuto può essere ridisegnato dopo una modifica. Se questo parametro è **FALSE,** il contenuto non può essere ridisegnato dopo una modifica.

`lParam`

Questo parametro non viene usato.

## <a name="return-value"></a>Valore restituito

L'applicazione deve restituire 0 se elabora questo messaggio.

## <a name="remarks"></a>Commenti

Questo messaggio può essere utile se l'applicazione deve aggiungere più elementi a una casella di riepilogo. L'applicazione può chiamare questo messaggio con *wParam* impostato su **FALSE,** aggiungere gli elementi e quindi chiamare nuovamente il messaggio con *wParam* impostato su **TRUE.** Infine, l'applicazione può chiamare [**RedrawWindow**](/windows/win32/api/Winuser/nf-winuser-redrawwindow)(*hWnd*, **NULL**, **NULL**, \_ RDW ERASE \| RDW \_ FRAME \| RDW \_ INVALIDATE \| RDW \_ ALLCHILDREN) per fare in modo che la casella di riepilogo venga ridisegnata.

> [!NOTE] 
> È consigliabile usare [**RedrawWindow**](/windows/win32/api/Winuser/nf-winuser-redrawwindow) con i flag specificati, anziché [**InvalidateRect**](/windows/win32/api/Winuser/nf-winuser-invalidaterect), perché il primo è necessario per alcuni controlli che hanno un'area non client o hanno stili di finestra che ne determinano l'applicazione a un'area non client ( ad esempio **WS_THICKFRAME**, **WS_BORDER** o **WS_EX_CLIENTEDGE**). Se il controllo non ha un'area non client, **RedrawWindow** con questi flag esegue solo l'invalidazione di **InvalidateRect.**

Il passaggio **WM_SETREDRAW** messaggio alla funzione **DefWindowProc** rimuove lo stile WS_VISIBLE dalla finestra quando *wParam* è impostato su **FALSE.**  Anche se il contenuto della finestra rimane visibile sullo schermo, la [**funzione IsWindowVisible**](/windows/win32/api/winuser/nf-winuser-iswindowvisible) restituisce **FALSE** quando viene chiamato su una finestra in questo stato. 

Il **passaggio WM_SETREDRAW** messaggio alla funzione **DefWindowProc** aggiunge lo stile **WS_VISIBLE** alla finestra, se non impostato, quando *wParam* è impostato su **TRUE.** Se l'applicazione invia **WM_SETREDRAW** messaggio con *wParam* impostato su TRUE su **una** finestra nascosta, la finestra diventa visibile. 

**Windows 10 e versioni successive; Windows Server 2016 e versioni successive.** Il sistema imposta una proprietà denominata *SysSetRedraw* in una finestra la cui routine della finestra passa WM_SETREDRAW **messaggi** a **DefWindowProc**. È possibile usare la [**funzione GetProp**](/windows/win32/api/Winuser/nf-winuser-getpropa) per ottenere il valore della proprietà quando è disponibile. **GetProp** restituisce un valore diverso da zero quando il ridisegno è disabilitato. **GetProp** restituirà zero quando il ridisegno è abilitato o quando la proprietà della finestra non esiste. 

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-|-|
| Client minimo supportato | Windows 2000 Professional \[solo app desktop\] |
| Server minimo supportato | Windows 2000 Server \[solo app desktop\] |
| Intestazione | <dl><dt>Winuser.h (includere Windows.h)</dt></dl> |

## <a name="see-also"></a>Vedi anche

* [Panoramica del disegno e del disegno](painting-and-drawing.md)
* [Disegnare e disegnare messaggi](painting-and-drawing-messages.md)
* [RidisegnaWindow](/windows/win32/api/Winuser/nf-winuser-redrawwindow)
