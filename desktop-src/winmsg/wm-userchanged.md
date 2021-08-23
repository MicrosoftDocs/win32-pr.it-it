---
description: Inviato a tutte le finestre dopo che l'utente ha eseguito l'accesso o la disconnessione. Quando l'utente accede o si disconnette, il sistema aggiorna le impostazioni specifiche dell'utente. Il sistema invia questo messaggio immediatamente dopo l'aggiornamento delle impostazioni.
title: WM_USERCHANGED messaggio (Winuser.h)
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
ms.openlocfilehash: 2bb466e80070fe1be5cd7af7889fc5727c81f8caad89ad60c48c7a105b688fb4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119705701"
---
# <a name="wm_userchanged-message"></a>Messaggio WM \_ USERCHANGED

Inviato a tutte le finestre dopo che l'utente ha eseguito l'accesso o la disconnessione. Quando l'utente accede o si disconnette, il sistema aggiorna le impostazioni specifiche dell'utente. Il sistema invia questo messaggio immediatamente dopo l'aggiornamento delle impostazioni.

Una finestra riceve questo messaggio tramite la relativa [**funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))

> [!Note]  
> Questo messaggio non è supportato a Windows Vista.

 


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
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                                              |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Windows Panoramica](windows.md)
</dt> </dl>

 

 
