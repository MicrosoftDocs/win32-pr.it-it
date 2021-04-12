---
title: Messaggio LVM_GETTOOLTIPS (COMmctrl. h)
description: Recupera il controllo ToolTip utilizzato dal controllo visualizzazione elenco per visualizzare le descrizioni comandi. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro ListView GetToolTips.
ms.assetid: a3522c64-9498-40b8-9062-c112b7c8cacc
keywords:
- Controlli di Windows Message LVM_GETTOOLTIPS
topic_type:
- apiref
api_name:
- LVM_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f409c85ed6157e8cfc837e5efa3a68488aec504
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478509"
---
# <a name="lvm_gettooltips-message"></a>Messaggio di LVM \_ GETtooltips

Recupera il controllo ToolTip utilizzato dal controllo visualizzazione elenco per visualizzare le descrizioni comandi. È possibile inviare questo messaggio in modo esplicito o usare la macro [**ListView \_ GetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettooltips) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'handle del controllo ToolTip.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_descrizioni comando LVM**](lvm-settooltips.md)
</dt> </dl>

 

 





