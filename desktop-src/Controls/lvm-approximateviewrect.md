---
title: Messaggio LVM_APPROXIMATEVIEWRECT (COMmctrl. h)
description: Calcola la larghezza e l'altezza approssimative richieste per visualizzare un determinato numero di elementi. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro ApproximateViewRect di ListView.
ms.assetid: a14331a8-217d-48c6-9489-fb90c4d31b91
keywords:
- Controlli di Windows Message LVM_APPROXIMATEVIEWRECT
topic_type:
- apiref
api_name:
- LVM_APPROXIMATEVIEWRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be929d34acad46b75a53a9e0cc8825ec9801e998
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963771"
---
# <a name="lvm_approximateviewrect-message"></a>\_Messaggio APPROXIMATEVIEWRECT LVM

Calcola la larghezza e l'altezza approssimative richieste per visualizzare un determinato numero di elementi. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ ApproximateViewRect di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_approximateviewrect) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Numero di elementi da visualizzare nel controllo. Se questo parametro è impostato su-1, il messaggio utilizza il numero totale di elementi nel controllo.

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) è la dimensione x proposta del controllo, in pixel. Questo parametro può essere impostato su-1 per consentire al messaggio di usare il valore della larghezza corrente.

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) è la dimensione y proposta del controllo, in pixel. Questo parametro può essere impostato su-1 per consentire al messaggio di usare il valore di altezza corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **DWORD** che include la larghezza approssimativa (in [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))) e l'altezza (in [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))) necessarie per visualizzare gli elementi, in pixel.

## <a name="remarks"></a>Commenti

L'impostazione delle dimensioni del controllo di visualizzazione elenco in base alle dimensioni fornite da questo messaggio può ottimizzare il riprogetto e ridurre lo sfarfallio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

