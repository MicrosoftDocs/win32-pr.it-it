---
title: CB_SHOWDROPDOWN messaggio (Winuser.h)
description: Un'applicazione invia un messaggio CB SHOWDROPDOWN per visualizzare o nascondere la casella di riepilogo di una casella combinata con lo stile CBS DROPDOWN o \_ \_ CBS \_ DROPDOWNLIST.
ms.assetid: 32b995d7-eed6-4173-8525-0d356dea39b3
keywords:
- CB_SHOWDROPDOWN di controllo Windows messaggio
topic_type:
- apiref
api_name:
- CB_SHOWDROPDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c820c65c053f7acbcffb379228ea5f7720476b6d2165ac4988ce8789e912cdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117832239"
---
# <a name="cb_showdropdown-message"></a>Messaggio CB \_ SHOWDROPDOWN

Un'applicazione invia un **messaggio CB \_ SHOWDROPDOWN** per visualizzare o nascondere la casella di riepilogo di una casella combinata con lo stile [**CBS \_ DROPDOWN**](combo-box-styles.md) o [**CBS \_ DROPDOWNLIST.**](combo-box-styles.md)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

VALORE **BOOL** che specifica se la casella di riepilogo a discesa deve essere visualizzata o nascosta. Il valore **TRUE mostra** la casella di riepilogo. il valore **FALSE** lo nasconde.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è sempre **TRUE.**

## <a name="remarks"></a>Commenti

Questo messaggio non ha effetto su una casella combinata creata con lo [**stile \_ SIMPLE di CBS.**](combo-box-styles.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CB \_ GETDROPPEDSTATE**](cb-getdroppedstate.md)
</dt> </dl>

 

 





