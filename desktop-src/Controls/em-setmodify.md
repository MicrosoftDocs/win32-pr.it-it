---
title: EM_SETMODIFY messaggio (Winuser.h)
description: Imposta o cancella il flag di modifica per un controllo di modifica. Il flag di modifica indica se il testo all'interno del controllo di modifica è stato modificato. È possibile inviare questo messaggio a un controllo di modifica o a un controllo Rich Edit.
ms.assetid: 9393f03e-0719-458b-8122-616df738c417
keywords:
- EM_SETMODIFY del messaggio Windows controlli
topic_type:
- apiref
api_name:
- EM_SETMODIFY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcd367a828e7f431b6177a2ec99fe508fec3e48c4743d492277f00ed4965e001
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831163"
---
# <a name="em_setmodify-message"></a>Messaggio \_ EM SETMODIFY

Imposta o cancella il flag di modifica per un controllo di modifica. Il flag di modifica indica se il testo all'interno del controllo di modifica è stato modificato. È possibile inviare questo messaggio a un controllo di modifica o a un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Nuovo valore per il flag di modifica. Il valore **TRUE** indica che il testo è stato modificato e il valore **FALSE** indica che non è stato modificato.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce un valore.

## <a name="remarks"></a>Commenti

Il sistema cancella automaticamente il flag di modifica su zero quando viene creato il controllo. Se l'utente modifica il testo del controllo, il sistema imposta il flag su un valore diverso da zero. È possibile inviare [**il \_ messaggio EM GETMODIFY**](em-getmodify.md) al controllo di modifica per recuperare lo stato corrente del flag.

**Rich Edit 1.0:** Gli oggetti creati senza il flag **REO \_ DYNAMICSIZE** verranno bloccati nei relativi extent quando il flag di modifica è impostato su **FALSE.**

**Rich Edit:** Supportato in Microsoft Rich Edit 1.0 e versioni successive. Per informazioni sulla compatibilità delle versioni rich edit con le varie versioni di sistema, vedere [Informazioni sui controlli Rich Edit.](about-rich-edit-controls.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**EM \_ GETMODIFY**](em-getmodify.md)
</dt> <dt>

[**REOBJECT**](/windows/desktop/api/Richole/ns-richole-reobject)
</dt> </dl>

 

 





