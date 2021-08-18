---
title: SB_SETPARTS messaggio (Commctrl.h)
description: Imposta il numero di parti in una finestra di stato e la coordinata del bordo destro di ogni parte.
ms.assetid: e29e8b09-c018-4ea4-8b47-6f3713113427
keywords:
- SB_SETPARTS dei controlli Windows messaggio
topic_type:
- apiref
api_name:
- SB_SETPARTS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a63694ba40eb77cd887454b634ba8cdd2bff2c6ee7bb75beb9a7230eb3d1e1d0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637031"
---
# <a name="sb_setparts-message"></a>Messaggio \_ SETPARTS SB

Imposta il numero di parti in una finestra di stato e la coordinata del bordo destro di ogni parte.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Numero di parti da impostare (non può essere maggiore di 256).

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una matrice di interi. Il numero di elementi è specificato in *wParam.* Ogni elemento specifica la posizione, in coordinate client, del bordo destro della parte corrispondente. Se un elemento è -1, il bordo destro della parte corrispondente si estende al bordo della finestra.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo oppure FALSE **in** caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





