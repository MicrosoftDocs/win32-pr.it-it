---
title: LVM_GETORIGIN messaggio (Commctrl.h)
description: Recupera l'origine della visualizzazione corrente per un controllo di visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro ListView GetOrigin.
ms.assetid: 913c8339-fbe4-43c8-a997-5a972920dc3b
keywords:
- LVM_GETORIGIN dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- LVM_GETORIGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a274e81c276d70eb1ab6c7f214b62ae5c346a59dda026bb13c5ab6b3ce80f68d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118411358"
---
# <a name="lvm_getorigin-message"></a>Messaggio \_ LVM GETORIGIN

Recupera l'origine della visualizzazione corrente per un controllo di visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ ListView GetOrigin.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getorigin)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura POINT**](/previous-versions//dd162805(v=vs.85)) che riceve l'origine della vista.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE se** l'operazione ha esito positivo oppure **FALSE** se la visualizzazione corrente è di tipo elenco o report.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

