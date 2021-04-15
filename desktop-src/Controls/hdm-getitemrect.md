---
title: Messaggio HDM_GETITEMRECT (COMmctrl. h)
description: Ottiene il rettangolo di delimitazione per un elemento specificato in un controllo intestazione. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro GetItemRect dell'intestazione.
ms.assetid: b483ef97-3700-425b-8160-81c673850f68
keywords:
- Controlli di Windows Message HDM_GETITEMRECT
topic_type:
- apiref
api_name:
- HDM_GETITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4baec72bd914a9d2dad72556a5444c0059452cf3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477584"
---
# <a name="hdm_getitemrect-message"></a>\_Messaggio HDM GETITEMRECT

Ottiene il rettangolo di delimitazione per un elemento specificato in un controllo intestazione. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ GetItemRect dell'intestazione**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitemrect) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

Indice in base zero dell'elemento di controllo dell'intestazione per il quale recuperare il rettangolo di delimitazione.

</dd> <dt>

*lParam* \[ in uscita\]
</dt> <dd>

Puntatore a una struttura [**Rect**](/windows/win32/api/windef/ns-windef-rect) che riceve le informazioni sul rettangolo di delimitazione. Il mittente del messaggio è responsabile dell'allocazione della struttura. Le coordinate restituite nella struttura RECT sono espresse in relazione all'elemento padre del controllo Header.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





