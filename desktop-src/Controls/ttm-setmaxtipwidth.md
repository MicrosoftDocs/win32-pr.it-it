---
title: Messaggio TTM_SETMAXTIPWIDTH (COMmctrl. h)
description: Imposta la larghezza massima per una finestra della descrizione comando.
ms.assetid: 3cfb6011-d0c3-4a57-aead-d4ec09a057cc
keywords:
- Controlli di Windows Message TTM_SETMAXTIPWIDTH
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
ms.openlocfilehash: 55ce930b289205b5fb0d2768068b8cb28cd11aec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104225209"
---
# <a name="ttm_setmaxtipwidth-message"></a>\_Messaggio TTM SETMAXTIPWIDTH

Imposta la larghezza massima per una finestra della descrizione comando.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Lunghezza massima della finestra ToolTip oppure-1 per consentire qualsiasi larghezza.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce la larghezza massima precedente della descrizione comando.

## <a name="remarks"></a>Commenti

Il valore di larghezza massima non indica la larghezza effettiva della finestra descrizione comando. Se invece una stringa della descrizione comando supera la larghezza massima, il controllo suddivide il testo in più righe, usando spazi per determinare le interruzioni di riga. Se il testo non può essere segmentato in più righe, viene visualizzato su una sola riga, che può superare la larghezza massima della descrizione comando.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_GETMAXTIPWIDTH TTM**](ttm-getmaxtipwidth.md)
</dt> </dl>

 

 





