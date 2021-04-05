---
title: Messaggio LVM_SETSELECTIONMARK (COMmctrl. h)
description: Imposta il contrassegno di selezione in un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro SetSelectionMark di ListView.
ms.assetid: 3218f1b3-b934-4083-aaaa-e10ef1dbb6bd
keywords:
- Controlli di Windows Message LVM_SETSELECTIONMARK
topic_type:
- apiref
api_name:
- LVM_SETSELECTIONMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3efc01068f22585061cae5a6f2c5c0c841810f52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739935"
---
# <a name="lvm_setselectionmark-message"></a>\_Messaggio SETSELECTIONMARK LVM

Imposta il contrassegno di selezione in un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ SetSelectionMark di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setselectionmark) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Indice in base zero del nuovo contrassegno di selezione. Se è impostato su-1, il contrassegno di selezione verrà rimosso.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il contrassegno di selezione precedente oppure-1 se non è presente alcun contrassegno di selezione precedente.

## <a name="remarks"></a>Commenti

Il *contrassegno di selezione* è l'indice dell'elemento da cui inizia una selezione multipla. Questo messaggio non influisce sullo stato di selezione dell'elemento.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_GETSELECTIONMARK LVM**](lvm-getselectionmark.md)
</dt> </dl>

 

 





