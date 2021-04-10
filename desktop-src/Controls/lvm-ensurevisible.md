---
title: Messaggio LVM_ENSUREVISIBLE (COMmctrl. h)
description: Garantisce che un elemento della visualizzazione elenco sia interamente o parzialmente visibile, scorrendo il controllo elenco-visualizzazione, se necessario. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro EnsureVisible di ListView.
ms.assetid: 3564b6e6-b8b6-401b-85bc-8bd6261fc054
keywords:
- Controlli di Windows Message LVM_ENSUREVISIBLE
topic_type:
- apiref
api_name:
- LVM_ENSUREVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d0ff4009399988f20f3e162114f91e4cff02820
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963769"
---
# <a name="lvm_ensurevisible-message"></a>\_Messaggio ENSUREVISIBLE LVM

Garantisce che un elemento della visualizzazione elenco sia interamente o parzialmente visibile, scorrendo il controllo elenco-visualizzazione, se necessario. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ EnsureVisible di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_ensurevisible) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice dell'elemento della visualizzazione elenco.

</dd> <dt>

*lParam* 
</dt> <dd>

Valore che specifica se l'elemento deve essere interamente visibile. Se questo parametro è **true**, non viene eseguito alcuno scorrimento se l'elemento è almeno parzialmente visibile.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="remarks"></a>Commenti

Il messaggio ha esito negativo se lo stile della finestra include [**LVS \_ NoScroll**](list-view-window-styles.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





