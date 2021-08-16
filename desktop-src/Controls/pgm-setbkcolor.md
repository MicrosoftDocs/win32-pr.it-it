---
title: PGM_SETBKCOLOR messaggio (Commctrl.h)
description: Imposta il colore di sfondo corrente per il controllo pager. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro Pager SetBkColor.
ms.assetid: 720a25d7-3854-4f28-b227-bafab7b1e8c9
keywords:
- PGM_SETBKCOLOR dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- PGM_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d727bf401fae3b8c58b96fe8b5190a3ad427abb40b0478d59de087add553ddf5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117830182"
---
# <a name="pgm_setbkcolor-message"></a>Messaggio PGM \_ SETBKCOLOR

Imposta il colore di sfondo corrente per il controllo pager. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ Pager SetBkColor.**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbkcolor)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

**Valore COLORREF** che contiene il nuovo colore di sfondo del controllo pager.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore COLORREF** che contiene il colore di sfondo precedente.

## <a name="remarks"></a>Commenti

Per impostazione predefinita, il controllo pager userà il colore del viso del pulsante di sistema come colore di sfondo. Questo è lo stesso colore che può essere recuperato chiamando [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) con COLOR \_ BTNFACE.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

