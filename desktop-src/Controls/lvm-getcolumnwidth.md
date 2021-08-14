---
title: LVM_GETCOLUMNWIDTH messaggio (Commctrl.h)
description: Ottiene la larghezza di una colonna nella visualizzazione report o elenco. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro ListView GetColumnWidth.
ms.assetid: 06e8ec36-3bc5-4516-ac29-17c36fb6d962
keywords:
- LVM_GETCOLUMNWIDTH del messaggio Windows controlli
topic_type:
- apiref
api_name:
- LVM_GETCOLUMNWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 800ab7172ec489b84506cc55a342325527f38e447fc2bae635c2e5688a142b25
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118411507"
---
# <a name="lvm_getcolumnwidth-message"></a>Messaggio LVM \_ GETCOLUMNWIDTH

Ottiene la larghezza di una colonna nella visualizzazione report o elenco. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ ListView GetColumnWidth.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumnwidth)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice della colonna. Questo parametro viene ignorato nella visualizzazione elenco.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce la larghezza della colonna in caso di esito positivo oppure zero in caso contrario. Se questo messaggio viene inviato a un controllo visualizzazione elenco con lo stile [**\_ LVS REPORT**](list-view-window-styles.md) e la colonna specificata non esiste, il valore restituito non è definito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





