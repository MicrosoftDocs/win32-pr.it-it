---
title: RB_PUSHCHEVRON messaggio (Commctrl.h)
description: Inviato a un controllo rebar per eseguire il push di una chevron a livello di codice.
ms.assetid: 00a8ce10-1fb2-488a-a6f9-1814f73f82bd
keywords:
- RB_PUSHCHEVRON dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- RB_PUSHCHEVRON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2d095cd824970b7ea90541420274b204a1e2f63ce6e1218e62221741f572feb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434971"
---
# <a name="rb_pushchevron-message"></a>Messaggio \_ PUSHCHEVRON RB

Inviato a un controllo rebar per eseguire il push di una chevron a livello di codice.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero della banda di cui eseguire il push della chevron.

</dd> <dt>

*lParam* 
</dt> <dd>

Valore a 32 bit definito dall'applicazione. Verrà passato nuovamente all'applicazione come membro **lParamNM** della struttura [**NMREBARCHEVRON**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron) passata con la notifica [RBN \_ CHEVRONPUSHED.](rbn-chevronpushed.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito per questo messaggio non viene usato.

## <a name="remarks"></a>Commenti

Quando questo messaggio viene inviato, il controllo rebar invierà all'applicazione un codice di notifica [RBN \_ CHEVRONPUSHED,](rbn-chevronpushed.md) richiedendo di visualizzare il menu a scacchi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





