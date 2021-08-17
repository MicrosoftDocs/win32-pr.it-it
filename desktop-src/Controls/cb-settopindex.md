---
title: CB_SETTOPINDEX messaggio (Winuser.h)
description: Un'applicazione invia il messaggio CB SETTOPINDEX per garantire che un particolare elemento sia visibile nella casella \_ di riepilogo di una casella combinata.
ms.assetid: vs|controls|~\controls\comboboxes\comboboxreference\comboboxmessages\cb_settopindex.htm
keywords:
- CB_SETTOPINDEX di controllo Windows messaggio
topic_type:
- apiref
api_name:
- CB_SETTOPINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9364ef5013ef692adda76f96752f11691d5f4cc87c857386914105d16decb11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117832289"
---
# <a name="cb_settopindex-message"></a>CB \_ SETTOPINDEX message

Un'applicazione invia il **messaggio \_ CB SETTOPINDEX** per garantire che un particolare elemento sia visibile nella casella di riepilogo di una casella combinata. Il sistema scorre il contenuto della casella di riepilogo in modo che l'elemento specificato venga visualizzato nella parte superiore della casella di riepilogo o che sia stato raggiunto l'intervallo di scorrimento massimo.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica l'indice in base zero dell'elemento dell'elenco.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il messaggio ha esito positivo, il valore restituito è zero.

Se il messaggio ha esito negativo, il valore restituito è CB \_ ERR.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CB \_ GETTOPINDEX**](cb-gettopindex.md)
</dt> </dl>

 

 





