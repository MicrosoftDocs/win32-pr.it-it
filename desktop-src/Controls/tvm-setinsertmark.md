---
title: Messaggio TVM_SETINSERTMARK (COMmctrl. h)
description: Imposta il segno di inserimento in un controllo di visualizzazione ad albero. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro SetInsertMark di TreeView.
ms.assetid: 35441807-406a-408c-ad89-6dd40c907e3c
keywords:
- Controlli di Windows Message TVM_SETINSERTMARK
topic_type:
- apiref
api_name:
- TVM_SETINSERTMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff5a9cc9b05e9cd7dc3281d778734bee1048ffd2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874009"
---
# <a name="tvm_setinsertmark-message"></a>\_Messaggio SETINSERTMARK TVM

Imposta il segno di inserimento in un controllo di visualizzazione ad albero. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ SetInsertMark di TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setinsertmark) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Valore **bool** che specifica se il segno di inserimento viene inserito prima o dopo l'elemento specificato. Se questo argomento è diverso da zero, il segno di inserimento verrà inserito dopo l'elemento. Se questo argomento è zero, il segno di inserimento verrà inserito prima dell'elemento.

</dd> <dt>

*lParam* 
</dt> <dd>

**HTREEITEM** che specifica in quale elemento verrà inserito il segno di inserimento. Se questo argomento è **null**, il segno di inserimento verrà rimosso.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.

## <a name="remarks"></a>Commenti

In alcuni casi, il contrassegno di inserimento può essere visualizzato in due posizioni dopo l'espansione di un nodo. Se si utilizzano segni di inserimento, è consigliabile forzare un aggiornamento del controllo dopo l'espansione di un nodo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





