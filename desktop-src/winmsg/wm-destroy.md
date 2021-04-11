---
description: Inviato quando una finestra viene distrutta. Viene inviata alla routine della finestra che viene distrutta dopo la rimozione della finestra dallo schermo.
ms.assetid: 089c0645-199b-4a90-9cbc-740f0cf3267d
title: Messaggio WM_DESTROY (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1db195c22c38759146fb76e98edf4ca7f605a1c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232464"
---
# <a name="wm_destroy-message"></a>\_Messaggio WM Destroy

Inviato quando una finestra viene distrutta. Viene inviata alla routine della finestra che viene distrutta dopo la rimozione della finestra dallo schermo.

Questo messaggio viene inviato prima alla finestra distrutta e quindi alle finestre figlio (se presenti) distrutte. Durante l'elaborazione del messaggio, è possibile presupporre che tutte le finestre figlio esistano ancora.

Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_DESTROY                      0x0002
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

Se la finestra distrutta fa parte della catena del visualizzatore degli Appunti (impostata chiamando la funzione [**SetClipboardViewer**](/windows/win32/api/winuser/nf-winuser-setclipboardviewer) ), la finestra deve rimuovere se stessa dalla catena elaborando la funzione [**ChangeClipboardChain**](/windows/win32/api/winuser/nf-winuser-changeclipboardchain) prima di restituire il messaggio **WM \_ Destroy** .

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

[**ChangeClipboardChain**](/windows/win32/api/winuser/nf-winuser-changeclipboardchain)
</dt> <dt>

[**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow)
</dt> <dt>

[**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage)
</dt> <dt>

[**SetClipboardViewer**](/windows/win32/api/winuser/nf-winuser-setclipboardviewer)
</dt> <dt>

[**\_chiusura WM**](wm-close.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
