---
title: TVM_ENDEDITLABELNOW messaggio (Commctrl.h)
description: Termina la modifica dell'etichetta di un elemento della visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro TreeView EndEditLabelNow.
ms.assetid: 68de2020-9311-4958-859a-de55f5e41fcf
keywords:
- TVM_ENDEDITLABELNOW controlli Windows messaggio
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
ms.openlocfilehash: 18355edc8efb18ea56a39e60c68361a7ef8d72e39af644707d6d102738fd60c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119387261"
---
# <a name="tvm_endeditlabelnow-message"></a>Messaggio TVM \_ ENDEDITLABELNOW

Termina la modifica dell'etichetta di un elemento della visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ TreeView EndEditLabelNow.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_endeditlabelnow)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Variabile che indica se la modifica viene annullata senza essere salvata nell'etichetta. Se questo parametro è **TRUE,** il sistema annulla la modifica senza salvare le modifiche. In caso contrario, il sistema salva le modifiche apportate all'etichetta.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo oppure FALSE **in** caso contrario.

## <a name="remarks"></a>Commenti

Questo messaggio determina l'invio del codice di notifica [ \_ TVN ENDLABELEDIT](tvn-endlabeledit.md) alla finestra padre del controllo di visualizzazione albero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





