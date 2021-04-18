---
title: Messaggio LVM_INSERTCOLUMN (COMmctrl. h)
description: Inserisce una nuova colonna in un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro InsertColumn di ListView.
ms.assetid: 1326e38e-bb45-4d0d-b5bc-ec684b3b92ef
keywords:
- Controlli di Windows Message LVM_INSERTCOLUMN
topic_type:
- apiref
api_name:
- LVM_INSERTCOLUMN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8be89ff0b4ef417a715085582544112cb90cb6b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518646"
---
# <a name="lvm_insertcolumn-message"></a>\_Messaggio INSERTCOLUMN LVM

Inserisce una nuova colonna in un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ InsertColumn di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertcolumn) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice della nuova colonna.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) che contiene gli attributi della nuova colonna.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'indice della nuova colonna se ha esito positivo oppure-1 in caso contrario.

## <a name="remarks"></a>Commenti

Le colonne sono visibili solo nella visualizzazione report (Dettagli).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





