---
title: LVM_SETWORKAREAS messaggio (Commctrl.h)
description: Imposta le aree di lavoro all'interno di un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro ListView SetWorkAreas.
ms.assetid: 87ac192d-f481-43ac-b8a5-c754cf33e487
keywords:
- LVM_SETWORKAREAS del messaggio Windows controlli
topic_type:
- apiref
api_name:
- LVM_SETWORKAREAS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f1060377fd9aec9014d18d206444355b052f4aafb796403e3e47fa92a0a7aaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117830662"
---
# <a name="lvm_setworkareas-message"></a>Messaggio \_ LVM SETWORKAREAS

Imposta le aree di lavoro all'interno di un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ ListView SetWorkAreas.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setworkareas)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Numero di strutture nella matrice in *corrispondenza di lprc*. Il numero massimo di aree di lavoro consentite è definito dal valore LV \_ MAX \_ WORKAREAS.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una matrice [**di strutture RECT**](/previous-versions//dd162897(v=vs.85)) che contengono le nuove aree di lavoro del controllo visualizzazione elenco. I valori in queste strutture sono in coordinate client. Se questo parametro è **NULL,** l'area di lavoro verrà impostata sull'area client del controllo. *wParam* specifica il numero di strutture in questa matrice.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito per questo messaggio non viene utilizzato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Uso di List-View personalizzati](using-list-view-controls.md)
</dt> </dl>

 

