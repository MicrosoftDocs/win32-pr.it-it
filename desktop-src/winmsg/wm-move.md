---
description: Inviato dopo lo spostamento di una finestra.
ms.assetid: 552ddc26-fe63-449b-8c82-bb927a2c1c41
title: WM_MOVE messaggio (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84c18d7a4f4411f45a3338a057a60942d01905ccefd25b40ee511d3b8a5d915d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810471"
---
# <a name="wm_move-message"></a>Messaggio WM \_ MOVE

Inviato dopo lo spostamento di una finestra.

Una finestra riceve questo messaggio tramite la [**relativa funzione WindowProc.**](/windows/win32/api/winuser/nf-winuser-defwindowproca)


```C++
#define WM_MOVE                         0x0003
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> <dt>

*lParam* 
</dt> <dd>

Coordinate x e y dell'angolo superiore sinistro dell'area client della finestra. La parola di ordine più basso contiene la coordinata x, mentre la parola di ordine superiore contiene la coordinata y.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **LRESULT**

Se un'applicazione elabora questo messaggio, deve restituire zero.

## <a name="remarks"></a>Commenti

I parametri sono specificati nelle coordinate dello schermo per le finestre sovrapposte e popup e nelle coordinate padre-client per le finestre figlio.

Nell'esempio seguente viene illustrato come ottenere la posizione dal *parametro lParam.*


```
xPos = (int)(short) LOWORD(lParam);   // horizontal position 
yPos = (int)(short) HIWORD(lParam);   // vertical position 
```



È anche possibile usare la macro [**MAKEPOINTS**](/windows/win32/api/wingdi/nf-wingdi-makepoints) per convertire il *parametro lParam* in una [**struttura POINTS.**](/previous-versions//dd162808(v=vs.85))

La [**funzione DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) invia i **messaggi WM \_ SIZE** e **WM \_ MOVE** quando elabora il [**messaggio WM \_ WINDOWPOSCHANGED.**](wm-windowposchanged.md)
I **messaggi WM \_ SIZE** e **WM \_ MOVE** non vengono inviati se un'applicazione gestisce il messaggio **WM \_ WINDOWPOSCHANGED** senza **chiamare DefWindowProc.**

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

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**WM \_ WINDOWPOSCHANGED**](wm-windowposchanged.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**PUNTI DI APPLICAZIONE**](/windows/win32/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

[**Punti**](/previous-versions//dd162808(v=vs.85))
</dt> </dl>

 

 
