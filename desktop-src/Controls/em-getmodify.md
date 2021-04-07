---
title: Messaggio EM_GETMODIFY (winuser. h)
description: Ottiene lo stato del flag di modifica del controllo di modifica. Il flag indica se il contenuto del controllo di modifica è stato modificato. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.
ms.assetid: 4229e2f2-3493-4721-8b52-8933c9dc0a77
keywords:
- Controlli di Windows Message EM_GETMODIFY
topic_type:
- apiref
api_name:
- EM_GETMODIFY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f8c525df061717255051c49abaa3bda88f317b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873433"
---
# <a name="em_getmodify-message"></a>\_Messaggio GETMODIFY em

Ottiene lo stato del flag di modifica del controllo di modifica. Il flag indica se il contenuto del controllo di modifica è stato modificato. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.

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

Se il contenuto del controllo di modifica è stato modificato, il valore restituito è diverso da zero; in caso contrario, è zero.

## <a name="remarks"></a>Commenti

Il sistema cancella automaticamente il flag di modifica a zero quando viene creato il controllo. Se l'utente modifica il testo del controllo, il sistema imposta il flag su un valore diverso da zero. Per impostare o deselezionare il flag, è possibile inviare il messaggio di modifica [**em \_**](em-setmodify.md) per il controllo di modifica.

**Modifica avanzata:** Supportato in Microsoft Rich Edit 1,0 e versioni successive. Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MODIFICA di EM \_**](em-setmodify.md)
</dt> </dl>

 

 





