---
title: Messaggio EM_SETPASSWORDCHAR (winuser. h)
description: Imposta o rimuove il carattere della password per un controllo di modifica. Quando viene impostato un carattere della password, il carattere viene visualizzato al posto dei caratteri digitati dall'utente. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.
ms.assetid: 9091892c-9f37-4e06-a084-9326c5f7f31e
keywords:
- Controlli di Windows Message EM_SETPASSWORDCHAR
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
ms.openlocfilehash: 8dd2c75039a6d447809cc17e5c44d70c6e612ede
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476336"
---
# <a name="em_setpasswordchar-message"></a>\_Messaggio SETPASSWORDCHAR em

Imposta o rimuove il carattere della password per un controllo di modifica. Quando viene impostato un carattere della password, il carattere viene visualizzato al posto dei caratteri digitati dall'utente. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Carattere da visualizzare al posto dei caratteri digitati dall'utente. Se questo parametro è zero, il controllo rimuove il carattere della password corrente e Visualizza i caratteri digitati dall'utente.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce alcun valore.

## <a name="remarks"></a>Commenti

Quando un controllo di modifica riceve il messaggio **\_ SETPASSWORDCHAR em** , il controllo ridisegni tutti i caratteri visibili usando il carattere specificato dal parametro *wParam* . Se *wParam* è zero, il controllo ridisegni tutti i caratteri visibili usando i caratteri digitati dall'utente.

Se viene creato un controllo di modifica con lo stile di [**\_ password es**](edit-control-styles.md) , il carattere predefinito della password viene impostato su un asterisco ( \* ). Se un controllo di modifica viene creato senza lo stile di **\_ password es** , non è presente alcun carattere di password. Lo stile di **\_ password es** viene rimosso se viene inviato un messaggio **\_ SETPASSWORDCHAR em** con il parametro *wParam* impostato su zero.

**Controlli di modifica:** I controlli di modifica su più righe non supportano lo stile o i messaggi della password.

**Modifica avanzata:** Supportato in Microsoft Rich Edit 2,0 e versioni successive. I controlli di modifica a riga singola e a più righe supportano lo stile e i messaggi della password. Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_GETPASSWORDCHAR em**](em-getpasswordchar.md)
</dt> </dl>

 

 





