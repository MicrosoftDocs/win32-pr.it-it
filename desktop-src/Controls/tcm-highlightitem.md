---
title: Messaggio TCM_HIGHLIGHTITEM (COMmctrl. h)
description: Imposta lo stato di evidenziazione di un elemento di scheda. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro TabCtrl HighlightItem.
ms.assetid: b0d0850a-62d9-46a1-8846-81f67a886ea8
keywords:
- Controlli di Windows Message TCM_HIGHLIGHTITEM
topic_type:
- apiref
api_name:
- TCM_HIGHLIGHTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55664aeeeefadfcb5205b9a5bde4fee1aafdfef3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874401"
---
# <a name="tcm_highlightitem-message"></a>\_Messaggio TCM HIGHLIGHTITEM

Imposta lo stato di evidenziazione di un elemento di scheda. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**TabCtrl \_ HighlightItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_highlightitem) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Valore **int** che specifica l'indice in base zero di un elemento di controllo Tab.

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) è un **bool** che specifica lo stato di evidenziazione da impostare. Se questo valore è **true**, la scheda è evidenziata; Se **false**, la scheda è impostata sullo stato predefinito. Il valore di [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.

## <a name="remarks"></a>Commenti

In Comctl32.dll versione 6,0, questo messaggio non ha alcun effetto visibile quando un tema è attivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

