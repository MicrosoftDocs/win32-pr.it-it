---
title: Codice di notifica TBN_WRAPHOTITEM (COMmctrl. h)
description: Notifica a un'applicazione due o più barre degli strumenti che l'elemento critico sta per cambiare. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 169309ec-68dd-4cbb-8963-f842cf75b4fc
keywords:
- Controlli di Windows per il codice di notifica TBN_WRAPHOTITEM
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
ms.openlocfilehash: 58eb513780da464ead40f8a4fb1264f6268d4370
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476300"
---
# <a name="tbn_wraphotitem-notification-code"></a>\_Codice di notifica WRAPHOTITEM di TBN

Notifica a un'applicazione due o più barre degli strumenti che l'elemento critico sta per cambiare. Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .


```C++
TBN_WRAPHOTITEM

    lpnmtb = (NMTBWRAPHOTITEM) lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura che contiene il vecchio elemento attivo (**Tart**) e se il nuovo elemento attivo è precedente (**Idir** =-1) o dopo di esso (**Idir** = 1), nonché un motivo per cui l'elemento critico sta cambiando.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**True** se l'applicazione sta gestendo la modifica dell'elemento critico; in caso contrario, **false**.

## <a name="remarks"></a>Commenti

La struttura **NMTBWRAPHOTITEM** deve essere definita dall'applicazione come segue:

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
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





