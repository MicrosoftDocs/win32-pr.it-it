---
title: Messaggio WM_CHANGEUISTATE (winuser. h)
description: Un'applicazione invia il \_ messaggio WM CHANGEUISTATE per indicare che lo stato dell'interfaccia utente deve essere modificato.
ms.assetid: d8dfc2fe-c64f-4e7e-b021-127aa85d5dd6
keywords:
- Menu del messaggio WM_CHANGEUISTATE e altre risorse
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
ms.openlocfilehash: 1cdfec2a26b3b3d160d3d207c338c8ebecd32bf2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743583"
---
# <a name="wm_changeuistate-message"></a>\_Messaggio CHANGEUISTATE WM

Un'applicazione invia il messaggio **WM \_ CHANGEUISTATE** per indicare che lo stato dell'interfaccia utente deve essere modificato.


```C++
#define WM_CHANGEUISTATE                0x0127
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

La parola di ordine inferiore specifica l'azione da intraprendere. Il membro può essere uno dei valori seguenti.



| Valore                                                                                                                                                                                                                   | Significato                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UIS_CLEAR"></span><span id="uis_clear"></span><dl> <dt>**Interfacce utente \_ Cancella**</dt> <dt>2</dt> </dl>                | I flag di stato dell'interfaccia utente specificati dalla parola di ordine superiore devono essere cancellati.<br/>                                                                  |
| <span id="UIS_INITIALIZE"></span><span id="uis_initialize"></span><dl> <dt>**Interfacce utente \_ Inizializza**</dt> <dt>3</dt> </dl> | I flag di stato dell'interfaccia utente specificati dalla parola di ordine superiore devono essere modificati in base all'ultimo evento di input. Per altre informazioni, vedere la sezione Osservazioni.<br/> |
| <span id="UIS_SET"></span><span id="uis_set"></span><dl> <dt>**Interfacce utente \_ SET**</dt> <dt>1</dt> </dl>                      | È necessario impostare i flag di stato dell'interfaccia utente specificati dalla parola più avanzata.<br/>                                                                      |



 

La parola più ordinata specifica quali elementi di stato dell'interfaccia utente sono interessati o lo stile del controllo. Il membro può essere costituito da uno o più dei valori seguenti.



| Valore                                                                                                                                                                                                                     | Significato                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="UISF_ACTIVE"></span><span id="uisf_active"></span><dl> <dt>**UISF \_**</dt> <dt>0x4</dt> attivo </dl>          | Un controllo deve essere disegnato nello stile usato per i controlli attivi.<br/> |
| <span id="UISF_HIDEACCEL"></span><span id="uisf_hideaccel"></span><dl> <dt>**UISF \_**</dt> <dt>0x2</dt> HIDEACCEL </dl> | Gli acceleratori tastiera sono nascosti.<br/>                                |
| <span id="UISF_HIDEFOCUS"></span><span id="uisf_hidefocus"></span><dl> <dt>**UISF \_**</dt> <dt>0x1</dt> hideFocus </dl> | Gli indicatori di stato attivo sono nascosti.<br/>                                     |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene utilizzato e deve essere 0.

</dd> </dl>

## <a name="remarks"></a>Commenti

Una finestra deve inviare questo messaggio a se stesso o al relativo padre quando deve modificare gli elementi di stato dell'interfaccia utente di tutte le finestre nella stessa gerarchia. La routine della finestra deve consentire a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) di elaborare questo messaggio in modo che l'intero albero della finestra abbia uno stato coerente dell'interfaccia utente. Quando la finestra di primo livello riceve il messaggio **WM \_ CHANGEUISTATE** , invia un messaggio [**WM \_ UPDATEUISTATE**](wm-updateuistate.md) con gli stessi parametri a tutte le finestre figlio. Quando il sistema elabora il messaggio **WM \_ UPDATEUISTATE** , apporta la modifica nello stato dell'interfaccia utente.

Se la parola più bassa di *wParam* è l'inizializzazione di interfacce utente \_ , il sistema invierà il messaggio [**WM \_ UPDATEUISTATE**](wm-updateuistate.md) con lo stato dell'interfaccia utente in base all'ultimo evento di input. Se, ad esempio, l'ultimo input proviene dal mouse, il sistema nasconderà i segnali da tastiera. Se l'ultimo input proviene dalla tastiera, il sistema visualizzerà i suggerimenti da tastiera. Se lo stato risultante dall'elaborazione di **WM \_ CHANGEUISTATE** è uguale a quello precedente, [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) non invia questo messaggio.

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

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**\_QUERYUISTATE WM**](wm-queryuistate.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Tasti di scelta rapida](keyboard-accelerators.md)
</dt> </dl>

 

