---
title: HDM_GETORDERARRAY messaggio (Commctrl.h)
description: Ottiene l'ordine corrente da sinistra a destra degli elementi in un controllo intestazione. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro Header GetOrderArray.
ms.assetid: b287d3c1-ae61-41a4-a884-dc008eb24ad8
keywords:
- HDM_GETORDERARRAY controlli di Windows messaggio
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
ms.openlocfilehash: f374424fe3f1d84c4919c26948486a9bae1660072975556aecaac4b08b85b33b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062831"
---
# <a name="hdm_getorderarray-message"></a>Messaggio \_ HDM GETORDERARRAY

Ottiene l'ordine corrente da sinistra a destra degli elementi in un controllo intestazione. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ Header GetOrderArray.**](/windows/desktop/api/Commctrl/nf-commctrl-header_getorderarray)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Numero di elementi integer che *lParam* può contenere. Questo valore deve essere uguale al numero di elementi nel controllo (vedere [**HDM \_ GETITEMCOUNT).**](hdm-getitemcount.md)

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una matrice di interi che ricevono i valori di indice per gli elementi nell'intestazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero in caso di esito positivo e il buffer in corrispondenza di *lParam* riceve il numero di elemento per ogni elemento nel controllo intestazione nell'ordine in cui vengono visualizzati da sinistra a destra. In caso contrario, il messaggio restituisce zero.

## <a name="remarks"></a>Commenti

Il numero di elementi in *lParam* è specificato in *wParam* e deve essere uguale al numero di elementi nel controllo. Ad esempio, il frammento di codice seguente riserva memoria sufficiente per contenere i valori di indice.


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
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





