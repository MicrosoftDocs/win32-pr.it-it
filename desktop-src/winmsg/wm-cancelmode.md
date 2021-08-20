---
description: Inviato per annullare determinate modalità, ad esempio mouse capture.
ms.assetid: c801233a-c4d8-4fd9-aaf0-3d4503bbce26
title: WM_CANCELMODE messaggio (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae26cef4919ed93bb2a1c60376ab450560cd2142cef7b3040032f791c45ab09f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117849300"
---
# <a name="wm_cancelmode-message"></a>Messaggio \_ CANCELMODE WM

Inviato per annullare determinate modalità, ad esempio mouse capture. Ad esempio, il sistema invia questo messaggio alla finestra attiva quando viene visualizzata una finestra di dialogo o una finestra di messaggio. Alcune funzioni inviano anche questo messaggio in modo esplicito alla finestra specificata, indipendentemente dal fatto che si tratta della finestra attiva. Ad esempio, la [**funzione EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow) invia questo messaggio quando si disabilita la finestra specificata.

Una finestra riceve questo messaggio tramite la [**relativa funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


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

Se un'applicazione elabora questo messaggio, deve restituire zero.

## <a name="remarks"></a>Commenti

Quando viene inviato il messaggio **\_ WM CANCELMODE,** la funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) annulla l'elaborazione interna dell'input della barra di scorrimento standard, annulla l'elaborazione interna del menu e rilascia l'acquisizione del mouse.

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

[**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow)
</dt> <dt>

[**ReleaseCapture**](/windows/win32/api/winuser/nf-winuser-releasecapture)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
