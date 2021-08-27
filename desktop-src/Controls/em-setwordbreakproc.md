---
title: EM_SETWORDBREAKPROC messaggio (Winuser.h)
description: Sostituisce la funzione Wordwrap predefinita di un controllo di modifica con una funzione Wordwrap definita dall'applicazione. È possibile inviare questo messaggio a un controllo di modifica o a un controllo Rich Edit.
ms.assetid: e5029b75-5f35-43a5-876d-24e81605bb49
keywords:
- EM_SETWORDBREAKPROC di controllo Windows messaggio
topic_type:
- apiref
api_name:
- EM_SETWORDBREAKPROC
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90617545fab7c8c5cf75babd98e9d6ef85c5713778c52a6a00966a131d0a0581
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048021"
---
# <a name="em_setwordbreakproc-message"></a>Messaggio EM \_ SETWORDBREAKPROC

Sostituisce la funzione Wordwrap predefinita di un controllo di modifica con una funzione Wordwrap definita dall'applicazione. È possibile inviare questo messaggio a un controllo di modifica o a un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> <dt>

*lParam* 
</dt> <dd>

Indirizzo della funzione Wordwrap definita dall'applicazione. Per altre informazioni sulle righe che causano un'interruzione, vedere la descrizione della funzione di callback [*EditWordBreakProc.*](/windows/win32/api/winuser/nc-winuser-editwordbreakproca)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce un valore.

## <a name="remarks"></a>Commenti

Una funzione Wordwrap analizza un buffer di testo che contiene il testo da inviare alla schermata, cercando la prima parola che non rientra nella riga corrente dello schermo. La funzione Wordwrap inserisce questa parola all'inizio della riga successiva sullo schermo.

Una funzione Wordwrap definisce il punto in cui il sistema deve interrompere una riga di testo per i controlli di modifica su più righe, in genere in corrispondenza di uno spazio che separa due parole. Un controllo di modifica su più righe o su una sola riga potrebbe chiamare questa funzione quando l'utente preme i tasti di direzione in combinazione con il tasto CTRL per spostare il cursore sulla parola successiva o sulla parola precedente. La funzione Wordwrap predefinita interrompe una riga di testo in corrispondenza di uno spazio. La funzione definita dall'applicazione può definire il wordwrap in modo che si verifichi in corrispondenza di un trattino o di un carattere diverso dal carattere spazio.

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

[**EM \_ GETWORDBREAKPROC**](em-getwordbreakproc.md)
</dt> </dl>

 

