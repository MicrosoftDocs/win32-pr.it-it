---
title: LVM_GETFOOTERRECT messaggio (Commctrl.h)
description: Recupera le coordinate del piè di pagina per un controllo di visualizzazione elenco. Inviare questo messaggio in modo esplicito o usando la \_ macro ListView GetFooterRect.
ms.assetid: f8816f35-c1d2-4072-81d3-0a9a3df53d64
keywords:
- LVM_GETFOOTERRECT di controllo Windows messaggio
topic_type:
- apiref
api_name:
- LVM_GETFOOTERRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39bc2c5cd724c9b5b4885b99123489e49ead52243d43388e7eb22808fb43a826
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118411460"
---
# <a name="lvm_getfooterrect-message"></a>Messaggio LVM \_ GETFOOTERRECT

Recupera le coordinate del piè di pagina per un controllo di visualizzazione elenco. Inviare questo messaggio in modo esplicito o usando la macro [**\_ ListView GetFooterRect.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooterrect)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non usato. Deve essere 0.

</dd> <dt>

*lParam* \[ in, out\]
</dt> <dd>

Puntatore a una [**struttura RECT**](/previous-versions//dd162897(v=vs.85)) per ricevere le coordinate. Il processo chiamante è responsabile dell'allocazione di questa struttura. Le coordinate ricevute sono espresse come coordinate client.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo oppure FALSE **in** caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

