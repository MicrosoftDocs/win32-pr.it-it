---
title: SB_GETBORDERS messaggio (Commctrl.h)
description: Recupera le larghezze correnti dei bordi orizzontale e verticale di una finestra di stato.
ms.assetid: 120c1e0d-6f42-424e-94e0-a080d216d39d
keywords:
- SB_GETBORDERS dei controlli Windows messaggio
topic_type:
- apiref
api_name:
- SB_GETBORDERS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dafa7a8c27b5c274a981e43edc5c55ec0cade67cac08a1d09a898916d792795c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118169054"
---
# <a name="sb_getborders-message"></a>Messaggio SB \_ GETBORDERS

Recupera le larghezze correnti dei bordi orizzontale e verticale di una finestra di stato.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una matrice di interi con tre elementi. Il primo elemento riceve lo spessore del bordo orizzontale, il secondo riceve lo spessore del bordo verticale e il terzo riceve lo spessore del bordo tra rettangoli.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo oppure FALSE **in** caso contrario.

## <a name="remarks"></a>Commenti

I bordi determinano la spaziatura tra il bordo esterno della finestra e i rettangoli all'interno della finestra che contengono testo. I bordi determinano anche la spaziatura tra rettangoli.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





