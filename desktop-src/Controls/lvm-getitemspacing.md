---
title: LVM_GETITEMSPACING messaggio (Commctrl.h)
description: Determina la spaziatura tra gli elementi in un controllo visualizzazione elenco. Puoi inviare questo messaggio in modo esplicito o usando la \_ macro ListView GetItemSpacing.
ms.assetid: 4e43fb43-468c-4b8a-9e3b-1694e90ffef8
keywords:
- LVM_GETITEMSPACING controlli di Windows messaggio
topic_type:
- apiref
api_name:
- LVM_GETITEMSPACING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 687a1aa75d71b96cebe855bb97ea57f0a9c628ed49b1ef7a51a7557b23b5ce41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088891"
---
# <a name="lvm_getitemspacing-message"></a>Messaggio \_ LVM GETITEMSPACING

Determina la spaziatura tra gli elementi in un controllo visualizzazione elenco. Puoi inviare questo messaggio in modo esplicito o usando la macro [**\_ ListView GetItemSpacing.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemspacing)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Visualizzazione per la quale recuperare la spaziatura dell'elemento. Questo parametro è **TRUE per** la visualizzazione icona piccola o **FALSE per** la visualizzazione icona.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce la quantità di spaziatura tra gli elementi. La spaziatura orizzontale è contenuta in [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) e la spaziatura verticale è contenuta in [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

