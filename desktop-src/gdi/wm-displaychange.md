---
description: Il \_ messaggio WM DISPLAYCHANGE viene inviato a tutte le finestre quando la risoluzione dello schermo è cambiata.
ms.assetid: 5a6111fd-648e-41a9-aaf8-e5d93f5d54cd
title: Messaggio WM_DISPLAYCHANGE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 682612529fd40b22481612bb26a954bec45e3901
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227136"
---
# <a name="wm_displaychange-message"></a>\_Messaggio DISPLAYCHANGE WM

Il messaggio **WM \_ DISPLAYCHANGE** viene inviato a tutte le finestre quando la risoluzione dello schermo è cambiata.

Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


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

La parola di ordine superiore specifica la risoluzione verticale dello schermo.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questo messaggio viene inviato solo alle finestre di primo livello. Per tutte le altre finestre pubblicate.

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

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> </dl>

 

 
