---
title: Messaggio TCM_ADJUSTRECT (COMmctrl. h)
description: Calcola l'area di visualizzazione di un controllo scheda in base a un rettangolo della finestra oppure calcola il rettangolo della finestra che corrisponderebbe a un'area di visualizzazione specificata. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro TabCtrl AdjustRect.
ms.assetid: 2f14201a-e4a3-4ae5-b9cf-4a674c52f24a
keywords:
- Controlli di Windows Message TCM_ADJUSTRECT
topic_type:
- apiref
api_name:
- TCM_ADJUSTRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9c1612a4f6c2fc436f858807fca59112c376a35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302368"
---
# <a name="tcm_adjustrect-message"></a>\_Messaggio TCM ADJUSTRECT

Calcola l'area di visualizzazione di un controllo scheda in base a un rettangolo della finestra oppure calcola il rettangolo della finestra che corrisponderebbe a un'area di visualizzazione specificata. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**TabCtrl \_ AdjustRect**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_adjustrect) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Operazione da eseguire. Se questo parametro è **true**, *lParam* specifica un rettangolo di visualizzazione e riceve il rettangolo della finestra corrispondente. Se questo parametro è **false**, *lParam* specifica un rettangolo della finestra e riceve l'area di visualizzazione corrispondente.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) che specifica il rettangolo specificato e riceve il rettangolo calcolato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Questo messaggio si applica solo ai controlli struttura a schede presenti nella parte superiore. Non si applica ai controlli struttura a schede che si trovano sui lati o in basso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

