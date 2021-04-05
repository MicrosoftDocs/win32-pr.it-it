---
description: Notifica a una finestra che la relativa area non client viene eliminata definitivamente. La funzione DestroyWindow invia il \_ messaggio WM NCDESTROY alla finestra che segue il \_ messaggio WM Destroy.
ms.assetid: 64ab268d-0e90-4401-81d3-a4da64196001
title: Messaggio WM_NCDESTROY (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a462f679a29f471638299e037749adaf32a85dea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967564"
---
# <a name="wm_ncdestroy-message"></a>\_Messaggio NCDESTROY WM

Notifica a una finestra che la relativa area non client viene eliminata definitivamente. La funzione [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) invia il messaggio **WM \_ NCDESTROY** alla finestra che segue il messaggio [**WM \_ Destroy**](wm-destroy.md) .[**WM \_ Destroy**](wm-destroy.md) viene usato per liberare l'oggetto Memory allocato associato alla finestra.

Il messaggio **WM \_ NCDESTROY** viene inviato dopo che le finestre figlio sono state eliminate definitivamente. Al contrario, [**WM \_ Destroy**](wm-destroy.md) viene inviato prima che vengano distrutte le finestre figlio.

Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_NCDESTROY                    0x0082
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

Se un'applicazione elabora il messaggio, deve restituire zero.

## <a name="remarks"></a>Commenti

Questo messaggio libera la memoria allocata internamente per la finestra.

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

[**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow)
</dt> <dt>

[**eliminazione di WM \_**](wm-destroy.md)
</dt> <dt>

[**\_NCCREATE WM**](wm-nccreate.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
