---
description: Indica una richiesta di terminazione di un'applicazione e viene generata quando l'applicazione chiama la funzione PostQuitMessage. Questo messaggio causa la restituzione di zero da parte della funzione GetMessage.
ms.assetid: a9bff5dc-cab8-4e08-838e-d92c87c265d6
title: Messaggio WM_QUIT (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8e0d7413d65e9a0fb451fe63504f2ed5be02064
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050045"
---
# <a name="wm_quit-message"></a>\_Messaggio WM Quit

Indica una richiesta di terminazione di un'applicazione e viene generata quando l'applicazione chiama la funzione [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) . Questo messaggio causa la restituzione di zero da parte della funzione [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) .


```C++
#define WM_QUIT                         0x0012
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Codice di uscita specificato nella funzione [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) .

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **LRESULT**

Questo messaggio non ha un valore restituito perché causa l'interruzione del ciclo di messaggi prima che il messaggio venga inviato alla routine della finestra dell'applicazione.

## <a name="remarks"></a>Commenti

Il messaggio **WM \_ Quit** non è associato a una finestra e pertanto non verrà mai ricevuto tramite la procedura finestra di una finestra. Viene recuperato solo dalle funzioni [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) o [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) .

Non pubblicare il messaggio **WM \_ Quit** usando la funzione [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) ; usare [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage).

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

[**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage)
</dt> <dt>

[**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea)
</dt> <dt>

[**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
