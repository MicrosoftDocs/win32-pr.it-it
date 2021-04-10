---
title: Messaggio CB_GETDROPPEDSTATE (winuser. h)
description: Determina se la casella di riepilogo di una casella combinata viene rilasciata.
ms.assetid: a3f4e352-298d-45ea-a5a7-007f1fc1a387
keywords:
- Controlli di Windows Message CB_GETDROPPEDSTATE
topic_type:
- apiref
api_name:
- CB_GETDROPPEDSTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ae321bbaa3078a04ffc97d4a8083a674d03d651
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048778"
---
# <a name="cb_getdroppedstate-message"></a>\_Messaggio GETDROPPEDSTATE CB

Determina se la casella di riepilogo di una casella combinata viene rilasciata.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilizzato; deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilizzato; deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la casella di riepilogo è visibile, il valore restituito è **true**; in caso contrario, è **false**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CB \_ SHOWDROPDOWN**](cb-showdropdown.md)
</dt> </dl>

 

 





