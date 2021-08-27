---
title: TVM_HITTEST messaggio (Commctrl.h)
description: Determina la posizione del punto specificato rispetto all'area client di un controllo di visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o usando la macro HitTest di \_ TreeView.
ms.assetid: 18ea3737-f429-4c10-9133-3b5729aa36fa
keywords:
- TVM_HITTEST controlli Windows messaggio
topic_type:
- apiref
api_name:
- TVM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e564b6d82c04c0d007784aac39284db13b3776267d524d2f615353ede50eb945
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060151"
---
# <a name="tvm_hittest-message"></a>Messaggio TVM \_ HITTEST

Determina la posizione del punto specificato rispetto all'area client di un controllo di visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ HitTest di TreeView.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_hittest)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura TVHITTESTINFO.**](/windows/win32/api/commctrl/ns-commctrl-tvhittestinfo) Quando il messaggio viene inviato, il **membro pt** specifica le coordinate del punto da testare. Quando il messaggio viene restituito, il membro **hItem** è l'handle per l'elemento nel punto specificato oppure **NULL se** nessun elemento occupa il punto. Inoltre, quando il messaggio viene restituito, il **membro flags** è un valore di hit test che indica la posizione del punto specificato. Per un elenco di valori di hit test, vedere la descrizione della **struttura TVHITTESTINFO.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'handle all'elemento della visualizzazione albero che occupa il punto specificato oppure **NULL** se nessun elemento occupa il punto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





