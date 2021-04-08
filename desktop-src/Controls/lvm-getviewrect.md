---
title: Messaggio LVM_GETVIEWRECT (COMmctrl. h)
description: Recupera il rettangolo di delimitazione di tutti gli elementi nel controllo elenco-visualizzazione. La visualizzazione elenco deve essere visualizzata nell'icona o nella visualizzazione icona piccola. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro GetViewRect di ListView.
ms.assetid: 69b96f86-8b7e-42c1-ad73-f9b2732ab9f9
keywords:
- Controlli di Windows Message LVM_GETVIEWRECT
topic_type:
- apiref
api_name:
- LVM_GETVIEWRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d4c4fdf0e8466d3fb0b2ad164241c3f6a541570
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048642"
---
# <a name="lvm_getviewrect-message"></a>\_Messaggio GETVIEWRECT LVM

Recupera il rettangolo di delimitazione di tutti gli elementi nel controllo elenco-visualizzazione. La visualizzazione elenco deve essere visualizzata nell'icona o nella visualizzazione icona piccola. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ GetViewRect di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getviewrect) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) che riceve il rettangolo di delimitazione. Tutte le coordinate sono relative all'area visibile del controllo visualizzazione elenco.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

