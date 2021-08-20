---
title: MCM_GETUNICODEFORMAT messaggio (Commctrl.h)
description: Recupera il flag di formato carattere Unicode per il controllo . È possibile inviare questo messaggio in modo esplicito o usare la \_ macro MonthCal GetUnicodeFormat.
ms.assetid: 28261e11-0fd0-407e-9f62-446536d62460
keywords:
- MCM_GETUNICODEFORMAT di Windows messaggi
topic_type:
- apiref
api_name:
- MCM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1253fe4164067a484164f8198cda5c1f95a7f63a77acbfbf0ec563b3fec8401d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118005402"
---
# <a name="mcm_getunicodeformat-message"></a>Messaggio \_ MCM GETUNICODEFORMAT

Recupera il flag di formato carattere Unicode per il controllo . È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ MonthCal GetUnicodeFormat.**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getunicodeformat)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il flag di formato Unicode per il controllo. Se questo valore è diverso da zero, il controllo utilizza caratteri Unicode. Se questo valore è zero, il controllo utilizza caratteri ANSI.

## <a name="remarks"></a>Commenti

Per una descrizione di questo messaggio, vedere le osservazioni relative a [**CCM \_ GETUNICODEFORMAT.**](ccm-getunicodeformat.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCM \_ SETUNICODEFORMAT**](mcm-setunicodeformat.md)
</dt> </dl>

 

 





