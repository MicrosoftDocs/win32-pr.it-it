---
title: Messaggio TVM_SETITEM (COMmctrl. h)
description: Il messaggio della macchina virtuale TVM \_ imposta alcuni o tutti gli attributi di un elemento della visualizzazione struttura ad albero. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro elemento TreeView.
ms.assetid: 28d288bf-a557-4fce-870c-ffa368ece5a9
keywords:
- Controlli di Windows Message TVM_SETITEM
topic_type:
- apiref
api_name:
- TVM_SETITEM
- TVM_SETITEMA
- TVM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95750af3aa43a25f0ff4eae5533df5d9aef23537
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476949"
---
# <a name="tvm_setitem-message"></a>\_Messaggio di SETITEM TVM

Il messaggio della macchina virtuale **TVM \_** imposta alcuni o tutti gli attributi di un elemento della visualizzazione struttura ad albero. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**\_ elemento TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitem) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) che contiene gli attributi del nuovo elemento. Con la [versione 4,71](common-control-versions.md) e successive, è invece possibile usare una struttura [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="remarks"></a>Commenti

Il membro **hitey** della struttura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) o [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) identifica l'elemento e il membro **mask** specifica gli attributi da impostare.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TVM \_ SETITEMW** (Unicode) e **TVM \_ seitema** (ANSI)<br/>                   |



 

 





