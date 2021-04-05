---
description: Imposta il tipo di carattere che un controllo deve usare durante il disegno del testo.
ms.assetid: 7db6b8af-dbec-4c29-8bf7-d7e95d9813c3
title: Messaggio WM_SETFONT (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fc334e6b8c937759555c471f00ec56254a629c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967562"
---
# <a name="wm_setfont-message"></a>\_Messaggio del tipo di carattere WM

Imposta il tipo di carattere che un controllo deve usare durante il disegno del testo.


```C++
#define WM_SETFONT                      0x0030
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per il tipo di carattere (**Hfont**). Se questo parametro è **null**, il controllo Usa il tipo di carattere di sistema predefinito per creare il testo.

</dd> <dt>

*lParam* 
</dt> <dd>

La parola di basso livello di *lParam* specifica se il controllo deve essere ridisegnato immediatamente dopo l'impostazione del tipo di carattere. Se questo parametro è **true**, il controllo viene ridisegnato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **LRESULT**

Questo messaggio non restituisce alcun valore.

## <a name="remarks"></a>Commenti

Il messaggio **WM di \_ tipo carattere** si applica a tutti i controlli, non solo alle finestre di dialogo.

Il momento migliore per il proprietario di un controllo finestra di dialogo per impostare il tipo di carattere del controllo è quando riceve il messaggio [**WM \_ INITDIALOG**](../dlgbox/wm-initdialog.md) . L'applicazione deve chiamare la funzione [**DeleteObject**](/windows/win32/api/wingdi/nf-wingdi-deleteobject) per eliminare il tipo di carattere quando non è più necessario. ad esempio, dopo l'eliminazione del controllo.

Le dimensioni del controllo non cambiano in seguito alla ricezione del messaggio. Per evitare di ritagliare il testo che non rientra nei limiti del controllo, l'applicazione deve correggere le dimensioni della finestra del controllo prima di impostare il tipo di carattere.

Quando in una finestra di dialogo viene utilizzato lo stile del [ \_ tipo di carattere DS](../dlgbox/about-dialog-boxes.md) per impostare il testo nei relativi controlli, il sistema invia il messaggio di **carattere di \_ tipo WM** alla routine della finestra di dialogo prima di creare i controlli. Un'applicazione può creare una finestra di dialogo che contiene lo \_ stile del tipo di carattere DS chiamando una delle funzioni seguenti:

-   [**CreateDialogIndirect**](/windows/win32/api/winuser/nf-winuser-createdialogindirecta)
-   [**CreateDialogIndirectParam**](/windows/win32/api/winuser/nf-winuser-createdialogindirectparama)
-   [**DialogBoxIndirect**](/windows/win32/api/winuser/nf-winuser-dialogboxindirecta)
-   [**DialogBoxIndirectParam**](/windows/win32/api/winuser/nf-winuser-dialogboxindirectparama)

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

[**\_tipo di carattere WM GetFont**](wm-getfont.md)
</dt> <dt>

[**\_INITDIALOG WM**](../dlgbox/wm-initdialog.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**DeleteObject**](/windows/win32/api/wingdi/nf-wingdi-deleteobject)
</dt> </dl>

 

 
