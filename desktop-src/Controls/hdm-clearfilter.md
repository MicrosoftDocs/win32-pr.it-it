---
title: Messaggio HDM_CLEARFILTER (COMmctrl. h)
description: Cancella il filtro per un controllo intestazione specificato. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro ClearFilter dell'intestazione.
ms.assetid: 74c0265e-68d1-4414-8fd9-20f5f041d4b4
keywords:
- Controlli di Windows Message HDM_CLEARFILTER
topic_type:
- apiref
api_name:
- HDM_CLEARFILTER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b1184432517761a567cd76bdd488e4593b1e999
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120311"
---
# <a name="hdm_clearfilter-message"></a>\_Messaggio HDM CLEARFILTER

Cancella il filtro per un controllo intestazione specificato. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ ClearFilter dell'intestazione**](/windows/desktop/api/Commctrl/nf-commctrl-header_clearfilter) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Valore di colonna che indica il filtro da cancellare.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un Integer. Viene eseguito il cast di **LRESULT** a un Integer che indica **true**(1) o **false**(0).

## <a name="remarks"></a>Commenti

Se il valore della colonna viene specificato come-1, tutti i filtri vengono cancellati e la notifica [HDN \_ FILTERCHANGE](hdn-filterchange.md) viene inviata una sola volta.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_ClearAllFilters intestazione**](/windows/desktop/api/Commctrl/nf-commctrl-header_clearallfilters)
</dt> </dl>

 

 





