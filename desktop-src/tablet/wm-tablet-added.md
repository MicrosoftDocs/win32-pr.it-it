---
description: Il \_ \_ messaggio di aggiunta del Tablet WM viene pubblicato quando un dispositivo tablet viene aggiunto a Windows.
ms.assetid: 74323b34-2364-47eb-b8ac-b97546e43b32
title: Messaggio WM_TABLET_ADDED (Tpcshrd. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a721f83cbab3c520a5502fa2f1262de9a26b25a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306701"
---
# <a name="wm_tablet_added-message"></a>\_Messaggio di \_ aggiunta Tablet WM

Il messaggio di **\_ \_ aggiunta del Tablet WM** viene pubblicato quando un dispositivo tablet viene aggiunto a Windows.


```C++
#define WM_TABLET_DEFBASE  0x02C0
#define WM_TABLET_ADDED    (WM_TABLET_DEFBASE + 8)      
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice di un dispositivo Tablet aggiunto

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilizzato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questo messaggio viene inviato a tutte le finestre di primo livello del sistema, incluse le finestre senza proprietà disabilitate o invisibili, le finestre sovrapposte e le finestre popup; ma il messaggio non viene inviato alle finestre figlio.

Gli indici passati in *wParam* sono correlati all'indice usato dal metodo [**ITabletManager:: gettablet**](/previous-versions/windows/desktop/legacy/aa373683(v=vs.85)) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                        |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                            |
| Intestazione<br/>                   | <dl> <dt>Tpcshrd. h</dt> </dl> |



 

 
