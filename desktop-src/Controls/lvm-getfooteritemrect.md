---
title: LVM_GETFOOTERITEMRECT messaggio (Commctrl.h)
description: Ottiene le coordinate di un piè di pagina per un elemento specificato in un controllo di visualizzazione elenco. Inviare questo messaggio in modo esplicito o usando la \_ macro ListView GetFooterItemRect.
ms.assetid: 4a6055d3-1cc1-4c3d-a5f6-006617ff3bce
keywords:
- LVM_GETFOOTERITEMRECT dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- LVM_GETFOOTERITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f5df635c18de3dec7cad128fe23ceeea2829b273984c561f5f289e2f0533b0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117830672"
---
# <a name="lvm_getfooteritemrect-message"></a>Messaggio LVM \_ GETFOOTERITEMRECT

Ottiene le coordinate di un piè di pagina per un elemento specificato in un controllo di visualizzazione elenco. Inviare questo messaggio in modo esplicito o usando la macro [**\_ ListView GetFooterItemRect.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooteritemrect)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ Pollici\]
</dt> <dd>

Indice dell'elemento nel controllo visualizzazione elenco.

</dd> <dt>

*lParam* \[ in, out\]
</dt> <dd>

Puntatore a una [**struttura RECT**](/previous-versions//dd162897(v=vs.85)) per ricevere le coordinate. L'applicazione chiamante è responsabile dell'allocazione di questa struttura. Le coordinate ricevute sono espresse come coordinate client.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo oppure FALSE **in** caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

