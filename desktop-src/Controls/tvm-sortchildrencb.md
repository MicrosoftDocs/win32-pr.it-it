---
title: TVM_SORTCHILDRENCB messaggio (Commctrl.h)
description: Ordina gli elementi della visualizzazione albero usando una funzione di callback definita dall'applicazione che confronta gli elementi. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro SortChildrenCB di TreeView.
ms.assetid: 1669e576-5e57-49f6-8097-7d6547306014
keywords:
- TVM_SORTCHILDRENCB dei controlli Windows messaggio
topic_type:
- apiref
api_name:
- TVM_SORTCHILDRENCB
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45f0ec311cc5ce0f972f3363ea97cd42874ca85807bf852296de0283fccc95c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118669477"
---
# <a name="tvm_sortchildrencb-message"></a>Messaggio TVM \_ SORTCHILDRENCB

Ordina gli elementi della visualizzazione albero usando una funzione di callback definita dall'applicazione che confronta gli elementi. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ SortChildrenCB di TreeView.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sortchildrencb)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Riservato. Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura TVSORTCB.**](/windows/win32/api/commctrl/ns-commctrl-tvsortcb) Il **membro lpfnCompare** è l'indirizzo della funzione di callback definita dall'applicazione, che viene chiamata durante l'operazione di ordinamento ogni volta che è necessario confrontare l'ordine relativo di due elementi dell'elenco. Per altre informazioni sulla funzione di callback, vedere la descrizione di **TVSORTCB.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo oppure FALSE **in** caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





