---
title: Messaggio TTM_GETMAXTIPWIDTH (COMmctrl. h)
description: Recupera la larghezza massima per una finestra della descrizione comando.
ms.assetid: 0f0a5403-fe2e-4e5a-96c2-a435827a5fd7
keywords:
- Controlli di Windows Message TTM_GETMAXTIPWIDTH
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
ms.openlocfilehash: f89c56692db9d451eb18db61af262cc0f3a715f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964239"
---
# <a name="ttm_getmaxtipwidth-message"></a>\_Messaggio TTM GETMAXTIPWIDTH

Recupera la larghezza massima per una finestra della descrizione comando.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **int** che rappresenta la larghezza massima della descrizione comando, in pixel. Se la larghezza massima non è stata impostata in precedenza, il messaggio restituisce-1.

## <a name="remarks"></a>Commenti

Il valore di larghezza massima della descrizione comando non indica la larghezza effettiva della finestra descrizione comando. Se invece una stringa della descrizione comando supera la larghezza massima, il controllo suddivide il testo in più righe, usando spazi per determinare le interruzioni di riga. Se il testo non può essere segmentato in più righe, verrà visualizzato su una sola riga. La lunghezza di questa riga può superare la larghezza massima della descrizione comando.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_SETMAXTIPWIDTH TTM**](ttm-setmaxtipwidth.md)
</dt> </dl>

 

 





