---
title: Messaggio BM_GETCHECK (winuser. h)
description: Ottiene lo stato di selezione di un pulsante di opzione o di una casella di controllo. È possibile inviare questo messaggio in modo esplicito o usare la macro del pulsante \_ GetCheck.
ms.assetid: a25b2c8d-0b32-4807-bfb4-e277675924f1
keywords:
- Controlli di Windows Message BM_GETCHECK
topic_type:
- apiref
api_name:
- BM_GETCHECK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f1aa89dc256ea9e0036259239d1c74e1e82b272
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121163"
---
# <a name="bm_getcheck-message"></a>\_Messaggio BM GETcheck

Ottiene lo stato di selezione di un pulsante di opzione o di una casella di controllo. È possibile inviare questo messaggio in modo esplicito o usare la macro del [**pulsante \_ GetCheck**](/windows/desktop/api/Windowsx/nf-windowsx-button_getcheck) .

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

Il valore restituito da un pulsante creato con le [**caselle di controllo \_ AUTOCHECKBOX**](button-styles.md)BS, [**BS \_ AUTORADIOBUTTON**](button-styles.md), [**BS \_ AUTO3STATE**](button-styles.md), BS [**\_ CheckBox**](button-styles.md), [**BS \_ RadioButton**](button-styles.md)o [**BS \_ 3STATE**](button-styles.md) può essere uno dei seguenti.



| Codice restituito                                                                                       | Descrizione                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_controllo BST**</dt> </dl>       | Pulsante selezionato.<br/>                                                                                                                                                                                     |
| <dl> <dt>**BST \_ INdeterminato**</dt> </dl> | Il pulsante è visualizzato in grigio, che indica uno stato indeterminato (si applica solo se il pulsante ha lo stile [**BS \_ 3STATE**](button-styles.md) o [**BS \_ AUTO3STATE**](button-styles.md) ).<br/> |
| <dl> <dt>**BST \_ DEselezionata**</dt> </dl>     | Il pulsante è deselezionato<br/>                                                                                                                                                                                      |



 

## <a name="remarks"></a>Commenti

Se il pulsante presenta uno stile diverso da quelli elencati, il valore restituito è zero.

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

[**BM \_ GETstate**](bm-getstate.md)
</dt> <dt>

[**\_controllo BM**](bm-setcheck.md)
</dt> </dl>

 

 





