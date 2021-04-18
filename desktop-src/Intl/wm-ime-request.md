---
description: Inviato a un'applicazione per fornire comandi e informazioni sulla richiesta. Una finestra riceve questo messaggio tramite la funzione WindowProc.
ms.assetid: c5e9f256-eed2-46cb-bb33-0e640a975f1f
title: Messaggio WM_IME_REQUEST (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d0cea120d088fe1423b1d7dcb822307886675b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307277"
---
# <a name="wm_ime_request-message"></a>Messaggio WM_IME_REQUEST

Inviato a un'applicazione per fornire comandi e informazioni sulla richiesta. Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,       
  WM_IME_REQUEST,  
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
<dd><a href="imr-candidatewindow.md">IMR_CANDIDATEWINDOW</a></dd> 
<dd><a href="imr-compositionfont.md">IMR_COMPOSITIONFONT</a></dd> 
<dd><a href="imr-compositionwindow.md">IMR_COMPOSITIONWINDOW</a></dd> 
<dd><a href="imr-confirmreconvertstring.md">IMR_CONFIRMRECONVERTSTRING</a></dd> 
<dd><a href="imr-documentfeed.md">IMR_DOCUMENTFEED</a></dd> 
<dd><a href="imr-querycharposition.md">IMR_QUERYCHARPOSITION</a></dd> 
<dd><a href="imr-reconvertstring.md">IMR_RECONVERTSTRING</a></dd> 
</dl> 
</dd> 
<dt>

*lParam* 
</dt> <dd>

Dati specifici del comando. Per ulteriori informazioni, vedere la descrizione di ogni comando.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore specifico del comando.

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

[IMR_CANDIDATEWINDOW](imr-candidatewindow.md)
</dt> <dt>

[IMR_COMPOSITIONFONT](imr-compositionfont.md)
</dt> <dt>

[IMR_COMPOSITIONWINDOW](imr-compositionwindow.md)
</dt> <dt>

[IMR_CONFIRMRECONVERTSTRING](imr-confirmreconvertstring.md)
</dt> <dt>

[IMR_DOCUMENTFEED](imr-documentfeed.md)
</dt> <dt>

[IMR_QUERYCHARPOSITION](imr-querycharposition.md)
</dt> <dt>

[IMR_RECONVERTSTRING](imr-reconvertstring.md)
</dt> </dl>

 

 
