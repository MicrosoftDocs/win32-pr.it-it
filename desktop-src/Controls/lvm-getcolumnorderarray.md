---
title: Messaggio LVM_GETCOLUMNORDERARRAY (COMmctrl. h)
description: Ottiene l'ordine da sinistra a destra corrente delle colonne in un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro GetColumnOrderArray di ListView.
ms.assetid: d4636aa8-c61e-4467-abc7-eea897bf370e
keywords:
- Controlli di Windows Message LVM_GETCOLUMNORDERARRAY
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
ms.openlocfilehash: aee387f65abd3f30826e361778d5acac02dfab7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047863"
---
# <a name="lvm_getcolumnorderarray-message"></a>\_Messaggio GETCOLUMNORDERARRAY LVM

Ottiene l'ordine da sinistra a destra corrente delle colonne in un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ GetColumnOrderArray di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumnorderarray) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Numero di colonne nel controllo visualizzazione elenco.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una matrice di numeri interi che riceve i valori di indice delle colonne nel controllo visualizzazione elenco. La matrice deve essere sufficientemente grande da contenere gli elementi *wParam* .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

In caso di esito positivo, restituisce un valore diverso da zero e il buffer in *lParam* riceve l'indice di colonna di ogni colonna nel controllo nell'ordine in cui appaiono da sinistra a destra. In caso contrario, il valore restituito è zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





