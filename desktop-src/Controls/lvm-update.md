---
title: Messaggio LVM_UPDATE (COMmctrl. h)
description: Aggiorna un elemento della visualizzazione elenco. Se il controllo elenco-visualizzazione dispone dello \_ stile LVS AutoArrange, questa macro causa la disposizione del controllo elenco-visualizzazione. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro di aggiornamento ListView.
ms.assetid: 81b332e9-4bea-481e-a7c5-613371103550
keywords:
- Controlli di Windows Message LVM_UPDATE
topic_type:
- apiref
api_name:
- LVM_UPDATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6cf2a4316e3ae3fc4dbab5e1afe780b03829b30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873373"
---
# <a name="lvm_update-message"></a>\_Messaggio di aggiornamento LVM

Aggiorna un elemento della visualizzazione elenco. Se il controllo elenco-visualizzazione dispone dello stile [**LVS \_ AutoArrange**](list-view-window-styles.md) , questa macro causa la disposizione del controllo elenco-visualizzazione. È possibile inviare questo messaggio in modo esplicito o usando la macro di [**\_ aggiornamento ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_update) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice dell'elemento da aggiornare.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





