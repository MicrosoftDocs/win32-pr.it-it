---
title: LVM_HITTEST messaggio (Commctrl.h)
description: Determina quale elemento della visualizzazione elenco, se presente, si trova in una posizione specificata. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro ListView HitTest.
ms.assetid: 81df4ed1-30bd-4b63-9cb9-5163cb7cf52c
keywords:
- LVM_HITTEST controlli Windows messaggio
topic_type:
- apiref
api_name:
- LVM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81308249992b134dd3fa2bd0bc43ff0074bc3bae7048072ada7d68b0a867a979
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958170"
---
# <a name="lvm_hittest-message"></a>Messaggio LVM \_ HITTEST

Determina quale elemento della visualizzazione elenco, se presente, si trova in una posizione specificata. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ ListView HitTest.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_hittest)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere 0. **Windows Vista.** Deve essere -1 se i **membri iGroup** e **iSubItem** della struttura *lParam* devono essere recuperati.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) che contiene la posizione in cui eseguire l'hit test e riceve informazioni sui risultati dell'hit test.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'indice dell'elemento nella posizione specificata, se presente, oppure -1 in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





