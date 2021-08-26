---
title: TVM_GETCOUNT messaggio (Commctrl.h)
description: Recupera un conteggio degli elementi in un controllo di visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o tramite la macro GetCount di \_ TreeView.
ms.assetid: cb8477be-51c9-4e96-8fa6-f978e0c1595f
keywords:
- TVM_GETCOUNT dei messaggi Windows controlli
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
ms.openlocfilehash: 3fce2d3ed6580acc875007ff3962bbeb21e9c0d3c3cb38128a2339da79597f3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060351"
---
# <a name="tvm_getcount-message"></a>Messaggio TVM \_ GETCOUNT

Recupera un conteggio degli elementi in un controllo di visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**\_ GetCount di TreeView.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getcount)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il conteggio degli elementi.

## <a name="remarks"></a>Commenti

Il numero di nodi restituito [**da TreeView \_ GetCount**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getcount) è limitato ai valori integer. Se si aggiunge un nodo oltre 32767, la macro restituisce un valore negativo. Dopo aver aggiunto 65536 nodi, il conteggio torna a zero. In questo caso, il controllo visualizzazione struttura ad albero appare vuoto senza barre di scorrimento.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





