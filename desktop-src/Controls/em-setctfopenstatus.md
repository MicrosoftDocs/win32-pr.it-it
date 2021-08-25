---
title: EM_SETCTFOPENSTATUS messaggio (Richedit.h)
description: Apre o chiude la tastiera Framework servizi di testo (TSF).
ms.assetid: 9bdabf5a-93db-4b0e-9528-807d262de866
keywords:
- EM_SETCTFOPENSTATUS dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- EM_SETCTFOPENSTATUS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85ac27017abbadeb038f5b881aefe1aff394036931529c84c9c5a34a36e556c7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048631"
---
# <a name="em_setctfopenstatus-message"></a>Messaggio EM \_ SETCTFOPENSTATUS

Apre o chiude la tastiera Framework servizi di testo (TSF).

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Per attivare la tastiera TSF, usare **TRUE.** Per disattivare la tastiera TSF, usare **FALSE.**

</dd> <dt>

*lParam* 
</dt> <dd>

Non usato; deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se ha esito positivo, questo messaggio restituisce **TRUE.** Se ha esito negativo, questo messaggio restituisce **FALSE.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP con solo app desktop SP1 \[\]<br/>                                  |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**EM \_ GETCTFOPENSTATUS**](em-getctfopenstatus.md)
</dt> </dl>

 

 





