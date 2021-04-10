---
title: Messaggio CB_SHOWDROPDOWN (winuser. h)
description: Un'applicazione invia un \_ messaggio CB SHOWDROPDOWN per mostrare o nascondere la casella di riepilogo di una casella combinata con lo \_ stile di menu a discesa CBS o CBS \_ DropDownList.
ms.assetid: 32b995d7-eed6-4173-8525-0d356dea39b3
keywords:
- Controlli di Windows Message CB_SHOWDROPDOWN
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
ms.openlocfilehash: fb66e9a0ecf3b6680fce9aca7f680fd6e6fd13e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121054"
---
# <a name="cb_showdropdown-message"></a>\_Messaggio SHOWDROPDOWN CB

Un'applicazione invia un messaggio **CB \_ SHOWDROPDOWN** per mostrare o nascondere la casella di riepilogo di una casella combinata con lo stile di [**menu a \_ discesa CBS**](combo-box-styles.md) o [**CBS \_ DropDownList**](combo-box-styles.md) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Valore **booleano** che specifica se la casella di riepilogo a discesa deve essere mostrata o nascosta. Il valore **true** Mostra la casella di riepilogo; il valore **false** lo nasconde.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è sempre **true**.

## <a name="remarks"></a>Commenti

Questo messaggio non ha alcun effetto su una casella combinata creata con lo stile [**\_ semplice CBS**](combo-box-styles.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CB \_ GETDROPPEDSTATE**](cb-getdroppedstate.md)
</dt> </dl>

 

 





