---
title: TB_GETUNICODEFORMAT messaggio (Commctrl.h)
description: 'TB_GETUNICODEFORMAT messaggio: recupera il flag di formato carattere Unicode per il controllo.'
ms.assetid: aadce646-daf1-4f1e-9171-2aeac12d3484
keywords:
- TB_GETUNICODEFORMAT controlli di Windows messaggio
topic_type:
- apiref
api_name:
- TB_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa59269813dde63f15980abc919e50cfaf4dcf5a3c86da311f2aa5206618e88e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061371"
---
# <a name="tb_getunicodeformat-message"></a>MESSAGGIO \_ GETUNICODEFORMAT DA TB

Recupera il flag di formato carattere Unicode per il controllo .

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

[**TB \_ SETUNICODEFORMAT**](tb-setunicodeformat.md)
</dt> </dl>

 

 





