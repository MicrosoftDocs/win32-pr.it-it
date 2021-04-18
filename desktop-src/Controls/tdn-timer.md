---
title: Codice di notifica TDN_TIMER (COMmctrl. h)
description: Inviato da una finestra di dialogo attività approssimativamente ogni 200 millisecondi.
ms.assetid: 5a162d97-6912-45bc-8151-1ea56cc459ea
keywords:
- Controlli di Windows per il codice di notifica TDN_TIMER
topic_type:
- apiref
api_name:
- TDN_TIMER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2eea7a1604c70c187299c9f2c99abbe934926317
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302636"
---
# <a name="tdn_timer-notification-code"></a>\_Codice di notifica del timer TDN

Inviato da una finestra di dialogo attività approssimativamente ogni 200 millisecondi. Questo codice di notifica viene inviato quando il \_ \_ flag del timer di callback TDF è stato impostato nel membro **DwFlags** della struttura [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) che è stato passato alla funzione [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) . Questo codice di notifica viene ricevuto solo tramite la funzione di callback della finestra di dialogo attività, che può essere registrata tramite il metodo **TaskDialogIndirect** .


```C++
TDN_TIMER    

   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

**DWORD** che specifica il numero di millisecondi trascorsi dal momento della creazione della finestra di dialogo oppure il codice di notifica ha restituito **\_ false**.

</dd> <dt>

*lParam* 
</dt> <dd>

Deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per reimpostare il TickCount, l'applicazione deve restituire **S \_ false**, in caso contrario il TickCount continuerà ad aumentare.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





