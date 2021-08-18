---
title: Messaggio HELPMSGSTRING (Commdlg.h)
description: Una finestra di dialogo comune invia il messaggio registrato HELPMSGSTRING alla procedura della finestra della finestra proprietaria quando l'utente fa clic sul pulsante ? .
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
ms.openlocfilehash: ec8a446164bb7ae51d36d1a89219f6c3b84eff74b9af3a40c2121b3bd205a581
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119741741"
---
# <a name="helpmsgstring-message"></a>Messaggio HELPMSGSTRING

Una finestra di dialogo comune invia il **messaggio registrato HELPMSGSTRING** alla procedura della finestra della finestra proprietaria quando l'utente fa clic sul **pulsante ?** .


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

Puntatore alla struttura di inizializzazione per la finestra di dialogo comune. Questa struttura può essere [**chooseCOLOR,**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) [**CHOOSEFONT,**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) [**FINDREPLACE,**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) [**OPENFILENAME,**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) [**o PAGESETUPDLG.**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non ha alcun valore restituito.

## <a name="remarks"></a>Commenti

È necessario specificare la **costante HELPMSGSTRING** in una chiamata alla funzione [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) per ottenere l'identificatore per il messaggio inviato dalla finestra di dialogo.

Quando si crea la finestra di dialogo, usare il **membro hwndOwner** della struttura di inizializzazione per identificare la finestra per ricevere **messaggi HELPMSGSTRING.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Commdlg.h (includere Windows.h)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **HELPMSGSTRINGW** (Unicode) e **HELPMSGSTRINGA** (ANSI)<br/>                                    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**\_rete CDN Guida**](cdn-help.md)
</dt> <dt>

[**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1)
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

[Libreria di finestre di dialogo comuni](common-dialog-box-library.md)
</dt> </dl>

 

