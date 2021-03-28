---
description: Un'applicazione invia il \_ messaggio WM FONTCHANGE a tutte le finestre di primo livello nel sistema dopo aver modificato il pool di risorse del tipo di carattere.
ms.assetid: 4774308e-2f18-4a35-a769-56871f3c29a2
title: Messaggio WM_FONTCHANGE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3b40650f0077ed854b87a6fd10e1dae610f0c3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980287"
---
# <a name="wm_fontchange-message"></a>\_Messaggio FONTCHANGE WM

Un'applicazione invia il messaggio **WM \_ FONTCHANGE** a tutte le finestre di primo livello nel sistema dopo aver modificato il pool di risorse del tipo di carattere.

Per inviare questo messaggio, chiamare la funzione [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) con i parametri seguenti.


```C++
SendMessage( 
  (HWND)  hWnd,              
  WM_FONTCHANGE,            
  (WPARAM)  wParam,          
  (LPARAM)  lParam            
);
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

## <a name="remarks"></a>Commenti

Un'applicazione che aggiunge o rimuove i tipi di carattere dal sistema, ad esempio tramite la funzione [**AddFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-addfontresourcea) o [**RemoveFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea) , deve inviare questo messaggio a tutte le finestre di primo livello.

Per inviare il messaggio **WM \_ FONTCHANGE** a tutte le finestre di primo livello, un'applicazione può chiamare la funzione **SendMessage** con il parametro *HWND* impostato su HWND \_ broadcast.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Cenni preliminari su tipi di carattere e testo](fonts-and-text.md)
</dt> <dt>

[Tipi di carattere e messaggi di testo](font-and-text-messages.md)
</dt> <dt>

[**AddFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-addfontresourcea)
</dt> <dt>

[**RemoveFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea)
</dt> </dl>

 

 
