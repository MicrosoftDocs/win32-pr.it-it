---
title: IPM_SETADDRESS messaggio (Commctrl.h)
description: Imposta i valori degli indirizzi per tutti e quattro i campi nel controllo degli indirizzi IP.
ms.assetid: 52e72437-3558-4789-844f-5ab5b0b7967c
keywords:
- IPM_SETADDRESS di controllo Windows messaggio
topic_type:
- apiref
api_name:
- IPM_SETADDRESS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54817d2206295432e9b477532268a000fc43047ae928ab02224d668912474519
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434491"
---
# <a name="ipm_setaddress-message"></a>Messaggio \_ IPM SETADDRESS

Imposta i valori degli indirizzi per tutti e quattro i campi nel controllo degli indirizzi IP.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Valore **DWORD** che contiene il nuovo indirizzo. Il valore del campo 3 è contenuto nei bit da 0 a 7. Il valore del campo 2 è contenuto nei bit da 8 a 15. Il valore del campo 1 è contenuto nei bit da 16 a 23. Il valore del campo 0 è contenuto nei bit da 24 a 31. La macro [**MAKEIPADDRESS**](/windows/desktop/api/Commctrl/nf-commctrl-makeipaddress) può essere usata anche per creare le informazioni sull'indirizzo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito non viene usato.

## <a name="remarks"></a>Commenti

Questo messaggio non genera una notifica [**\_ FIELDCHANGED IPN.**](ipn-fieldchanged.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





