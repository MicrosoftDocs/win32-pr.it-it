---
title: Messaggio HDM_GETOVERFLOWRECT (COMmctrl. h)
description: Ottiene il rettangolo di delimitazione del pulsante di overflow quando lo \_ stile di overflow HDS è impostato sul controllo intestazione e il pulsante di overflow è visibile. Inviare questo messaggio in modo esplicito o utilizzando la \_ macro GetOverflowRect dell'intestazione.
ms.assetid: 52fb3dc3-ce22-40da-8222-20fd75c005ae
keywords:
- Controlli di Windows Message HDM_GETOVERFLOWRECT
topic_type:
- apiref
api_name:
- HDM_GETOVERFLOWRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58f521bb6b188a10bb7af52ead46423e7ae0cf58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518118"
---
# <a name="hdm_getoverflowrect-message"></a>\_Messaggio HDM GETOVERFLOWRECT

Ottiene il rettangolo di delimitazione del pulsante di overflow quando lo stile di [**\_ overflow HDS**](header-control-styles.md) è impostato sul controllo intestazione e il pulsante di overflow è visibile. Inviare questo messaggio in modo esplicito o utilizzando la macro [**\_ GetOverflowRect dell'intestazione**](/windows/desktop/api/Commctrl/nf-commctrl-header_getoverflowrect) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non usato. Deve essere zero.

</dd> <dt>

*lParam* \[ in\]
</dt> <dd>

Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) per ricevere le informazioni sul rettangolo di delimitazione. Il mittente del messaggio è responsabile dell'allocazione della struttura. Le coordinate restituite nella struttura **Rect** sono espresse come coordinate dello schermo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo; in caso contrario, **false**.

## <a name="remarks"></a>Commenti

Il controllo intestazione deve avere lo stile **HDF \_ SPLITBUTTON**.

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

 

