---
title: BM_GETCHECK messaggio (Winuser.h)
description: Ottiene lo stato di controllo di un pulsante di opzione o di una casella di controllo. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro Button GetCheck.
ms.assetid: a25b2c8d-0b32-4807-bfb4-e277675924f1
keywords:
- BM_GETCHECK dei controlli Windows messaggio
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
ms.openlocfilehash: e5eb87d98752bd0cd447d48c648bc4a55e93c3f8eb418a81a07e04113a86633a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921291"
---
# <a name="bm_getcheck-message"></a>Messaggio \_ GETCHECK BM

Ottiene lo stato di controllo di un pulsante di opzione o di una casella di controllo. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ Button GetCheck.**](/windows/desktop/api/Windowsx/nf-windowsx-button_getcheck)

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

Il valore restituito da un pulsante creato con lo stile [**BS \_ AUTOCHECKBOX**](button-styles.md), [**BS \_ AUTORADIOBUTTON**](button-styles.md), [**BS \_ AUTO3STATE**](button-styles.md), [**BS \_ CHECKBOX,**](button-styles.md) [**BS \_ RADIOBUTTON**](button-styles.md)o [**BS \_ 3STATE**](button-styles.md) può essere uno dei seguenti.



| Codice restituito                                                                                       | Descrizione                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**BST \_ CHECKED**</dt> </dl>       | Il pulsante è selezionato.<br/>                                                                                                                                                                                     |
| <dl> <dt>**BST \_ INDETERMINATO**</dt> </dl> | Il pulsante è in grigio, a indicare uno stato indeterminato (si applica solo se il pulsante ha lo stile [**BS \_ 3STATE**](button-styles.md) o [**BS \_ AUTO3STATE).**](button-styles.md)<br/> |
| <dl> <dt>**BST \_ UNCHECKED**</dt> </dl>     | Il pulsante è deselezionato<br/>                                                                                                                                                                                      |



 

## <a name="remarks"></a>Commenti

Se il pulsante ha uno stile diverso da quelli elencati, il valore restituito è zero.

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

[**BM \_ GETSTATE**](bm-getstate.md)
</dt> <dt>

[**BM \_ SETCHECK**](bm-setcheck.md)
</dt> </dl>

 

 





