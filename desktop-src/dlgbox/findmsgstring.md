---
title: Messaggio FINDMSGSTRING (COMMDLG. h)
description: Una finestra di dialogo Trova o Sostituisci invia il messaggio registrato FINDMSGSTRING alla procedura della finestra proprietaria quando l'utente fa clic sul pulsante Trova successivo, Sostituisci o Sostituisci tutto oppure chiude la finestra di dialogo.
ms.assetid: ed0b256a-96df-4588-b8f3-f7d1f89ffe74
keywords:
- Finestre di dialogo del messaggio FINDMSGSTRING
topic_type:
- apiref
api_name:
- FINDMSGSTRING
- FINDMSGSTRINGA
- FINDMSGSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe0d3a73d8734d79d5ed0862f66bf9ba5c030e46
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518874"
---
# <a name="findmsgstring-message"></a>Messaggio FINDMSGSTRING

Una finestra di dialogo **trova** o **Sostituisci** invia il messaggio registrato **FINDMSGSTRING** alla procedura della finestra proprietaria quando l'utente fa clic sul pulsante **Trova successivo**, **Sostituisci** o **Sostituisci tutto** oppure chiude la finestra di dialogo.


```C++
#define FINDMSGSTRING TEXT("commdlg_FindReplace")
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**FindReplace**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) . I membri di questa struttura contengono l'input dell'utente più recente, inclusa la stringa da cercare, la stringa di sostituzione (se presente) e le opzioni di ricerca e sostituzione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce alcun valore.

## <a name="remarks"></a>Commenti

È necessario specificare la costante **FINDMSGSTRING** in una chiamata alla funzione [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) per ottenere l'identificatore del messaggio inviato dalla finestra di dialogo.

Quando si crea la finestra di dialogo, utilizzare il membro **hwndOwner** della struttura [**FindReplace**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) per identificare la finestra per la ricezione di messaggi **FINDMSGSTRING** .

Il membro **Flags** della struttura [**FindReplace**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) include uno dei flag seguenti per indicare l'evento che ha causato il messaggio.



| Contrassegno                            | Significato                                                                                                                                                                                                     |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Fr \_ DIALOGTERM** (0x00000040) | La finestra di dialogo sta per essere chiusa. Quando la finestra proprietaria elabora questo messaggio, un handle per la finestra di dialogo non è più valido.                                                                                    |
| **Fr \_ TROVASUCCESSIVO** (0x00000008)   | L'utente ha fatto clic sul pulsante **Trova successivo** in una finestra di dialogo **trova** o **Sostituisci** . Il membro **lpstrFindWhat** specifica la stringa da cercare.                                                         |
| **Fr \_ SOSTITUISCi** (0x00000010)    | L'utente ha fatto clic sul pulsante **Sostituisci** in una finestra di dialogo **Sostituisci** . Il membro **lpstrFindWhat** specifica la stringa da sostituire e il membro **lpstrReplaceWith** specifica la stringa di sostituzione.     |
| **Fr \_ REPLACEALL** (0x00000020) | L'utente ha fatto clic sul pulsante **Sostituisci tutto** in una finestra di dialogo **Sostituisci** . Il membro **lpstrFindWhat** specifica la stringa da sostituire e il membro **lpstrReplaceWith** specifica la stringa di sostituzione. |



 

Per un messaggio **Trova successivo** o **Sostituisci tutto** , il membro **Flags** può includere uno o più dei flag seguenti per indicare le opzioni di ricerca.



| Contrassegno                           | Significato                                                                                                                                                                                                                                                                                         |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Fr \_ GIÙ** (0x00000001)      | Se impostato, viene selezionato il pulsante **giù** dei pulsanti di opzione direzione che indica che l'utente desidera eseguire la ricerca dalla posizione corrente fino alla fine del documento. Se **fr \_ Down** non è impostato, viene selezionato il pulsante **su** in modo che l'utente desideri eseguire la ricerca all'inizio del documento.       |
| **Fr \_ MATCHCASE** (0x00000004) | Se impostato, viene selezionata la casella di controllo **maiuscole/minuscole** che indica che l'utente desidera che la ricerca venga fatta distinzione tra maiuscole e minuscole. Se **fr \_ MATCHCASE** non è impostato, la casella di controllo è deselezionata, quindi la ricerca deve essere senza distinzione tra maiuscole e minuscole.                                                                         |
| **Fr \_ WHOLEWORD** (0x00000002) | Se impostata, la casella di controllo trova **solo parola intera** è selezionata indicando che l'utente desidera eseguire la ricerca solo di parole intere che corrispondono alla stringa di ricerca. Se **fr \_ WHOLEWORD** non è impostato, la casella di controllo è deselezionata, quindi è necessario cercare anche frammenti di parola che corrispondono alla stringa di ricerca. |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>COMMDLG. h (include Windows. h)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **FINDMSGSTRINGW** (Unicode) e **FINDMSGSTRINGA** (ANSI)<br/>                                    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea)
</dt> <dt>

[**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Libreria finestra di dialogo comune](common-dialog-box-library.md)
</dt> </dl>

 

