---
title: Messaggio UDM_GETRANGE32 (COMmctrl. h)
description: Recupera l'intervallo di 32 bit di un controllo di scorrimento.
ms.assetid: a94b50c9-cd2f-430d-875f-720e51f544f1
keywords:
- Controlli di Windows Message UDM_GETRANGE32
topic_type:
- apiref
api_name:
- UDM_GETRANGE32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca418cd08dc4c81b3ff734d74f3ca9deeef7d848
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476289"
---
# <a name="udm_getrange32-message"></a>\_Messaggio UDM GETRANGE32

Recupera l'intervallo di 32 bit di un controllo di scorrimento.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Puntatore a un intero con segno che riceve il limite inferiore dell'intervallo di controllo di scorrimento. Questo parametro può essere **null**.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a un intero con segno che riceve il limite superiore dell'intervallo di controllo di scorrimento. Questo parametro può essere **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito per questo messaggio non viene utilizzato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





