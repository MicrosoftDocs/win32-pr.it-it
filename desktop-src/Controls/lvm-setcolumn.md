---
title: Messaggio LVM_SETCOLUMN (COMmctrl. h)
description: Imposta gli attributi di una colonna della visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro ListView secolumn.
ms.assetid: 8ca1c269-fd86-4561-940d-b75f8ca2b731
keywords:
- Controlli di Windows Message LVM_SETCOLUMN
topic_type:
- apiref
api_name:
- LVM_SETCOLUMN
- LVM_SETCOLUMNW
- LVM_SETCOLUMNW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7251da70c7ac1e2cb7bbcf7b3e220a2f6cdf055f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964256"
---
# <a name="lvm_setcolumn-message"></a>\_Messaggio di colonna LVM

Imposta gli attributi di una colonna della visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**ListView \_ secolumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumn) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice della colonna.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) che contiene i nuovi attributi della colonna. Il membro **mask** specifica gli attributi di colonna da impostare. Se il membro **mask** specifica il \_ valore di testo LVCF, il membro **pszText** è l'indirizzo di una stringa con terminazione null e il membro **cchTextMax** viene ignorato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **LVM \_ SETCOLUMNW** (Unicode) e **LVM \_ SETCOLUMNW** (ANSI)<br/>               |



 

 





