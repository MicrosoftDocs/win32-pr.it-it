---
title: Messaggio PGM_GETBKCOLOR (COMmctrl. h)
description: Recupera il colore di sfondo corrente per il controllo pager. È possibile inviare questo messaggio in modo esplicito o utilizzare la \_ macro GetBkColor del cercapersone.
ms.assetid: c39ad721-fe39-44e9-8305-67444acc5d65
keywords:
- Controlli di Windows Message PGM_GETBKCOLOR
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
ms.openlocfilehash: 4b58b139dd1caafcdefc6893e2b8a5e3312d3e28
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742527"
---
# <a name="pgm_getbkcolor-message"></a>\_Messaggio GETBKCOLOR PGM

Recupera il colore di sfondo corrente per il controllo pager. È possibile inviare questo messaggio in modo esplicito o utilizzare la macro [**\_ GetBkColor del cercapersone**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbkcolor) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **COLORREF** che contiene il colore di sfondo corrente.

## <a name="remarks"></a>Commenti

Per impostazione predefinita, il controllo pager utilizzerà il colore della superficie del pulsante di sistema come colore di sfondo. Si tratta dello stesso colore che può essere recuperato chiamando [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) con il colore \_ BTNFACE.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

