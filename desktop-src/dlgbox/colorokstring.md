---
title: Messaggio COLOROKSTRING (Commdlg.h)
description: Una finestra di dialogo Colore invia il messaggio registrato COLOROKSTRING alla routine hook CCHookProc quando l'utente seleziona un colore e fa clic sul pulsante OK.
ms.assetid: 18b28558-1262-4c88-becf-76ce799b7542
keywords:
- Finestre di dialogo del messaggio COLOROKSTRING
topic_type:
- apiref
api_name:
- COLOROKSTRING
- COLOROKSTRINGA
- COLOROKSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd55db4bb935880438290a83cd99c420ebcabf23ca8cb1bb238ea15f39e06247
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726281"
---
# <a name="colorokstring-message"></a>Messaggio DI COLOROKSTRING

Una **finestra di** dialogo Colore invia il messaggio registrato **COLOROKSTRING** alla routine hook [*CCHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcchookproc)quando l'utente seleziona un colore e fa clic sul **pulsante OK.** La procedura hook può accettare il colore e consentire la chiusura della finestra di dialogo oppure rifiutare il colore e forzare la finestra di dialogo a rimanere aperta.


```C++
#define COLOROKSTRING TEXT("commdlg_ColorOK")
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura CHOOSECOLOR.**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) Il **membro rgbResult** di questa struttura contiene il valore del colore RGB del colore selezionato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la routine hook restituisce zero, la **finestra di** dialogo Colore accetta il colore selezionato e si chiude.

Se la routine hook restituisce un valore diverso da zero, la finestra di dialogo **Colore** rifiuta il colore selezionato e rimane aperta.

## <a name="remarks"></a>Commenti

La routine hook deve specificare la costante **COLOROKSTRING** in una chiamata alla funzione [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) per ottenere l'identificatore del messaggio inviato dalla finestra di dialogo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Commdlg.h (includere Windows.h)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **COLOROKSTRINGW** (Unicode) e **COLOROKSTRINGA** (ANSI)<br/>                                    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1)
</dt> <dt>

[**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Libreria di finestre di dialogo comuni](common-dialog-box-library.md)
</dt> </dl>

 

