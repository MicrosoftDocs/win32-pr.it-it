---
title: EM_SETLIMITTEXT messaggio (Winuser.h)
description: 'EM_SETLIMITTEXT messaggio: imposta il limite di testo di un controllo di modifica.'
ms.assetid: e2be7814-435b-495f-982a-32247fbc0165
keywords:
- EM_SETLIMITTEXT di windows del messaggio
topic_type:
- apiref
api_name:
- EM_SETLIMITTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b66d4e03b5c1824ab501226482fcf51fb9121cba
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109749"
---
# <a name="em_setlimittext-message"></a>Messaggio EM \_ SETLIMITTEXT

Imposta il limite di testo di un controllo di modifica. Il limite di testo è la quantità massima di testo, in **TCHAR** s, che l'utente può digitare nel controllo di modifica. È possibile inviare questo messaggio a un controllo di modifica o a un controllo Rich Edit.

Per i controlli di modifica e Microsoft Rich Edit 1.0, vengono usati i byte. Per Microsoft Rich Edit 2.0 e versioni successive, vengono usati caratteri.

Il **messaggio EM \_ SETLIMITTEXT** è identico al [**messaggio EM \_ LIMITTEXT.**](em-limittext.md)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Numero massimo di **TCHAR che** l'utente può immettere. Per il testo ANSI, questo è il numero di byte. per il testo Unicode, questo è il numero di caratteri. Questo numero non include il carattere Null di terminazione.

**Controlli Rich Edit:** Se questo parametro è zero, la lunghezza del testo viene impostata su 64.000 caratteri.

Se questo parametro è zero, la lunghezza del testo viene impostata su 0x7FFFFFFE caratteri per i controlli di modifica a riga singola o su 1 per i controlli di modifica su più righe.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce un valore.

## <a name="remarks"></a>Commenti

Il **messaggio EM \_ SETLIMITTEXT** limita solo il testo che l'utente può immettere. Non influisce sul testo già presente nel controllo di modifica quando viene inviato il messaggio, né sulla lunghezza del testo copiato nel controllo di modifica dal messaggio [**\_ WM SETTEXT.**](/windows/desktop/winmsg/wm-settext) Se un'applicazione usa il messaggio **WM \_ SETTEXT** per inserire più testo in un controllo di modifica rispetto a quello specificato nel messaggio **EM \_ SETLIMITTEXT,** l'utente può modificare l'intero contenuto del controllo di modifica.

Prima della chiamata a **EM \_ SETLIMITTEXT,** il limite predefinito per la quantità di testo che un utente può immettere in un controllo di modifica è di 32.767 caratteri.

Per i controlli di modifica a riga singola, il limite di testo è 0x7FFFFFFE byte o il valore del *parametro wParam,* a seconda del valore minore. Per i controlli di modifica su più righe, questo valore è pari a 1 byte o al valore del *parametro wParam,* a seconda del valore minore.

**Rich Edit:** Supportato in Microsoft Rich Edit 1.0 e versioni successive. Usare il messaggio [**EM \_ EXLIMITTEXT per**](em-exlimittext.md) i valori di lunghezza del testo maggiori di 64.000. Per informazioni sulla compatibilità delle versioni rich edit con le varie versioni di sistema, vedere [Informazioni sui controlli Rich Edit.](about-rich-edit-controls.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows Vista \[\]<br/>                                                           |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**EM \_ GETLIMITTEXT**](em-getlimittext.md)
</dt> </dl>

 

