---
title: LVM_SETHOTCURSOR messaggio (Commctrl.h)
description: Imposta il valore HCURSOR utilizzato dal controllo visualizzazione elenco quando il puntatore si trova su un elemento mentre è abilitato il rilevamento a caldo.
ms.assetid: e3ff8608-9389-4167-839b-ecc2be01bb64
keywords:
- LVM_SETHOTCURSOR di controllo Windows messaggio
topic_type:
- apiref
api_name:
- LVM_SETHOTCURSOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3407c5d8b53483d3a639fc40959768b3fa8eea0e7b439ab8871d36346b7079d0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077251"
---
# <a name="lvm_sethotcursor-message"></a>Messaggio LVM \_ SETHOTCURSOR

Imposta il valore HCURSOR utilizzato dal controllo visualizzazione elenco quando il puntatore si trova su un elemento mentre è abilitato il rilevamento a caldo. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ ListView SetHotCursor.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethotcursor) Per verificare se il rilevamento a caldo è abilitato, chiamare [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa).

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Handle per il cursore da impostare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore HCURSOR che rappresenta il cursore a caldo precedente.

## <a name="remarks"></a>Commenti

Un controllo visualizzazione elenco usa il rilevamento a caldo e la selezione al passaggio del mouse quando è impostato lo stile [**LVS \_ EX \_ TRACKSELECT.**](extended-list-view-styles.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

