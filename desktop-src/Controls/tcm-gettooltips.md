---
title: Messaggio TCM_GETTOOLTIPS (COMmctrl. h)
description: Recupera l'handle per il controllo ToolTip associato a un controllo struttura a schede. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro TabCtrl GetToolTips.
ms.assetid: d7dcca4f-8629-4eeb-844f-b3171438f528
keywords:
- Controlli di Windows Message TCM_GETTOOLTIPS
topic_type:
- apiref
api_name:
- TCM_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e49334a1fa7124dd6e7a0f0b739cd1ebd24b51b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121142"
---
# <a name="tcm_gettooltips-message"></a>\_Messaggio TCM GETtooltips

Recupera l'handle per il controllo ToolTip associato a un controllo struttura a schede. È possibile inviare questo messaggio in modo esplicito o usando la macro [**TabCtrl \_ GetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_gettooltips) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'handle per il controllo ToolTip se ha esito positivo o **null** in caso contrario.

## <a name="remarks"></a>Commenti

Un controllo struttura a schede crea un controllo ToolTip se dispone dello stile [**\_ Descrizione comando TCS**](tab-control-styles.md) . È anche possibile assegnare un controllo ToolTip a un controllo struttura a schede usando il messaggio [**TCM \_ setooltips**](tcm-settooltips.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





