---
title: Messaggio LVM_GETHOVERTIME (COMmctrl. h)
description: Recupera la quantità di tempo per cui il cursore del mouse deve passare il puntatore del mouse su un elemento prima che sia selezionato. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro GetHoverTime di ListView.
ms.assetid: e7646024-f868-459f-88be-b232b6b4bb2a
keywords:
- Controlli di Windows Message LVM_GETHOVERTIME
topic_type:
- apiref
api_name:
- LVM_GETHOVERTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83e243ece42f06ffe35eb31954d9ca0dd44957be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477573"
---
# <a name="lvm_gethovertime-message"></a>\_Messaggio GETHOVERTIME LVM

Recupera la quantità di tempo per cui il cursore del mouse deve passare il puntatore del mouse su un elemento prima che sia selezionato. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ GetHoverTime di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gethovertime) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce la quantità di tempo, in millisecondi, per cui il cursore del mouse deve passare il puntatore del mouse su un elemento prima che sia selezionato. Se il valore restituito è (**DWORD**)-1, l'ora del passaggio del mouse corrisponde al valore predefinito del passaggio del mouse.

## <a name="remarks"></a>Commenti

L'ora del passaggio del mouse influiscono solo sui controlli visualizzazione elenco con lo stile di visualizzazione elenco esteso [**LVS ex \_ \_ TRACKSELECT**](extended-list-view-styles.md), [**LVS \_ ex \_ ONECLICKACTIVATE**](extended-list-view-styles.md)o [**LVS \_ ex \_ TWOCLICKACTIVATE**](extended-list-view-styles.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





