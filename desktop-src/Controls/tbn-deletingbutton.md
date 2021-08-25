---
title: TBN_DELETINGBUTTON messaggio (Commctrl.h)
description: Inviato da un controllo barra degli strumenti quando un pulsante sta per essere eliminato. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 08116071-36d6-456b-88f9-62a22cdb7ed9
keywords:
- TBN_DELETINGBUTTON di controllo Windows messaggio
topic_type:
- apiref
api_name:
- TBN_DELETINGBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a426d32af308d6d254a4221bbf35b103b401f07ab1ba6fa74801b6debd46ab70
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876971"
---
# <a name="tbn_deletingbutton-message"></a>Messaggio TBN \_ DELETINGBUTTON

Inviato da un controllo barra degli strumenti quando un pulsante sta per essere eliminato. Questo codice di notifica viene inviato sotto forma di messaggio [**WM \_ NOTIFY.**](wm-notify.md)


```C++
 TBN_DELETINGBUTTON 

    lpnmtb = (LPNMTOOLBAR) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) che contiene informazioni sul pulsante da eliminare. Per questo codice di notifica, sono validi solo i membri **hdr** e **iItem** di questa struttura. Il **membro iItem** di questa struttura contiene l'identificatore di comando del pulsante da eliminare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito viene ignorato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





