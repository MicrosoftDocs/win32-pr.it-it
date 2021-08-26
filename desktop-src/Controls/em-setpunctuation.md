---
title: EM_SETPUNCTUATION messaggio (Richedit.h)
description: Imposta i caratteri di punteggiatura per un controllo Rich Edit.
ms.assetid: c0c8ad14-63e2-4be8-8fc0-6b8ef9be4522
keywords:
- EM_SETPUNCTUATION controlli Windows messaggio
topic_type:
- apiref
api_name:
- EM_SETPUNCTUATION
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a5e0856c1ee1882695dc5e6d7dfdd6b72ea0f6c4f16ee7396bbfde2b76b49b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062901"
---
# <a name="em_setpunctuation-message"></a>Messaggio \_ EM SETPUNCTUATION

Imposta i caratteri di punteggiatura per un controllo Rich Edit.

> [!Note]  
> Questo messaggio è supportato solo nelle versioni in lingua Asia di Microsoft Rich Edit 1.0. Non è supportato nelle versioni successive.

 

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica il tipo di punteggiatura, che può essere uno dei valori seguenti.



| Valore                                                                                                                                                      | Significato                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span id="PC_LEADING"></span><span id="pc_leading"></span><dl> <dt>**PC \_ LEADING**</dt> </dl>       | Caratteri di punteggiatura iniziali.<br/>   |
| <span id="PC_FOLLOWING"></span><span id="pc_following"></span><dl> <dt>**PC \_ SEGUENTE**</dt> </dl> | Caratteri di punteggiatura seguenti.<br/> |
| <span id="PC_DELIMITER"></span><span id="pc_delimiter"></span><dl> <dt>**DELIMITATORE \_ PC**</dt> </dl> | Delimitatore.<br/>                        |
| <span id="PC_OVERFLOW_"></span><span id="pc_overflow_"></span><dl> <dt>**PC \_ OVERFLOW**</dt> </dl> | Non supportata.<br/>                    |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura PUNCTUATION**](/windows/desktop/api/Richedit/ns-richedit-punctuation) che contiene i caratteri di punteggiatura.

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

[**EM \_ GETPUNCTUATION**](em-getpunctuation.md)
</dt> <dt>

[**Punteggiatura**](/windows/desktop/api/Richedit/ns-richedit-punctuation)
</dt> </dl>

 

 





