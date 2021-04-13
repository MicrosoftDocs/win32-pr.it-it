---
title: Messaggio LVM_FINDITEM (COMmctrl. h)
description: Cerca un elemento della visualizzazione elenco con le caratteristiche specificate. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro FindItem di ListView.
ms.assetid: 3b18c8ad-97e6-4f4d-bf89-afb95f925ed1
keywords:
- Controlli di Windows Message LVM_FINDITEM
topic_type:
- apiref
api_name:
- LVM_FINDITEM
- LVM_FINDITEMA
- LVM_FINDITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1f7dfc19e263a6ab7ad29b5e514fa4e52c1a9ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475185"
---
# <a name="lvm_finditem-message"></a>\_Messaggio FINDITEM LVM

Cerca un elemento della visualizzazione elenco con le caratteristiche specificate. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ FindItem di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_finditem) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice dell'elemento da cui iniziare la ricerca con o-1 per iniziare dall'inizio. L'elemento specificato è escluso dalla ricerca.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) contenente informazioni sugli elementi da cercare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'indice dell'elemento in caso di esito positivo; in caso contrario,-1.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **LVM \_ FINDITEMW** (Unicode) e **LVM \_ FINDITEMA** (ANSI)<br/>                 |



 

 





