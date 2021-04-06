---
title: Messaggio LVM_GETITEMCOUNT (COMmctrl. h)
description: Recupera il numero di elementi in un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro GetItemCount di ListView.
ms.assetid: 7c639d69-e42c-41b5-9fdd-4943166752a2
keywords:
- Controlli di Windows Message LVM_GETITEMCOUNT
topic_type:
- apiref
api_name:
- LVM_GETITEMCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff2791440c7285d054eca0d2945086d06e3c35a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742991"
---
# <a name="lvm_getitemcount-message"></a>\_Messaggio GETITEMCOUNT LVM

Recupera il numero di elementi in un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ GetItemCount di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemcount) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il numero di elementi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





