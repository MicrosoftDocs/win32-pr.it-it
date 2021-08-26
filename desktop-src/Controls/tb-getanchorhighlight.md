---
title: TB_GETANCHORHIGHLIGHT messaggio (Commctrl.h)
description: Recupera l'impostazione di evidenziazione dell'ancoraggio per una barra degli strumenti.
ms.assetid: 167d481c-8684-40eb-9323-cfa238be3643
keywords:
- TB_GETANCHORHIGHLIGHT dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- TB_GETANCHORHIGHLIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eadee4fd029cfe8ffb43960070538cf6574ca3bb178829f65af1ddc0753b9ef2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919081"
---
# <a name="tb_getanchorhighlight-message"></a>TB \_ GETANCHORHIGHLIGHT message

Recupera l'impostazione di evidenziazione dell'ancoraggio per una barra degli strumenti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore booleano che indica se è impostata l'evidenziazione dell'ancoraggio. Se questo valore è diverso da zero, l'evidenziazione dell'ancoraggio è abilitata. Se questo valore è zero, viene disabilitato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TB \_ SETANCHORHIGHLIGHT**](tb-setanchorhighlight.md)
</dt> </dl>

 

 





