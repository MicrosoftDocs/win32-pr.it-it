---
title: Messaggio LVM_SETWORKAREAS (COMmctrl. h)
description: Imposta le aree di lavoro all'interno di un controllo di visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro SetWorkAreas di ListView.
ms.assetid: 87ac192d-f481-43ac-b8a5-c754cf33e487
keywords:
- Controlli di Windows Message LVM_SETWORKAREAS
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
ms.openlocfilehash: 4166238c97b5766a5f2bbb19e0de853526d83385
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964731"
---
# <a name="lvm_setworkareas-message"></a>\_Messaggio SETWORKAREAS LVM

Imposta le aree di lavoro all'interno di un controllo di visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ SetWorkAreas di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setworkareas) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Numero di strutture nella matrice in corrispondenza di *LPRC*. Il numero massimo di aree di lavoro consentito è definito dal \_ valore LV Max \_ WORKAREAS.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una matrice di strutture [**Rect**](/previous-versions//dd162897(v=vs.85)) che contengono le nuove aree di lavoro del controllo visualizzazione elenco. I valori in queste strutture si trovano nelle coordinate del client. Se questo parametro è **null**, l'area di lavoro verrà impostata sull'area client del controllo. *wParam* specifica il numero di strutture in questa matrice.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito per questo messaggio non viene utilizzato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Uso di controlli List-View](using-list-view-controls.md)
</dt> </dl>

 

