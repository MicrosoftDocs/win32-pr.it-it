---
title: Messaggio WM_COMMAND (winuser. h)
description: Inviato quando l'utente seleziona un elemento di comando da un menu, quando un controllo Invia un messaggio di notifica alla relativa finestra padre o quando viene convertita una sequenza di tasti di scelta rapida.
ms.assetid: 5516098e-fd90-49c8-afb0-78164b028376
keywords:
- Menu del messaggio WM_COMMAND e altre risorse
topic_type:
- apiref
api_name:
- WM_COMMAND
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: 1826c4668f3be8a2991c914e60320b55de867e33
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330436"
---
# <a name="wm_command-message"></a>\_Messaggio di comando WM

Inviato quando l'utente seleziona un elemento di comando da un menu, quando un controllo Invia un messaggio di notifica alla relativa finestra padre o quando viene convertita una sequenza di tasti di scelta rapida.


```C++
#define WM_COMMAND                      0x0111
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Per una descrizione di questo parametro, vedere la sezione Osservazioni.

</dd> <dt>

*lParam* 
</dt> <dd>

Per una descrizione di questo parametro, vedere la sezione Osservazioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora il messaggio, deve restituire zero.

## <a name="example"></a>Esempio

```c
BOOL AboutDlg (
    HWND hDlg, 
    UINT message, 
    WPARAM wParam, 
    LPARAM lParam)
{
    BOOL bRet = FALSE;
    
    switch (message) 
    {
        case WM_INITDIALOG:
            bRet = TRUE;
            break;

        case WM_COMMAND:
            if (wParam == IDOK ||
                wParam == IDCANCEL) 
            {
                EndDialog(hDlg, TRUE);
                bRet = TRUE;
            }
            break;
    }

    return bRet;
}
```
Esempio tratto da [esempi di Windows classico](https://github.com/microsoft/Windows-classic-samples) in GitHub.


## <a name="remarks"></a>Commenti

L'uso dei parametri *wParam* e *lParam* è riepilogato qui.



| Origine messaggio | wParam (parola alta)                | wParam (parola bassa)                | lParam                       |
|----------------|-----------------------------------|----------------------------------|------------------------------|
| Menu           | 0                                 | Identificatore menu (IDM \_ \* )        | 0                            |
| Acceleratore    | 1                                 | Identificatore acceleratore (IDM \_ \* ) | 0                            |
| Control        | Codice di notifica definito dal controllo | Identificatore di controllo               | Handle per la finestra di controllo |



 

### <a name="menus"></a>Menu

Se un'applicazione Abilita un separatore di menu, il sistema invia un messaggio di **\_ comando WM** con la parola bassa del parametro *wParam* impostato su zero quando l'utente seleziona il separatore.

Se un menu viene definito con un valore [**MENUINFO. dwStyle**](/windows/win32/api/winuser/ns-winuser-menuinfo) di **MNS \_ NOTIFYBYPOS**, viene inviato [**WM \_ MENUCOMMAND**](wm-menucommand.md) anziché il **\_ comando WM**.

### <a name="accelerators"></a>Tasti di scelta rapida

Le sequenze di tasti dell'acceleratore che selezionano gli elementi dal menu finestra vengono convertite in messaggi [**WM \_ SYSCOMMAND**](wm-syscommand.md) .

Se si verifica una sequenza di tasti di scelta rapida che corrisponde a una voce di menu quando la finestra proprietaria del menu è ridotta a icona, non viene inviato alcun messaggio di **\_ comando WM** . Tuttavia, se si verifica una sequenza di tasti di scelta rapida che non corrisponde ad alcuno degli elementi nel menu della finestra o nel menu finestra, viene inviato un messaggio di **\_ comando WM** , anche se la finestra è ridotta a icona.

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

**Informazioni concettuali**
</dt> <dt>

[Menu](menus.md)
</dt> </dl>

 

