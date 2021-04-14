---
title: Messaggio MCM_GETCURRENTVIEW (COMmctrl. h)
description: Ottiene la visualizzazione corrente del calendario. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro MonthCal GetCurrentView.
ms.assetid: 9c42ebf6-611e-4e50-9dcc-cf7fd63b32eb
keywords:
- Controlli di Windows Message MCM_GETCURRENTVIEW
topic_type:
- apiref
api_name:
- MCM_GETCURRENTVIEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eebbd6a2b33043294b64b8b65308520b52dbe449
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478491"
---
# <a name="mcm_getcurrentview-message"></a>\_Messaggio GETCURRENTVIEW MCM

Ottiene la visualizzazione corrente del calendario. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MonthCal \_ GetCurrentView**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcurrentview) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Visualizzazione corrente. Uno dei valori seguenti.



| Codice restituito                                                                                  | Descrizione              |
|----------------------------------------------------------------------------------------------|--------------------------|
| <dl> <dt>**\_mese MCMV**</dt> </dl>   | Visualizzazione mensile.<br/> |
| <dl> <dt>**MCMV \_ anno**</dt> </dl>    | Visualizzazione annuale.<br/>  |
| <dl> <dt>**MCMV \_ decennio**</dt> </dl>  | Visualizzazione decade.<br/>  |
| <dl> <dt>**MCMV \_ secolo**</dt> </dl> | Visualizzazione secolo.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





