---
description: Notifica a una finestra che la relativa area non client viene distrutta. La funzione DestroyWindow invia il messaggio \_ WM NCDESTROY alla finestra che segue il messaggio WM \_ DESTROY.
ms.assetid: 64ab268d-0e90-4401-81d3-a4da64196001
title: WM_NCDESTROY messaggio (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a2e74db0abf22fc2fb3d2a16b5cc63187514d1bee26079490c8d19eae13787e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118200047"
---
# <a name="wm_ncdestroy-message"></a>Messaggio \_ WM NCDESTROY

Notifica a una finestra che la relativa area non client viene distrutta. La [**funzione DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) invia il **messaggio WM \_ NCDESTROY** alla finestra che segue il [**messaggio WM \_ DESTROY.**](wm-destroy.md) [**WM \_ DESTROY**](wm-destroy.md) viene usato per liberare l'oggetto memoria allocato associato alla finestra.

Il **messaggio \_ WM NCDESTROY** viene inviato dopo l'eliminazione delle finestre figlio. Al contrario, [**WM \_ DESTROY viene**](wm-destroy.md) inviato prima che le finestre figlio siano distrutte.

Una finestra riceve questo messaggio tramite la relativa [**funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


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

Se un'applicazione elabora questo messaggio, deve restituire zero.

## <a name="remarks"></a>Commenti

Questo messaggio libera la memoria allocata internamente per la finestra.

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

[**Destroywindow**](/windows/win32/api/winuser/nf-winuser-destroywindow)
</dt> <dt>

[**WM \_ DESTROY**](wm-destroy.md)
</dt> <dt>

[**WM \_ NCCREATE**](wm-nccreate.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
