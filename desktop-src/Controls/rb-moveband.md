---
title: RB_MOVEBAND messaggio (Commctrl.h)
description: Sposta una banda da un indice a un altro.
ms.assetid: bb5b45de-957e-46fb-b59a-18b55b69c395
keywords:
- RB_MOVEBAND di controllo Windows messaggio
topic_type:
- apiref
api_name:
- RB_MOVEBAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ab45f63b46b8bb883ef9f1fd8708f915dba2a6860ef2f6fabb09e2b00bd8fe6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119798541"
---
# <a name="rb_moveband-message"></a>Messaggio RB \_ MOVEBAND

Sposta una banda da un indice a un altro.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero della banda da spostare.

</dd> <dt>

*lParam* 
</dt> <dd>

Indice in base zero della nuova posizione della banda.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero in caso di esito positivo oppure zero in caso contrario.

## <a name="remarks"></a>Commenti

Questo messaggio modificherà molto probabilmente l'indice di altre bande nel controllo rebar. Se una banda viene spostata dall'indice 6 all'indice 0, l'indice di tutte le bande in mezzo verrà incrementato di uno.

*lParam non* deve mai essere maggiore del numero di bande meno uno. Il numero di bande può essere ottenuto con il [**messaggio RB \_ GETBANDCOUNT.**](rb-getbandcount.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





