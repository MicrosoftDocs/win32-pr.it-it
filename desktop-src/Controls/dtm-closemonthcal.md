---
title: Messaggio DTM_CLOSEMONTHCAL (COMmctrl. h)
description: Chiude un controllo di selezione data e ora (DTP). Inviare questo messaggio in modo esplicito o utilizzando la \_ macro DateTime CloseMonthCal.
ms.assetid: f60af77f-ec34-4f3d-9427-cda7ac6083bf
keywords:
- Controlli di Windows Message DTM_CLOSEMONTHCAL
topic_type:
- apiref
api_name:
- DTM_CLOSEMONTHCAL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd79f33576490196bf29fd51316f8ce3daf4ad4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047942"
---
# <a name="dtm_closemonthcal-message"></a>\_Messaggio CLOSEMONTHCAL DTM

Chiude un controllo di selezione data e ora (DTP). Inviare questo messaggio in modo esplicito o utilizzando la macro [**DateTime \_ CloseMonthCal**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_closemonthcal) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero.

## <a name="remarks"></a>Commenti

Elimina il controllo e invia una notifica [del \_ primo piano DTN](dtn-closeup.md) che il controllo sta chiudendo anziché il controllo è in apertura (a discesa come nella notifica a [ \_ discesa DTN](dtn-dropdown.md) ) all'elemento padre del controllo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[\_elenco a discesa DTN](dtn-dropdown.md)
</dt> <dt>

[primo piano DTN \_](dtn-closeup.md)
</dt> </dl>

 

 





