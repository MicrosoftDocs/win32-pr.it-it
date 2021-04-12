---
title: Messaggio LVM_GETWORKAREAS (COMmctrl. h)
description: Recupera le aree di lavoro da un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro GetWorkAreas di ListView.
ms.assetid: 956368d9-bbb4-414a-ba17-0e8e4f0f1a45
keywords:
- Controlli di Windows Message LVM_GETWORKAREAS
topic_type:
- apiref
api_name:
- LVM_GETWORKAREAS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a64546a17489eaf88a4d15430c6be26017a8d33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478503"
---
# <a name="lvm_getworkareas-message"></a>\_Messaggio GETWORKAREAS LVM

Recupera le aree di lavoro da un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ GetWorkAreas di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getworkareas) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Numero di strutture [**Rect**](/previous-versions//dd162897(v=vs.85)) nella matrice in *lParam*.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una matrice di strutture [**Rect**](/previous-versions//dd162897(v=vs.85)) che ricevono le aree di lavoro correnti del controllo visualizzazione elenco. I valori in queste strutture si trovano nelle coordinate del client. *wParam* specifica il numero di strutture in questa matrice.

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

 

