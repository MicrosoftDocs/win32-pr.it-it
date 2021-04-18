---
title: Messaggio LVM_GETSELECTIONMARK (COMmctrl. h)
description: Recupera il contrassegno di selezione da un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro GetSelectionMark di ListView.
ms.assetid: 21daf7d7-1217-4608-93f9-c390546f1591
keywords:
- Controlli di Windows Message LVM_GETSELECTIONMARK
topic_type:
- apiref
api_name:
- LVM_GETSELECTIONMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 076aff15ff69c4b442c74022ed5a7c02b92a8c52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302294"
---
# <a name="lvm_getselectionmark-message"></a>\_Messaggio GETSELECTIONMARK LVM

Recupera il contrassegno di selezione da un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ GetSelectionMark di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getselectionmark) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il contrassegno di selezione in base zero oppure-1 se non è presente alcun contrassegno di selezione.

## <a name="remarks"></a>Commenti

Il *contrassegno di selezione* è l'indice dell'elemento da cui inizia una selezione multipla.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_SETSELECTIONMARK LVM**](lvm-setselectionmark.md)
</dt> </dl>

 

 





