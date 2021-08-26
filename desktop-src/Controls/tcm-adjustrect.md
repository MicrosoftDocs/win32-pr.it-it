---
title: TCM_ADJUSTRECT messaggio (Commctrl.h)
description: Calcola l'area di visualizzazione di un controllo Struttura a schede in base a un rettangolo della finestra oppure calcola il rettangolo della finestra corrispondente a un'area di visualizzazione specificata. È possibile inviare questo messaggio in modo esplicito o tramite la \_ macro TabCtrl AdjustRect.
ms.assetid: 2f14201a-e4a3-4ae5-b9cf-4a674c52f24a
keywords:
- TCM_ADJUSTRECT di controllo Windows messaggio
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
ms.openlocfilehash: ba09a88f12a25b87f507d70961a816412f2679da0fb9e1cb6ed6c760ecca320e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105011"
---
# <a name="tcm_adjustrect-message"></a>Messaggio \_ TCM ADJUSTRECT

Calcola l'area di visualizzazione di un controllo Struttura a schede in base a un rettangolo della finestra oppure calcola il rettangolo della finestra corrispondente a un'area di visualizzazione specificata. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**\_ TabCtrl AdjustRect.**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_adjustrect)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Operazione da eseguire. Se questo parametro è **TRUE,** *lParam* specifica un rettangolo di visualizzazione e riceve il rettangolo della finestra corrispondente. Se questo parametro è **FALSE,** *lParam* specifica un rettangolo della finestra e riceve l'area di visualizzazione corrispondente.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura RECT**](/previous-versions//dd162897(v=vs.85)) che specifica il rettangolo specificato e riceve il rettangolo calcolato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Questo messaggio si applica solo ai controlli struttura a schede nella parte superiore. Non si applica ai controlli struttura a schede presenti sui lati o in basso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

