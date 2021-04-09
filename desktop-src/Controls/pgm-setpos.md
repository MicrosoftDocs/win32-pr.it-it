---
title: Messaggio PGM_SETPOS (COMmctrl. h)
description: Imposta la posizione di scorrimento corrente per il controllo cercapersone. È possibile inviare questo messaggio in modo esplicito o utilizzare la \_ macro SetPos del cercapersone.
ms.assetid: b882ea2d-9dab-4d36-9201-29522141f779
keywords:
- Controlli di Windows Message PGM_SETPOS
topic_type:
- apiref
api_name:
- PGM_SETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5af4497e97a8263fa9ec8e454d367bb57e830c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741223"
---
# <a name="pgm_setpos-message"></a>\_Messaggio SETPOS PGM

Imposta la posizione di scorrimento corrente per il controllo cercapersone. È possibile inviare questo messaggio in modo esplicito o utilizzare la macro [**\_ SetPos del cercapersone**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setpos) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Valore di tipo **int** che contiene la nuova posizione di scorrimento, in pixel.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito non viene utilizzato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





