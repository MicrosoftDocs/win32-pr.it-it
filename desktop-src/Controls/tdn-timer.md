---
title: TDN_TIMER codice di notifica (Commctrl.h)
description: Inviato da una finestra di dialogo attività circa ogni 200 millisecondi.
ms.assetid: 5a162d97-6912-45bc-8151-1ea56cc459ea
keywords:
- TDN_TIMER codice di notifica Windows controlli
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
ms.openlocfilehash: eaf3f5d72ef8267c6600decf070875b2dd109114f910d09a5ca343f8fde44005
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104451"
---
# <a name="tdn_timer-notification-code"></a>Codice di notifica \_ TDN TIMER

Inviato da una finestra di dialogo attività circa ogni 200 millisecondi. Questo codice di notifica viene inviato quando il flag TIMER CALLBACK TDF è stato impostato nel membro \_ \_ **dwFlags** della struttura [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) passato alla [**funzione TaskDialogIndirect.**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) Questo codice di notifica viene ricevuto solo tramite la funzione di callback del dialogo attività, che può essere registrata usando il **metodo TaskDialogIndirect.**


```C++
TDN_TIMER    

   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Valore **DWORD che** specifica il numero di millisecondi trascorsi dalla creazione della finestra di dialogo o il codice di notifica ha restituito **S \_ FALSE.**

</dd> <dt>

*lParam* 
</dt> <dd>

Deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per reimpostare il tickcount, l'applicazione deve restituire **S \_ FALSE,** in caso contrario il tickcount continuerà a incrementare.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





