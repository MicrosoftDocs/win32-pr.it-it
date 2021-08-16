---
title: TBM_GETTIC messaggio (Commctrl.h)
description: Recupera la posizione logica di un segno di graduazione in un trackbar. La posizione logica può essere uno qualsiasi dei valori interi nell'intervallo tra le posizioni minime e massime del dispositivo di scorrimento del trackbar.
ms.assetid: 9d70c860-de97-4579-bb10-e9e9db7f1784
keywords:
- TBM_GETTIC dei controlli Windows messaggio
topic_type:
- apiref
api_name:
- TBM_GETTIC
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b7cdd2c28f9add787c41da3cde3fabc3a5dff33812b3dd9c07a26a603d3a79e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829605"
---
# <a name="tbm_gettic-message"></a>Messaggio \_ GETTIC TBM

Recupera la posizione logica di un segno di graduazione in un trackbar. La posizione logica può essere uno qualsiasi dei valori interi nell'intervallo tra le posizioni minime e massime del dispositivo di scorrimento del trackbar.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero che identifica un segno di graduazione. Gli indici validi sono nell'intervallo compreso tra zero e due valori inferiori al numero di tick restituito dal messaggio [**\_ TBM GETNUMTICS.**](tbm-getnumtics.md)

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce la posizione logica del segno di graduazione specificato oppure -1 se *wParam* non specifica un indice valido.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





