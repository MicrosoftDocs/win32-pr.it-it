---
title: UDM_SETPOS32 messaggio (Commctrl.h)
description: Imposta la posizione di un controllo verso l'alto con precisione a 32 bit.
ms.assetid: a337f2a1-0e3d-4ff4-a224-57b7f25c4bd0
keywords:
- UDM_SETPOS32 controlli Windows messaggio
topic_type:
- apiref
api_name:
- UDM_SETPOS32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83d8dee48c580df72a32bb2072b00cc2dfbdf38b386825d686e8bc8510ba47e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088421"
---
# <a name="udm_setpos32-message"></a>Messaggio SETPOS32 di UDM \_

Imposta la posizione di un controllo verso l'alto con precisione a 32 bit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Variabile di tipo Integer che specifica la nuova posizione per il controllo verso l'alto. Se il parametro non è compreso nell'intervallo specificato del controllo, *lParam* viene impostato sul valore valido più vicino.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce la posizione precedente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**UDM \_ GETPOS**](udm-getpos.md)
</dt> <dt>

[**UDM \_ SETPOS**](udm-setpos.md)
</dt> <dt>

[**UDM \_ GETPOS32**](udm-getpos32.md)
</dt> </dl>

 

 





