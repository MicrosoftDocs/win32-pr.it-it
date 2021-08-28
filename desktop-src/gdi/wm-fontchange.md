---
description: Un'applicazione invia il messaggio WM FONTCHANGE a tutte le finestre di primo livello del sistema dopo aver \_ modificato il pool di risorse del tipo di carattere.
ms.assetid: 4774308e-2f18-4a35-a769-56871f3c29a2
title: WM_FONTCHANGE messaggio (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12c88edaf2db356fea2b92ce05769360ac9c8664e913ff6e5a05daaf245d1204
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119399931"
---
# <a name="wm_fontchange-message"></a>Messaggio \_ WM FONTCHANGE

Un'applicazione invia il **messaggio WM \_ FONTCHANGE** a tutte le finestre di primo livello del sistema dopo aver modificato il pool di risorse del tipo di carattere.

Per inviare questo messaggio, chiamare la [**funzione SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) con i parametri seguenti.


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

Un'applicazione che aggiunge o rimuove tipi di carattere dal sistema ,ad esempio usando la funzione [**AddFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-addfontresourcea) o [**RemoveFontResource,**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea) deve inviare questo messaggio a tutte le finestre di primo livello.

Per inviare il **messaggio WM \_ FONTCHANGE** a tutte le finestre di primo livello, un'applicazione può chiamare la funzione **SendMessage** con il parametro *hwnd* impostato su HWND \_ BROADCAST.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica di tipi di carattere e testo](fonts-and-text.md)
</dt> <dt>

[Tipi di carattere e messaggi di testo](font-and-text-messages.md)
</dt> <dt>

[**Addfontresource**](/windows/desktop/api/Wingdi/nf-wingdi-addfontresourcea)
</dt> <dt>

[**RemoveFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea)
</dt> </dl>

 

 
