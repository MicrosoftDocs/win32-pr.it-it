---
title: TBN_WRAPHOTITEM codice di notifica (Commctrl.h)
description: Notifica a un'applicazione con due o più barre degli strumenti che l'elemento a caldo sta per cambiare. Questo codice di notifica viene inviato sotto forma di messaggio WM \_ NOTIFY.
ms.assetid: 169309ec-68dd-4cbb-8963-f842cf75b4fc
keywords:
- TBN_WRAPHOTITEM del codice di notifica Windows controlli
topic_type:
- apiref
api_name:
- TBN_WRAPHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33c6bd1f2e750a2fd71dc053d31ca452fa581891037db73d356e5405476b28de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119293363"
---
# <a name="tbn_wraphotitem-notification-code"></a>Codice di \_ notifica WRAPHOTITEM TBN

Notifica a un'applicazione con due o più barre degli strumenti che l'elemento a caldo sta per cambiare. Questo codice di notifica viene inviato sotto forma di [**messaggio WM \_ NOTIFY.**](wm-notify.md)


```C++
TBN_WRAPHOTITEM

    lpnmtb = (NMTBWRAPHOTITEM) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura che contiene l'elemento di accesso rapido precedente (**iStart**) e indica se il nuovo elemento a caldo si trova prima di esso (**iDir** = -1) o dopo di esso (**iDir** = 1), nonché un motivo per cui l'elemento a caldo viene modificato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**TRUE** se l'applicazione gestisce la modifica dell'elemento a caldo; in caso **contrario, FALSE.**

## <a name="remarks"></a>Commenti

La **struttura NMTBWRAPHOTITEM** deve essere definita dall'applicazione nel modo seguente:

``` syntax
typedef struct tagNMTBWRAPHOTITEM {
    NMHDR hdr;
    int iStart;
    int iDir;
    UINT nReason;       // HICF_* flags
} NMTBWRAPHOTITEM, *LPNMTBWRAPHOTITEM;
```

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





