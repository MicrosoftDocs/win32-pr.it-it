---
title: RB_GETROWHEIGHT messaggio (Commctrl.h)
description: Recupera l'altezza di una riga specificata in un controllo rebar.
ms.assetid: 1ff6a32e-b344-4dbc-b4a4-fb13f11a9d8c
keywords:
- RB_GETROWHEIGHT dei messaggi Windows controllo
topic_type:
- apiref
api_name:
- RB_GETROWHEIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ac650fb50f1b6594964ec0bf10d23a8c8b6b75ff82e14af44bb63e2c9cf8af8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118409415"
---
# <a name="rb_getrowheight-message"></a>Messaggio \_ RB GETROWHEIGHT

Recupera l'altezza di una riga specificata in un controllo rebar.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero di una banda. Verrà recuperata l'altezza della riga che contiene la banda specificata.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore UINT** che rappresenta l'altezza della riga, in pixel.

## <a name="remarks"></a>Commenti

Per recuperare il numero di righe in un controllo rebar, usare il [**messaggio RB \_ GETROWCOUNT.**](rb-getrowcount.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





