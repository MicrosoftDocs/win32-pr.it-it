---
title: EM_GETPASSWORDCHAR messaggio (Winuser.h)
description: Ottiene il carattere della password visualizzato da un controllo di modifica quando l'utente immette testo. È possibile inviare questo messaggio a un controllo di modifica o a un controllo Rich Edit.
ms.assetid: 874336f6-701b-466a-afa6-0cb3e787ba4c
keywords:
- EM_GETPASSWORDCHAR controlli di Windows messaggio
topic_type:
- apiref
api_name:
- EM_GETPASSWORDCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8c4e7ac576f18d0ab28fcf8c2288d2bee7966866a71180a81c34896c2396f56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831208"
---
# <a name="em_getpasswordchar-message"></a>Messaggio \_ EM GETPASSWORDCHAR

Ottiene il carattere della password visualizzato da un controllo di modifica quando l'utente immette testo. È possibile inviare questo messaggio a un controllo di modifica o a un controllo Rich Edit.

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

Il valore restituito specifica il carattere da visualizzare al posto di qualsiasi carattere digitato dall'utente. Se il valore restituito **è NULL,** non è presente alcun carattere password e il controllo visualizza i caratteri digitati dall'utente.

## <a name="remarks"></a>Commenti

Se viene creato un controllo di modifica con lo [**stile password \_ ES,**](edit-control-styles.md) il carattere della password predefinito viene impostato su un asterisco ( \* ). Se viene creato un controllo di modifica senza lo **stile password \_ ES,** non è presente alcun carattere password. Per modificare il carattere della password, inviare il [**messaggio EM \_ SETPASSWORDCHAR.**](em-setpasswordchar.md)

**Controlli di modifica:** I controlli di modifica su più righe non supportano lo stile o i messaggi della password.

**Modifica rtf:** Supportato in Microsoft Rich Edit 2.0 e versioni successive. Sia i controlli di modifica a riga singola che i controlli di modifica su più righe supportano lo stile della password e i messaggi. Per informazioni sulla compatibilità delle versioni rich edit con le varie versioni di sistema, vedere [Informazioni sui controlli Rich Edit.](about-rich-edit-controls.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**EM \_ SETPASSWORDCHAR**](em-setpasswordchar.md)
</dt> </dl>

 

 





