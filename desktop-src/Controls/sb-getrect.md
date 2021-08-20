---
title: SB_GETRECT messaggio (Commctrl.h)
description: Recupera il rettangolo di delimitazione di una parte in una finestra di stato.
ms.assetid: 76b8d470-07ae-440b-9bf5-7875b80b0168
keywords:
- SB_GETRECT di Windows messaggi
topic_type:
- apiref
api_name:
- SB_GETRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85d874a5bf115918432bd6f0310a14ed026e0dc2df22da029bfca0be25649821
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118168735"
---
# <a name="sb_getrect-message"></a>Messaggio \_ GETRECT SB

Recupera il rettangolo di delimitazione di una parte in una finestra di stato.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero della parte di cui recuperare il rettangolo di delimitazione.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura RECT**](/previous-versions//dd162897(v=vs.85)) che riceve il rettangolo di delimitazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo oppure FALSE **in** caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

