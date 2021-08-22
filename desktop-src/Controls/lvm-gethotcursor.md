---
title: LVM_GETHOTCURSOR messaggio (Commctrl.h)
description: Recupera il valore HCURSOR utilizzato quando il puntatore si trova su un elemento mentre è abilitato il rilevamento a caldo. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro ListView GetHotCursor.
ms.assetid: 064d04b2-d74e-4a80-aec6-97a3c53fc4fb
keywords:
- LVM_GETHOTCURSOR di controllo Windows messaggio
topic_type:
- apiref
api_name:
- LVM_GETHOTCURSOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e5703d252d239124b78656c4a5991efdecb2107552fb6e2ab0f87701af4e18d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540801"
---
# <a name="lvm_gethotcursor-message"></a>Messaggio \_ LVM GETHOTCURSOR

Recupera il valore HCURSOR utilizzato quando il puntatore si trova su un elemento mentre è abilitato il rilevamento a caldo. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ ListView GetHotCursor.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gethotcursor)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore HCURSOR che rappresenta l'handle per il cursore utilizzato dal controllo visualizzazione elenco quando è abilitato il rilevamento dello stato attivo.

## <a name="remarks"></a>Commenti

Un controllo visualizzazione elenco usa il rilevamento dell'accesso a caldo e la selezione al passaggio del mouse quando è impostato lo stile [**\_ \_ TRACKSELECT di LVS EX.**](extended-list-view-styles.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





