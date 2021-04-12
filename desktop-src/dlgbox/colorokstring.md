---
title: Messaggio COLOROKSTRING (COMMDLG. h)
description: Una finestra di dialogo colore invia il messaggio registrato COLOROKSTRING alla routine hook, CCHookProc, quando l'utente seleziona un colore e fa clic sul pulsante OK.
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
ms.openlocfilehash: 86229c71f1234efb4b561ac73bc8aa20f6258cdc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119750"
---
# <a name="colorokstring-message"></a>Messaggio COLOROKSTRING

Una finestra di dialogo **colore** invia il messaggio registrato **COLOROKSTRING** alla routine hook, [*CCHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcchookproc), quando l'utente seleziona un colore e fa clic sul pulsante **OK** . La routine hook può accettare il colore e consentire la chiusura della finestra di dialogo oppure rifiutare il colore e forzare la finestra di dialogo in modo che rimanga aperta.


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

Puntatore a una struttura [**le CHOOSECOLOR.**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) . Il membro **rgbResult** della struttura contiene il valore di colore RGB del colore selezionato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la routine hook restituisce zero, la finestra di dialogo **colore** accetta il colore selezionato e si chiude.

Se la routine hook restituisce un valore diverso da zero, la finestra di dialogo **colore** rifiuta il colore selezionato e rimane aperto.

## <a name="remarks"></a>Commenti

La routine hook deve specificare la costante **COLOROKSTRING** in una chiamata alla funzione [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) per ottenere l'identificatore del messaggio inviato dalla finestra di dialogo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>COMMDLG. h (include Windows. h)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **COLOROKSTRINGW** (Unicode) e **COLOROKSTRINGA** (ANSI)<br/>                                    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**LE CHOOSECOLOR.**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1)
</dt> <dt>

[**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Libreria finestra di dialogo comune](common-dialog-box-library.md)
</dt> </dl>

 

