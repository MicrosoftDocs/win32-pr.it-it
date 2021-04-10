---
title: Messaggio LVM_GETNUMBEROFWORKAREAS (COMmctrl. h)
description: Recupera il numero di aree di lavoro in un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro GetNumberOfWorkAreas di ListView.
ms.assetid: ce0bcccd-62a2-45a4-959e-9959c9ca0c46
keywords:
- Controlli di Windows Message LVM_GETNUMBEROFWORKAREAS
topic_type:
- apiref
api_name:
- LVM_GETNUMBEROFWORKAREAS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a73c62b7184ba60b979356a98a93d2579c8f74a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964739"
---
# <a name="lvm_getnumberofworkareas-message"></a>\_Messaggio GETNUMBEROFWORKAREAS LVM

Recupera il numero di aree di lavoro in un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ GetNumberOfWorkAreas di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getnumberofworkareas) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a un valore UINT che riceve il numero di aree di lavoro nel controllo di visualizzazione elenco. Se viene inserito zero in questa variabile, non sono attualmente impostate aree di lavoro. Questo valore non può essere **null**.

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

 

 





