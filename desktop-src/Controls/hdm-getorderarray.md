---
title: Messaggio HDM_GETORDERARRAY (COMmctrl. h)
description: Ottiene l'ordine da sinistra a destra corrente degli elementi in un controllo intestazione. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro GetOrderArray dell'intestazione.
ms.assetid: b287d3c1-ae61-41a4-a884-dc008eb24ad8
keywords:
- Controlli di Windows Message HDM_GETORDERARRAY
topic_type:
- apiref
api_name:
- HDM_GETORDERARRAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e334b0023ad3441c20048273e9bc58c1b25622b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119831"
---
# <a name="hdm_getorderarray-message"></a>\_Messaggio HDM GETORDERARRAY

Ottiene l'ordine da sinistra a destra corrente degli elementi in un controllo intestazione. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ GetOrderArray dell'intestazione**](/windows/desktop/api/Commctrl/nf-commctrl-header_getorderarray) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Numero di elementi Integer che *lParam* può mantenere. Questo valore deve essere uguale al numero di elementi nel controllo (vedere [**HDM \_ GETITEMCOUNT**](hdm-getitemcount.md)).

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una matrice di numeri interi che ricevono i valori di indice per gli elementi nell'intestazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero se ha esito positivo e il buffer in *lParam* riceve il numero di elemento per ogni elemento nel controllo intestazione nell'ordine in cui appaiono da sinistra a destra. In caso contrario, il messaggio restituisce zero.

## <a name="remarks"></a>Commenti

Il numero di elementi in *lParam* è specificato in *wParam* e deve essere uguale al numero di elementi nel controllo. Il frammento di codice seguente, ad esempio, riserva memoria sufficiente per mantenere i valori di indice.


```
int iItems,

    *lpiArray;



// Get memory for buffer.

(iItems = SendMessage(hwndHD, HDM_GETITEMCOUNT, 0,0))!=-1)

    if(!(lpiArray = calloc(iItems,sizeof(int))))

MessageBox(hwnd, "Out of memory.","Error", MB_OK);
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





