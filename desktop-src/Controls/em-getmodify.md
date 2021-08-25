---
title: EM_GETMODIFY messaggio (Winuser.h)
description: Ottiene lo stato del flag di modifica di un controllo di modifica. Il flag indica se il contenuto del controllo di modifica è stato modificato. È possibile inviare questo messaggio a un controllo di modifica o a un controllo Rich Edit.
ms.assetid: 4229e2f2-3493-4721-8b52-8933c9dc0a77
keywords:
- EM_GETMODIFY controlli Windows messaggio
topic_type:
- apiref
api_name:
- EM_GETMODIFY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34156e363824e975af68449b40ed639eeeb7e3ab76bd680b9837f3d3dd907537
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048901"
---
# <a name="em_getmodify-message"></a>Messaggio \_ EM GETMODIFY

Ottiene lo stato del flag di modifica di un controllo di modifica. Il flag indica se il contenuto del controllo di modifica è stato modificato. È possibile inviare questo messaggio a un controllo di modifica o a un controllo Rich Edit.

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

Se il contenuto del controllo di modifica è stato modificato, il valore restituito è diverso da zero. in caso contrario, è zero.

## <a name="remarks"></a>Commenti

Il sistema cancella automaticamente il flag di modifica su zero quando viene creato il controllo. Se l'utente modifica il testo del controllo, il sistema imposta il flag su un valore diverso da zero. È possibile inviare [**il messaggio EM \_ SETMODIFY**](em-setmodify.md) al controllo di modifica per impostare o cancellare il flag.

**Rich Edit:** Supportato in Microsoft Rich Edit 1.0 e versioni successive. Per informazioni sulla compatibilità delle versioni rich edit con le varie versioni di sistema, vedere [Informazioni sui controlli Rich Edit.](about-rich-edit-controls.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**EM \_ SETMODIFY**](em-setmodify.md)
</dt> </dl>

 

 





