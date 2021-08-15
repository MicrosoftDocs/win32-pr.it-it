---
title: LVM_GETCOLUMN messaggio (Commctrl.h)
description: Ottiene gli attributi della colonna di un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro ListView GetColumn.
ms.assetid: 59b4bbfc-6c38-4faa-8f2e-3ea5d24e55a6
keywords:
- LVM_GETCOLUMN dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- LVM_GETCOLUMN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b65478d1d249740c630499fd4837e31d4eba7b992cf3ef3682c4e7b72d0706cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118411737"
---
# <a name="lvm_getcolumn-message"></a>Messaggio \_ LVM GETCOLUMN

Ottiene gli attributi della colonna di un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ ListView GetColumn.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumn)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice della colonna.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) che specifica le informazioni da recuperare e riceve informazioni sulla colonna. Il **membro mask** specifica gli attributi di colonna da recuperare. Se il membro **mask** specifica il valore LVCF TEXT, il membro pszText deve contenere l'indirizzo del buffer che riceve il testo dell'elemento e il membro \_  **cchTextMax** deve specificare le dimensioni del buffer.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo oppure FALSE **in** caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





