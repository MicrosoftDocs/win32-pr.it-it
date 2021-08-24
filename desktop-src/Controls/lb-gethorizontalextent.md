---
title: LB_GETHORIZONTALEXTENT messaggio (Winuser.h)
description: Ottiene la larghezza, in pixel, di scorrimento orizzontale di una casella di riepilogo (larghezza scorrevole) se la casella di riepilogo dispone di una barra di scorrimento orizzontale.
ms.assetid: 52461724-c06a-436a-ac95-94c5189ba37e
keywords:
- LB_GETHORIZONTALEXTENT del messaggio Windows controlli
topic_type:
- apiref
api_name:
- LB_GETHORIZONTALEXTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01f754b62ad0f51a236662fdfba2304221d58e1288e2756c0330343c63a0699e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799511"
---
# <a name="lb_gethorizontalextent-message"></a>Messaggio \_ LB GETHORIZONTALEXTENT

Ottiene la larghezza, in pixel, di scorrimento orizzontale di una casella di riepilogo (larghezza scorrevole) se la casella di riepilogo dispone di una barra di scorrimento orizzontale.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non usato; deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Non usato; deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è la larghezza scorrevole, in pixel, della casella di riepilogo.

## <a name="remarks"></a>Commenti

Per rispondere al messaggio **LB \_ GETHORIZONTALEXTENT,** la casella di riepilogo deve essere stata definita con lo [**stile \_ HSCROLL WS.**](/windows/desktop/winmsg/window-styles)

Se l'applicazione non imposta l'extent orizzontale della casella di riepilogo (usando [**\_ LB SETHORIZONTALEXTENT),**](lb-sethorizontalextent.md)l'extent orizzontale predefinito è zero. Si noti che la casella di riepilogo non aggiorna dinamicamente l'extent orizzontale.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LB \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md)
</dt> </dl>

 

