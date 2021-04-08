---
description: Inviato a tutte le finestre dopo che l'utente ha effettuato l'accesso o la disconnessione. Quando l'utente effettua l'accesso o la disattivazione, il sistema aggiorna le impostazioni specifiche dell'utente. Il sistema invia questo messaggio immediatamente dopo l'aggiornamento delle impostazioni.
title: Messaggio WM_USERCHANGED (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowmessages\wm_userchanged.htm
api_name:
- WM_USERCHANGED
api_type:
- HeaderDef
api_location:
- Winuser.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 14458bdafa0bbf4421c67db8102491db4e1fe6b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968408"
---
# <a name="wm_userchanged-message"></a>\_Messaggio USERCHANGED WM

Inviato a tutte le finestre dopo che l'utente ha effettuato l'accesso o la disconnessione. Quando l'utente effettua l'accesso o la disattivazione, il sistema aggiorna le impostazioni specifiche dell'utente. Il sistema invia questo messaggio immediatamente dopo l'aggiornamento delle impostazioni.

Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .

> [!Note]  
> Questo messaggio non è supportato in Windows Vista.

 


```C++
#define WM_USERCHANGED                  0x0054
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **LRESULT**

Un'applicazione deve restituire zero se elabora questo messaggio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                                              |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica di Windows](windows.md)
</dt> </dl>

 

 
