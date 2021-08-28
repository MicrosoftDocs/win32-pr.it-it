---
title: EM_CANPASTE messaggio (Richedit.h)
description: Determina se un controllo Rich Edit può incollare un formato degli Appunti specificato.
ms.assetid: 1b858ad8-1312-407b-b12a-c63668ba9f72
keywords:
- EM_CANPASTE controlli di Windows messaggio
topic_type:
- apiref
api_name:
- EM_CANPASTE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24f2d831cd3b3d04fcb7859d2b5936b7354fbb6b638558d605c9f8c5a6ee6333
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916061"
---
# <a name="em_canpaste-message"></a>Messaggio \_ EM CANPASTE

Determina se un controllo Rich Edit può incollare un formato degli Appunti specificato.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica i formati [degli Appunti da](/windows/desktop/dataxchg/clipboard-formats) provare. Per provare qualsiasi formato attualmente presente negli Appunti, impostare questo parametro su zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato. deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se è possibile incollare il formato degli Appunti, il valore restituito è un valore diverso da zero.

Se non è possibile incollare il formato degli Appunti, il valore restituito è zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> </dl>

 

