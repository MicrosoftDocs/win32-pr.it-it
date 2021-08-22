---
title: BM_GETSTATE messaggio (Winuser.h)
description: Recupera lo stato di un pulsante o di una casella di controllo. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro Button GetState.
ms.assetid: ca4c2f1a-b657-490a-ac8b-5f0cfef64d76
keywords:
- BM_GETSTATE controlli Windows messaggio
topic_type:
- apiref
api_name:
- BM_GETSTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd44921c61477e26cd5570fcbaa6f96a4e61f96ee22ad1c705bf553788d8cfba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118674841"
---
# <a name="bm_getstate-message"></a>Messaggio \_ GETSTATE BM

Recupera lo stato di un pulsante o di una casella di controllo. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ Button GetState.**](/windows/desktop/api/Windowsx/nf-windowsx-button_getstate)

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

Il valore restituito specifica lo stato corrente del pulsante. È una combinazione dei valori seguenti.



| Codice restituito                                                                                        | Descrizione                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**BST \_ CHECKED**</dt> </dl>        | Il pulsante è selezionato.<br/>                                                                                                                                                                                        |
| <dl> <dt>**ELENCO A \_ DISCESA BSTPUSHED**</dt> </dl> | [Windows Vista](common-control-versions.md). Il pulsante si trova nello stato a discesa. Si applica solo se il pulsante ha lo stile [**TBSTYLE \_ DROPDOWN.**](toolbar-control-and-button-styles.md)<br/> |
| <dl> <dt>**BST \_ FOCUS**</dt> </dl>          | Il pulsante ha lo stato attivo della tastiera.<br/>                                                                                                                                                                            |
| <dl> <dt>**BST \_ HOT**</dt> </dl>            | Il pulsante è di tipo hot; ciò significa che il puntatore del mouse è posizionato su di esso.<br/>                                                                                                                                                    |
| <dl> <dt>**BST \_ INDETERMINATO**</dt> </dl>  | Lo stato del pulsante è indeterminato. Si applica solo se il pulsante ha lo [**stile BS \_ 3STATE**](button-styles.md) o [**BS \_ AUTO3STATE.**](button-styles.md)<br/>                    |
| <dl> <dt>**BST \_ PUSH**</dt> </dl>         | Il pulsante viene visualizzato nello stato di push.<br/>                                                                                                                                                                |
| <dl> <dt>**BST \_ UNCHECKED**</dt> </dl>      | Nessuno stato speciale. Equivalente a zero.<br/>                                                                                                                                                                         |



 

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

[**BM \_ GETCHECK**](bm-getcheck.md)
</dt> <dt>

[**BM \_ SETSTATE**](bm-setstate.md)
</dt> </dl>

 

 





