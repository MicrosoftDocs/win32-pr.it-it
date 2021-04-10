---
title: Messaggio TVM_SETHOT (COMmctrl. h)
description: Imposta l'elemento attivo per un controllo di visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro SetHot di TreeView.
ms.assetid: 5e7368f5-40ce-4e7b-bbe3-5fe0b17181a8
keywords:
- Controlli di Windows Message TVM_SETHOT
topic_type:
- apiref
api_name:
- TVM_SETHOT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: beccd5429267350682a6721cde66cca9316cf438
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964788"
---
# <a name="tvm_sethot-message"></a>\_Messaggio SETHOT TVM

\[Progettato per uso interno; sconsigliato per l'utilizzo nelle applicazioni. Questo messaggio potrebbe non essere supportato nelle versioni future di Windows.\]

Imposta l'elemento attivo per un controllo di visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ SetHot di TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sethot) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per il nuovo elemento attivo. Se questo valore è **null**, il controllo di visualizzazione albero verrà impostato in modo da non avere alcun elemento attivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="security-considerations"></a>Considerazioni relative alla sicurezza

L'uso di questo messaggio potrebbe compromettere la sicurezza del programma.

## <a name="remarks"></a>Commenti

L' *elemento critico* è l'elemento su cui è posizionato il mouse. Questo messaggio rende un elemento simile a quello dell'elemento attivo anche se il mouse non è posizionato su di esso.

Questo messaggio non ha alcun effetto visibile se lo stile [**\_ TRACKSELECT TV**](tree-view-control-window-styles.md) non è impostato.

Se ha esito positivo, questo messaggio causa il ridisegnato dell'elemento sensibile.

Questo messaggio viene ignorato se *lParam* è **null** e il controllo di visualizzazione albero tiene traccia del mouse.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_SetHot TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sethot)
</dt> </dl>

 

 





