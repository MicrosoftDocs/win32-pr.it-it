---
title: CB_RESETCONTENT messaggio (Winuser.h)
description: Rimuove tutti gli elementi dalla casella di riepilogo e dal controllo di modifica di una casella combinata.
ms.assetid: 55203c34-87ca-46e9-a914-a480d43ccadd
keywords:
- CB_RESETCONTENT di controllo Windows messaggio
topic_type:
- apiref
api_name:
- CB_RESETCONTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4918437d7b0d347e071386486b31e5f4b9d948b4ff55b4c6eea6e3afe93fb1c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117832249"
---
# <a name="cb_resetcontent-message"></a>Messaggio CB \_ RESETCONTENT

Rimuove tutti gli elementi dalla casella di riepilogo e dal controllo di modifica di una casella combinata.

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

Questo messaggio restituisce sempre CB \_ OK.

## <a name="remarks"></a>Commenti

Se si crea la casella combinata con uno stile disegnato dal proprietario ma senza lo stile [**\_ CBS HASSTRINGS,**](combo-box-styles.md) il proprietario della casella combinata riceve un messaggio [**WM \_ DELETEITEM**](wm-deleteitem.md) per ogni elemento nella casella combinata.

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

[**CB \_ DELETESTRING**](cb-deletestring.md)
</dt> <dt>

[**WM \_ DELETEITEM**](wm-deleteitem.md)
</dt> </dl>

 

 





