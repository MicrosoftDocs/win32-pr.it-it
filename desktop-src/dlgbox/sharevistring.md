---
title: Messaggio SHAREVISTRING (Commdlg.h)
description: Una finestra di dialogo Apri o Salva con nome invia il messaggio registrato SHAREVISTRING alla procedura hook OFNHookProc, se si verifica una violazione di condivisione per il file selezionato quando l'utente fa clic sul pulsante OK.
ms.assetid: 53884497-4872-4aa8-b56e-2bb98df58fed
keywords:
- Finestre di dialogo del messaggio SHAREVISTRING
topic_type:
- apiref
api_name:
- SHAREVISTRING
- SHAREVISTRINGA
- SHAREVISTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 043bed9edd08269e4e030482cbd44debea3a3695
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548766"
---
# <a name="sharevistring-message"></a>Messaggio SHAREVISTRING

\[A partire da Windows  Vista, le **finestre** di dialogo comuni Apri e Salva con nome sono state sostituite dalla [finestra di dialogo Elemento comune](../shell/common-file-dialog.md). È consigliabile usare l'API Common Item Dialog al posto di queste finestre di dialogo da Common Dialog Box Library.\]

Una **finestra** di dialogo Apri o Salva con nome invia il messaggio registrato **SHAREVISTRING** alla procedura hook [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)se si verifica una violazione di condivisione per il file selezionato quando l'utente fa clic sul pulsante **OK.** 


```C++
#define SHAREVISTRING TEXT("commdlg_ShareViolation")
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura OPENFILENAME.**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) Il **membro lpstrFile** di questa struttura contiene il nome file che ha causato la violazione di condivisione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La routine hook deve restituire uno dei valori seguenti per indicare in che modo la finestra di dialogo deve gestire la violazione di condivisione.



| Codice/valore restituito                                                                                                                                           | Descrizione                                                                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OFN \_ SHAREFALLTHROUGH**</dt> <dt>2</dt> </dl> | Accettare il nome del file<br/>                                                                                            |
| <dl> <dt>**OFN \_ SHARENOWARN**</dt> <dt>1</dt> </dl>      | Rifiutare il nome del file ma non avvisare l'utente. L'applicazione è responsabile della visualizzazione di un messaggio di avviso.<br/> |
| <dl> <dt>**OFN \_ SHAREWARN**</dt> <dt>0</dt> </dl>        | Rifiutare il nome del file e visualizzare un messaggio di avviso (lo stesso risultato di una procedura hook).<br/>       |



 

## <a name="remarks"></a>Commenti

La routine hook deve specificare la **costante SHAREVISTRING** in una chiamata alla funzione [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) per ottenere l'identificatore per il messaggio inviato dalla finestra di dialogo.

La finestra di dialogo invia il messaggio registrato **SHAREVISTRING** solo se non è stato specificato il flag **OFN \_ SHAREAWARE** nel membro **Flags** della struttura [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) al momento della creazione della finestra di dialogo.

Se la routine hook restituisce un valore non definito, la finestra di dialogo risponde come se fosse stato restituito **OFN \_ SHAREWARN.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Commdlg.h (includere Windows.h)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **SHAREVISTRINGW** (Unicode) e **SHAREVISTRINGA** (ANSI)<br/>                                    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**CONDIVISIONE DELLA \_ RETE CDNVIOLATION**](cdn-shareviolation.md)
</dt> <dt>

[**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Libreria di finestre di dialogo comune](common-dialog-box-library.md)
</dt> </dl>

