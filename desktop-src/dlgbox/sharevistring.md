---
title: Messaggio SHAREVISTRING (COMMDLG. h)
description: Una finestra di dialogo Apri o Salva con nome Invia il messaggio SHAREVISTRING registrato alla routine hook, OFNHookProc, se si verifica una violazione di condivisione per il file selezionato quando l'utente fa clic sul pulsante OK.
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
ms.openlocfilehash: c23c17280ad1156e35f7e0f503816c07645cf4f6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477980"
---
# <a name="sharevistring-message"></a>Messaggio SHAREVISTRING

\[A partire da Windows Vista, le finestre di dialogo **Apri** e **Salva come** comuni sono state sostituite dalla [finestra di dialogo elemento comune](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)). È consigliabile usare l'API della finestra di dialogo elemento comune anziché queste finestre di dialogo dalla libreria di finestre di dialogo comuni.\]

Una finestra di dialogo **Apri** o **Salva con nome** invia il messaggio **SHAREVISTRING** registrato alla routine hook, [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc), se si verifica una violazione di condivisione per il file selezionato quando l'utente fa clic sul pulsante **OK** .


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

Puntatore a una struttura [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) . Il membro **lpstrFile** della struttura contiene il nome del file che ha causato la violazione di condivisione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La routine hook deve restituire uno dei valori seguenti per indicare la modalità di gestione della violazione di condivisione da parte della finestra di dialogo.



| Codice/valore restituito                                                                                                                                           | Descrizione                                                                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OFN \_ SHAREFALLTHROUGH**</dt> <dt>2</dt> </dl> | Accetta il nome del file<br/>                                                                                            |
| <dl> <dt>**OFN \_ SHARENOWARN**</dt> <dt>1</dt> </dl>      | Rifiutare il nome del file ma non avvisare l'utente. L'applicazione è responsabile della visualizzazione di un messaggio di avviso.<br/> |
| <dl> <dt>**OFN \_ SHAREWARN**</dt> <dt>0</dt> </dl>        | Rifiutare il nome del file e visualizzare un messaggio di avviso, ovvero lo stesso risultato di una procedura di hook.<br/>       |



 

## <a name="remarks"></a>Commenti

La routine hook deve specificare la costante **SHAREVISTRING** in una chiamata alla funzione [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) per ottenere l'identificatore del messaggio inviato dalla finestra di dialogo.

La finestra di dialogo Invia il messaggio **SHAREVISTRING** registrato solo se non è stato specificato il flag **OFN \_ SHAREAWARE** nel membro **Flags** della struttura [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) quando è stata creata la finestra di dialogo.

Se la routine hook restituisce un valore non definito, la finestra di dialogo risponde come se **OFN \_ SHAREWARN** fosse stato restituito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>COMMDLG. h (include Windows. h)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **SHAREVISTRINGW** (Unicode) e **SHAREVISTRINGA** (ANSI)<br/>                                    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**SHAREVIOLATION rete CDN \_**](cdn-shareviolation.md)
</dt> <dt>

[**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Libreria finestra di dialogo comune](common-dialog-box-library.md)
</dt> </dl>

 

