---
title: LVM_GETCOLUMNORDERARRAY messaggio (Commctrl.h)
description: Ottiene l'ordine corrente da sinistra a destra delle colonne in un controllo di visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro ListView GetColumnOrderArray.
ms.assetid: d4636aa8-c61e-4467-abc7-eea897bf370e
keywords:
- LVM_GETCOLUMNORDERARRAY dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- LVM_GETCOLUMNORDERARRAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea54c633c7ffc9bc580609678e8ba5f62e29429aaea6f866bb7d72b6ea326eb2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118411497"
---
# <a name="lvm_getcolumnorderarray-message"></a>Messaggio LVM \_ GETCOLUMNORDERARRAY

Ottiene l'ordine corrente da sinistra a destra delle colonne in un controllo di visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ ListView GetColumnOrderArray.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumnorderarray)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Numero di colonne nel controllo visualizzazione elenco.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una matrice di interi che riceve i valori di indice delle colonne nel controllo visualizzazione elenco. La matrice deve essere sufficientemente grande da contenere *gli elementi wParam.*

</dd> </dl>

## <a name="return-value"></a>Valore restituito

In caso di esito positivo, restituisce un valore diverso da zero e il buffer in *lParam* riceve l'indice di colonna di ogni colonna nel controllo nell'ordine in cui vengono visualizzate da sinistra a destra. In caso contrario, il valore restituito è zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





