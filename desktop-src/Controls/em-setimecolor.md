---
title: EM_SETIMECOLOR messaggio (Richedit.h)
description: Imposta il colore di composizione IME (Input Method Editor) per un controllo Rich Edit.
ms.assetid: ea5449c9-7d0f-4340-8e3e-1e0b77d443f6
keywords:
- EM_SETIMECOLOR di controllo Windows messaggio
topic_type:
- apiref
api_name:
- EM_SETIMECOLOR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a0f68e548a36cbdaa28f292feb69b6d56cbc3264b0bea8bdb1938088717bd62
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048401"
---
# <a name="em_setimecolor-message"></a>Messaggio EM \_ SETIMECOLOR

Imposta il colore di composizione IME (Input Method Editor) per un controllo Rich Edit.

> [!Note]  
> Questo messaggio è supportato solo nelle versioni in lingua Asia di Microsoft Rich Edit 1.0. Non è supportato nelle versioni successive.

 

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato. deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura COMPCOLOR**](/windows/desktop/api/Richedit/ns-richedit-compcolor) che contiene il colore di composizione da impostare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'operazione ha esito positivo, il valore restituito è un valore diverso da zero.

Se l'operazione non riesce, il valore restituito è zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**EM \_ GETIMECOLOR**](em-getimecolor.md)
</dt> <dt>

[**COMPCOLOR**](/windows/desktop/api/Richedit/ns-richedit-compcolor)
</dt> </dl>

 

 





