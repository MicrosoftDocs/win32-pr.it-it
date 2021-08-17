---
title: EM_GETWORDBREAKPROC messaggio (Winuser.h)
description: Ottiene l'indirizzo della funzione Wordwrap corrente. È possibile inviare questo messaggio a un controllo di modifica o a un controllo Rich Edit.
ms.assetid: 564b4b1b-913f-4040-bb28-eea50c0c3738
keywords:
- EM_GETWORDBREAKPROC controlli Windows messaggio
topic_type:
- apiref
api_name:
- EM_GETWORDBREAKPROC
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f615721328ce0062d6bba9c282466744e7b47c78ad335b905343893f9c1b6343
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119438061"
---
# <a name="em_getwordbreakproc-message"></a>Messaggio \_ EM GETWORDBREAKPROC

Ottiene l'indirizzo della funzione Wordwrap corrente. È possibile inviare questo messaggio a un controllo di modifica o a un controllo Rich Edit.

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

Il valore restituito specifica l'indirizzo della funzione Wordwrap definita dall'applicazione. Il valore restituito è **NULL** se non esiste alcuna funzione Wordwrap.

## <a name="remarks"></a>Commenti

Una funzione Wordwrap analizza un buffer di testo che contiene il testo da inviare alla visualizzazione, cercando la prima parola che non rientra nella riga di visualizzazione corrente. La funzione wordwrap inserisce questa parola all'inizio della riga successiva sullo schermo. Una funzione Wordwrap definisce il punto in cui il sistema deve interrompere una riga di testo per i controlli di modifica su più righe, in genere in corrispondenza di uno spazio che separa due parole.

**Rich Edit:** Supportato in Microsoft Rich Edit 1.0 e versioni successive. Per informazioni sulla compatibilità delle versioni rich edit con le varie versioni di sistema, vedere [Informazioni sui controlli Rich Edit.](about-rich-edit-controls.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[*EditWordBreakProc*](/windows/win32/api/winuser/nc-winuser-editwordbreakproca)
</dt> <dt>

[**EM \_ FMTLINES**](em-fmtlines.md)
</dt> <dt>

[**EM \_ SETWORDBREAKPROC**](em-setwordbreakproc.md)
</dt> </dl>

 

