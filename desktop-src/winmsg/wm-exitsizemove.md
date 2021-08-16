---
description: Inviato una volta a una finestra, dopo l'uscita dal ciclo modale di spostamento o ridimensionamento.
ms.assetid: 3466bfb5-c38d-49d8-a4ab-bf23d09c454c
title: WM_EXITSIZEMOVE messaggio (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f451e846f2a262a30ccc73121d52c3732dbdfb160fe529535dcf353f077c351
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117849253"
---
# <a name="wm_exitsizemove-message"></a>Messaggio \_ WM EXITSIZEMOVE

Inviato una volta a una finestra, dopo l'uscita dal ciclo modale di spostamento o ridimensionamento. La finestra entra nel ciclo modale di spostamento o ridimensionamento quando l'utente fa clic sulla barra del titolo o sul bordo di ridimensionamento della finestra oppure quando la finestra passa il messaggio [**\_ SYSCOMMAND WM**](../menurc/wm-syscommand.md) alla funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) e il parametro *wParam* del messaggio specifica il valore **SC \_ MOV** E o **SC \_ SIZE.** L'operazione viene completata al [**termine di DefWindowProc.**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)

Una finestra riceve questo messaggio tramite la [**relativa funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_EXITSIZEMOVE                 0x0232
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **LRESULT**

Un'applicazione deve restituire zero se elabora questo messaggio.

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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**WM \_ ENTERSIZEMOVE**](wm-entersizemove.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
