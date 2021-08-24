---
title: LB_ITEMFROMPOINT messaggio (Winuser.h)
description: Ottiene l'indice in base zero dell'elemento più vicino al punto specificato in una casella di riepilogo.
ms.assetid: 5739eccb-e708-4ddb-ac97-d3e6c6120842
keywords:
- LB_ITEMFROMPOINT dei messaggi Windows controllo
topic_type:
- apiref
api_name:
- LB_ITEMFROMPOINT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddddd58780cb4b140501c567d699373cb1fa03cbf212332bea71611a4add3788
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119575931"
---
# <a name="lb_itemfrompoint-message"></a>LB \_ ITEMFROMPOINT message

Ottiene l'indice in base zero dell'elemento più vicino al punto specificato in una casella di riepilogo.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> <dt>

*lParam* 
</dt> <dd>

La [**parola chiave LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifica la coordinata x di un punto, relativa all'angolo superiore sinistro dell'area client della casella di riepilogo.

HiWORD [**specifica**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) la coordinata y di un punto, rispetto all'angolo superiore sinistro dell'area client della casella di riepilogo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito contiene l'indice dell'elemento più vicino in [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)). HIWORD [**è**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) zero se il punto specificato si trova nell'area client della casella di riepilogo o uno se si trova all'esterno dell'area client.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MAKELPARAM**](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> </dl>

 

