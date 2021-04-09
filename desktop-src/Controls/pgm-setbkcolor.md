---
title: Messaggio PGM_SETBKCOLOR (COMmctrl. h)
description: Imposta il colore di sfondo corrente per il controllo pager. È possibile inviare questo messaggio in modo esplicito o utilizzare la \_ macro SetBkColor del cercapersone.
ms.assetid: 720a25d7-3854-4f28-b227-bafab7b1e8c9
keywords:
- Controlli di Windows Message PGM_SETBKCOLOR
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
ms.openlocfilehash: fa9e8dc1c0cad3e60bdde3f3c05d77d8c57b98ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119586"
---
# <a name="pgm_setbkcolor-message"></a>\_Messaggio SETBKCOLOR PGM

Imposta il colore di sfondo corrente per il controllo pager. È possibile inviare questo messaggio in modo esplicito o utilizzare la macro [**\_ SetBkColor del cercapersone**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbkcolor) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Valore **COLORREF** che contiene il nuovo colore di sfondo del controllo pager.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **COLORREF** che contiene il colore di sfondo precedente.

## <a name="remarks"></a>Commenti

Per impostazione predefinita, il controllo pager utilizzerà il colore della superficie del pulsante di sistema come colore di sfondo. Si tratta dello stesso colore che può essere recuperato chiamando [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) con il colore \_ BTNFACE.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

