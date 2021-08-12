---
title: WM_CHOOSEFONT_GETLOGFONT messaggio (Commdlg.h)
description: Un'applicazione invia il messaggio WM CHOOSEFONT GETLOGFONT a una finestra di dialogo Tipo di carattere per recuperare informazioni sulle selezioni correnti del tipo \_ \_ di carattere dell'utente.
ms.assetid: afbf953a-13dd-409b-a988-f1426c8bbd31
keywords:
- WM_CHOOSEFONT_GETLOGFONT finestre di dialogo del messaggio
topic_type:
- apiref
api_name:
- WM_CHOOSEFONT_GETLOGFONT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fb429c3cd66af28485edf2979d2efbe50b3205a2142e963c8c3bb51ef5713f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118280433"
---
# <a name="wm_choosefont_getlogfont-message"></a>Messaggio \_ WM CHOOSEFONT \_ GETLOGFONT

Un'applicazione invia il **messaggio WM \_ CHOOSEFONT \_ GETLOGFONT** **a** una finestra di dialogo Tipo di carattere per recuperare informazioni sulle selezioni correnti del tipo di carattere dell'utente.


```C++
#define WM_USER                        0x0400
#define WM_CHOOSEFONT_GETLOGFONT      (WM_USER + 1)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) che riceve informazioni sulle selezioni correnti del tipo di carattere dell'utente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce un valore.

## <a name="remarks"></a>Commenti

La [**funzione ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) crea una **finestra di dialogo Tipo** di carattere. Quando l'utente chiude la finestra **di** dialogo Tipo di carattere, la funzione **ChooseFont** restituisce informazioni sulle selezioni del tipo di carattere dell'utente nella [**struttura CHOOSEFONT.**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) Il **membro lpLogFont** della struttura **CHOOSEFONT** è un puntatore a una [**struttura LOGFONT.**](/windows/win32/api/wingdi/ns-wingdi-logfonta)

Usare il **messaggio WM \_ CHOOSEFONT \_ GETLOGFONT** per ottenere informazioni sulle selezioni correnti del tipo di carattere dell'utente mentre la **finestra** di dialogo Carattere è aperta. Ad esempio, se si abilita  il **pulsante** Applica nella finestra di dialogo Tipo di carattere, inviare il messaggio per ottenere le informazioni sul tipo di carattere da applicare alla selezione di testo corrente.

In genere, si abilita una procedura hook [*CFHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) per elaborare [**i messaggi WM \_ COMMAND**](/windows/desktop/menurc/wm-command) per il **pulsante** Applica. Quando l'utente fa clic sul **pulsante Applica,** la procedura hook invia il messaggio **WM \_ CHOOSEFONT \_ GETLOGFONT** alla finestra di dialogo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Commdlg.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**CFHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc)
</dt> <dt>

[**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[**COMANDO \_ WM**](/windows/desktop/menurc/wm-command)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Libreria di finestre di dialogo comuni](common-dialog-box-library.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**Logfont**](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> </dl>

 

