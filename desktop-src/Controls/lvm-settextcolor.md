---
title: Messaggio LVM_SETTEXTCOLOR (COMmctrl. h)
description: Imposta il colore del testo di un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro SetTextColor di ListView.
ms.assetid: ff90c18b-0cd7-4331-bcd8-61044e891d1f
keywords:
- Controlli di Windows Message LVM_SETTEXTCOLOR
topic_type:
- apiref
api_name:
- LVM_SETTEXTCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64b30c965bd523cd5638c894b47fc4785ffbdd09
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119462"
---
# <a name="lvm_settextcolor-message"></a>\_Messaggio SETTEXTCOLOR LVM

Imposta il colore del testo di un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ SetTextColor di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settextcolor) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Oggetto [**COLORREF**](/windows/desktop/gdi/colorref) che specifica il nuovo colore del testo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

