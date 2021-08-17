---
title: EM_SETPASSWORDCHAR messaggio (Winuser.h)
description: Imposta o rimuove il carattere della password per un controllo di modifica. Quando viene impostato un carattere della password, tale carattere viene visualizzato al posto dei caratteri digitati dall'utente. È possibile inviare questo messaggio a un controllo di modifica o a un controllo Rich Edit.
ms.assetid: 9091892c-9f37-4e06-a084-9326c5f7f31e
keywords:
- EM_SETPASSWORDCHAR controlli di Windows messaggio
topic_type:
- apiref
api_name:
- EM_SETPASSWORDCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56cdfbc108ad5bc1b3e2e11b72937a92da473bcbfa01e974056743ed2e6fde1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118412316"
---
# <a name="em_setpasswordchar-message"></a>Messaggio EM \_ SETPASSWORDCHAR

Imposta o rimuove il carattere della password per un controllo di modifica. Quando viene impostato un carattere della password, tale carattere viene visualizzato al posto dei caratteri digitati dall'utente. È possibile inviare questo messaggio a un controllo di modifica o a un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Carattere da visualizzare al posto dei caratteri digitati dall'utente. Se questo parametro è zero, il controllo rimuove il carattere della password corrente e visualizza i caratteri digitati dall'utente.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce un valore.

## <a name="remarks"></a>Commenti

Quando un controllo di modifica riceve il messaggio **EM \_ SETPASSWORDCHAR,** il controllo ridisegna tutti i caratteri visibili usando il carattere specificato dal *parametro wParam.* Se *wParam* è zero, il controllo ridisegna tutti i caratteri visibili usando i caratteri digitati dall'utente.

Se viene creato un controllo di modifica con lo [**stile password \_ ES,**](edit-control-styles.md) il carattere della password predefinito viene impostato su un asterisco ( \* ). Se viene creato un controllo di modifica senza lo **stile password \_ ES,** non è presente alcun carattere password. Lo **stile ES \_ PASSWORD** viene rimosso se viene inviato un **messaggio EM \_ SETPASSWORDCHAR** con il *parametro wParam* impostato su zero.

**Controlli di modifica:** I controlli di modifica su più righe non supportano lo stile o i messaggi della password.

**Rich Edit:** Supportato in Microsoft Rich Edit 2.0 e versioni successive. Sia i controlli di modifica a riga singola che i controlli di modifica su più righe supportano lo stile della password e i messaggi. Per informazioni sulla compatibilità delle versioni rich edit con le varie versioni di sistema, vedere [Informazioni sui controlli Rich Edit.](about-rich-edit-controls.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**EM \_ GETPASSWORDCHAR**](em-getpasswordchar.md)
</dt> </dl>

 

 





