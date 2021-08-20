---
title: EM_GETTEXTRANGE messaggio (Richedit.h)
description: Recupera un intervallo specificato di caratteri da un controllo Rich Edit.
ms.assetid: 18398963-eb2c-4f64-99f5-9614a5d34b52
keywords:
- EM_GETTEXTRANGE di controllo Windows messaggio
topic_type:
- apiref
api_name:
- EM_GETTEXTRANGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e12282b970c38164e5b28a31ed778a3320f88bbdf16b6d182586e492e5e699eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118006576"
---
# <a name="em_gettextrange-message"></a>Messaggio \_ EM GETTEXTRANGE

Recupera un intervallo specificato di caratteri da un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato. deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura TEXTRANGE**](/windows/win32/api/richedit/ns-richedit-textrangea) che specifica l'intervallo di caratteri da recuperare e un buffer in cui copiare i caratteri.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il messaggio restituisce il numero di caratteri copiati, senza includere il carattere Null di terminazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Textrange**](/windows/win32/api/richedit/ns-richedit-textrangea)
</dt> </dl>

 

 





