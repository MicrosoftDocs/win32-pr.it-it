---
description: Inviato per annullare determinate modalità, ad esempio l'acquisizione del mouse.
ms.assetid: c801233a-c4d8-4fd9-aaf0-3d4503bbce26
title: Messaggio WM_CANCELMODE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c23b842dfdfde7dc550d8ec6d942bcc83ea25f3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314874"
---
# <a name="wm_cancelmode-message"></a>\_Messaggio CANCELMODE WM

Inviato per annullare determinate modalità, ad esempio l'acquisizione del mouse. Ad esempio, il sistema invia questo messaggio alla finestra attiva quando viene visualizzata una finestra di dialogo o una finestra di messaggio. Alcune funzioni inviano inoltre questo messaggio in modo esplicito alla finestra specificata, indipendentemente dal fatto che sia la finestra attiva. Ad esempio, la funzione [**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow) Invia questo messaggio quando si disabilita la finestra specificata.

Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_CANCELMODE                   0x001F
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

Quando viene inviato il messaggio **WM \_ CANCELMODE** , la funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) Annulla l'elaborazione interna dell'input della barra di scorrimento standard, Annulla l'elaborazione interna dei menu e rilascia l'acquisizione del mouse.

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

[**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow)
</dt> <dt>

[**ReleaseCapture**](/windows/win32/api/winuser/nf-winuser-releasecapture)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
