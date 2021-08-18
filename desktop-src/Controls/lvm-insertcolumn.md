---
title: LVM_INSERTCOLUMN messaggio (Commctrl.h)
description: Inserisce una nuova colonna in un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro InsertColumn di ListView.
ms.assetid: 1326e38e-bb45-4d0d-b5bc-ec684b3b92ef
keywords:
- LVM_INSERTCOLUMN controlli Windows messaggio
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
ms.openlocfilehash: c5c2316ed2a74c82cd4530eff2d71d4771f4042b903c7ee17fc62886009ed5b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019239"
---
# <a name="lvm_insertcolumn-message"></a>Messaggio \_ INSERTCOLUMN di LVM

Inserisce una nuova colonna in un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ InsertColumn di ListView.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertcolumn)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice della nuova colonna.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) che contiene gli attributi della nuova colonna.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'indice della nuova colonna in caso di esito positivo oppure -1 in caso contrario.

## <a name="remarks"></a>Commenti

Le colonne sono visibili solo nella visualizzazione report (dettagli).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





