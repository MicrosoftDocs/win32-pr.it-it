---
title: TTM_GETMAXTIPWIDTH messaggio (Commctrl.h)
description: Recupera la larghezza massima per una finestra della descrizione comando.
ms.assetid: 0f0a5403-fe2e-4e5a-96c2-a435827a5fd7
keywords:
- TTM_GETMAXTIPWIDTH di controllo Windows messaggio
topic_type:
- apiref
api_name:
- TTM_GETMAXTIPWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bce561b254645932b214b48879aa0be04deb31b32e8dc591fc3183ec39871273
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751051"
---
# <a name="ttm_getmaxtipwidth-message"></a>Messaggio TTM \_ GETMAXTIPWIDTH

Recupera la larghezza massima per una finestra della descrizione comando.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **INT** che rappresenta la larghezza massima della descrizione comando, in pixel. Se in precedenza non è stata impostata alcuna larghezza massima, il messaggio restituisce -1.

## <a name="remarks"></a>Commenti

Il valore della larghezza massima della descrizione comando non indica la larghezza effettiva di una finestra della descrizione comando. Se invece una stringa di descrizione comando supera la larghezza massima, il controllo suddivide il testo in più righe, usando spazi per determinare le interruzioni di riga. Se il testo non può essere segmentato in più righe, verrà visualizzato su una singola riga. La lunghezza di questa riga può superare la larghezza massima della descrizione comando.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TTM \_ SETMAXTIPWIDTH**](ttm-setmaxtipwidth.md)
</dt> </dl>

 

 





