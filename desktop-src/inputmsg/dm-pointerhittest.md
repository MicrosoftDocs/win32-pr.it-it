---
title: DM_POINTERHITTEST messaggio
description: Inviato a una finestra, quando viene rilevato l'input del puntatore per la prima volta, per determinare la destinazione di input più probabile per la manipolazione diretta.
ms.assetid: E4CE60F0-0C2A-440A-8F64-B070867A1572
keywords:
- DM_POINTERHITTEST messaggi di input e notifiche
topic_type:
- apiref
api_name:
- DM_POINTERHITTEST
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 9fda57a0c7084ae0c6ab85514244ed531a182108ec5dce7aae7794de2c38c903
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118482472"
---
# <a name="dm_pointerhittest-message"></a>DM_POINTERHITTEST messaggio

\[Alcune informazioni riguardano prodotti pre-rilasciati che possono essere modificati in modo sostanziale prima che venga rilasciato commercialmente. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Inviato a una finestra, quando viene rilevato l'input del puntatore per la prima volta, per determinare la destinazione di input più probabile per [la manipolazione diretta.](/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal)

> \[! Importante\]  
> Le app desktop devono essere in grado di riconoscere DPI. Se l'app non è in grado di riconoscere DPI, le coordinate dello schermo contenute nei messaggi del puntatore e nelle strutture correlate potrebbero apparire inesatte a causa della virtualizzazione DPI. La virtualizzazione DPI offre il supporto automatico del ridimensionamento per le applicazioni che non supportano DPI ed è attiva per impostazione predefinita (gli utenti possono disattivarla). Per altre informazioni, vedere [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).

 


```C++
#define DM_POINTERHITTEST       0x0250
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilizzato.

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilizzato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

NULL

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | \[Windows Server 2016 solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Messaggi](messages.md)
</dt> </dl>

 

