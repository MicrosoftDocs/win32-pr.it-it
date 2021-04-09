---
title: Messaggio LVM_GETITEMPOSITION (COMmctrl. h)
description: Recupera la posizione di un elemento della visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro GetItemPosition di ListView.
ms.assetid: e5841089-c34e-498e-b94c-45c845bfc747
keywords:
- Controlli di Windows Message LVM_GETITEMPOSITION
topic_type:
- apiref
api_name:
- LVM_GETITEMPOSITION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f40b5899634e2f357068caa6ef96339be82f600b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874329"
---
# <a name="lvm_getitemposition-message"></a>\_Messaggio GETITEMPOSITION LVM

Recupera la posizione di un elemento della visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ GetItemPosition di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemposition) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice dell'elemento della visualizzazione elenco.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura di [**punti**](/previous-versions//dd162805(v=vs.85)) che riceve la posizione dell'angolo superiore sinistro dell'elemento, in coordinate della visualizzazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

