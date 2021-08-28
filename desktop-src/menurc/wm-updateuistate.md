---
title: WM_UPDATEUISTATE messaggio (Winuser.h)
description: Un'applicazione invia il messaggio \_ WM UPDATEUISTATE per modificare lo stato dell'interfaccia utente per la finestra specificata e tutte le relative finestre figlio.
ms.assetid: cbdeeddd-59b2-4a73-bfe9-17647d32bcf3
keywords:
- WM_UPDATEUISTATE menu e altre risorse del messaggio
topic_type:
- apiref
api_name:
- WM_UPDATEUISTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 351770019f18c52c4ff1588a09c803d07f0f58ce032b35af53501ff4e47b6aed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112861"
---
# <a name="wm_updateuistate-message"></a>Messaggio \_ WM UPDATEUISTATE

Un'applicazione invia il **messaggio \_ WM UPDATEUISTATE** per modificare lo stato dell'interfaccia utente per la finestra specificata e tutte le relative finestre figlio.


```C++
#define WM_UPDATEUISTATE                0x0128
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

La parola più bassa specifica l'azione da eseguire. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                                                                   | Significato                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UIS_CLEAR"></span><span id="uis_clear"></span><dl> <dt>**UiS \_ CLEAR**</dt> <dt>2</dt> </dl>                | L'elemento dello stato dell'interfaccia utente specificato dalla parola più importante deve essere nascosto.<br/>                                                                   |
| <span id="UIS_INITIALIZE"></span><span id="uis_initialize"></span><dl> <dt>**UiS \_ INITIALIZE**</dt> <dt>3</dt> </dl> | L'elemento dello stato dell'interfaccia utente specificato dalla parola più importante deve essere modificato in base all'ultimo evento di input. Per altre informazioni, vedere la sezione Osservazioni.<br/> |
| <span id="UIS_SET"></span><span id="uis_set"></span><dl> <dt>**UiS \_ SET**</dt> <dt>1</dt> </dl>                      | L'elemento dello stato dell'interfaccia utente specificato dalla parola più importante deve essere visibile.<br/>                                                                  |



 

La parola più alta specifica quali elementi dello stato dell'interfaccia utente sono interessati o lo stile del controllo. Questo parametro può essere uno o più dei valori seguenti.



| Valore                                                                                                                                                                                                                     | Significato                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="UISF_ACTIVE"></span><span id="uisf_active"></span><dl> <dt>**UISF \_ Active**</dt> <dt>0x4</dt> </dl>          | Un controllo deve essere disegnato nello stile usato per i controlli attivi.<br/> |
| <span id="UISF_HIDEACCEL"></span><span id="uisf_hideaccel"></span><dl> <dt>**UISF \_ HideACCEL**</dt> <dt>0x2</dt> </dl> | Tasti di scelta rapida.<br/>                                           |
| <span id="UISF_HIDEFOCUS"></span><span id="uisf_hidefocus"></span><dl> <dt>**UISF \_ HIDEFOCUS**</dt> <dt>0x1</dt> </dl> | Indicatori di stato attivo.<br/>                                                |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Una finestra deve inviare questo messaggio per modificare lo stato dell'interfaccia utente di tutte le finestre figlio. A differenza del messaggio [**\_ WM CHANGEUISTATE,**](wm-changeuistate.md) che è una notifica, quando [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) elabora il messaggio **WM \_ UPDATEUISTATE** cambia lo stato dell'interfaccia utente e propaga le modifiche a tutte le finestre figlio.

La [**funzione DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) aggiorna lo stato dell'interfaccia utente in base al *valore wParam.* Se lo stato dell'interfaccia utente viene modificato, la funzione invia il messaggio a tutte le finestre figlio immediate. **DefWindowProc** invia questo messaggio anche quando riceve un messaggio [**WM \_ CHANGEUISTATE**](wm-changeuistate.md) che notifica al sistema che una finestra figlio intende modificare lo stato dell'interfaccia utente.

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

[**WM \_ CHANGEUISTATE**](wm-changeuistate.md)
</dt> <dt>

[**WM \_ QUERYUISTATE**](wm-queryuistate.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Tasti di scelta rapida](keyboard-accelerators.md)
</dt> </dl>

 

