---
description: Imposta il tipo di carattere che deve essere utilizzato da un controllo durante il disegno di testo.
ms.assetid: 7db6b8af-dbec-4c29-8bf7-d7e95d9813c3
title: WM_SETFONT messaggio (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 811bee30237a64955197588f87866d4a64af89edc640762ec16333839aee9220
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118199937"
---
# <a name="wm_setfont-message"></a>Messaggio \_ WM SETFONT

Imposta il tipo di carattere che deve essere utilizzato da un controllo durante il disegno di testo.


```C++
#define WM_SETFONT                      0x0030
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per il tipo di carattere (**HFONT**). Se questo parametro è **NULL,** il controllo usa il tipo di carattere di sistema predefinito per disegnare testo.

</dd> <dt>

*lParam* 
</dt> <dd>

La parola meno ordinata di *lParam* specifica se il controllo deve essere ridisegnato immediatamente dopo l'impostazione del tipo di carattere. Se questo parametro è **TRUE,** il controllo si ridisegna.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **LRESULT**

Questo messaggio non restituisce un valore.

## <a name="remarks"></a>Commenti

Il **messaggio \_ WM SETFONT** si applica a tutti i controlli, non solo a quelli nelle finestre di dialogo.

Il momento migliore per il proprietario di un controllo finestra di dialogo per impostare il tipo di carattere del controllo è quando riceve il [**messaggio \_ WM INITDIALOG.**](../dlgbox/wm-initdialog.md) L'applicazione deve chiamare [**la funzione DeleteObject**](/windows/win32/api/wingdi/nf-wingdi-deleteobject) per eliminare il tipo di carattere quando non è più necessario. ad esempio dopo l'eliminazione del controllo.

Le dimensioni del controllo non cambiano in seguito alla ricezione di questo messaggio. Per evitare di ritagliare testo che non rientra nei limiti del controllo, l'applicazione deve correggere le dimensioni della finestra di controllo prima di impostare il tipo di carattere.

Quando una finestra di dialogo usa lo stile [ \_ DS SETFONT](../dlgbox/about-dialog-boxes.md) per impostare il testo nei relativi controlli, il sistema invia il messaggio **WM \_ SETFONT** alla procedura della finestra di dialogo prima di creare i controlli. Un'applicazione può creare una finestra di dialogo contenente lo stile SETFONT DS \_ chiamando una delle funzioni seguenti:

-   [**CreateDialogIndirect**](/windows/win32/api/winuser/nf-winuser-createdialogindirecta)
-   [**CreateDialogIndirectParam**](/windows/win32/api/winuser/nf-winuser-createdialogindirectparama)
-   [**DialogBoxIndirect**](/windows/win32/api/winuser/nf-winuser-dialogboxindirecta)
-   [**DialogBoxIndirectParam**](/windows/win32/api/winuser/nf-winuser-dialogboxindirectparama)

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

[**CreateDialogIndirect**](/windows/win32/api/winuser/nf-winuser-createdialogindirecta)
</dt> <dt>

[**CreateDialogIndirectParam**](/windows/win32/api/winuser/nf-winuser-createdialogindirectparama)
</dt> <dt>

[**DialogBoxIndirect**](/windows/win32/api/winuser/nf-winuser-dialogboxindirecta)
</dt> <dt>

[**DialogBoxIndirectParam**](/windows/win32/api/winuser/nf-winuser-dialogboxindirectparama)
</dt> <dt>

[**DLGTEMPLATE**](/windows/win32/api/winuser/ns-winuser-dlgtemplate)
</dt> <dt>

[**MAKELPARAM**](/windows/win32/api/winuser/nf-winuser-makelparam)
</dt> <dt>

[**WM \_ GETFONT**](wm-getfont.md)
</dt> <dt>

[**WM \_ INITDIALOG**](../dlgbox/wm-initdialog.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**DeleteObject**](/windows/win32/api/wingdi/nf-wingdi-deleteobject)
</dt> </dl>

 

 
