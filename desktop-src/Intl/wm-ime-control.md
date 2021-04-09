---
description: Inviato da un'applicazione per indirizzare la finestra IME per eseguire il comando richiesto.
ms.assetid: 5d3b7f8a-57c9-41e3-8022-9a3f515fc32e
title: Messaggio WM_IME_CONTROL (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd0adc534883bc0b31984c8d3e9b57a04b555987
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879294"
---
# <a name="wm_ime_control-message"></a>Messaggio WM_IME_CONTROL

Inviato da un'applicazione per indirizzare la finestra IME per eseguire il comando richiesto. L'applicazione utilizza questo messaggio per controllare la finestra IME creata. Per inviare questo messaggio, l'applicazione chiama la funzione [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) con i parametri seguenti.


```C++
SendMessage(
  HWND   hwnd,
  WM_IME_CONTROL, 
  WPARAM wParam,
  LPARAM lParam             
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*HWND* 
</dt> <dd>

Handle per la finestra.

</dd> <dt>

*wParam* 
</dt> <dd>

Comando. Per il parametro è possibile specificare uno dei valori riportati di seguito:

<dl>
<dd><a href="imc-closestatuswindow.md">IMC_CLOSESTATUSWINDOW</a></dd> 
<dd><a href="imc-getcandidatepos.md">IMC_GETCANDIDATEPOS</a></dd> 
<dd><a href="imc-getcompositionfont.md">IMC_GETCOMPOSITIONFONT</a></dd> 
<dd><a href="imc-getcompositionwindow.md">IMC_GETCOMPOSITIONWINDOW</a></dd> 
<dd><a href="imc-getstatuswindowpos.md">IMC_GETSTATUSWINDOWPOS</a></dd> 
<dd><a href="imc-openstatuswindow.md">IMC_OPENSTATUSWINDOW</a></dd> 
<dd><a href="imc-setcandidatepos.md">IMC_SETCANDIDATEPOS</a></dd> 
<dd><a href="imc-setcompositionfont.md">IMC_SETCOMPOSITIONFONT</a>></dd> 
<dd><a href="imc-setcompositionwindow.md">IMC_SETCOMPOSITIONWINDOW</a></dd> 
<dd><a href="imc-setstatuswindowpos.md">IMC_SETSTATUSWINDOWPOS</a></dd> 
</dl>
</dd>

<dt>

*lParam* 
</dt> <dd>

Dati specifici del comando, con formato dipendente dal valore del parametro *wParam* . Per ulteriori informazioni, fare riferimento alla documentazione per ogni comando.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il messaggio restituisce un valore specifico del comando.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                                                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                                                                      |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h); </dt> <dt>Imm. h (Includi Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Gestione metodo di input](input-method-manager.md)
</dt> <dt>

[Messaggi di gestione metodo di input](input-method-manager-messages.md)
</dt> <dt>

[IMC_CLOSESTATUSWINDOW](imc-closestatuswindow.md)
</dt> <dt>

[IMC_GETCANDIDATEPOS](imc-getcandidatepos.md)
</dt> <dt>

[IMC_GETCOMPOSITIONFONT](imc-getcompositionfont.md)
</dt> <dt>

[IMC_GETCOMPOSITIONWINDOW](imc-getcompositionwindow.md)
</dt> <dt>

[IMC_GETSTATUSWINDOWPOS](imc-getstatuswindowpos.md)
</dt> <dt>

[IMC_OPENSTATUSWINDOW](imc-openstatuswindow.md)
</dt> <dt>

[IMC_SETCANDIDATEPOS](imc-setcandidatepos.md)
</dt> <dt>

[IMC_SETCOMPOSITIONFONT](imc-setcompositionfont.md)
</dt> <dt>

[IMC_SETCOMPOSITIONWINDOW](imc-setcompositionwindow.md)
</dt> <dt>

[IMC_SETSTATUSWINDOWPOS](imc-setstatuswindowpos.md)
</dt> </dl>

 

 
