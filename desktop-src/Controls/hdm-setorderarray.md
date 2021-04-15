---
title: Messaggio HDM_SETORDERARRAY (COMmctrl. h)
description: Imposta l'ordine da sinistra a destra degli elementi di intestazione. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro SetOrderArray dell'intestazione.
ms.assetid: 094c424f-10bd-484d-8236-937811b703a6
keywords:
- Controlli di Windows Message HDM_SETORDERARRAY
topic_type:
- apiref
api_name:
- HDM_SETORDERARRAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f07874bfc102babec18b142a087b14e330044ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476973"
---
# <a name="hdm_setorderarray-message"></a>\_Messaggio HDM SETORDERARRAY

Imposta l'ordine da sinistra a destra degli elementi di intestazione. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ SetOrderArray dell'intestazione**](/windows/desktop/api/Commctrl/nf-commctrl-header_setorderarray) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Dimensione del buffer in *lParam*, in Elements. Questo valore deve essere uguale al valore restituito da [**HDM \_ GETITEMCOUNT**](hdm-getitemcount.md).

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una matrice che specifica l'ordine in cui gli elementi devono essere visualizzati, da sinistra a destra. Se, ad esempio, il contenuto della matrice è {2,0,1} , il controllo Visualizza l'elemento 2, l'elemento 0 e l'elemento 1, da sinistra a destra.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





