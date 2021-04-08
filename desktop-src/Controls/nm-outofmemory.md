---
title: Codice di notifica NM_OUTOFMEMORY (COMmctrl. h)
description: Notifica alla finestra padre di un controllo che il controllo non è stato in grado di completare un'operazione perché la memoria disponibile non è sufficiente. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: d7d80515-ae6c-4817-a698-d486a9d86c4a
keywords:
- Controlli di Windows per il codice di notifica NM_OUTOFMEMORY
topic_type:
- apiref
api_name:
- NM_OUTOFMEMORY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f1321f88360d168b13d16b36f984d9b797dc094
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047924"
---
# <a name="nm_outofmemory-notification-code"></a>\_Codice di notifica OutOfMemory Nm

Notifica alla finestra padre di un controllo che il controllo non è stato in grado di completare un'operazione perché la memoria disponibile non è sufficiente. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
NM_OUTOFMEMORY

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) che contiene informazioni aggiuntive su questa notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito viene ignorato dal controllo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





