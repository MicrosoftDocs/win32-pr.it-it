---
title: RB_SIZETORECT messaggio (Commctrl.h)
description: Tenta di trovare il layout migliore delle bande per il rettangolo specificato.
ms.assetid: c6242b54-bd65-489b-b417-9680cc39b64a
keywords:
- RB_SIZETORECT di controllo Windows messaggio
topic_type:
- apiref
api_name:
- RB_SIZETORECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba63630fc64f56dff914b4fb576ecc6cef43d12d192606a5088924fd6a5832e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078551"
---
# <a name="rb_sizetorect-message"></a>Messaggio RB \_ SIZETORECT

Tenta di trovare il layout migliore delle bande per il rettangolo specificato.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura RECT**](/previous-versions//dd162897(v=vs.85)) che specifica il rettangolo in cui deve essere ridimensionato il controllo rebar.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero se si è verificata una modifica del layout oppure zero in caso contrario.

## <a name="remarks"></a>Commenti

Le bande rebar verranno disposte e incapsulate in base alle esigenze per adattarle al rettangolo. Le bande con lo stile RBBS VARIABLEHEIGHT verranno ridimensionate nel modo più uniforme possibile per \_ adattarle al rettangolo. L'altezza di un rebar orizzontale o la larghezza di un rebar verticale può cambiare, a seconda del nuovo layout.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

