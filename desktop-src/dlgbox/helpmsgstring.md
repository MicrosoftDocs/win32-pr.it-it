---
title: Messaggio HELPMSGSTRING (COMMDLG. h)
description: Una finestra di dialogo comune invia il messaggio registrato HELPMSGSTRING alla routine della finestra proprietaria quando l'utente fa clic sul pulsante?.
ms.assetid: 21c0fcf5-785b-4005-8133-e48347f991a8
keywords:
- Finestre di dialogo del messaggio HELPMSGSTRING
topic_type:
- apiref
api_name:
- HELPMSGSTRING
- HELPMSGSTRINGA
- HELPMSGSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac3f7a883f50b06c8d142cb83bedf0bfa2920191
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121326"
---
# <a name="helpmsgstring-message"></a>Messaggio HELPMSGSTRING

Una finestra di dialogo comune invia il messaggio registrato **HELPMSGSTRING** alla routine della finestra proprietaria quando l'utente fa clic sul **pulsante?** .


```C++
#define HELPMSGSTRING TEXT("commdlg_help")
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per la finestra di dialogo comune.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore alla struttura di inizializzazione per la finestra di dialogo comune. Questa struttura può essere una struttura [**le CHOOSECOLOR.**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1), [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta), [**FindReplace**](/windows/win32/api/commdlg/ns-commdlg-findreplacea), [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea), [**PrintDlg**](/windows/win32/api/commdlg/ns-commdlg-printdlga) o [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce alcun valore.

## <a name="remarks"></a>Commenti

È necessario specificare la costante **HELPMSGSTRING** in una chiamata alla funzione [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) per ottenere l'identificatore del messaggio inviato dalla finestra di dialogo.

Quando si crea la finestra di dialogo, utilizzare il membro **hwndOwner** della struttura di inizializzazione per identificare la finestra per la ricezione di messaggi **HELPMSGSTRING** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>COMMDLG. h (include Windows. h)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **HELPMSGSTRINGW** (Unicode) e **HELPMSGSTRINGA** (ANSI)<br/>                                    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**Guida della rete CDN \_**](cdn-help.md)
</dt> <dt>

[**LE CHOOSECOLOR.**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1)
</dt> <dt>

[**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea)
</dt> <dt>

[**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga)
</dt> <dt>

[**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga)
</dt> <dt>

[**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Libreria finestra di dialogo comune](common-dialog-box-library.md)
</dt> </dl>

 

