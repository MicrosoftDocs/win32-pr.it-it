---
title: Messaggio BM_SETCHECK (winuser. h)
description: Imposta lo stato di selezione di un pulsante di opzione o di una casella di controllo. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro di controllo Button.
ms.assetid: 8294e6c4-caac-4c60-85ff-38698a1d2ae4
keywords:
- Controlli di Windows Message BM_SETCHECK
topic_type:
- apiref
api_name:
- BM_SETCHECK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c298fb865fe34946bfedc9f1d6d1924f6d32202
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047944"
---
# <a name="bm_setcheck-message"></a>Messaggio BM ( \_ SEcheck)

Imposta lo stato di selezione di un pulsante di opzione o di una casella di controllo. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro di [**\_ controllo Button**](/windows/desktop/api/Windowsx/nf-windowsx-button_setcheck) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Stato di selezione. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                     | Significato                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BST_CHECKED"></span><span id="bst_checked"></span><dl> <dt>**\_controllo BST**</dt> </dl>                   | Imposta lo stato del pulsante su controllato.<br/>                                                                                                                                                                                           |
| <span id="BST_INDETERMINATE"></span><span id="bst_indeterminate"></span><dl> <dt>**BST \_ INdeterminato**</dt> </dl> | Imposta lo stato del pulsante su grigio, che indica uno stato indeterminato. Usare questo valore solo se il pulsante ha lo stile [**BS \_ 3STATE**](button-styles.md) o [**BS \_ AUTO3STATE**](button-styles.md) .<br/> |
| <span id="BST_UNCHECKED"></span><span id="bst_unchecked"></span><dl> <dt>**BST \_ DEselezionata**</dt> </dl>             | Imposta lo stato del pulsante su deselezionato.<br/>                                                                                                                                                                                           |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio restituisce sempre zero.

## <a name="remarks"></a>Commenti

Il messaggio **BM \_ secheck** non ha alcun effetto sui pulsanti di push.

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

[**BM \_ GETstate**](bm-getstate.md)
</dt> <dt>

[**STATO di BM \_**](bm-setstate.md)
</dt> </dl>

 

 





