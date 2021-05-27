---
title: Messaggio FILEOKSTRING (Commdlg.h)
description: Una finestra di dialogo Apri o Salva con nome invia il messaggio registrato fileOKSTRING alla procedura hook OFNHookProc, quando l'utente specifica un nome di file e fa clic sul pulsante OK.
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
ms.openlocfilehash: 24dd07faecc66bc50c408eab36bcbd8c93c460ef
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549216"
---
# <a name="fileokstring-message"></a>Messaggio FILEOKSTRING

\[A partire da Windows Vista, le **finestre di** **dialogo** comuni Apri e Salva con nome sono state sostituite dalla finestra di dialogo [Elemento comune](../shell/common-file-dialog.md). È consigliabile usare l'API Common Item Dialog al posto di queste finestre di dialogo di Common Dialog Box Library.\]

Una finestra  **di** dialogo Apri o Salva con nome invia il messaggio registrato **fileOKSTRING** alla procedura hook [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)quando l'utente specifica un nome di file e fa clic sul **pulsante OK.** La procedura hook può accettare il nome del file e consentire la chiusura della finestra di dialogo oppure rifiutare il nome del file e forzare la finestra di dialogo a rimanere aperta.


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

Puntatore a una [**struttura OPENFILENAME.**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) Il **membro lpstrFile** di questa struttura contiene l'unità, il percorso e il nome file specificati dall'utente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la routine hook restituisce zero, la **finestra di** dialogo Apri o **Salva** con nome accetta il nome file specificato e viene chiusa.

Se la routine hook restituisce un  valore  diverso da zero, la finestra di dialogo Apri o Salva con nome rifiuta il nome file specificato e rimane aperta.

## <a name="remarks"></a>Commenti

La routine hook deve specificare la **costante FILEOKSTRING** in una chiamata alla funzione [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) per ottenere l'identificatore per il messaggio inviato dalla finestra di dialogo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Commdlg.h (includere Windows.h)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **FILEOKSTRINGW** (Unicode) e **FILEOKSTRINGA** (ANSI)<br/>                                      |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**FILEOK della rete CDN \_**](cdn-fileok.md)
</dt> <dt>

[**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Libreria di finestre di dialogo comune](common-dialog-box-library.md)
</dt> </dl>

