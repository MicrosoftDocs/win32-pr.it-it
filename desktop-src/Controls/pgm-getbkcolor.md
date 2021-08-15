---
title: PGM_GETBKCOLOR messaggio (Commctrl.h)
description: Recupera il colore di sfondo corrente per il controllo pager. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro Pager GetBkColor.
ms.assetid: c39ad721-fe39-44e9-8305-67444acc5d65
keywords:
- PGM_GETBKCOLOR di controllo Windows messaggio
topic_type:
- apiref
api_name:
- PGM_GETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff3ee3a4be09a948654d337a47eecdd2a7b15d16b0602016aa99500cd1c3728c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985941"
---
# <a name="pgm_getbkcolor-message"></a>Messaggio PGM \_ GETBKCOLOR

Recupera il colore di sfondo corrente per il controllo pager. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ Pager GetBkColor.**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbkcolor)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore COLORREF** che contiene il colore di sfondo corrente.

## <a name="remarks"></a>Commenti

Per impostazione predefinita, il controllo pager userà il colore del viso del pulsante di sistema come colore di sfondo. Questo è lo stesso colore che può essere recuperato chiamando [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) con COLOR \_ BTNFACE.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

