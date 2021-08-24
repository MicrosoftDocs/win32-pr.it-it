---
description: Inviato quando una finestra viene distrutta. Viene inviato alla routine della finestra che viene eliminata definitivamente dopo che la finestra è stata rimossa dallo schermo.
ms.assetid: 089c0645-199b-4a90-9cbc-740f0cf3267d
title: WM_DESTROY messaggio (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7acff03f01e9bf0c8021f8324411f646341a29a5b3b6dc1f9b3493ec89010c1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119587451"
---
# <a name="wm_destroy-message"></a>Messaggio WM \_ DESTROY

Inviato quando una finestra viene distrutta. Viene inviato alla routine della finestra che viene eliminata definitivamente dopo che la finestra è stata rimossa dallo schermo.

Questo messaggio viene inviato prima alla finestra in fase di eliminazione e quindi alle finestre figlio (se presenti) quando vengono distrutte. Durante l'elaborazione del messaggio, si può presumere che tutte le finestre figlio esistano ancora.

Una finestra riceve questo messaggio tramite la relativa [**funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


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

Se un'applicazione elabora questo messaggio, deve restituire zero.

## <a name="remarks"></a>Commenti

Se la finestra da eliminare fa parte della catena del visualizzatore appunti (impostata chiamando la funzione [**SetClipboardViewer),**](/windows/win32/api/winuser/nf-winuser-setclipboardviewer) la finestra deve rimuovere se stessa dalla catena elaborando la funzione [**ChangeClipboardChain**](/windows/win32/api/winuser/nf-winuser-changeclipboardchain) prima di restituire il messaggio **WM \_ DESTROY.**

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

[**ChangeClipboardChain**](/windows/win32/api/winuser/nf-winuser-changeclipboardchain)
</dt> <dt>

[**Destroywindow**](/windows/win32/api/winuser/nf-winuser-destroywindow)
</dt> <dt>

[**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage)
</dt> <dt>

[**SetClipboardViewer**](/windows/win32/api/winuser/nf-winuser-setclipboardviewer)
</dt> <dt>

[**WM \_ CLOSE**](wm-close.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
