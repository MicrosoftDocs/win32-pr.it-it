---
title: Messaggio TVM_HITTEST (COMmctrl. h)
description: Determina la posizione del punto specificato rispetto all'area client di un controllo di visualizzazione ad albero. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro di TreeView HitTest.
ms.assetid: 18ea3737-f429-4c10-9133-3b5729aa36fa
keywords:
- Controlli di Windows Message TVM_HITTEST
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
ms.openlocfilehash: 50b91a11892a2bb904d2cd7d82b5b08cea18331b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048104"
---
# <a name="tvm_hittest-message"></a>Messaggio di HITTEST di TVM \_

Determina la posizione del punto specificato rispetto all'area client di un controllo di visualizzazione ad albero. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro di [**TreeView \_ HitTest**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_hittest) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**TVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tvhittestinfo) . Quando il messaggio viene inviato, il membro **PT** specifica le coordinate del punto da testare. Quando il messaggio viene restituito, il membro **Hite** è l'handle per l'elemento in corrispondenza del punto specificato o **null** se nessun elemento occupa il punto. Inoltre, quando il messaggio viene restituito, il membro **Flags** è un valore di hit test che indica la posizione del punto specificato. Per un elenco di valori di hit test, vedere la descrizione della struttura **TVHITTESTINFO** .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'handle per l'elemento della visualizzazione struttura ad albero che occupa il punto specificato o **null** se nessun elemento occupa il punto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





