---
title: UDM_GETUNICODEFORMAT messaggio (Commctrl.h)
description: 'UDM_GETUNICODEFORMAT messaggio: recupera il flag di formato carattere Unicode per il controllo.'
ms.assetid: 8c09d37b-95a2-49cd-b578-919f9c39fa8b
keywords:
- UDM_GETUNICODEFORMAT di controllo Windows messaggio
topic_type:
- apiref
api_name:
- UDM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbce0af6ad559524d7662a0ce386777a5186777a4cb65b4270fc7c4c9bdff70d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957750"
---
# <a name="udm_getunicodeformat-message"></a>Messaggio UDM \_ GETUNICODEFORMAT

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

[**UDM \_ SETUNICODEFORMAT**](udm-setunicodeformat.md)
</dt> </dl>

 

 





