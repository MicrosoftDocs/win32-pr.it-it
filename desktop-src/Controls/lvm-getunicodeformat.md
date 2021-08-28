---
title: LVM_GETUNICODEFORMAT messaggio (Commctrl.h)
description: Recupera il flag di formato carattere UNICODE per il controllo . È possibile inviare questo messaggio in modo esplicito o usare la \_ macro ListView GetUnicodeFormat.
ms.assetid: b0598b60-4d0e-4c68-b63a-e614c6268129
keywords:
- LVM_GETUNICODEFORMAT dei controlli Windows messaggio
topic_type:
- apiref
api_name:
- LVM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b3166d7349bf138fa853523c019a4c1db86e3f1a2d81a6da86c4ef25b5ed405
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019259"
---
# <a name="lvm_getunicodeformat-message"></a>Messaggio \_ LVM GETUNICODEFORMAT

Recupera il flag di formato carattere UNICODE per il controllo . È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ ListView GetUnicodeFormat.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getunicodeformat)

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

[**LVM \_ SETUNICODEFORMAT**](lvm-setunicodeformat.md)
</dt> </dl>

 

 





