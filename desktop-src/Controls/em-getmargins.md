---
title: Messaggio EM_GETMARGINS (winuser. h)
description: Ottiene le larghezze dei margini sinistro e destro per un controllo di modifica.
ms.assetid: 2482354b-aae0-4abd-8287-65c423f30abb
keywords:
- Controlli di Windows Message EM_GETMARGINS
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
ms.openlocfilehash: 239ad7e7888f5bceef60bf2719c3b67798b56220
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740298"
---
# <a name="em_getmargins-message"></a>\_Messaggio GETmargins em

Ottiene le larghezze dei margini sinistro e destro per un controllo di modifica.

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

Restituisce la larghezza del margine sinistro in LOWORD e la larghezza del margine destro in HIWORD.

## <a name="remarks"></a>Commenti

**Modifica avanzata:** Il **messaggio \_ GetMargins em** non è supportato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_margini em**](em-setmargins.md)
</dt> </dl>

 

 





