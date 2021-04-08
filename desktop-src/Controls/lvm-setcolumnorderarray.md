---
title: Messaggio LVM_SETCOLUMNORDERARRAY (COMmctrl. h)
description: Imposta l'ordine da sinistra a destra delle colonne in un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro SetColumnOrderArray di ListView.
ms.assetid: 9b491832-42cc-4262-8f6c-23cbc2c889bf
keywords:
- Controlli di Windows Message LVM_SETCOLUMNORDERARRAY
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
ms.openlocfilehash: 94fdeb27074a3f6762e7fb3788fd7ccc0a2dcc5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047855"
---
# <a name="lvm_setcolumnorderarray-message"></a>\_Messaggio SETCOLUMNORDERARRAY LVM

Imposta l'ordine da sinistra a destra delle colonne in un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ SetColumnOrderArray di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumnorderarray) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Dimensioni, in elementi, del buffer in *lParam*.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una matrice che specifica l'ordine in cui devono essere visualizzate le colonne, da sinistra a destra. Se, ad esempio, il contenuto della matrice è {2,0,1} , il controllo Visualizza la colonna 2, la colonna 0 e la colonna 1 in tale ordine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





