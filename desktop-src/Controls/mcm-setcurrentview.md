---
title: MCM_SETCURRENTVIEW messaggio (Commctrl.h)
description: Imposta la visualizzazione corrente del calendario. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro MonthCal SetCurrentView.
ms.assetid: 26ccbb80-0dba-4241-a2eb-b79000fc3618
keywords:
- MCM_SETCURRENTVIEW di controllo Windows messaggio
topic_type:
- apiref
api_name:
- MCM_SETCURRENTVIEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33cf7206fb7e778c0ab7d28ee8947b9327e8cc98bd8ae8c9063213814676a77e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019039"
---
# <a name="mcm_setcurrentview-message"></a>MESSAGGIO \_ DI MCM SETCURRENTVIEW

Imposta la visualizzazione corrente del calendario. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ MonthCal SetCurrentView.**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcurrentview)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Nuova visualizzazione. Una delle costanti seguenti.



| Valore                                                                                                                                                      | Significato                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="MCMV_MONTH"></span><span id="mcmv_month"></span><dl> <dt>**MCMV \_ MONTH**</dt> </dl>       | Visualizzazione mensile.<br/> |
| <span id="MCMV_YEAR"></span><span id="mcmv_year"></span><dl> <dt>**MCMV \_ YEAR**</dt> </dl>          | Visualizzazione annuale.<br/>  |
| <span id="MCMV_DECADE"></span><span id="mcmv_decade"></span><dl> <dt>**MCMV \_ DECADE**</dt> </dl>    | Visualizzazione Decennale.<br/>  |
| <span id="MCMV_CENTURY"></span><span id="mcmv_century"></span><dl> <dt>**MCMV \_ CENTURY**</dt> </dl> | Visualizzazione Century.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero in caso di esito positivo oppure zero in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





