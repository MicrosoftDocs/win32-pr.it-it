---
title: Messaggio TVM_EXPAND (COMmctrl. h)
description: Il \_ messaggio di espansione TVM espande o comprime l'elenco di elementi figlio associati all'elemento padre specificato, se presente. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro di espansione TreeView.
ms.assetid: d6c2e5b2-ce36-4c2b-b527-91c6de56e305
keywords:
- Controlli di Windows Message TVM_EXPAND
topic_type:
- apiref
api_name:
- TVM_EXPAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14d5cd7577c6f4581865569c3aefca93f13aa305
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478485"
---
# <a name="tvm_expand-message"></a>\_Messaggio espansione TVM

Il messaggio di **\_ espansione TVM** espande o comprime l'elenco di elementi figlio associati all'elemento padre specificato, se presente. È possibile inviare questo messaggio in modo esplicito o usando la macro di [**\_ espansione TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_expand) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Flag di azione. Il parametro può essere costituito da uno o più dei valori seguenti:



| Valore                                                                                                                                                                     | Significato                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TVE_COLLAPSE"></span><span id="tve_collapse"></span><dl> <dt>**\_compressione TVE**</dt> </dl>                | Comprime l'elenco. <br/>                                                                                                                                                                                                                                                       |
| <span id="TVE_COLLAPSERESET"></span><span id="tve_collapsereset"></span><dl> <dt>**\_COLLAPSERESET TVE**</dt> </dl> | Comprime l'elenco e rimuove gli elementi figlio. Il flag di stato [**\_ EXPANDEDONCE di TVIS**](tree-view-control-item-states.md) viene reimpostato. Questo flag deve essere usato con il \_ flag di compressione TVE.<br/>                                                                 |
| <span id="TVE_EXPAND"></span><span id="tve_expand"></span><dl> <dt>**\_espansione TVE**</dt> </dl>                      | Espande l'elenco.<br/>                                                                                                                                                                                                                                                          |
| <span id="TVE_EXPANDPARTIAL"></span><span id="tve_expandpartial"></span><dl> <dt>**\_EXPANDPARTIAL TVE**</dt> </dl> | [Versione 4,70](common-control-versions.md). Espande parzialmente l'elenco. In questo stato gli elementi figlio sono visibili e il segno più (+) dell'elemento padre, che indica che è possibile espanderlo, viene visualizzato. Questo flag deve essere usato in combinazione con il \_ flag di espansione TVE.<br/> |
| <span id="TVE_TOGGLE"></span><span id="tve_toggle"></span><dl> <dt>**\_interruttore TVE**</dt> </dl>                      | Comprime l'elenco se è espanso o lo espande se è compresso.<br/>                                                                                                                                                                                                     |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per l'elemento padre da espandere o comprimere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero se l'operazione ha avuto esito positivo oppure zero in caso contrario.

## <a name="remarks"></a>Commenti

L'espansione di un nodo già espanso è considerata un'operazione riuscita e [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) restituisce un valore diverso da zero. Se il nodo è già compresso, il collasso di un nodo restituisce zero. in caso contrario, restituisce un valore diverso da zero. Il tentativo di espandere o comprimere un nodo privo di elementi figlio viene considerato un errore e **SendMessage** restituisce zero.

Quando un elemento viene espanso per la prima volta da un messaggio di **\_ espansione TVM** , l'azione genera i codici di notifica [TVN \_ ITEMEXPANDING](tvn-itemexpanding.md) e [TVN \_ ITEMEXPANDED](tvn-itemexpanded.md) e viene impostato il flag di stato [**TVIS \_ EXPANDEDONCE**](tree-view-control-item-states.md) dell'elemento. Fino a quando questo flag di stato rimane impostato, i messaggi di **\_ espansione TVM** successivi non generano le \_ notifiche TVN ITEMEXPANDING o TVN \_ ITEMEXPANDED. Per reimpostare il flag di stato **TVIS \_ EXPANDEDONCE** , è necessario inviare un messaggio di **\_ espansione TVM** con i \_ flag TVE Collapse e TVE \_ COLLAPSERESET impostati. Il tentativo di impostare in modo esplicito **TVIS \_ EXPANDEDONCE** comporterà un comportamento imprevedibile.

L'operazione di espansione potrebbe non riuscire se il proprietario del controllo TreeView nega l'operazione in risposta a una notifica [ \_ ITEMEXPANDING di TVN](tvn-itemexpanding.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

