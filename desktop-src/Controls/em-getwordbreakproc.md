---
title: Messaggio EM_GETWORDBREAKPROC (winuser. h)
description: Ottiene l'indirizzo della funzione WordWrap corrente. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.
ms.assetid: 564b4b1b-913f-4040-bb28-eea50c0c3738
keywords:
- Controlli di Windows Message EM_GETWORDBREAKPROC
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
ms.openlocfilehash: feb9499492668abac24774b66304ae8a87a2d739
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478107"
---
# <a name="em_getwordbreakproc-message"></a>\_Messaggio GETWORDBREAKPROC em

Ottiene l'indirizzo della funzione WordWrap corrente. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.

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

Il valore restituito specifica l'indirizzo della funzione WordWrap definita dall'applicazione. Il valore restituito è **null** se non esiste alcuna funzione WordWrap.

## <a name="remarks"></a>Commenti

Una funzione WordWrap analizza un buffer di testo contenente il testo da inviare alla visualizzazione, cercando la prima parola che non rientra nella riga di visualizzazione corrente. La funzione WordWrap posiziona questa parola all'inizio della riga successiva sullo schermo. Una funzione WordWrap definisce il punto in cui il sistema deve suddividere una riga di testo per i controlli di modifica su più righe, in genere in un carattere spazio che separa due parole.

**Modifica avanzata:** Supportato in Microsoft Rich Edit 1,0 e versioni successive. Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).

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

[*EditWordBreakProc*](/windows/win32/api/winuser/nc-winuser-editwordbreakproca)
</dt> <dt>

[**\_FMTLINES em**](em-fmtlines.md)
</dt> <dt>

[**\_SETWORDBREAKPROC em**](em-setwordbreakproc.md)
</dt> </dl>

 

