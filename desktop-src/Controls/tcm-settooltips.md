---
title: Messaggio TCM_SETTOOLTIPS (COMmctrl. h)
description: Assegna un controllo ToolTip a un controllo struttura a schede. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro TabCtrl di descrizione comando.
ms.assetid: c1b173b1-9da6-441a-a2b6-3875e2c343f8
keywords:
- Controlli di Windows Message TCM_SETTOOLTIPS
topic_type:
- apiref
api_name:
- TCM_SETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25e00166fb97c49c33b22811d28b79165bed4e9b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739871"
---
# <a name="tcm_settooltips-message"></a>\_Messaggio TCM SEtooltips

Assegna un controllo ToolTip a un controllo struttura a schede. È possibile inviare questo messaggio in modo esplicito o usando la macro [**TabCtrl di \_ Descrizione comando**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_settooltips) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per il controllo ToolTip.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

È possibile recuperare il controllo ToolTip associato a un controllo struttura a schede usando il messaggio [**TCM \_ GetToolTips**](tcm-gettooltips.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





