---
title: TTM_SETMAXTIPWIDTH messaggio (Commctrl.h)
description: Imposta la larghezza massima per una finestra della descrizione comando.
ms.assetid: 3cfb6011-d0c3-4a57-aead-d4ec09a057cc
keywords:
- TTM_SETMAXTIPWIDTH dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- TTM_SETMAXTIPWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d344a3abcbe2b3bf57a71c8020d383f76ab1922b9009cd69411912d4468fa19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119433761"
---
# <a name="ttm_setmaxtipwidth-message"></a>TTM \_ SETMAXTIPWIDTH message

Imposta la larghezza massima per una finestra della descrizione comando.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Larghezza massima della finestra della descrizione comando oppure -1 per consentire qualsiasi larghezza.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce la larghezza massima della descrizione comando precedente.

## <a name="remarks"></a>Commenti

Il valore di larghezza massima non indica la larghezza effettiva di una finestra della descrizione comando. Se invece una stringa di descrizione comando supera la larghezza massima, il controllo suddivide il testo in più righe, usando spazi per determinare le interruzioni di riga. Se il testo non può essere segmentato in più righe, viene visualizzato su una singola riga, che può superare la larghezza massima della descrizione comando.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TTM \_ GETMAXTIPWIDTH**](ttm-getmaxtipwidth.md)
</dt> </dl>

 

 





