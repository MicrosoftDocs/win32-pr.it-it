---
title: EM_GETSCROLLPOS messaggio (Richedit.h)
description: Ottiene la posizione di scorrimento corrente del controllo di modifica.
ms.assetid: 26e122da-f1b4-4694-978c-ff678dad5d9f
keywords:
- EM_GETSCROLLPOS dei messaggi Windows controllo
topic_type:
- apiref
api_name:
- EM_GETSCROLLPOS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42bde137096ae3c13582017f91b82c1eb9100097bb76f0d1babb91fa47b52196
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119800031"
---
# <a name="em_getscrollpos-message"></a>Messaggio \_ EM GETSCROLLPOS

Ottiene la posizione di scorrimento corrente del controllo di modifica.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato. deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura POINT.**](/previous-versions//dd162805(v=vs.85)) Dopo aver **chiamato EM \_ GETSCROLLPOS,** questo parametro contiene un punto nello spazio di testo virtuale del documento, espresso in pixel. Questo punto sarà il punto che si trova attualmente nell'angolo superiore sinistro della finestra di controllo di modifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio restituisce sempre 1.

## <a name="remarks"></a>Commenti

I valori restituiti nella [**struttura POINT**](/previous-versions//dd162805(v=vs.85)) sono valori a 16 bit (anche nei campi a 32 bit).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Componente ridistribuibile<br/>          | Rich Edit 3.0<br/>                                                              |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**EM \_ SETSCROLLPOS**](em-setscrollpos.md)
</dt> </dl>

 

