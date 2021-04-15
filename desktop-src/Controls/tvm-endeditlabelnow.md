---
title: Messaggio TVM_ENDEDITLABELNOW (COMmctrl. h)
description: Termina la modifica dell'etichetta di un elemento della visualizzazione struttura ad albero. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro EndEditLabelNow di TreeView.
ms.assetid: 68de2020-9311-4958-859a-de55f5e41fcf
keywords:
- Controlli di Windows Message TVM_ENDEDITLABELNOW
topic_type:
- apiref
api_name:
- TVM_ENDEDITLABELNOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f059be20560adeb8cbcb0c63a2555283f6b7051
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517589"
---
# <a name="tvm_endeditlabelnow-message"></a>\_Messaggio ENDEDITLABELNOW TVM

Termina la modifica dell'etichetta di un elemento della visualizzazione struttura ad albero. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ EndEditLabelNow di TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_endeditlabelnow) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Variabile che indica se la modifica viene annullata senza essere salvata nell'etichetta. Se questo parametro è **true**, il sistema Annulla la modifica senza salvare le modifiche. In caso contrario, il sistema salva le modifiche nell'etichetta.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="remarks"></a>Commenti

Questo messaggio fa in modo che il codice di notifica di [TVN \_ ENDLABELEDIT](tvn-endlabeledit.md) venga inviato alla finestra padre del controllo di visualizzazione albero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





