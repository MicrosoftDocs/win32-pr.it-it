---
title: UDM_SETBASE messaggio (Commctrl.h)
description: Imposta la base di base per un controllo di tipo up-down. Il valore di base determina se nella finestra del controllo vengono visualizzati numeri in cifre decimali o esadecimali. I numeri esadecimali sono sempre senza segno e i numeri decimali sono con segno.
ms.assetid: c76cdec1-e73b-4b4b-89be-9a00ff2ea172
keywords:
- UDM_SETBASE di controllo Windows messaggio
topic_type:
- apiref
api_name:
- UDM_SETBASE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f9fd3750a70e676c3e9f32efe9ff0bfd9b300b812d09f4a04c34e4a90f36933
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118669079"
---
# <a name="udm_setbase-message"></a>Messaggio SETBASE UDM \_

Imposta la base di base per un controllo di tipo up-down. Il valore di base determina se nella finestra del controllo vengono visualizzati numeri in cifre decimali o esadecimali. I numeri esadecimali sono sempre senza segno e i numeri decimali sono con segno.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Nuovo valore di base per il controllo. Questo parametro può essere 10 per decimal o 16 per esadecimale.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è il valore di base precedente. Se viene specificata una base non valida, il valore restituito è zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





