---
title: HDN_ENDDRAG codice di notifica (Commctrl.h)
description: Inviato da un controllo intestazione al termine di un'operazione di trascinamento su uno dei relativi elementi. Questo codice di notifica viene inviato come messaggio WM \_ NOTIFY. Solo i controlli intestazione impostati sullo stile DRAGDROP HDS \_ inviano questo codice di notifica.
ms.assetid: a28df985-73f1-4fc7-a1db-81a86a131c06
keywords:
- HDN_ENDDRAG codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- HDN_ENDDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05df56beb0b5b4a75716723330711714b7db9f4f27100ffe3296626d2be5798a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544620"
---
# <a name="hdn_enddrag-notification-code"></a>Codice di \_ notifica ENDDRAG HDN

Inviato da un controllo intestazione al termine di un'operazione di trascinamento su uno dei relativi elementi. Questo codice di notifica viene inviato come [**messaggio WM \_ NOTIFY.**](wm-notify.md) Solo i controlli intestazione impostati sullo stile [**\_ DRAGDROP HDS**](header-control-styles.md) inviano questo codice di notifica.


```C++
HDN_ENDDRAG

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) contenente informazioni sull'elemento di intestazione trascinato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per consentire al controllo di posizionare e riordinare automaticamente l'elemento, restituire **FALSE.** Per impedire che l'elemento venga inserito, restituire **TRUE.**

## <a name="remarks"></a>Commenti

Se il proprietario esegue la gestione del trascinamento della selezione esterna (manuale), deve restituire **FALSE.** Il proprietario deve quindi riordinare manualmente gli elementi di intestazione inviando [**HDM \_ SETITEM**](hdm-setitem.md) [**o HDM \_ SETORDERARRAY**](hdm-setorderarray.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





