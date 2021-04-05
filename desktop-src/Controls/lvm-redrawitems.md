---
title: Messaggio LVM_REDRAWITEMS (COMmctrl. h)
description: Impone a un controllo di visualizzazione elenco di ricreare un intervallo di elementi. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro RedrawItems di ListView.
ms.assetid: a717b17f-6e0a-4804-96f9-da93392a19ec
keywords:
- Controlli di Windows Message LVM_REDRAWITEMS
topic_type:
- apiref
api_name:
- LVM_REDRAWITEMS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42568a9ab78361a28a99eee372674287a24d03cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048345"
---
# <a name="lvm_redrawitems-message"></a>\_Messaggio REDRAWITEMS LVM

Impone a un controllo di visualizzazione elenco di ricreare un intervallo di elementi. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ RedrawItems di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_redrawitems) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice del primo elemento da ricreare.

</dd> <dt>

*lParam* 
</dt> <dd>

Indice dell'ultimo elemento da ricreare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="remarks"></a>Commenti

Gli elementi specificati non vengono effettivamente ridisegnati fino a quando la finestra elenco-visualizzazione non riceve un messaggio di [**\_ disegno WM**](/windows/desktop/gdi/wm-paint) da ridisegnare. Per ridisegnare immediatamente, chiamare la funzione [**UpdateWindow**](/windows/desktop/api/winuser/nf-winuser-updatewindow) dopo l'uso di questa macro.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

