---
title: Messaggio LVM_SETTOOLTIPS (COMmctrl. h)
description: Imposta il controllo ToolTip che il controllo visualizzazione elenco utilizzerà per visualizzare le descrizioni comandi. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro ListView Setooltips.
ms.assetid: 5b4335a4-e9f0-4b13-b00b-516af3b60bf1
keywords:
- Controlli di Windows Message LVM_SETTOOLTIPS
topic_type:
- apiref
api_name:
- LVM_SETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ff749c24a35cf73de2d75b8a3b516197b57aac4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476073"
---
# <a name="lvm_settooltips-message"></a>Messaggio di controllo delle \_ descrizioni LVM

Imposta il controllo ToolTip che il controllo visualizzazione elenco utilizzerà per visualizzare le descrizioni comandi. È possibile inviare questo messaggio in modo esplicito o usare la macro [**ListView \_ setooltips**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settooltips) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Handle per il controllo ToolTip da impostare.</dd> <dt>

*lParam* 
</dt> <dd>

Deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'handle per il controllo ToolTip precedente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_GETtooltips LVM**](lvm-gettooltips.md)
</dt> </dl>

 

 





