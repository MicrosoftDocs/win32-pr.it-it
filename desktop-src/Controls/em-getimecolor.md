---
title: EM_GETIMECOLOR messaggio (Richedit.h)
description: Recupera il colore della composizione IME (Input Method Editor).
ms.assetid: 788ac56c-f2d8-4e9a-8829-b92dcd76e6de
keywords:
- EM_GETIMECOLOR controlli Windows messaggio
topic_type:
- apiref
api_name:
- EM_GETIMECOLOR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46ac9d49f4fe178bdda45359da8aabd40badcd68aceadc4a57890279fc9fda01
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049101"
---
# <a name="em_getimecolor-message"></a>Messaggio \_ EM GETIMECOLOR

Recupera il colore della composizione IME (Input Method Editor).

> [!Note]  
> Questo messaggio è supportato solo nelle versioni in lingua asia di Microsoft Rich Edit 1.0. Non è supportato nelle versioni successive di Rich Edit.

 

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato. deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Matrice di quattro elementi di [**strutture COMPCOLOR**](/windows/desktop/api/Richedit/ns-richedit-compcolor) che riceve il colore della composizione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'operazione ha esito positivo, il valore restituito è un valore diverso da zero.

Se l'operazione non riesce, il valore restituito è zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**COMPCOLOR**](/windows/desktop/api/Richedit/ns-richedit-compcolor)
</dt> </dl>

 

 





