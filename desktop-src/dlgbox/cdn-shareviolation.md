---
title: Codice di notifica CDN_SHAREVIOLATION (COMMDLG. h)
description: Inviato da una finestra di dialogo Apri o Salva con nome in stile esploratore quando l'utente fa clic sul pulsante OK e si verifica una violazione di condivisione di rete per il file selezionato.
ms.assetid: a62ca550-0997-4379-aaaf-a5bc9414bd69
keywords:
- Finestre di dialogo CDN_SHAREVIOLATION codice di notifica
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
ms.openlocfilehash: acfa3a91e9c84f15984285f99d071fcde24a4d66
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301590"
---
# <a name="cdn_shareviolation-notification-code"></a>Codice di notifica SHAREVIOLATION della rete CDN \_

\[A partire da Windows Vista, le finestre di dialogo **Apri** e **Salva come** comuni sono state sostituite dalla [finestra di dialogo elemento comune](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)). È consigliabile usare l'API della finestra di dialogo elemento comune anziché queste finestre di dialogo dalla libreria di finestre di dialogo comuni.\]

Inviato da una finestra di dialogo **Apri** o **Salva con nome in** stile esploratore quando l'utente fa clic sul pulsante **OK** e si verifica una violazione di condivisione di rete per il file selezionato.

La procedura [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook riceve questo messaggio sotto forma di messaggio di [**\_ notifica WM**](../controls/wm-notify.md) .


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

Puntatore a una struttura [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) . Il membro **pszFile** di questa struttura è un puntatore al nome del file in cui si è verificata la violazione di condivisione. La struttura **OFNOTIFY** contiene una struttura [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) il cui membro di **codice** indica il messaggio di notifica **\_ SHAREVIOLATION** della rete CDN.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito indica la modalità di gestione della violazione di condivisione da parte della finestra di dialogo.

Se la routine hook restituisce zero, nella finestra di dialogo viene visualizzato il messaggio di avviso standard per una violazione di condivisione.

Per evitare la visualizzazione del messaggio di avviso standard, restituire un valore diverso da zero dalla routine hook e chiamare la funzione [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) per impostare uno dei valori **\_ MSGRESULT DWL** seguenti.



| Codice/valore restituito                                                                                                                                           | Descrizione                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OFN \_ SHAREFALLTHROUGH**</dt> <dt>2</dt> </dl> | Fa in modo che la finestra di dialogo restituisca il nome del file senza avvisare l'utente sulla violazione della condivisione.<br/>  |
| <dl> <dt>**OFN \_ SHARENOWARN**</dt> <dt>1</dt> </dl>      | Fa in modo che la finestra di dialogo rifiuti il nome del file senza avvisare l'utente sulla violazione della condivisione. <br/> |



 

## <a name="remarks"></a>Commenti

Questa notifica viene inviata dal sistema solo se la finestra di dialogo è stata creata con il valore di **OFN \_ Explorer** .

Questa notifica viene inviata dal sistema solo se il valore **\_ SHAREAWARE di OFN** non è stato specificato al momento della creazione della finestra di dialogo.

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

[**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[**GetSaveFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

[**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Libreria finestra di dialogo comune](common-dialog-box-library.md)
</dt> </dl>

 

