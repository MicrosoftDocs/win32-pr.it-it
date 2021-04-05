---
title: Messaggio LVM_SETHOTITEM (COMmctrl. h)
description: Imposta l'elemento attivo per un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro SetHotItem di ListView.
ms.assetid: 0aa2b15d-4983-4234-9863-f1fdee09f913
keywords:
- Controlli di Windows Message LVM_SETHOTITEM
topic_type:
- apiref
api_name:
- LVM_SETHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82c17bc67c530581b79a87030b31b655f856dd0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739943"
---
# <a name="lvm_sethotitem-message"></a>\_Messaggio SETHOTITEM LVM

Imposta l'elemento attivo per un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ SetHotItem di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethotitem) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero dell'elemento da impostare come elemento attivo.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'indice dell'elemento precedentemente attivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





