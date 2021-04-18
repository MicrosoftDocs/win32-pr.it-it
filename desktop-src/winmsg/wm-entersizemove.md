---
description: Inviato una volta a una finestra dopo l'immissione del ciclo modale di passaggio o di ridimensionamento.
ms.assetid: fe09db71-2c79-47f2-b575-516e960915d4
title: Messaggio WM_ENTERSIZEMOVE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfaf27c888311991b88278a9d4e69482efd06111
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314869"
---
# <a name="wm_entersizemove-message"></a>\_Messaggio ENTERSIZEMOVE WM

Inviato una volta a una finestra dopo l'immissione del ciclo modale di passaggio o di ridimensionamento. La finestra entra nel ciclo modale di spostamento o di ridimensionamento quando l'utente fa clic sulla barra del titolo della finestra o sul bordo di ridimensionamento oppure quando la finestra passa il messaggio [**WM \_ SYSCOMMAND**](../menurc/wm-syscommand.md) alla funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) e il parametro *wParam* del messaggio specifica il valore **SC \_ Move** o **SC \_ size** . L'operazione è completa quando [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) restituisce.

Il sistema invia il messaggio **WM \_ ENTERSIZEMOVE** indipendentemente dal fatto che il trascinamento delle finestre complete sia abilitato.

Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_ENTERSIZEMOVE                0x0231
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
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**\_EXITSIZEMOVE WM**](wm-exitsizemove.md)
</dt> <dt>

[**\_SYSCOMMAND WM**](../menurc/wm-syscommand.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
