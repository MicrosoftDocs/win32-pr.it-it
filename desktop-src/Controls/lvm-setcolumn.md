---
title: LVM_SETCOLUMN messaggio (Commctrl.h)
description: Imposta gli attributi di una colonna di visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o tramite la \_ macro ListView SetColumn.
ms.assetid: 8ca1c269-fd86-4561-940d-b75f8ca2b731
keywords:
- LVM_SETCOLUMN dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- LVM_SETCOLUMN
- LVM_SETCOLUMNW
- LVM_SETCOLUMNW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cca00e62d941a753c70e0dd31c1af4003fe639d49503be7009fe5a010febf0c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019219"
---
# <a name="lvm_setcolumn-message"></a>Messaggio LVM \_ SETCOLUMN

Imposta gli attributi di una colonna di visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**\_ ListView SetColumn.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumn)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice della colonna.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) che contiene i nuovi attributi di colonna. Il **membro mask** specifica gli attributi di colonna da impostare. Se il **membro mask** specifica il valore LVCF TEXT, il membro pszText è l'indirizzo di una stringa con terminazione Null e il membro \_ **cchTextMax** viene ignorato. 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo oppure FALSE **in** caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **LVM \_ SETCOLUMNW** (Unicode) e **LVM \_ SETCOLUMNW** (ANSI)<br/>               |



 

 





