---
title: Messaggio EM_GETPASSWORDCHAR (winuser. h)
description: Ottiene il carattere della password visualizzato da un controllo di modifica quando l'utente immette il testo. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.
ms.assetid: 874336f6-701b-466a-afa6-0cb3e787ba4c
keywords:
- Controlli di Windows Message EM_GETPASSWORDCHAR
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
ms.openlocfilehash: 6285f002554e22c89896711d3d1d355a95c6bb7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874362"
---
# <a name="em_getpasswordchar-message"></a>\_Messaggio GETPASSWORDCHAR em

Ottiene il carattere della password visualizzato da un controllo di modifica quando l'utente immette il testo. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilizzato; deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilizzato; deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito specifica il carattere da visualizzare al posto di tutti i caratteri digitati dall'utente. Se il valore restituito è **null**, non è presente alcun carattere della password e il controllo Visualizza i caratteri digitati dall'utente.

## <a name="remarks"></a>Commenti

Se viene creato un controllo di modifica con lo stile di [**\_ password es**](edit-control-styles.md) , il carattere predefinito della password viene impostato su un asterisco ( \* ). Se un controllo di modifica viene creato senza lo stile di **\_ password es** , non è presente alcun carattere di password. Per modificare il carattere della password, inviare il messaggio [**\_ SETPASSWORDCHAR em**](em-setpasswordchar.md) .

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

[**\_SETPASSWORDCHAR em**](em-setpasswordchar.md)
</dt> </dl>

 

 





