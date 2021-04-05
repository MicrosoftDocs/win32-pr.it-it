---
title: Messaggio EM_GETTHUMB (winuser. h)
description: Ottiene la posizione della casella di scorrimento (Thumb) nella barra di scorrimento verticale di un controllo di modifica su più righe. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.
ms.assetid: 04bd0102-1652-405b-8c42-50e138abaf75
keywords:
- Controlli di Windows Message EM_GETTHUMB
topic_type:
- apiref
api_name:
- EM_GETTHUMB
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e6689c530794e11897f1f88a7d5864058d53aa8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120726"
---
# <a name="em_getthumb-message"></a>\_Messaggio GETTHUMB em

Ottiene la posizione della casella di scorrimento (Thumb) nella barra di scorrimento verticale di un controllo di modifica su più righe. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.

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

Il valore restituito è la posizione della casella di scorrimento.

## <a name="remarks"></a>Commenti

**Modifica avanzata:** Supportato in Microsoft Rich Edit 2,0 e versioni successive. Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



 

 





