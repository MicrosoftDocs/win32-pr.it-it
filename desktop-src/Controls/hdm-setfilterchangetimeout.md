---
title: HDM_SETFILTERCHANGETIMEOUT messaggio (Commctrl.h)
description: Imposta l'intervallo di timeout tra il momento in cui viene apportata una modifica negli attributi di filtro e la pubblicazione di una notifica \_ FILTERCHANGE HDN. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro Header SetFilterChangeTimeout.
ms.assetid: 9bc8e0e7-d7c1-4dd6-9d39-6ae937f19d60
keywords:
- HDM_SETFILTERCHANGETIMEOUT dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- HDM_SETFILTERCHANGETIMEOUT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23b5f8df12a7f30baa5f8b7d4bf15698b30cfbb6619fb71a81d4977b259c318b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119435861"
---
# <a name="hdm_setfilterchangetimeout-message"></a>Messaggio DI \_ HDM SETFILTERCHANGETIMEOUT

Imposta l'intervallo di timeout tra il momento in cui viene apportata una modifica negli attributi di filtro e la pubblicazione di [una notifica \_ FILTERCHANGE HDN.](hdn-filterchange.md) È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ Header SetFilterChangeTimeout.**](/windows/desktop/api/Commctrl/nf-commctrl-header_setfilterchangetimeout)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Valore di timeout in millisecondi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'indice del controllo filtro modificato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[HDN \_ FILTERCHANGE](hdn-filterchange.md)
</dt> </dl>

 

 





