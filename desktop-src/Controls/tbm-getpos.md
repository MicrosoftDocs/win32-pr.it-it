---
title: TBM_GETPOS messaggio (Commctrl.h)
description: Recupera la posizione logica corrente del dispositivo di scorrimento in un trackbar. Le posizioni logiche sono i valori interi nell'intervallo di posizioni del dispositivo di scorrimento minimo e massimo del trackbar.
ms.assetid: 6f082ab2-2f9a-4bc0-bfca-56f7b1a2d921
keywords:
- TBM_GETPOS di controllo Windows messaggio
topic_type:
- apiref
api_name:
- TBM_GETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54ed3b8afed7b96e657984a437ff54b1099f196b8dc3d0035468835152b5a841
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078085"
---
# <a name="tbm_getpos-message"></a>Messaggio \_ GETPOS TBM

Recupera la posizione logica corrente del dispositivo di scorrimento in un trackbar. Le posizioni logiche sono i valori interi nell'intervallo di posizioni del dispositivo di scorrimento minimo e massimo del trackbar.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore a 32 bit che specifica la posizione logica corrente del dispositivo di scorrimento del trackbar.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TBM \_ SETPOS**](tbm-setpos.md)
</dt> </dl>

 

 





