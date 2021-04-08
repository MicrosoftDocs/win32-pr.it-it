---
title: Messaggio LVM_ISITEMVISIBLE (COMmctrl. h)
description: Indica se un elemento del controllo visualizzazione elenco è visibile. Inviare questo messaggio in modo esplicito o utilizzando la \_ macro IsItemVisible di ListView.
ms.assetid: 355be527-e2b9-46be-96a0-951d72216d92
keywords:
- Controlli di Windows Message LVM_ISITEMVISIBLE
topic_type:
- apiref
api_name:
- LVM_ISITEMVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a95116d2d6da6e3554e63a8149c9b91d6c97f76
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874309"
---
# <a name="lvm_isitemvisible-message"></a>\_Messaggio ISITEMVISIBLE LVM

Indica se un elemento del controllo visualizzazione elenco è visibile. Inviare questo messaggio in modo esplicito o utilizzando la macro [**\_ IsItemVisible di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_isitemvisible) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

Indice dell'elemento nel controllo visualizzazione elenco.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se visibile o **false** in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





