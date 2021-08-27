---
title: UDM_GETPOS32 messaggio (Commctrl.h)
description: Restituisce la posizione a 32 bit di un controllo verso l'alto.
ms.assetid: 90feffbd-a472-446f-8a67-5da408cde002
keywords:
- UDM_GETPOS32 di controllo Windows messaggio
topic_type:
- apiref
api_name:
- UDM_GETPOS32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a11d043ca4f6b69a554b43d5abeaf35e4c2a2a6d72797e829900529df70b6c47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120059791"
---
# <a name="udm_getpos32-message"></a>Messaggio GETPOS32 di UDM \_

Restituisce la posizione a 32 bit di un controllo verso l'alto.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a **un valore BOOL** impostato su zero se il valore viene recuperato correttamente o diverso da zero se si verifica un errore. Se questo parametro è impostato su **NULL,** gli errori non vengono segnalati.

Se **UDM \_ GETPOS32** viene usato in una situazione cross-process, questo parametro deve essere **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce la posizione di un controllo verso l'alto con precisione a 32 bit. Le applicazioni devono controllare il *valore lParam* per determinare se il valore restituito è valido.

## <a name="remarks"></a>Commenti

Quando elabora questo messaggio, il controllo up-down aggiorna la posizione corrente in base alla didascalia della finestra degli amici. Restituisce un errore se non è presente alcuna finestra di controllo o se la didascalia specifica un valore non valido o non compreso nell'intervallo.

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

[**UDM \_ GETPOS**](udm-getpos.md)
</dt> <dt>

[**UDM \_ SETPOS**](udm-setpos.md)
</dt> <dt>

[**UDM \_ SETPOS32**](udm-setpos32.md)
</dt> </dl>

 

 





