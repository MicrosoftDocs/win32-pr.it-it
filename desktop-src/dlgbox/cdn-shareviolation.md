---
title: CDN_SHAREVIOLATION di notifica (Commdlg.h)
description: Inviato da una finestra di dialogo Apri o Salva con nome di tipo Esplora risorse quando l'utente fa clic sul pulsante OK e si verifica una violazione della condivisione di rete per il file selezionato.
ms.assetid: a62ca550-0997-4379-aaaf-a5bc9414bd69
keywords:
- CDN_SHAREVIOLATION di dialogo del codice di notifica
topic_type:
- apiref
api_name:
- CDN_SHAREVIOLATION
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77cd862fa1c3598a4e81a776004f26ef02290477
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548856"
---
# <a name="cdn_shareviolation-notification-code"></a>Codice di notifica \_ SHAREVIOLATION della rete CDN

\[A partire da Windows Vista, le **finestre di** **dialogo** comuni Apri e Salva con nome sono state sostituite dalla finestra di dialogo [Elemento comune](../shell/common-file-dialog.md). È consigliabile usare l'API Common Item Dialog al posto di queste finestre di dialogo di Common Dialog Box Library.\]

Inviato da una  finestra  di dialogo Apri o Salva con nome di tipo Esplora risorse quando l'utente fa clic sul pulsante **OK** e si verifica una violazione della condivisione di rete per il file selezionato.

La procedura hook [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) riceve questo messaggio sotto forma di messaggio [**WM \_ NOTIFY.**](../controls/wm-notify.md)


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_SHAREVIOLATION      (CDN_FIRST - 0x0003)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura OFNOTIFY.**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) Il **membro pszFile** di questa struttura è un puntatore al nome del file che ha avuto la violazione di condivisione. La **struttura OFNOTIFY** contiene una [**struttura NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) il cui membro di codice indica il messaggio di notifica **\_ SHAREVIOLATION** della rete CDN. 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito indica il modo in cui la finestra di dialogo deve gestire la violazione di condivisione.

Se la routine hook restituisce zero, nella finestra di dialogo viene visualizzato il messaggio di avviso standard per una violazione di condivisione.

Per impedire la visualizzazione del messaggio di avviso standard, restituire un valore diverso da zero dalla routine hook e chiamare la [**funzione SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) per impostare uno dei valori **\_ MSGRESULT DWL** seguenti.



| Codice/valore restituito                                                                                                                                           | Descrizione                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OFN \_ SHAREFALLTHROUGH**</dt> <dt>2</dt> </dl> | Fa in modo che la finestra di dialogo restituirà il nome del file senza avvisare l'utente della violazione di condivisione.<br/>  |
| <dl> <dt>**OFN \_ SHARENOWARN**</dt> <dt>1</dt> </dl>      | Fa sì che la finestra di dialogo rifiuti il nome del file senza avvisare l'utente della violazione di condivisione. <br/> |



 

## <a name="remarks"></a>Commenti

Il sistema invia questa notifica solo se la finestra di dialogo è stata creata usando il **valore OFN \_ EXPLORER.**

Il sistema invia questa notifica solo se il **valore DI \_ SHAREAWARE OFN** non è stato specificato al momento della creazione della finestra di dialogo.

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

[**Getopenfilename**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[**GetSaveFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

[**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[**Setwindowlong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Libreria di finestre di dialogo comuni](common-dialog-box-library.md)
</dt> </dl>

