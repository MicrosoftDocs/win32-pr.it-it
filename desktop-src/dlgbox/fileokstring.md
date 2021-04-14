---
title: Messaggio FILEOKSTRING (COMMDLG. h)
description: Una finestra di dialogo Apri o Salva con nome Invia il messaggio registrato FILEOKSTRING alla routine hook, OFNHookProc, quando l'utente specifica un nome file e fa clic sul pulsante OK.
ms.assetid: 32bf3cc7-76a2-4b78-81d7-682b088c4e14
keywords:
- Finestre di dialogo del messaggio FILEOKSTRING
topic_type:
- apiref
api_name:
- FILEOKSTRING
- FILEOKSTRINGA
- FILEOKSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61208ddebc63f1186c2947416e451231f0bea24e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478982"
---
# <a name="fileokstring-message"></a>Messaggio FILEOKSTRING

\[A partire da Windows Vista, le finestre di dialogo **Apri** e **Salva come** comuni sono state sostituite dalla [finestra di dialogo elemento comune](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)). È consigliabile usare l'API della finestra di dialogo elemento comune anziché queste finestre di dialogo dalla libreria di finestre di dialogo comuni.\]

Una finestra di dialogo **Apri** o **Salva con** nome Invia il messaggio registrato **FILEOKSTRING** alla routine hook, [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc), quando l'utente specifica un nome file e fa clic sul pulsante **OK** . La procedura di hook può accettare il nome del file e consentire la chiusura della finestra di dialogo oppure rifiutare il nome del file e forzare la finestra di dialogo in modo che rimanga aperta.


```C++
#define FILEOKSTRING TEXT("commdlg_FileNameOK")
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) . Il membro **lpstrFile** della struttura contiene l'unità, il percorso e il nome file specificati dall'utente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la routine hook restituisce zero, la finestra di dialogo **Apri** o **Salva con** nome accetta il nome file specificato e si chiude.

Se la routine hook restituisce un valore diverso da zero, la finestra di dialogo **Apri** o **Salva con** nome rifiuta il nome file specificato e rimane aperto.

## <a name="remarks"></a>Commenti

La routine hook deve specificare la costante **FILEOKSTRING** in una chiamata alla funzione [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) per ottenere l'identificatore del messaggio inviato dalla finestra di dialogo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>COMMDLG. h (include Windows. h)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **FILEOKSTRINGW** (Unicode) e **FILEOKSTRINGA** (ANSI)<br/>                                      |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**FILEOK rete CDN \_**](cdn-fileok.md)
</dt> <dt>

[**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Libreria finestra di dialogo comune](common-dialog-box-library.md)
</dt> </dl>

 

