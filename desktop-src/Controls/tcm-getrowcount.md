---
title: Messaggio TCM_GETROWCOUNT (COMmctrl. h)
description: Recupera il numero corrente di righe di schede in un controllo struttura a schede. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro TabCtrl GetRowCount.
ms.assetid: ef104374-1030-46c3-876e-083df73854ab
keywords:
- Controlli di Windows Message TCM_GETROWCOUNT
topic_type:
- apiref
api_name:
- TCM_GETROWCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9bc3d9985591a08b96be2f21d55b8a6cade9b7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874406"
---
# <a name="tcm_getrowcount-message"></a>TCM- \_ messaggio GETrowcount

Recupera il numero corrente di righe di schede in un controllo struttura a schede. È possibile inviare questo messaggio in modo esplicito o usando la macro [**TabCtrl \_ GetRowCount**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getrowcount) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il numero di righe di tabulazioni.

## <a name="remarks"></a>Commenti

Solo i controlli struttura a schede con lo stile [**\_ multiriga TCS**](tab-control-styles.md) possono avere più righe di schede.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





