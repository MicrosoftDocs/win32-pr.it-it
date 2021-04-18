---
description: Inviato dopo lo spostamento di una finestra.
ms.assetid: 552ddc26-fe63-449b-8c82-bb927a2c1c41
title: Messaggio WM_MOVE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56004ec47266a50bf2ac82a828b9046c84a8ebfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312371"
---
# <a name="wm_move-message"></a>\_Messaggio di spostamento WM

Inviato dopo lo spostamento di una finestra.

Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) .


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

Coordinate x e y dell'angolo superiore sinistro dell'area client della finestra. La parola di ordine inferiore contiene la coordinata x mentre la parola più significativa contiene la coordinata y.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **LRESULT**

Se un'applicazione elabora il messaggio, deve restituire zero.

## <a name="remarks"></a>Commenti

I parametri vengono specificati nelle coordinate dello schermo per le finestre sovrapposte e popup e nelle coordinate padre-client per le finestre figlio.

Nell'esempio seguente viene illustrato come ottenere la posizione dal parametro *lParam* .


```
xPos = (int)(short) LOWORD(lParam);   // horizontal position 
yPos = (int)(short) HIWORD(lParam);   // vertical position 
```



È anche possibile usare la macro [**MAKEPOINTS**](/windows/win32/api/wingdi/nf-wingdi-makepoints) per convertire il parametro *lParam* in una struttura [**Points**](/previous-versions//dd162808(v=vs.85)) .

La funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) invia i messaggi di **\_ dimensioni WM** e di **\_ spostamento WM** quando elabora il messaggio [**WM \_ WINDOWPOSCHANGED**](wm-windowposchanged.md) .
I messaggi WM **\_ size** e **WM \_ Move** non vengono inviati se un'applicazione gestisce il messaggio **WM \_ WINDOWPOSCHANGED** senza chiamare **DefWindowProc**.

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

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**\_WINDOWPOSCHANGED WM**](wm-windowposchanged.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**MAKEPOINTS**](/windows/win32/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

[**PUNTI**](/previous-versions//dd162808(v=vs.85))
</dt> </dl>

 

 
