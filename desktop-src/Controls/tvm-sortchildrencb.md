---
title: Messaggio TVM_SORTCHILDRENCB (COMmctrl. h)
description: Ordina gli elementi della visualizzazione albero utilizzando una funzione di callback definita dall'applicazione che confronta gli elementi. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro SortChildrenCB di TreeView.
ms.assetid: 1669e576-5e57-49f6-8097-7d6547306014
keywords:
- Controlli di Windows Message TVM_SORTCHILDRENCB
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
ms.openlocfilehash: 4b1dab4abbbc019a81d7a066c81dbb3537a0d80d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478946"
---
# <a name="tvm_sortchildrencb-message"></a>\_Messaggio SORTCHILDRENCB TVM

Ordina gli elementi della visualizzazione albero utilizzando una funzione di callback definita dall'applicazione che confronta gli elementi. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ SortChildrenCB di TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sortchildrencb) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Riservato. Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**TVSORTCB**](/windows/win32/api/commctrl/ns-commctrl-tvsortcb) . Il membro **lpfnCompare** è l'indirizzo della funzione di callback definita dall'applicazione, che viene chiamata durante l'operazione di ordinamento ogni volta che è necessario confrontare l'ordine relativo di due elementi dell'elenco. Per ulteriori informazioni sulla funzione di callback, vedere la descrizione di **TVSORTCB**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





