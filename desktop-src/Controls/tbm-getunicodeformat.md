---
title: TBM_GETUNICODEFORMAT messaggio (Commctrl.h)
description: 'TBM_GETUNICODEFORMAT messaggio: recupera il flag di formato carattere Unicode per il controllo.'
ms.assetid: cecd7e55-f482-4381-bde8-a60b8c5173eb
keywords:
- TBM_GETUNICODEFORMAT dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- TBM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e15f5b12a60b58958dad1364848120f391c91906bb6057727f3a4e22b8a7813
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046171"
---
# <a name="tbm_getunicodeformat-message"></a>Messaggio \_ TBM GETUNICODEFORMAT

Recupera il flag di formato carattere Unicode per il controllo.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il flag di formato Unicode per il controllo. Se questo valore è diverso da zero, il controllo usa caratteri Unicode. Se questo valore è zero, il controllo usa caratteri ANSI.

## <a name="remarks"></a>Commenti

Per una descrizione di questo messaggio, vedere le osservazioni per [**CCM \_ GETUNICODEFORMAT.**](ccm-getunicodeformat.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TBM \_ SETUNICODEFORMAT**](tbm-setunicodeformat.md)
</dt> </dl>

 

 





