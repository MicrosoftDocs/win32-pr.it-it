---
title: UDM_GETPOS messaggio (Commctrl.h)
description: Recupera la posizione corrente di un controllo verso l'alto con precisione a 16 bit.
ms.assetid: 5f395de0-11b3-44f8-9bf4-42e27ce88a0c
keywords:
- UDM_GETPOS dei messaggi Windows controllo
topic_type:
- apiref
api_name:
- UDM_GETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e92ca5fe5d902980560b6879ac7c345230056987308a1e390b0af351281eac62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120059781"
---
# <a name="udm_getpos-message"></a>Messaggio GETPOS di UDM \_

Recupera la posizione corrente di un controllo verso l'alto con precisione a 16 bit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

In caso di esito positivo, [**la parola chiave HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) viene impostata su zero e [**la parola chiave LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) viene impostata sulla posizione corrente del controllo. Se si verifica un errore, **la parola chiave HIWORD** viene impostata su un valore diverso da zero.

## <a name="remarks"></a>Commenti

Durante l'elaborazione di questo messaggio, il controllo up-down aggiorna la posizione corrente in base alla didascalia della finestra dell'amico. Il controllo up-down restituisce un errore se non è presente alcuna finestra di tipo amico o se la didascalia specifica un valore non valido o non compreso nell'intervallo. Inoltre, viene impostato un flag di errore nella parola chiave HIWORD del valore restituito se il controllo viene creato senza lo stile [**\_ SETBUDDYINT UDS,**](up-down-control-styles.md) anche se restituisce un valore di posizione valido nella loWORD del valore restituito.

Se sono stati abilitati valori a 32 bit per un controllo up-down con [**UDM \_ SETRANGE32,**](udm-setrange32.md)questo messaggio restituisce solo i 16 bit inferiori della posizione. Per recuperare la posizione completa a 32 bit, usare [**UDM \_ GETPOS32**](udm-getpos32.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**UDM \_ GETRANGE**](udm-getrange.md)
</dt> <dt>

[**UDM \_ GETRANGE32**](udm-getrange32.md)
</dt> <dt>

[**UDM \_ SETPOS**](udm-setpos.md)
</dt> <dt>

[**SETRANGE32 di UDM \_**](udm-setrange32.md)
</dt> </dl>

 

