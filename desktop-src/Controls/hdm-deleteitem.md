---
title: Messaggio HDM_DELETEITEM (COMmctrl. h)
description: Elimina un elemento da un controllo intestazione. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro DeleteItem dell'intestazione.
ms.assetid: 1dd1f233-2812-41ae-8a36-c42b9ac70ffc
keywords:
- Controlli di Windows Message HDM_DELETEITEM
topic_type:
- apiref
api_name:
- HDM_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6a3ec4b48c3dcc77579f70d26cd55b7127f5a6d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048521"
---
# <a name="hdm_deleteitem-message"></a>\_Messaggio HDM DeleteItem

Elimina un elemento da un controllo intestazione. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ DeleteItem dell'intestazione**](/windows/desktop/api/Commctrl/nf-commctrl-header_deleteitem) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice dell'elemento da eliminare.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





