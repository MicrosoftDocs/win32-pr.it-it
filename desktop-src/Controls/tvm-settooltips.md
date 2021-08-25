---
title: TVM_SETTOOLTIPS messaggio (Commctrl.h)
description: Imposta il controllo descrizione comando figlio di un controllo visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o tramite la \_ macro TreeView SetToolTips.
ms.assetid: beb9a739-868e-46a8-95d9-9dc032c79dd4
keywords:
- TVM_SETTOOLTIPS di controllo Windows messaggio
topic_type:
- apiref
api_name:
- TVM_SETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd18a5217db0d105841722d208904c1b65199504750576acf1ff8035f31bd585
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913961"
---
# <a name="tvm_settooltips-message"></a>Messaggio \_ TVM SETTOOLTIPS

Imposta il controllo descrizione comando figlio di un controllo visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**\_ TreeView SetToolTips.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_settooltips)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per un controllo descrizione comando.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'handle per il controllo descrizione comando impostato in precedenza per il controllo di visualizzazione ad albero oppure **NULL** se le descrizioni comando non sono state usate in precedenza.

## <a name="remarks"></a>Commenti

Quando vengono creati, i controlli visualizzazione albero creano automaticamente un controllo descrizione comando figlio. Per impedire a un controllo visualizzazione albero di usare le descrizioni comando, creare il controllo con lo stile [**\_ TVS NOTOOLTIPS.**](tree-view-control-window-styles.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**GETTOOLTIPS DI TVM \_**](tvm-gettooltips.md)
</dt> </dl>

 

 





