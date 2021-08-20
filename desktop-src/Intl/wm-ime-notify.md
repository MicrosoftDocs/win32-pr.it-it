---
description: Inviato a un'applicazione per notificare le modifiche alla finestra IME. Una finestra riceve questo messaggio tramite la relativa funzione WindowProc.
ms.assetid: 20e064b8-2baf-4b4c-8341-36c3e4643eff
title: WM_IME_NOTIFY messaggio (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a072ff41b5731662afa94e387ec48de7d14bc245906e581303fe976dcf455708
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014219"
---
# <a name="wm_ime_notify-message"></a>WM_IME_NOTIFY messaggio

Inviato a un'applicazione per notificare le modifiche alla finestra IME. Una finestra riceve questo messaggio tramite la relativa [**funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,       
  WM_IME_NOTIFY,   
  WPARAM wParam,   
  LPARAM lParam     
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Hwnd* 
</dt> <dd>

Handle per la finestra.

</dd> <dt>

*wParam* 
</dt> <dd>

Comando. Questo parametro può avere uno dei valori seguenti.

<dl>
<dd><a href="imn-changecandidate.md">IMN_CHANGECANDIDATE</a></dd> 
<dd><a href="imn-closecandidate.md">IMN_CLOSECANDIDATE</a></dd> 
<dd><a href="imn-closestatuswindow.md">IMN_CLOSESTATUSWINDOW</a></dd> 
<dd><a href="imn-guideline.md">IMN_GUIDELINE</a></dd> 
<dd><a href="imn-opencandidate.md">IMN_OPENCANDIDATE</a></dd> 
<dd><a href="imn-openstatuswindow.md">IMN_OPENSTATUSWINDOW</a></dd> 
<dd><a href="imn-setcandidatepos.md">IMN_SETCANDIDATEPOS</a></dd> 
<dd><a href="imn-setcompositionfont.md">IMN_SETCOMPOSITIONFONT</a></dd> 
<dd><a href="imn-setcompositionwindow.md">IMN_SETCOMPOSITIONWINDOW</a></dd> 
<dd><a href="imn-setconversionmode.md">IMN_SETCONVERSIONMODE</a></dd> 
<dd><a href="imn-setopenstatus.md">IMN_SETOPENSTATUS</a></dd> 
<dd><a href="imn-setsentencemode.md">IMN_SETSENTENCEMODE</a></dd> 
<dd><a href="imn-setstatuswindowpos.md">IMN_SETSTATUSWINDOWPOS</a></dd> 
</dl> 
</dd> 
<dt>

*lParam* 
</dt> <dd>

Dati specifici del comando, con formato dipendente dal valore del *parametro wParam.* Per altre informazioni, vedere la documentazione per ogni comando.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito dipende dal comando inviato.

## <a name="remarks"></a>Commenti

Un'applicazione elabora questo messaggio se è responsabile della gestione della finestra IME.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                                                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                                                                      |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h);</dt> <dt>Imm.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Gestione metodi di input](input-method-manager.md)
</dt> <dt>

[Messaggi di Gestione metodi di input](input-method-manager-messages.md)
</dt> <dt>

[IMN_CHANGECANDIDATE](imn-changecandidate.md)
</dt> <dt>

[IMN_CLOSECANDIDATE](imn-closecandidate.md)
</dt> <dt>

[IMN_CLOSESTATUSWINDOW](imn-closestatuswindow.md)
</dt> <dt>

[IMN_GUIDELINE](imn-guideline.md)
</dt> <dt>

[IMN_OPENCANDIDATE](imn-opencandidate.md)
</dt> <dt>

[IMN_OPENSTATUSWINDOW](imn-openstatuswindow.md)
</dt> <dt>

[IMN_SETCANDIDATEPOS](imn-setcandidatepos.md)
</dt> <dt>

[IMN_SETCOMPOSITIONFONT](imn-setcompositionfont.md)
</dt> <dt>

[IMN_SETCOMPOSITIONWINDOW](imn-setcompositionwindow.md)
</dt> <dt>

[IMN_SETCONVERSIONMODE](imn-setconversionmode.md)
</dt> <dt>

[IMN_SETOPENSTATUS](imn-setopenstatus.md)
</dt> <dt>

[IMN_SETSENTENCEMODE](imn-setsentencemode.md)
</dt> <dt>

[IMN_SETSTATUSWINDOWPOS](imn-setstatuswindowpos.md)
</dt> </dl>

 

 
