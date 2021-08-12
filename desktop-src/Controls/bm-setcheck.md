---
title: BM_SETCHECK messaggio (Winuser.h)
description: Imposta lo stato di controllo di un pulsante di opzione o di una casella di controllo. È possibile inviare questo messaggio in modo esplicito o tramite la \_ macro Button SetCheck.
ms.assetid: 8294e6c4-caac-4c60-85ff-38698a1d2ae4
keywords:
- BM_SETCHECK dei controlli Windows messaggio
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
ms.openlocfilehash: 171515cb3c8498537bd0f9cc6d8c06017ff9d5d00f5505e193862f6cf9ebff76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118674804"
---
# <a name="bm_setcheck-message"></a>Messaggio \_ SETCHECK BM

Imposta lo stato di controllo di un pulsante di opzione o di una casella di controllo. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**\_ Button SetCheck.**](/windows/desktop/api/Windowsx/nf-windowsx-button_setcheck)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Stato del controllo. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                     | Significato                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BST_CHECKED"></span><span id="bst_checked"></span><dl> <dt>**BST \_ CHECKED**</dt> </dl>                   | Imposta lo stato del pulsante su checked.<br/>                                                                                                                                                                                           |
| <span id="BST_INDETERMINATE"></span><span id="bst_indeterminate"></span><dl> <dt>**BST \_ INDETERMINATO**</dt> </dl> | Imposta lo stato del pulsante su disattivato, a indicare uno stato indeterminato. Usare questo valore solo se il pulsante ha lo [**stile BS \_ 3STATE**](button-styles.md) o [**BS \_ AUTO3STATE.**](button-styles.md)<br/> |
| <span id="BST_UNCHECKED"></span><span id="bst_unchecked"></span><dl> <dt>**BST \_ UNCHECKED**</dt> </dl>             | Imposta lo stato del pulsante su deselezionato.<br/>                                                                                                                                                                                           |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio restituisce sempre zero.

## <a name="remarks"></a>Commenti

Il **messaggio \_ BM SETCHECK** non ha effetto sui pulsanti di comando.

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

[**BM \_ GETSTATE**](bm-getstate.md)
</dt> <dt>

[**BM \_ SETSTATE**](bm-setstate.md)
</dt> </dl>

 

 





