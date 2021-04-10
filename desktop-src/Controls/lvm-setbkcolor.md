---
title: Messaggio LVM_SETBKCOLOR (COMmctrl. h)
description: Imposta il colore di sfondo di un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro SetBkColor di ListView.
ms.assetid: d579249d-421d-4e7e-8992-4c7fd7277593
keywords:
- Controlli di Windows Message LVM_SETBKCOLOR
topic_type:
- apiref
api_name:
- LVM_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80977ed6c95a1353889265e52cfc05c26aaa2a5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964472"
---
# <a name="lvm_setbkcolor-message"></a>\_Messaggio SETBKCOLOR LVM

Imposta il colore di sfondo di un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ SetBkColor di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setbkcolor) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Colore di sfondo da impostare o \_ valore CLR None per nessun colore di sfondo. I controlli visualizzazione elenco con i colori di sfondo si ritraggono molto più velocemente rispetto a quelli senza colori di sfondo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





