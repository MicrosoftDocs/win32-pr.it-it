---
title: Messaggio TCM_DESELECTALL (COMmctrl. h)
description: Reimposta gli elementi in un controllo struttura a schede, cancellando tutti i set impostati sullo \_ stato TCIS ButtonPressed. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro TabCtrl DeselectAll.
ms.assetid: cc2e5131-3c1b-473a-a0ca-274a2d39a2f1
keywords:
- Controlli di Windows Message TCM_DESELECTALL
topic_type:
- apiref
api_name:
- TCM_DESELECTALL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f606538075a9163d8b8dc8328b5585b51b769aa5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121150"
---
# <a name="tcm_deselectall-message"></a>\_Messaggio TCM DESELECTALL

Reimposta gli elementi in un controllo struttura a schede, cancellando tutti i set impostati sullo stato [**TCIS \_ ButtonPressed**](tab-control-item-states.md) . È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**TabCtrl \_ DeselectAll**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_deselectall) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Flag che specifica l'ambito della deselezione dell'elemento. Se questo parametro è impostato su **false**, tutti gli elementi della scheda verranno reimpostati. Se è impostato su **true**, tutti gli elementi della scheda eccetto quello attualmente selezionato verranno reimpostati.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito per questo messaggio non viene utilizzato.

## <a name="remarks"></a>Commenti

Questo messaggio è significativo solo se è stato impostato il flag di stile dei [**\_ pulsanti TCS**](tab-control-styles.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





