---
title: Messaggio PGM_GETPOS (COMmctrl. h)
description: Recupera la posizione di scorrimento corrente del controllo cercapersone. È possibile inviare questo messaggio in modo esplicito o utilizzare la \_ macro GetPos del cercapersone.
ms.assetid: 1e0f967a-3290-43b7-b812-8cf56abf2d32
keywords:
- Controlli di Windows Message PGM_GETPOS
topic_type:
- apiref
api_name:
- PGM_GETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 611a27e9cb952c5be190fa041af3d238f0184b03
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302049"
---
# <a name="pgm_getpos-message"></a>\_Messaggio GETPOS PGM

Recupera la posizione di scorrimento corrente del controllo cercapersone. È possibile inviare questo messaggio in modo esplicito o utilizzare la macro [**\_ GetPos del cercapersone**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getpos) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore INT che contiene la posizione di scorrimento corrente, in pixel.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





