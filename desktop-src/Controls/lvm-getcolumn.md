---
title: Messaggio LVM_GETCOLUMN (COMmctrl. h)
description: Ottiene gli attributi della colonna di un controllo di visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro ListView GetColumn.
ms.assetid: 59b4bbfc-6c38-4faa-8f2e-3ea5d24e55a6
keywords:
- Controlli di Windows Message LVM_GETCOLUMN
topic_type:
- apiref
api_name:
- LVM_GETCOLUMN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3eebf57138d27c31c5594f271e5d36a052b81673
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475173"
---
# <a name="lvm_getcolumn-message"></a>\_Messaggio GETCOLUMN LVM

Ottiene gli attributi della colonna di un controllo di visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**ListView \_ GetColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumn) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice della colonna.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) che specifica le informazioni per recuperare e ricevere informazioni sulla colonna. Il membro **mask** specifica gli attributi di colonna da recuperare. Se il membro **mask** specifica il \_ valore di testo LVCF, il membro **pszText** deve contenere l'indirizzo del buffer che riceve il testo dell'elemento e il membro **cchTextMax** deve specificare le dimensioni del buffer.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





