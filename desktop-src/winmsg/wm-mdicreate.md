---
description: Un'applicazione invia il messaggio WM MDICREATE a una finestra client dell'interfaccia a documenti multipli \_ (MDI) per creare una finestra figlio MDI.
ms.assetid: f2313ffd-867f-4870-a667-3e5f5402776f
title: WM_MDICREATE messaggio (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c69a894ebd2e55bb74486e26cd118366b1e533a490cc50feb5f77aad64c6be3f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056011"
---
# <a name="wm_mdicreate-message"></a>Messaggio \_ WM MDICREATE

Un'applicazione invia **il \_ messaggio WM MDICREATE** a una finestra client dell'interfaccia a documenti multipli (MDI) per creare una finestra figlio MDI.


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

Puntatore a una [**struttura MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) contenente le informazioni utilizzate dal sistema per creare la finestra figlio MDI.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HWND**

Se il messaggio ha esito positivo, il valore restituito è l'handle per la nuova finestra figlio.

Se il messaggio ha esito negativo, il valore restituito è **NULL.**

## <a name="remarks"></a>Commenti

La finestra figlio MDI viene creata con i [**bit**](window-styles.md) di stile della finestra **WS \_ CHILD,** **WS \_ CLIPSIBLINGS,** **WS \_ CLIPCHILDREN, WS** **\_ SYSMENU,** **WS \_ CAPTION,** **WS \_ THICKFRAME,** **WS \_ MINIMIZEBOX** e **WS \_ MAXIMIZEBOX,** oltre a bit di stile aggiuntivi specificati nella [**struttura MDICREATESTRUCT.**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) Il sistema aggiunge il titolo della nuova finestra figlio al menu della finestra della finestra cornice. Un'applicazione deve usare questo messaggio per creare tutte le finestre figlio della finestra client.

Se una finestra del client MDI riceve un messaggio che modifica l'attivazione delle finestre figlio mentre la finestra figlio attiva è ingrandita, il sistema ripristina la finestra figlio attiva e ingrandisce la finestra figlio appena attivata.

Quando viene creata una finestra figlio MDI, il sistema invia il [**messaggio \_ WM CREATE**](wm-create.md) alla finestra. Il *parametro lParam* del messaggio **WM \_ CREATE** contiene un puntatore a una [**struttura CREATESTRUCT.**](/windows/win32/api/winuser/ns-winuser-createstructa) Il *membro lpCreateParams* di questa struttura contiene un puntatore alla struttura [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) passata con il messaggio **WM \_ MDICREATE** che ha creato la finestra figlio MDI.

Un'applicazione non deve inviare un secondo **messaggio \_ MDICREATE WM** mentre è ancora in corso l'elaborazione di un messaggio **\_ MDICREATE WM.** Ad esempio, non deve inviare un messaggio **WM \_ MDICREATE** mentre una finestra figlio MDI sta elaborando il messaggio **\_ MDICREATE WM.**

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

[**CreateMDIWindow**](/windows/win32/api/winuser/nf-winuser-createmdiwindowa)
</dt> <dt>

[**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa)
</dt> <dt>

[**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa)
</dt> <dt>

[**WM \_ CREATE**](wm-create.md)
</dt> <dt>

[**WM \_ MDIDESTROY**](wm-mdidestroy.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Interfaccia a documenti multipli](multiple-document-interface.md)
</dt> </dl>

 

 
