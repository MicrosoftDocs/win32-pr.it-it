---
title: Messaggio EM_LIMITTEXT (winuser. h)
description: Imposta il limite di testo di un controllo di modifica.
ms.assetid: 5a605de7-8dc7-4c54-8f18-e0b08c720856
keywords:
- Controlli di Windows Message EM_LIMITTEXT
topic_type:
- apiref
api_name:
- EM_LIMITTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf45f7ee9cfd88a25b78f0bd58911e516c146096
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476108"
---
# <a name="em_limittext-message"></a>\_Messaggio LIMITTEXT em

Imposta il limite di testo di un controllo di modifica. Il limite di testo è la quantità massima di testo, in **TCHAR** s, che l'utente può digitare nel controllo di modifica. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.

Per i controlli di modifica e Microsoft Rich Edit 1,0, vengono usati i byte. Per Microsoft Rich Edit 2,0 e versioni successive, vengono utilizzati i caratteri.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Il numero massimo di **TCHAR** che l'utente può immettere. Per testo ANSI, indica il numero di byte; per il testo Unicode, indica il numero di caratteri. Questo numero non include il carattere null di terminazione.

**Controlli Rich Edit:** Se questo parametro è zero, la lunghezza del testo viene impostata su 64.000 caratteri.

Se questo parametro è zero, la lunghezza del testo viene impostata su 0x7FFFFFFE caratteri per i controlli di modifica a riga singola o-1 per i controlli di modifica su più righe.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce alcun valore.

## <a name="remarks"></a>Commenti

Il **messaggio \_ LIMITTEXT em** limita solo il testo che l'utente può immettere. Non influisce sul testo già presente nel controllo di modifica quando il messaggio viene inviato, né sulla lunghezza del testo copiato nel controllo di modifica da parte del messaggio [**WM \_**](/windows/desktop/winmsg/wm-settext) . Se un'applicazione usa il messaggio di **\_ testo WM** per inserire più testo in un controllo di modifica rispetto a quanto specificato nel messaggio **\_ LIMITTEXT em** , l'utente può modificare l'intero contenuto del controllo di modifica.

Prima di chiamare **em \_ LIMITTEXT** , il limite predefinito per la quantità di testo che un utente può immettere in un controllo di modifica è di 32.767 caratteri.

Per i controlli di modifica a riga singola, il limite di testo è 0x7FFFFFFE byte o il valore del parametro *wParam* , a seconda del valore minore. Per i controlli di modifica su più righe, questo valore è-1 byte oppure il valore del parametro *wParam* , a seconda del valore minore.

**Modifica avanzata:** Supportato in Microsoft Rich Edit 1,0 e versioni successive. Usare il messaggio [**em \_ EXLIMITTEXT**](em-exlimittext.md) per i valori di lunghezza del testo maggiori di 64.000. Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**\_EXLIMITTEXT em**](em-exlimittext.md)
</dt> <dt>

[**Modifica \_ LimitText**](/windows/desktop/api/Windowsx/nf-windowsx-edit_limittext)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**\_testo WM**](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

