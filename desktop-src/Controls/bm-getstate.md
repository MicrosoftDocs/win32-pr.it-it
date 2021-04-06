---
title: Messaggio BM_GETSTATE (winuser. h)
description: Recupera lo stato di un pulsante o di una casella di controllo. È possibile inviare questo messaggio in modo esplicito o usare il pulsante \_ GetState macro.
ms.assetid: ca4c2f1a-b657-490a-ac8b-5f0cfef64d76
keywords:
- Controlli di Windows Message BM_GETSTATE
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
ms.openlocfilehash: a3b5e69f067acfc13cd8661be8a585fcfc8e6fe4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963813"
---
# <a name="bm_getstate-message"></a>\_Messaggio BM GETstate

Recupera lo stato di un pulsante o di una casella di controllo. È possibile inviare questo messaggio in modo esplicito o usare il [**pulsante \_ GetState**](/windows/desktop/api/Windowsx/nf-windowsx-button_getstate) macro.

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

Il valore restituito specifica lo stato corrente del pulsante. Si tratta di una combinazione dei valori seguenti.



| Codice restituito                                                                                        | Descrizione                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_controllo BST**</dt> </dl>        | Il pulsante è selezionato.<br/>                                                                                                                                                                                        |
| <dl> <dt>**\_DROPDOWNPUSHED BST**</dt> </dl> | [Windows Vista](common-control-versions.md). Il pulsante si trova nello stato a discesa. Si applica solo se il pulsante ha lo stile a [**\_ discesa TBSTYLE**](toolbar-control-and-button-styles.md) .<br/> |
| <dl> <dt>**\_stato attivo BST**</dt> </dl>          | Il pulsante ha lo stato attivo della tastiera.<br/>                                                                                                                                                                            |
| <dl> <dt>**BST \_ attivo**</dt> </dl>            | Il pulsante è attivo; ovvero il puntatore del mouse viene spostato su di esso.<br/>                                                                                                                                                    |
| <dl> <dt>**BST \_ INdeterminato**</dt> </dl>  | Lo stato del pulsante è indeterminato. Si applica solo se il pulsante ha lo stile [**BS \_ 3STATE**](button-styles.md) o [**BS \_ AUTO3STATE**](button-styles.md) .<br/>                    |
| <dl> <dt>**BST \_ push**</dt> </dl>         | Il pulsante viene visualizzato nello stato push.<br/>                                                                                                                                                                |
| <dl> <dt>**BST \_ DEselezionata**</dt> </dl>      | Nessuno stato speciale. Equivalente a zero.<br/>                                                                                                                                                                         |



 

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

[**GetCheck BM \_**](bm-getcheck.md)
</dt> <dt>

[**STATO di BM \_**](bm-setstate.md)
</dt> </dl>

 

 





