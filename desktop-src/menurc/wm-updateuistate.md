---
title: Messaggio WM_UPDATEUISTATE (winuser. h)
description: Un'applicazione invia il \_ messaggio WM UPDATEUISTATE per modificare lo stato dell'interfaccia utente per la finestra specificata e tutte le relative finestre figlio.
ms.assetid: cbdeeddd-59b2-4a73-bfe9-17647d32bcf3
keywords:
- Menu del messaggio WM_UPDATEUISTATE e altre risorse
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
ms.openlocfilehash: 003d9ca45b357a7d0ebc172000b1e2c01505db8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121619"
---
# <a name="wm_updateuistate-message"></a>\_Messaggio UPDATEUISTATE WM

Un'applicazione invia il messaggio **WM \_ UPDATEUISTATE** per modificare lo stato dell'interfaccia utente per la finestra specificata e tutte le relative finestre figlio.


```C++
#define WM_UPDATEUISTATE                0x0128
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

La parola di ordine inferiore specifica l'azione da eseguire. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                                                                   | Significato                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UIS_CLEAR"></span><span id="uis_clear"></span><dl> <dt>**Interfacce utente \_ Cancella**</dt> <dt>2</dt> </dl>                | L'elemento di stato dell'interfaccia utente specificato dalla parola più significativa deve essere nascosto.<br/>                                                                   |
| <span id="UIS_INITIALIZE"></span><span id="uis_initialize"></span><dl> <dt>**Interfacce utente \_ Inizializza**</dt> <dt>3</dt> </dl> | L'elemento di stato dell'interfaccia utente specificato dalla parola più significativa deve essere modificato in base all'ultimo evento di input. Per altre informazioni, vedere la sezione Osservazioni.<br/> |
| <span id="UIS_SET"></span><span id="uis_set"></span><dl> <dt>**Interfacce utente \_ SET**</dt> <dt>1</dt> </dl>                      | L'elemento di stato dell'interfaccia utente specificato dalla parola più significativa dovrebbe essere visibile.<br/>                                                                  |



 

La parola più ordinata specifica quali elementi di stato dell'interfaccia utente sono interessati o lo stile del controllo. Il parametro può essere costituito da uno o più dei valori seguenti.



| Valore                                                                                                                                                                                                                     | Significato                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="UISF_ACTIVE"></span><span id="uisf_active"></span><dl> <dt>**UISF \_**</dt> <dt>0x4</dt> attivo </dl>          | Un controllo deve essere disegnato nello stile usato per i controlli attivi.<br/> |
| <span id="UISF_HIDEACCEL"></span><span id="uisf_hideaccel"></span><dl> <dt>**UISF \_**</dt> <dt>0x2</dt> HIDEACCEL </dl> | Tasti di scelta rapida.<br/>                                           |
| <span id="UISF_HIDEFOCUS"></span><span id="uisf_hidefocus"></span><dl> <dt>**UISF \_**</dt> <dt>0x1</dt> hideFocus </dl> | Indicatori di stato attivo.<br/>                                                |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Una finestra deve inviare questo messaggio per modificare lo stato dell'interfaccia utente di tutte le relative finestre figlio. A differenza del messaggio [**WM \_ CHANGEUISTATE**](wm-changeuistate.md) , che è una notifica, quando [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) elabora il messaggio **WM \_ UPDATEUISTATE** modifica lo stato dell'interfaccia utente e propaga le modifiche a tutte le finestre figlio.

La funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) aggiorna lo stato dell'interfaccia utente in base al valore *wParam* . Se lo stato dell'interfaccia utente viene modificato, la funzione Invia il messaggio a tutte le finestre figlio immediate. **DefWindowProc** invia anche questo messaggio quando riceve un messaggio [**WM \_ CHANGEUISTATE**](wm-changeuistate.md) che comunica al sistema che la finestra figlio intende modificare lo stato dell'interfaccia utente.

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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**\_CHANGEUISTATE WM**](wm-changeuistate.md)
</dt> <dt>

[**\_QUERYUISTATE WM**](wm-queryuistate.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Tasti di scelta rapida](keyboard-accelerators.md)
</dt> </dl>

 

