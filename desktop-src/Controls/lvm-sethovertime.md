---
title: LVM_SETHOVERTIME messaggio (Commctrl.h)
description: Imposta l'intervallo di tempo durante il quale il cursore del mouse deve passare il puntatore del mouse su un elemento prima che venga selezionato. Puoi inviare questo messaggio in modo esplicito o usare la \_ macro ListView SetHoverTime.
ms.assetid: 454fbc38-f7fd-4dea-b223-56003b88528f
keywords:
- LVM_SETHOVERTIME controlli Windows messaggio
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
ms.openlocfilehash: 8f93edf917dc50384f3a09f7eadf013561715735a995c63a695cb8f9ad91dbce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077231"
---
# <a name="lvm_sethovertime-message"></a>Messaggio LVM \_ SETHOVERTIME

Imposta l'intervallo di tempo durante il quale il cursore del mouse deve passare il puntatore del mouse su un elemento prima che venga selezionato. Puoi inviare questo messaggio in modo esplicito o usare la macro [**\_ ListView SetHoverTime.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethovertime)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Nuova quantità di tempo, in millisecondi, per cui il cursore del mouse deve passare il puntatore del mouse su un elemento prima che venga selezionato. Se questo valore è (**DWORD**)-1, l'ora del passaggio del mouse viene impostata sull'ora predefinita del passaggio del mouse.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'ora precedente al passaggio del mouse.

## <a name="remarks"></a>Commenti

L'ora del passaggio del mouse influisce solo sui controlli di visualizzazione elenco con lo stile di visualizzazione elenco esteso [**LVS \_ EX \_ TRACKSELECT,**](extended-list-view-styles.md) [**LVS \_ EX \_ ONECLICKACTIVATE**](extended-list-view-styles.md)o [**LVS EX \_ \_ TWOCLICKACTIVATE.**](extended-list-view-styles.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





