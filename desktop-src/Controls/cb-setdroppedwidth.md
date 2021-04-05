---
title: Messaggio CB_SETDROPPEDWIDTH (winuser. h)
description: Un'applicazione invia il \_ messaggio CB SETDROPPEDWIDTH per impostare la larghezza minima consentita, in pixel, della casella di riepilogo di una casella combinata con lo \_ stile di menu a discesa CBS o CBS \_ DropDownList.
ms.assetid: 89f44733-aebe-44ea-b62d-8bd988f1bd6f
keywords:
- Controlli di Windows Message CB_SETDROPPEDWIDTH
topic_type:
- apiref
api_name:
- CB_SETDROPPEDWIDTH
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4c4f5ce64bfb1b48e9e811027792a11e4358edc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873789"
---
# <a name="cb_setdroppedwidth-message"></a>\_Messaggio SETDROPPEDWIDTH CB

Un'applicazione invia il messaggio **CB \_ SETDROPPEDWIDTH** per impostare la larghezza minima consentita, in pixel, della casella di riepilogo di una casella combinata con lo stile di [**menu a \_ discesa CBS**](combo-box-styles.md) o [**CBS \_ DropDownList**](combo-box-styles.md) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Larghezza minima consentita della casella di riepilogo, in pixel.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il messaggio ha esito positivo, il valore restituito è la nuova larghezza della casella di riepilogo.

Se il messaggio ha esito negativo, il valore restituito è CB \_ Err.

## <a name="remarks"></a>Commenti

Per impostazione predefinita, la larghezza minima consentita della casella di riepilogo a discesa è zero. La larghezza della casella di riepilogo è la larghezza minima consentita o la larghezza della casella combinata, a seconda del valore maggiore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CB \_ GETDROPPEDWIDTH**](cb-getdroppedwidth.md)
</dt> </dl>

 

 





