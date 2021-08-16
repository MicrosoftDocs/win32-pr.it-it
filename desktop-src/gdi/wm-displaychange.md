---
description: Il messaggio \_ WM DISPLAYCHANGE viene inviato a tutte le finestre quando viene modificata la risoluzione dello schermo.
ms.assetid: 5a6111fd-648e-41a9-aaf8-e5d93f5d54cd
title: WM_DISPLAYCHANGE messaggio (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d28f5708618ada0d766b140f01ff81a9427f443abb89cf41ba2c743223fbc70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119037439"
---
# <a name="wm_displaychange-message"></a>Messaggio \_ WM DISPLAYCHANGE

Il **messaggio \_ WM DISPLAYCHANGE** viene inviato a tutte le finestre quando viene modificata la risoluzione dello schermo.

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

Nuova profondità dell'immagine dello schermo, in bit per pixel.

</dd> <dt>

*lParam* 
</dt> <dd>

La parola di ordine inferiore specifica la risoluzione orizzontale dello schermo.

La parola più alta specifica la risoluzione verticale dello schermo.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questo messaggio viene inviato solo alle finestre di primo livello. Per tutte le altre finestre viene pubblicato.

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

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> </dl>

 

 
