---
title: EM_GETCTFMODEBIAS messaggio (Richedit.h)
description: Ottiene i valori Framework servizi di testo di distorsione della modalità predefinita per un controllo Microsoft Rich Edit.
ms.assetid: 2421d37d-169d-480f-a5f7-4c6033ca6c1a
keywords:
- EM_GETCTFMODEBIAS di controllo Windows messaggio
topic_type:
- apiref
api_name:
- EM_GETCTFMODEBIAS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60d6e030e3080ec9bf3d801583b9ade182483ba8560b3eccb2fb9813be7d39cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019749"
---
# <a name="em_getctfmodebias-message"></a>Messaggio \_ EM GETCTFMODEBIAS

Ottiene i valori Framework servizi di testo di distorsione della modalità predefinita per un controllo Microsoft Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non usato; deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Non usato; deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Valore di distorsione Framework servizi di testo corrente.

## <a name="remarks"></a>Commenti

Per ottenere la distorsione della modalità IME, chiamare [**EM \_ GETIMEMODEBIAS.**](em-getimemodebias.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP solo con \[ app desktop SP1\]<br/>                                  |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**EM \_ SETCTFMODEBIAS**](em-setctfmodebias.md)
</dt> <dt>

[**EM \_ GETIMEMODEBIAS**](em-getimemodebias.md)
</dt> </dl>

 

 





