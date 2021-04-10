---
title: Messaggio STM_SETICON (winuser. h)
description: Un'applicazione invia il \_ messaggio dell'icona STM per associare un'icona a un controllo icona.
ms.assetid: 105b0667-8e23-47ed-9fb1-0792a22d7100
keywords:
- Controlli di Windows Message STM_SETICON
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
ms.openlocfilehash: cb9c7e2a007c1f866a1c73b3a1c1a55b157add47
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047916"
---
# <a name="stm_seticon-message"></a>\_Messaggio di icona STM

Un'applicazione invia il messaggio dell' **\_ icona STM** per associare un'icona a un controllo icona.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per l'icona da associare al controllo icona.

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
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**\_icona GetIcon STM**](stm-geticon.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**LoadIcon**](/windows/desktop/api/winuser/nf-winuser-loadicona)
</dt> </dl>

 

