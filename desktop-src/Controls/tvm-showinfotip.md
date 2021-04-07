---
title: Messaggio TVM_SHOWINFOTIP (COMmctrl. h)
description: Mostra infotip per un elemento specificato in un controllo di visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro ShowInfoTip di TreeView.
ms.assetid: ed5a1bda-5754-4bb3-aa22-8faaf1af1268
keywords:
- Controlli di Windows Message TVM_SHOWINFOTIP
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
ms.openlocfilehash: 76f147253800469a800677a242ff0ab0ccdbdfa4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874590"
---
# <a name="tvm_showinfotip-message"></a>\_Messaggio SHOWINFOTIP TVM

Mostra infotip per un elemento specificato in un controllo di visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**\_ ShowInfoTip di TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_showinfotip) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* \[ in\]
</dt> <dd>

Handle per l'elemento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero.

## <a name="remarks"></a>Commenti

La maggior parte delle applicazioni non usa questo messaggio. Infotip vengono visualizzate automaticamente. Per altre informazioni, vedere uso di infotip di visualizzazione ad albero nella panoramica [sui controlli Tree-View](tree-view-controls.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





