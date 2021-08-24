---
title: PBM_GETBKCOLOR messaggio (Commctrl.h)
description: Ottiene il colore di sfondo dell'indicatore di stato.
ms.assetid: 9526ed78-08d9-468f-831b-72bb7c8c92d1
keywords:
- PBM_GETBKCOLOR di controllo Windows messaggio
topic_type:
- apiref
api_name:
- PBM_GETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1462d864df0440cd0567e6d6b1d04261818bb98ab4a6b5a803272e63abcb8d5d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919521"
---
# <a name="pbm_getbkcolor-message"></a>Messaggio PBM \_ GETBKCOLOR

Ottiene il colore di sfondo dell'indicatore di stato.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il colore di sfondo dell'indicatore di stato.

## <a name="remarks"></a>Commenti

Si tratta del colore impostato dal messaggio [**PBM \_ SETBKCOLOR.**](pbm-setbkcolor.md) Il valore predefinito è CLR \_ DEFAULT, definito in commctrl.h.

Questa funzione influisce solo sulla modalità classica, non su qualsiasi stile di visualizzazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





