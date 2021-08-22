---
title: CCM_GETUNICODEFORMAT messaggio (Commctrl.h)
description: Ottiene il flag di formato carattere Unicode per il controllo .
ms.assetid: 8a23cd1c-549e-4d48-891a-b37dbf5c524b
keywords:
- CCM_GETUNICODEFORMAT controlli Windows messaggio
topic_type:
- apiref
api_name:
- CCM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa115ba341478990b46600bc76ee02e4ecf750d5a7ccde9f1110aa8856d30fa7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119438281"
---
# <a name="ccm_getunicodeformat-message"></a>Messaggio \_ CCM GETUNICODEFORMAT

Ottiene il flag di formato carattere Unicode per il controllo .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il flag di formato Unicode per il controllo. Se questo valore è diverso da zero, il controllo utilizza caratteri Unicode. Se questo valore è zero, il controllo utilizza caratteri ANSI.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CCM \_ SETUNICODEFORMAT**](ccm-setunicodeformat.md)
</dt> </dl>

 

 





