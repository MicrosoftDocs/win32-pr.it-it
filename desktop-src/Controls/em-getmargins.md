---
title: EM_GETMARGINS messaggio (Winuser.h)
description: Ottiene le larghezze dei margini sinistro e destro per un controllo di modifica.
ms.assetid: 2482354b-aae0-4abd-8287-65c423f30abb
keywords:
- EM_GETMARGINS dei controlli Windows messaggio
topic_type:
- apiref
api_name:
- EM_GETMARGINS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33746bc44a7b1b0aadd11c573675fedd51e565a557da7601ebe35a4442ddc96c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119541071"
---
# <a name="em_getmargins-message"></a>Messaggio \_ EM GETMARGINS

Ottiene le larghezze dei margini sinistro e destro per un controllo di modifica.

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

Restituisce la larghezza del margine sinistro in LOWORD e la larghezza del margine destro in HIWORD.

## <a name="remarks"></a>Commenti

**Rich Edit:** Il **\_ messaggio EM GETMARGINS** non è supportato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**EM \_ SETMARGINS**](em-setmargins.md)
</dt> </dl>

 

 





