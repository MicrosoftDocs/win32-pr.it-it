---
title: RB_SETPALETTE messaggio (Commctrl.h)
description: Imposta il riquadro corrente del controllo rebar.
ms.assetid: 85f0726a-21fd-41b3-aa52-6a0a0c1947fa
keywords:
- RB_SETPALETTE dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- RB_SETPALETTE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85cd2968fa5fa74915e37f40f30dd47751e2316e8d91d0f51f9d3c7145b893fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434941"
---
# <a name="rb_setpalette-message"></a>Messaggio \_ RB SETPALETTE

Imposta il riquadro corrente del controllo rebar.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Oggetto **HPALETTE** che specifica il nuovo riquadro che verrà utilizzato dal controllo rebar.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **oggetto HPALETTE** che specifica il riquadro precedente del controllo rebar.

## <a name="remarks"></a>Commenti

È responsabilità dell'applicazione che invia questo messaggio eliminare **l'HPALETTE** passato in questo messaggio (vedere [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)). Il controllo rebar non eliminerà un set **HPALETTE** con questo messaggio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**RB \_ GETPALETTE**](rb-getpalette.md)
</dt> </dl>

 

