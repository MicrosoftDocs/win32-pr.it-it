---
title: PGM_SETBUTTONSIZE messaggio (Commctrl.h)
description: Imposta le dimensioni correnti del pulsante per il controllo pager. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro Pager SetButtonSize.
ms.assetid: b31960f8-87c2-4209-8213-df75ac883e11
keywords:
- PGM_SETBUTTONSIZE di controllo Windows messaggio
topic_type:
- apiref
api_name:
- PGM_SETBUTTONSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b120ed4bd6b7090621e09dd24b9e6a23b037fb5aed83e7ac6fc43254393330e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046791"
---
# <a name="pgm_setbuttonsize-message"></a>PGM \_ SETBUTTONSIZE message

Imposta le dimensioni correnti del pulsante per il controllo pager. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ Pager SetButtonSize.**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbuttonsize)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Valore di tipo **int** che contiene le nuove dimensioni del pulsante, in pixel.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore int** che contiene le dimensioni del pulsante precedente, in pixel.

## <a name="remarks"></a>Commenti

Se il controllo pager ha lo [**stile \_ HORZ PGS,**](pager-control-styles.md) le dimensioni del pulsante determinano la larghezza dei pulsanti del pager. Se il controllo pager ha lo stile [**\_ PGS VERT,**](pager-control-styles.md) le dimensioni del pulsante determinano l'altezza dei pulsanti del pager. Per impostazione predefinita, il controllo pager imposta le dimensioni del pulsante su tre-quattro della larghezza della barra di scorrimento.

Il pulsante pager ha una dimensione minima, attualmente di 12 pixel. Tuttavia, questo può cambiare in modo da non dipendere da questo valore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PGM \_ GETBUTTONSIZE**](pgm-getbuttonsize.md)
</dt> </dl>

 

 





