---
title: TBM_GETTICPOS messaggio (Commctrl.h)
description: Recupera la posizione fisica corrente di un segno di graduazione in un trackbar.
ms.assetid: a4b0ec32-ef4e-4607-ade1-5e2be02bebe4
keywords:
- TBM_GETTICPOS di controllo Windows messaggio
topic_type:
- apiref
api_name:
- TBM_GETTICPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56d191034fc1551d4ffc1840498e352e2f3cd82985f1bbc5a7ae8d5350a41fb1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046341"
---
# <a name="tbm_getticpos-message"></a>Messaggio \_ GETTICPOS TBM

Recupera la posizione fisica corrente di un segno di graduazione in un trackbar.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero che identifica un segno di graduazione. Le posizioni del primo e dell'ultimo segno di graduazione non sono direttamente disponibili tramite questo messaggio.

</dd> <dt>

*lParam* 
</dt> <dd>

Deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce la distanza, in coordinate client, dal lato sinistro o superiore dell'area client del trackbar al segno di graduazione specificato. Il valore restituito è la coordinata x del segno di graduazione per un trackbar orizzontale o la coordinata y per un trackbar verticale. Se *wParam non* è un indice valido, il valore restituito è -1.

## <a name="remarks"></a>Commenti

Poiché il primo e l'ultimo segno di graduazione non sono disponibili tramite questo messaggio, gli indici validi vengono compensati dalla posizione del segno di graduazione sul trackbar. Se la differenza tra [**TBM \_ GETRANGEMIN**](tbm-getrangemin.md) e [**TBM \_ GETRANGEMAX**](tbm-getrangemax.md) è minore di due, non esiste alcun indice valido e questo messaggio avrà esito negativo.

Di seguito viene illustrata la relazione tra i segni di graduazione in un trackbar, i segni di graduazione disponibili tramite questo messaggio e i relativi indici in base zero.

``` syntax
0 1 2 3 4 5 6 7 8 9    // Tick positions seen on the trackbar.
  1 2 3 4 5 6 7 8      // Tick positions whose position can be identified.
  0 1 2 3 4 5 6 7      // Index numbers for the identifiable positions.
```

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





