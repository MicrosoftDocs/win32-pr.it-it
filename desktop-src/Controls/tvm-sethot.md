---
title: TVM_SETHOT messaggio (Commctrl.h)
description: Imposta l'elemento a caldo per un controllo di visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro TreeView SetHot.
ms.assetid: 5e7368f5-40ce-4e7b-bbe3-5fe0b17181a8
keywords:
- TVM_SETHOT di controllo Windows messaggio
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
ms.openlocfilehash: 87ca61fd0bd3e25f37229cd5cee54f9bbb59b3a5c7556ae745821a8dc4d595d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913951"
---
# <a name="tvm_sethot-message"></a>Messaggio \_ SETHOT TVM

\[Destinato all'uso interno; non consigliato per l'uso nelle applicazioni. Questo messaggio potrebbe non essere supportato nelle versioni future di Windows.\]

Imposta l'elemento a caldo per un controllo di visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ TreeView SetHot.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sethot)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per il nuovo elemento ad accesso più caldo. Se questo valore è **NULL,** il controllo di visualizzazione struttura ad albero verrà impostato in modo da non avere elementi di tipo hot.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo oppure FALSE **in** caso contrario.

## <a name="security-considerations"></a>Considerazioni relative alla sicurezza

L'uso di questo messaggio potrebbe compromettere la sicurezza del programma.

## <a name="remarks"></a>Commenti

*L'elemento a caldo* è l'elemento su cui si posiziona il mouse. Questo messaggio fa sì che un elemento sia l'elemento più importante anche se il puntatore del mouse non vi passa sopra.

Questo messaggio non ha alcun effetto visibile se lo stile [**\_ TVS TRACKSELECT**](tree-view-control-window-styles.md) non è impostato.

Se ha esito positivo, questo messaggio fa sì che l'elemento ad accesso più a caldo venga ridisegnato.

Questo messaggio viene ignorato se *lParam* è **NULL** e il controllo di visualizzazione albero sta controllando il mouse.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SetHot di TreeView \_**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sethot)
</dt> </dl>

 

 





