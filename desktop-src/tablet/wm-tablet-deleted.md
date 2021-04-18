---
description: Il \_ messaggio di eliminazione del Tablet WM \_ viene pubblicato quando un dispositivo tablet viene rimosso da Windows.
ms.assetid: af5be7f0-a213-49a1-800e-c922281522c8
title: Messaggio WM_TABLET_DELETED (Tpcshrd. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da8ade03d199f8ee7a258b9db2aeea039fd725e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306700"
---
# <a name="wm_tablet_deleted-message"></a>Messaggio di eliminazione del \_ Tablet WM \_

Il messaggio di **\_ \_ eliminazione del Tablet WM** viene pubblicato quando un dispositivo tablet viene rimosso da Windows.


```C++
#define WM_TABLET_DEFBASE   0x02C0
#define WM_TABLET_DELETED   (WM_TABLET_DEFBASE + 9)     
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice del dispositivo tablet da rimuovere.

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



 

 
