---
title: CB_LIMITTEXT messaggio (Winuser.h)
description: Limita la lunghezza del testo che l'utente può digitare nel controllo di modifica di una casella combinata.
ms.assetid: 95b7d07a-594b-4096-afbb-4dab77bdc41d
keywords:
- CB_LIMITTEXT dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- CB_LIMITTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e94cdb1bedfb1c0aa3efb401649524782183ced7728304951596c9383efaa0e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089081"
---
# <a name="cb_limittext-message"></a>CB \_ LIMITTEXT message

Limita la lunghezza del testo che l'utente può digitare nel controllo di modifica di una casella combinata.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Numero massimo di **TCHAR che** l'utente può immettere, senza includere il carattere Null di terminazione. Se questo parametro è zero, la lunghezza del testo è limitata 0x7FFFFFFE caratteri.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è sempre **TRUE.**

## <a name="remarks"></a>Commenti

Se la casella combinata non ha lo stile [**\_ CBS AUTOHSCROLL,**](combo-box-styles.md) l'impostazione del limite di testo su maggiore delle dimensioni del controllo di modifica non ha alcun effetto.

Il **messaggio CB \_ LIMITTEXT** limita solo il testo che l'utente può immettere. Non influisce su alcun testo già presente nel controllo di modifica quando viene inviato il messaggio, né influisce sulla lunghezza del testo copiato nel controllo di modifica quando viene selezionata una stringa nella casella di riepilogo.

Il limite predefinito per il testo che un utente può immettere nel controllo di modifica è 30.000 **TCHAR.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



 

 





