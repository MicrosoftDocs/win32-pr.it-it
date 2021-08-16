---
title: EM_GETLIMITTEXT messaggio (Winuser.h)
description: Ottiene il limite di testo corrente per un controllo di modifica. È possibile inviare questo messaggio a un controllo di modifica o a un controllo Rich Edit.
ms.assetid: 778967f0-c090-46a2-9f27-194b17bbb1be
keywords:
- EM_GETLIMITTEXT controlli di Windows messaggio
topic_type:
- apiref
api_name:
- EM_GETLIMITTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de2066bf03fd8ea05851a9cef58f4e308db49f82bdee94c2d503cadf1c20a2c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831682"
---
# <a name="em_getlimittext-message"></a>Messaggio \_ EM GETLIMITTEXT

Ottiene il limite di testo corrente per un controllo di modifica. È possibile inviare questo messaggio a un controllo di modifica o a un controllo Rich Edit.

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

Il valore restituito è il limite di testo.

## <a name="remarks"></a>Commenti

**Controlli di modifica, Rich Edit 2.0 e versioni successive:** Il limite di testo è la quantità massima di testo, in **TCHAR** s, che il controllo può contenere. Per il testo ANSI, questo è il numero di byte. per il testo Unicode, questo è il numero di caratteri. Due documenti con lo stesso limite di caratteri producono lo stesso limite di testo, anche se uno è ANSI e l'altro è Unicode.

**Rich Edit 1.0:** Il limite di testo è la quantità massima di testo, in byte, che il controllo Rich Edit può contenere.

**Rich Edit:** Supportato in Microsoft Rich Edit 1.0 e versioni successive. Per informazioni sulla compatibilità delle versioni rich edit con le varie versioni di sistema, vedere [Informazioni sui controlli Rich Edit.](about-rich-edit-controls.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**EM \_ SETLIMITTEXT**](em-setlimittext.md)
</dt> </dl>

 

 





