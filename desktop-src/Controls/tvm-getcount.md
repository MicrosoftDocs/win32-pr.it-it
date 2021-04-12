---
title: Messaggio TVM_GETCOUNT (COMmctrl. h)
description: Recupera un conteggio degli elementi in un controllo di visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro di TreeView GetCount.
ms.assetid: cb8477be-51c9-4e96-8fa6-f978e0c1595f
keywords:
- Controlli di Windows Message TVM_GETCOUNT
topic_type:
- apiref
api_name:
- TVM_GETCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 870ca0d1e4bf04d054d29d78ab60371863648a8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478479"
---
# <a name="tvm_getcount-message"></a>\_Messaggio TVM GETcount

Recupera un conteggio degli elementi in un controllo di visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro di [**TreeView \_ GetCount**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getcount) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il numero di elementi.

## <a name="remarks"></a>Commenti

Il numero di nodi restituito da [**TreeView \_ GetCount**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getcount) è limitato ai valori integer. Se si aggiunge un nodo oltre 32767, la macro restituisce un valore negativo. Dopo aver aggiunto i nodi 65536, il conteggio torna a zero. Quando si verifica questo problema, il controllo di visualizzazione albero appare vuoto senza barre di scorrimento.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





