---
title: LVM_GETHOVERTIME messaggio (Commctrl.h)
description: Recupera l'intervallo di tempo durante il quale il cursore del mouse deve passare il puntatore del mouse su un elemento prima di essere selezionato. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro ListView GetHoverTime.
ms.assetid: e7646024-f868-459f-88be-b232b6b4bb2a
keywords:
- LVM_GETHOVERTIME dei messaggi Windows controlli
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
ms.openlocfilehash: 150a8eff54f8b3c27f0e7783ceda67af60c326e370d1a518d83e6bdd214fb529
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119920101"
---
# <a name="lvm_gethovertime-message"></a>Messaggio \_ LVM GETHOVERTIME

Recupera l'intervallo di tempo durante il quale il cursore del mouse deve passare il puntatore del mouse su un elemento prima di essere selezionato. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ ListView GetHoverTime.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gethovertime)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce la quantità di tempo, in millisecondi, per cui il cursore del mouse deve passare il mouse su un elemento prima di essere selezionato. Se il valore restituito è (**DWORD**)-1, l'ora del passaggio del mouse è l'ora predefinita del passaggio del mouse.

## <a name="remarks"></a>Commenti

L'ora del passaggio del mouse influisce solo sui controlli visualizzazione elenco con lo stile di visualizzazione elenco esteso [**LVS \_ EX \_ TRACKSELECT,**](extended-list-view-styles.md) [**LVS \_ EX \_ ONECLICKACTIVATE**](extended-list-view-styles.md)o [**LVS EX \_ \_ TWOCLICKACTIVATE.**](extended-list-view-styles.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





