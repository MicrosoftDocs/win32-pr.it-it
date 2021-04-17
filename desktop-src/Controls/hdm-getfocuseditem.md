---
title: Messaggio HDM_GETFOCUSEDITEM (COMmctrl. h)
description: Ottiene l'elemento in un controllo intestazione con lo stato attivo. Inviare questo messaggio in modo esplicito o utilizzando la \_ macro GetFocusedItem dell'intestazione.
ms.assetid: 9ad8e497-6f81-4226-b138-d1101f2fd8b3
keywords:
- Controlli di Windows Message HDM_GETFOCUSEDITEM
topic_type:
- apiref
api_name:
- HDM_GETFOCUSEDITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c21fcb29f5f431e32ca3f07265b7e96620d5a67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477585"
---
# <a name="hdm_getfocuseditem-message"></a>\_Messaggio HDM GETFOCUSEDITEM

Ottiene l'elemento in un controllo intestazione con lo stato attivo. Inviare questo messaggio in modo esplicito o utilizzando la macro [**\_ GetFocusedItem dell'intestazione**](/windows/desktop/api/Commctrl/nf-commctrl-header_getfocuseditem) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Non usato. Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Non usato. Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'indice dell'elemento nello stato attivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Informazioni sui controlli intestazione](header-controls.md)
</dt> </dl>

 

 





