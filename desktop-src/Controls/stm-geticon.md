---
title: Messaggio STM_GETICON (winuser. h)
description: Un'applicazione invia il \_ messaggio STM GetIcon per recuperare un handle per l'icona associata a un controllo statico con \_ stile icona SS.
ms.assetid: e6b0a006-696b-401d-b894-b1db697c8939
keywords:
- Controlli di Windows Message STM_GETICON
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
ms.openlocfilehash: f64f55d2a2f8315b99526e51a69891f6f0056e8b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119231"
---
# <a name="stm_geticon-message"></a>\_Messaggio STM GETicon

Un'applicazione invia il messaggio **STM \_ GetIcon** per recuperare un handle per l'icona associata a un controllo statico con \_ stile icona SS.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilizzato; deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilizzato; deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è un handle per l'icona oppure **null** se il controllo statico non dispone di un'icona associata o se si è verificato un errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ICONA di STM \_**](stm-seticon.md)
</dt> </dl>

 

 





