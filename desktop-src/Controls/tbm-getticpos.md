---
title: Messaggio TBM_GETTICPOS (COMmctrl. h)
description: Recupera la posizione fisica corrente di un segno di graduazione in un TrackBar.
ms.assetid: a4b0ec32-ef4e-4607-ade1-5e2be02bebe4
keywords:
- Controlli di Windows Message TBM_GETTICPOS
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
ms.openlocfilehash: 5bb1346f63e9bb10b919c678373e0e8df0724861
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301664"
---
# <a name="tbm_getticpos-message"></a>\_Messaggio GETTICPOS TBM

Recupera la posizione fisica corrente di un segno di graduazione in un TrackBar.

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

Restituisce la distanza, espressa in coordinate client, dal lato sinistro o superiore dell'area client del TrackBar al segno di graduazione specificato. Il valore restituito è la coordinata x del segno di graduazione per un TrackBar orizzontale o la coordinata y di un TrackBar verticale. Se *wParam* non è un indice valido, il valore restituito è-1.

## <a name="remarks"></a>Commenti

Poiché il primo e l'ultimo segno di graduazione non sono disponibili tramite questo messaggio, gli indici validi vengono spostati rispetto alla relativa posizione di graduazione nel TrackBar. Se la differenza tra [**TBM \_ GETRANGEMIN**](tbm-getrangemin.md) e [**TBM \_ GETRANGEMAX**](tbm-getrangemax.md) è minore di due, non esiste alcun indice valido e questo messaggio avrà esito negativo.

Nell'esempio seguente viene illustrata la relazione tra i cicli di un TrackBar, i segni di avanzamento disponibili tramite questo messaggio e gli indici in base zero.

``` syntax
0 1 2 3 4 5 6 7 8 9    // Tick positions seen on the trackbar.
  1 2 3 4 5 6 7 8      // Tick positions whose position can be identified.
  0 1 2 3 4 5 6 7      // Index numbers for the identifiable positions.
```

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





