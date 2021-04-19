---
title: Messaggio WM_CHOOSEFONT_GETLOGFONT (COMMDLG. h)
description: Un'applicazione invia il \_ messaggio WM ChooseFont \_ GETLOGFONT a una finestra di dialogo tipo di carattere per recuperare le informazioni sulle selezioni dei tipi di carattere correnti dell'utente.
ms.assetid: afbf953a-13dd-409b-a988-f1426c8bbd31
keywords:
- Finestre di dialogo WM_CHOOSEFONT_GETLOGFONT messaggio
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
ms.openlocfilehash: 696246d26c2b87e9b299844a9dc7e78d39ac632f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302084"
---
# <a name="wm_choosefont_getlogfont-message"></a>\_ \_ Messaggio GETLOGFONT di WM ChooseFont

Un'applicazione invia il messaggio **WM \_ ChooseFont \_ GETLOGFONT** a una finestra di dialogo tipo di **carattere** per recuperare le informazioni sulle selezioni dei tipi di carattere correnti dell'utente.


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

Puntatore a una struttura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) che riceve informazioni sulle selezioni del tipo di carattere correnti dell'utente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce alcun valore.

## <a name="remarks"></a>Commenti

La funzione [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) crea una finestra di dialogo del **tipo di carattere** . Quando l'utente chiude la finestra di dialogo **tipo di carattere** , la funzione **ChooseFont** restituisce informazioni sulle selezioni del tipo di carattere dell'utente nella struttura [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) . Il membro **LPLOGFONT** della struttura **ChooseFont** è un puntatore a una struttura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .

Usare il messaggio **WM \_ ChooseFont \_ GETLOGFONT** per ottenere informazioni sulle selezioni del tipo di carattere corrente dell'utente mentre è aperta la finestra di dialogo tipo di **carattere** . Se ad esempio si Abilita il pulsante **applica** nella finestra di dialogo **tipo di carattere** , inviare il messaggio per ottenere le informazioni sul tipo di carattere da applicare alla selezione di testo corrente.

In genere, si abilita una procedura [*CFHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc) hook per elaborare i messaggi di [**\_ comando WM**](/windows/desktop/menurc/wm-command) per il pulsante **applica** . Quando l'utente fa clic sul pulsante **applica** , la procedura hook invia il messaggio **WM \_ ChooseFont \_ GETLOGFONT** alla finestra di dialogo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>COMMDLG. h (include Windows. h)</dt> </dl> |



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

[**\_comando WM**](/windows/desktop/menurc/wm-command)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Libreria finestra di dialogo comune](common-dialog-box-library.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> </dl>

 

