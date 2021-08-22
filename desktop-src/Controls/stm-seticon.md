---
title: STM_SETICON messaggio (Winuser.h)
description: Un'applicazione invia il messaggio \_ STM SETICON per associare un'icona a un controllo icona.
ms.assetid: 105b0667-8e23-47ed-9fb1-0792a22d7100
keywords:
- STM_SETICON dei messaggi Windows controllo
topic_type:
- apiref
api_name:
- STM_SETICON
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55ff1cbaa6a1083751b3619392fbb0d3b60695e829907c2dfe27fdb41170e167
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119281421"
---
# <a name="stm_seticon-message"></a>Messaggio STM \_ SETICON

Un'applicazione invia il **messaggio STM \_ SETICON** per associare un'icona a un controllo icona.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle all'icona da associare al controllo icona.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è un handle per l'icona associata in precedenza al controllo icona oppure zero se si verifica un errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**STM \_ GETICON**](stm-geticon.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**LoadIcon**](/windows/desktop/api/winuser/nf-winuser-loadicona)
</dt> </dl>

 

