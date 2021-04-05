---
title: Messaggio CB_RESETCONTENT (winuser. h)
description: Rimuove tutti gli elementi dalla casella di riepilogo e il controllo di modifica di una casella combinata.
ms.assetid: 55203c34-87ca-46e9-a914-a480d43ccadd
keywords:
- Controlli di Windows Message CB_RESETCONTENT
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
ms.openlocfilehash: 3567f31ef98fffe42e53c4811acc786d41ae9f78
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873793"
---
# <a name="cb_resetcontent-message"></a>\_Messaggio ResetContent CB

Rimuove tutti gli elementi dalla casella di riepilogo e il controllo di modifica di una casella combinata.

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

Questo messaggio restituisce sempre CB \_ OK.

## <a name="remarks"></a>Commenti

Se si crea la casella combinata con uno stile disegnato dal proprietario ma senza lo stile [**CBS \_ HASSTRINGS**](combo-box-styles.md) , il proprietario della casella combinata riceve un messaggio [**WM \_ DeleteItem**](wm-deleteitem.md) per ogni elemento nella casella combinata.

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

[**CB \_ DELETESTRING**](cb-deletestring.md)
</dt> <dt>

[**\_DeleteItem WM**](wm-deleteitem.md)
</dt> </dl>

 

 





