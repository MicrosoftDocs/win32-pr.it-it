---
title: TVM_SHOWINFOTIP messaggio (Commctrl.h)
description: Visualizza il suggerimento per un elemento specificato in un controllo visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o tramite la \_ macro TreeView ShowInfoTip.
ms.assetid: ed5a1bda-5754-4bb3-aa22-8faaf1af1268
keywords:
- TVM_SHOWINFOTIP dei messaggi Windows controllo
topic_type:
- apiref
api_name:
- TVM_SHOWINFOTIP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0e1cf61511e8c9e69c42d89f99fc4ddae90de78701e5e75170ff1b793671120
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913921"
---
# <a name="tvm_showinfotip-message"></a>Messaggio TVM \_ SHOWINFOTIP

Visualizza il suggerimento per un elemento specificato in un controllo visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**\_ TreeView ShowInfoTip.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_showinfotip)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* \[ Pollici\]
</dt> <dd>

Handle per l'elemento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero.

## <a name="remarks"></a>Commenti

La maggior parte delle applicazioni non usa questo messaggio. I suggerimenti vengono visualizzati automaticamente. Per altre informazioni, vedere Using Tree-view Infotips (Uso dei suggerimenti per la visualizzazione albero) nella panoramica [Tree-View dei controlli.](tree-view-controls.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





