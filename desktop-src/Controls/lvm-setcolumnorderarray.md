---
title: LVM_SETCOLUMNORDERARRAY messaggio (Commctrl.h)
description: Imposta l'ordine da sinistra a destra delle colonne in un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro ListView SetColumnOrderArray.
ms.assetid: 9b491832-42cc-4262-8f6c-23cbc2c889bf
keywords:
- LVM_SETCOLUMNORDERARRAY di controllo Windows messaggio
topic_type:
- apiref
api_name:
- LVM_SETCOLUMNORDERARRAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9931a7d2c12da02f928c21727292d7d1ce4a430790660afb99ede4bf717c38c7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077301"
---
# <a name="lvm_setcolumnorderarray-message"></a>Messaggio LVM \_ SETCOLUMNORDERARRAY

Imposta l'ordine da sinistra a destra delle colonne in un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ ListView SetColumnOrderArray.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumnorderarray)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Dimensione, in elementi, del buffer in *corrispondenza di lParam*.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una matrice che specifica l'ordine di visualizzazione delle colonne, da sinistra a destra. Ad esempio, se il contenuto della matrice è , il controllo visualizza la colonna 2, la colonna 0 e la {2,0,1} colonna 1 in questo ordine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero in caso di esito positivo oppure zero in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





