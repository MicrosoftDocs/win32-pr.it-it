---
description: Un'applicazione invia il \_ messaggio WM MDICREATE a una finestra del client di interfaccia a documenti multipli (MDI) per creare una finestra figlio MDI.
ms.assetid: f2313ffd-867f-4870-a667-3e5f5402776f
title: Messaggio WM_MDICREATE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fc11e9dfc561b138a95b711d68ecd831a43d2ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314863"
---
# <a name="wm_mdicreate-message"></a>\_Messaggio MDICREATE WM

Un'applicazione invia il messaggio **WM \_ MDICREATE** a una finestra del client di interfaccia a documenti multipli (MDI) per creare una finestra figlio MDI.


```C++
#define WM_MDICREATE                    0x0220
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) contenente le informazioni utilizzate dal sistema per creare la finestra figlio MDI.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HWND**

Se il messaggio ha esito positivo, il valore restituito è l'handle per la nuova finestra figlio.

Se il messaggio ha esito negativo, il valore restituito è **null**.

## <a name="remarks"></a>Commenti

La finestra figlio MDI viene creata con i bit di [**stile della finestra**](window-styles.md) **WS \_ child**, **WS \_ CLIPSIBLINGS**, WS **\_ CLIPCHILDREN**, **WS \_ SYSMENU**, **WS \_ Caption**, **WS \_ THICKFRAME**, **WS \_ MINIMIZEBOX** e **WS \_ MAXIMIZEBOX**, più altri bit di stile specificati nella struttura [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) . Il sistema aggiunge il titolo della nuova finestra figlio al menu finestra della finestra cornice. Un'applicazione deve usare questo messaggio per creare tutte le finestre figlio della finestra client.

Se una finestra client MDI riceve un messaggio che modifica l'attivazione delle finestre figlio mentre la finestra figlio attiva è ingrandita, il sistema ripristina la finestra figlio attiva e ingrandisce la finestra figlio appena attivata.

Quando viene creata una finestra figlio MDI, il sistema invia il messaggio [**WM \_ create**](wm-create.md) alla finestra. Il parametro *lParam* del messaggio **WM \_ create** contiene un puntatore a una struttura [**struttura CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) . Il membro *lpCreateParams* di questa struttura contiene un puntatore alla struttura [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) passata con il messaggio **WM \_ MDICREATE** che ha creato la finestra figlio MDI.

Un'applicazione non deve inviare un secondo messaggio **WM \_ MDICREATE** mentre un messaggio **WM \_ MDICREATE** è ancora in fase di elaborazione. Ad esempio, non deve inviare un messaggio **WM \_ MDICREATE** mentre una finestra figlio MDI sta elaborando il relativo messaggio **WM \_ MDICREATE** .

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

[**CreateMDIWindow**](/windows/win32/api/winuser/nf-winuser-createmdiwindowa)
</dt> <dt>

[**STRUTTURA CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa)
</dt> <dt>

[**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa)
</dt> <dt>

[**creazione di WM \_**](wm-create.md)
</dt> <dt>

[**\_MDIDESTROY WM**](wm-mdidestroy.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Interfaccia a documenti multipli](multiple-document-interface.md)
</dt> </dl>

 

 
