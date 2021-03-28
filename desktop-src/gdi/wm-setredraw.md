---
description: Un'applicazione invia il \_ messaggio WM SETREDRAW a una finestra per consentire il ritracciamento delle modifiche in tale finestra o per impedire che le modifiche apportate alla finestra vengano ridisegnato.
ms.assetid: 0085a55e-7bf6-4eb6-a649-832b685db1cc
title: Messaggio WM_SETREDRAW (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 184401e70c8233b03c57db4f8a01bbd6a42e1a35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232543"
---
# <a name="wm_setredraw-message"></a>\_Messaggio SETREDRAW WM

Un'applicazione invia il messaggio **WM \_ SETREDRAW** a una finestra per consentire il ritracciamento delle modifiche in tale finestra o per impedire che le modifiche apportate alla finestra vengano ridisegnato.

Per inviare questo messaggio, chiamare la funzione [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) con i parametri seguenti.


```C++
SendMessage( 
  (HWND) hWnd,              
  WM_SETREDRAW,             
  (WPARAM) wParam,          
  (LPARAM) lParam            
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Stato di riestrazione. Se questo parametro è **true**, il contenuto può essere ridisegnato dopo una modifica. Se questo parametro è **false**, il contenuto non può essere ridisegnato dopo una modifica.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Un'applicazione restituisce zero se elabora questo messaggio.

## <a name="remarks"></a>Commenti

Questo messaggio può essere utile se un'applicazione deve aggiungere diversi elementi a una casella di riepilogo. L'applicazione può chiamare questo messaggio con *wParam* impostato su **false**, aggiungere gli elementi, quindi chiamare di nuovo il messaggio con *wParam* impostato su **true**. Infine, l'applicazione può chiamare [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow)(*HWND*, **null**, **null**, RDW \_ Erase \| RDW \_ frame \| RDW \_ Invalidate \| RDW ALLCHILDREN \_ ) per fare in modo che la casella di riepilogo venga ridisegnata.

> [!Note]  
> [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) con i flag specificati viene usato al posto di [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) , perché il primo è necessario per alcuni controlli che hanno un'area non client autonomamente o con stili di finestra che ne determinano l'uso di un'area non client, ad esempio **WS \_ THICKFRAME**, **WS \_ Border** o **WS \_ ex \_ CLIENTEDGE**. Se il controllo non dispone di un'area non client, **RedrawWindow** con questi flag eseguirà solo la maggior parte dell'invalidamento di **InvalidateRect** .

 

Se l'applicazione invia il messaggio **WM \_ SETREDRAW** a una finestra nascosta, la finestra diventa visibile (ovvero, il sistema operativo aggiunge lo stile **\_ visibile WS** alla finestra).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Cenni preliminari su disegno e disegno](painting-and-drawing.md)
</dt> <dt>

[Disegno e creazione di messaggi](painting-and-drawing-messages.md)
</dt> <dt>

[**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow)
</dt> </dl>

 

 
