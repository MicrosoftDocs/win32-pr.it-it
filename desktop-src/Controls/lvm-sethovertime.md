---
title: Messaggio LVM_SETHOVERTIME (COMmctrl. h)
description: Imposta la quantità di tempo per cui il cursore del mouse deve passare il puntatore del mouse su un elemento prima che sia selezionato. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro SetHoverTime di ListView.
ms.assetid: 454fbc38-f7fd-4dea-b223-56003b88528f
keywords:
- Controlli di Windows Message LVM_SETHOVERTIME
topic_type:
- apiref
api_name:
- LVM_SETHOVERTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3aecd3c0d48cddc2cbaae49e7e888f91a985575
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104118991"
---
# <a name="lvm_sethovertime-message"></a>\_Messaggio SETHOVERTIME LVM

Imposta la quantità di tempo per cui il cursore del mouse deve passare il puntatore del mouse su un elemento prima che sia selezionato. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ SetHoverTime di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethovertime) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

La nuova quantità di tempo, in millisecondi, in base alla quale il cursore del mouse deve passare il puntatore del mouse su un elemento prima che sia selezionato. Se questo valore è (**DWORD**)-1, l'ora del passaggio del mouse viene impostata sull'ora del passaggio del mouse predefinita.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'ora precedente del passaggio del mouse.

## <a name="remarks"></a>Commenti

L'ora del passaggio del mouse influiscono solo sui controlli visualizzazione elenco con lo stile di visualizzazione elenco esteso [**LVS ex \_ \_ TRACKSELECT**](extended-list-view-styles.md), [**LVS \_ ex \_ ONECLICKACTIVATE**](extended-list-view-styles.md)o [**LVS \_ ex \_ TWOCLICKACTIVATE**](extended-list-view-styles.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





