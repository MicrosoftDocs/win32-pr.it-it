---
title: Messaggio MCM_SETMONTHDELTA (COMmctrl. h)
description: Imposta la velocità di scorrimento per un controllo di calendario mensile. La velocità di scorrimento indica il numero di mesi durante i quali il controllo sposta la visualizzazione quando l'utente fa clic su un pulsante di scorrimento. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro MonthCal SetMonthDelta.
ms.assetid: 2d01b95f-3be8-4548-80b5-ac01d3e49e9f
keywords:
- Controlli di Windows Message MCM_SETMONTHDELTA
topic_type:
- apiref
api_name:
- MCM_SETMONTHDELTA
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 123eddb55a7ee8ddf8e3f6d8136e9ee57dfc8681
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302518"
---
# <a name="mcm_setmonthdelta-message"></a>\_Messaggio SETMONTHDELTA MCM

Imposta la velocità di scorrimento per un controllo di calendario mensile. La velocità di scorrimento indica il numero di mesi durante i quali il controllo sposta la visualizzazione quando l'utente fa clic su un pulsante di scorrimento. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MonthCal \_ SetMonthDelta**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setmonthdelta) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Valore che rappresenta il numero di mesi da impostare come velocità di scorrimento del controllo. Se questo valore è zero, il Delta del mese viene reimpostato sul valore predefinito, ovvero sul numero di mesi visualizzato nel controllo.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore INT che rappresenta la velocità di scorrimento precedente. Se la frequenza di scorrimento non è stata impostata in precedenza, il valore restituito è zero.

## <a name="remarks"></a>Commenti

I tasti PGSU e PGGIÙ, \_ ovvero VK prima e VK, \_ cambiano il mese selezionato per uno, indipendentemente dal numero di mesi visualizzato o dal valore impostato da **MCM \_ SETMONTHDELTA**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





