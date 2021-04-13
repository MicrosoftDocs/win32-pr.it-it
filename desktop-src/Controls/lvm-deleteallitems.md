---
title: Messaggio LVM_DELETEALLITEMS (COMmctrl. h)
description: Rimuove tutti gli elementi da un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro DeleteAllItems di ListView.
ms.assetid: 816bf565-79e9-4f5d-b5b4-5cdecce8a61c
keywords:
- Controlli di Windows Message LVM_DELETEALLITEMS
topic_type:
- apiref
api_name:
- LVM_DELETEALLITEMS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e92344e3cccf7578b8953206a9550022f6c6095
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475202"
---
# <a name="lvm_deleteallitems-message"></a>\_Messaggio DELETEALLITEMS LVM

Rimuove tutti gli elementi da un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ DeleteAllItems di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_deleteallitems) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="remarks"></a>Commenti

Quando un controllo visualizzazione elenco riceve il messaggio **LVM \_ DELETEALLITEMS** , invia il codice di [**notifica \_ DELETEALLITEMS LVN**](lvn-deleteallitems.md) alla relativa finestra padre.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





