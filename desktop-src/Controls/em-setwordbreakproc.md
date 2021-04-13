---
title: Messaggio EM_SETWORDBREAKPROC (winuser. h)
description: Sostituisce la funzione WordWrap predefinita di un controllo di modifica con una funzione WordWrap definita dall'applicazione. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.
ms.assetid: e5029b75-5f35-43a5-876d-24e81605bb49
keywords:
- Controlli di Windows Message EM_SETWORDBREAKPROC
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
ms.openlocfilehash: e85335562c9e9881093d89293e7e2ace9cf43b0a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517974"
---
# <a name="em_setwordbreakproc-message"></a>\_Messaggio SETWORDBREAKPROC em

Sostituisce la funzione WordWrap predefinita di un controllo di modifica con una funzione WordWrap definita dall'applicazione. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> <dt>

*lParam* 
</dt> <dd>

Indirizzo della funzione WordWrap definita dall'applicazione. Per ulteriori informazioni sulle interruzioni delle righe, vedere la descrizione della funzione di callback [*EditWordBreakProc*](/windows/win32/api/winuser/nc-winuser-editwordbreakproca) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce alcun valore.

## <a name="remarks"></a>Commenti

Una funzione WordWrap analizza un buffer di testo contenente il testo da inviare allo schermo, cercando la prima parola che non rientra nella riga della schermata corrente. La funzione WordWrap posiziona questa parola all'inizio della riga successiva sullo schermo.

Una funzione WordWrap definisce il punto in cui il sistema deve suddividere una riga di testo per i controlli di modifica su più righe, in genere in un carattere spazio che separa due parole. Un controllo di modifica su più righe o su una sola riga potrebbe chiamare questa funzione quando l'utente preme i tasti di direzione in combinazione con il tasto CTRL per spostare il punto di inserimento alla parola successiva o alla parola precedente. La funzione WordWrap predefinita interrompe una riga di testo in un carattere spazio. La funzione definita dall'applicazione può definire WordWrap in modo che si verifichino a un trattino o a un carattere diverso dal carattere spazio.

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

[**\_GETWORDBREAKPROC em**](em-getwordbreakproc.md)
</dt> </dl>

 

