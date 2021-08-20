---
title: TB_MOVEBUTTON messaggio (Commctrl.h)
description: Sposta un pulsante da un indice a un altro.
ms.assetid: 030aedc5-2de5-4751-90b2-63794322f503
keywords:
- TB_MOVEBUTTON di controllo Windows messaggio
topic_type:
- apiref
api_name:
- TB_MOVEBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 857592f852b21d656be2a4ad5b59f691db9ac391f66960b98a70db138ea69f2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118168041"
---
# <a name="tb_movebutton-message"></a>Messaggio \_ MOVEBUTTON TB

Sposta un pulsante da un indice a un altro.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero del pulsante da spostare.

</dd> <dt>

*lParam* 
</dt> <dd>

Indice in base zero in cui verrà spostato il pulsante.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero in caso di esito positivo oppure zero in caso contrario.

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

 

 





