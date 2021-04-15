---
title: Messaggio WM_UNDO (winuser. h)
description: Un'applicazione invia un \_ messaggio di annullamento WM a un controllo di modifica per annullare l'ultima operazione. Quando questo messaggio viene inviato a un controllo di modifica, il testo eliminato in precedenza viene ripristinato o il testo aggiunto in precedenza viene eliminato.
ms.assetid: bb5a3425-bf99-4a08-8747-82c24c5889ad
keywords:
- Controlli di Windows Message WM_UNDO
topic_type:
- apiref
api_name:
- WM_UNDO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c5eb9182b6d8d3fc1360565f6661e989f3b6d0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477525"
---
# <a name="wm_undo-message"></a>\_Messaggio di annullamento WM

Un'applicazione invia un messaggio di **\_ annullamento WM** a un controllo di modifica per annullare l'ultima operazione. Quando questo messaggio viene inviato a un controllo di modifica, il testo eliminato in precedenza viene ripristinato o il testo aggiunto in precedenza viene eliminato.

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

Se il messaggio ha esito positivo, il valore restituito è **true**.

Se il messaggio ha esito negativo, il valore restituito è **false**.

## <a name="remarks"></a>Commenti

**Modifica avanzata:** È consigliabile usare l' [**\_ annullamento em**](em-undo.md) anziché **WM \_ Undo**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Altre risorse**
</dt> <dt>

[**chiaro di WM \_**](/windows/desktop/dataxchg/wm-clear)
</dt> <dt>

[**\_copia WM**](/windows/desktop/dataxchg/wm-copy)
</dt> <dt>

[**\_taglia WM**](/windows/desktop/dataxchg/wm-cut)
</dt> <dt>

[**\_Incolla WM**](/windows/desktop/dataxchg/wm-paste)
</dt> </dl>

 

