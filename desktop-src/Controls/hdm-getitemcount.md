---
title: Messaggio HDM_GETITEMCOUNT (COMmctrl. h)
description: Ottiene un conteggio degli elementi in un controllo intestazione. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro GetItemCount dell'intestazione.
ms.assetid: 0e6d2131-53b4-4927-bd0f-577b8eaf237a
keywords:
- Controlli di Windows Message HDM_GETITEMCOUNT
topic_type:
- apiref
api_name:
- HDM_GETITEMCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52ac0e647a675adf2bf29b9ff1f204bbd8b040d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120307"
---
# <a name="hdm_getitemcount-message"></a>\_Messaggio HDM GETITEMCOUNT

Ottiene un conteggio degli elementi in un controllo intestazione. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ GetItemCount dell'intestazione**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitemcount) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il numero di elementi in caso di esito positivo, oppure-1 in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





