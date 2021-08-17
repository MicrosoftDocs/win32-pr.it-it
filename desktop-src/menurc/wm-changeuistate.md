---
title: WM_CHANGEUISTATE messaggio (Winuser.h)
description: Un'applicazione invia il messaggio WM \_ CHANGEUISTATE per indicare che lo stato dell'interfaccia utente deve essere modificato.
ms.assetid: d8dfc2fe-c64f-4e7e-b021-127aa85d5dd6
keywords:
- WM_CHANGEUISTATE messaggio Menu e altre risorse
topic_type:
- apiref
api_name:
- WM_CHANGEUISTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3849f9a5d2ccd0cec1bcaba4280e125ea01a669c8535c2dc520ebb98c3a3fcdb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117869711"
---
# <a name="wm_changeuistate-message"></a>Messaggio \_ WM CHANGEUISTATE

Un'applicazione invia il **messaggio WM \_ CHANGEUISTATE** per indicare che lo stato dell'interfaccia utente deve essere modificato.


```C++
#define WM_CHANGEUISTATE                0x0127
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

La parola di ordine basso specifica l'azione da eseguire. Questo membro può essere uno dei valori seguenti.



| Valore                                                                                                                                                                                                                   | Significato                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UIS_CLEAR"></span><span id="uis_clear"></span><dl> <dt>**Interfaccia utente \_ CLEAR**</dt> <dt>2</dt> </dl>                | I flag di stato dell'interfaccia utente specificati dalla parola di ordine elevato devono essere cancellati.<br/>                                                                  |
| <span id="UIS_INITIALIZE"></span><span id="uis_initialize"></span><dl> <dt>**Interfaccia utente \_ INITIALIZE**</dt> <dt>3</dt> </dl> | I flag di stato dell'interfaccia utente specificati dalla parola di ordine elevato devono essere modificati in base all'ultimo evento di input. Per altre informazioni, vedere la sezione Osservazioni.<br/> |
| <span id="UIS_SET"></span><span id="uis_set"></span><dl> <dt>**Interfaccia utente \_ SET**</dt> <dt>1</dt> </dl>                      | I flag di stato dell'interfaccia utente specificati dalla parola di ordine elevato devono essere impostati.<br/>                                                                      |



 

La parola di ordine elevato specifica gli elementi dello stato dell'interfaccia utente interessati o lo stile del controllo. Questo membro può essere uno o più dei valori seguenti.



| Valore                                                                                                                                                                                                                     | Significato                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="UISF_ACTIVE"></span><span id="uisf_active"></span><dl> <dt>**UISF \_ ACTIVE**</dt> <dt>0x4</dt> </dl>          | Un controllo deve essere disegnato nello stile usato per i controlli attivi.<br/> |
| <span id="UISF_HIDEACCEL"></span><span id="uisf_hideaccel"></span><dl> <dt>**UISF \_ HideACCEL**</dt> <dt>0x2</dt> </dl> | I tasti di scelta rapida sono nascosti.<br/>                                |
| <span id="UISF_HIDEFOCUS"></span><span id="uisf_hidefocus"></span><dl> <dt>**UISF \_ HIDEFOCUS**</dt> <dt>0x1</dt> </dl> | Gli indicatori di stato attivo sono nascosti.<br/>                                     |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato e deve essere 0.

</dd> </dl>

## <a name="remarks"></a>Commenti

Una finestra deve inviare questo messaggio a se stesso o al relativo elemento padre quando deve modificare gli elementi dello stato dell'interfaccia utente di tutte le finestre nella stessa gerarchia. La routine della finestra deve consentire a [**DefWindowProc di**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) elaborare questo messaggio in modo che l'intera struttura ad albero della finestra abbia uno stato coerente dell'interfaccia utente. Quando la finestra di primo livello riceve il **messaggio WM \_ CHANGEUISTATE,** invia un messaggio [**WM \_ UPDATEUISTATE**](wm-updateuistate.md) con gli stessi parametri a tutte le finestre figlio. Quando il sistema elabora il **messaggio WM \_ UPDATEUISTATE,** apporta la modifica allo stato dell'interfaccia utente.

Se la parola in ordine basso di *wParam* è UIS INITIALIZE, il sistema invierà il messaggio WM UPDATEUISTATE con uno stato dell'interfaccia utente in base \_ all'ultimo evento [**\_**](wm-updateuistate.md) di input. Ad esempio, se l'ultimo input proveniva dal mouse, il sistema nasconderà i segnali della tastiera. E, se l'ultimo input proveniva dalla tastiera, il sistema mostrerà i segnali della tastiera. Se lo stato restituito dall'elaborazione **di WM \_ CHANGEUISTATE** è lo stesso dello stato precedente, [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) non invia questo messaggio.

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

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**WM \_ QUERYUISTATE**](wm-queryuistate.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Tasti di scelta rapida](keyboard-accelerators.md)
</dt> </dl>

 

