---
title: Messaggio EM_SCROLL (winuser. h)
description: Scorre il testo verticalmente in un controllo di modifica su più righe. Questo messaggio equivale all'invio \_ di un messaggio WM VSCROLL al controllo di modifica. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.
ms.assetid: 616b5ac2-d92f-4fc5-9a9e-2c7527fb0d97
keywords:
- Controlli di Windows Message EM_SCROLL
topic_type:
- apiref
api_name:
- EM_SCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09eb185fb14ef866ab0e7ea8c8064445193347d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121495"
---
# <a name="em_scroll-message"></a>\_Messaggio di scorrimento em

Scorre il testo verticalmente in un controllo di modifica su più righe. Questo messaggio equivale all'invio di un messaggio [**WM \_ VSCROLL**](wm-vscroll.md) al controllo di modifica. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Azione da eseguire sulla barra di scorrimento. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                   | Significato                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="SB_LINEDOWN"></span><span id="sb_linedown"></span><dl> <dt>**\_LINEDOWN SB**</dt> </dl> | Scorre verso il basso di una riga.<br/> |
| <span id="SB_LINEUP"></span><span id="sb_lineup"></span><dl> <dt>**\_lineup SB**</dt> </dl>       | Scorre verso l'alto di una riga.<br/>   |
| <span id="SB_PAGEDOWN"></span><span id="sb_pagedown"></span><dl> <dt>**\_PGGIÙ SB**</dt> </dl> | Scorre verso il basso di una pagina.<br/> |
| <span id="SB_PAGEUP"></span><span id="sb_pageup"></span><dl> <dt>**\_PAGEUP SB**</dt> </dl>       | Scorre verso l'alto di una pagina.<br/>   |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il messaggio ha esito positivo, [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) del valore restituito è **true** e [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) è il numero di righe Scorrete dal comando. Il numero restituito potrebbe non corrispondere al numero effettivo di righe a scorrimento se lo scorrimento si sposta all'inizio o alla fine del testo. Se il parametro *wParam* specifica un valore non valido, il valore restituito è **false**.

## <a name="remarks"></a>Commenti

Per scorrere fino a una riga o a una posizione specifica del carattere, usare il messaggio [**\_ LINESCROLL em**](em-linescroll.md) . Per scorrere il punto di inserimento nella visualizzazione, usare il messaggio [**\_ SCROLLCARET em**](em-scrollcaret.md) .

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

[**\_LINESCROLL em**](em-linescroll.md)
</dt> <dt>

[**\_SCROLLCARET em**](em-scrollcaret.md)
</dt> <dt>

[**\_VSCROLL WM**](wm-vscroll.md)
</dt> </dl>

 

