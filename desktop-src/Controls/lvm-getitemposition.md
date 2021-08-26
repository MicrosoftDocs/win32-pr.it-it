---
title: LVM_GETITEMPOSITION messaggio (Commctrl.h)
description: Recupera la posizione di un elemento della visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o tramite la \_ macro ListView GetItemPosition.
ms.assetid: e5841089-c34e-498e-b94c-45c845bfc747
keywords:
- LVM_GETITEMPOSITION di controllo Windows messaggio
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
ms.openlocfilehash: 92d4f4a55f88b6af9828420871de80117ae492bf53c8a62883e43f928c4f5c70
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002621"
---
# <a name="lvm_getitemposition-message"></a>Messaggio LVM \_ GETITEMPOSITION

Recupera la posizione di un elemento della visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**\_ ListView GetItemPosition.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemposition)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice dell'elemento della visualizzazione elenco.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura POINT**](/previous-versions//dd162805(v=vs.85)) che riceve la posizione dell'angolo superiore sinistro dell'elemento, nelle coordinate di visualizzazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo oppure FALSE **in** caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

