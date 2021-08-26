---
title: STM_GETICON messaggio (Winuser.h)
description: Un'applicazione invia il messaggio STM GETICON per recuperare un handle per l'icona associata a un controllo \_ statico con lo stile \_ SS ICON.
ms.assetid: e6b0a006-696b-401d-b894-b1db697c8939
keywords:
- STM_GETICON dei messaggi Windows controllo
topic_type:
- apiref
api_name:
- STM_GETICON
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d33aab01e668f4b77e36a0a62b8eab75f3ee5db82188416c295c04cdf9bcb078
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084951"
---
# <a name="stm_geticon-message"></a>Messaggio \_ GETICON STM

Un'applicazione invia il **messaggio \_ STM GETICON** per recuperare un handle per l'icona associata a un controllo statico con lo stile \_ SS ICON.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non usato; deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Non usato; deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è un handle per l'icona oppure **NULL** se al controllo statico non è associata un'icona o se si è verificato un errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**STM \_ SETICON**](stm-seticon.md)
</dt> </dl>

 

 





