---
description: Inviato una volta a una finestra, dopo l'uscita dal ciclo modale di passaggio o di ridimensionamento.
ms.assetid: 3466bfb5-c38d-49d8-a4ab-bf23d09c454c
title: Messaggio WM_EXITSIZEMOVE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22eda44827345ef491814aab69bf0b802b924e5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314866"
---
# <a name="wm_exitsizemove-message"></a>\_Messaggio EXITSIZEMOVE WM

Inviato una volta a una finestra, dopo l'uscita dal ciclo modale di passaggio o di ridimensionamento. La finestra entra nel ciclo modale di movimento o di ridimensionamento quando l'utente fa clic sulla barra del titolo della finestra o sul bordo di ridimensionamento oppure quando la finestra passa il messaggio [**WM \_ SYSCOMMAND**](../menurc/wm-syscommand.md) alla funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) e il parametro *wParam* del messaggio specifica il valore della **\_ dimensione** **SC \_ MOV** e o SC. L'operazione è completa quando [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) restituisce.

Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


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
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**\_ENTERSIZEMOVE WM**](wm-entersizemove.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
