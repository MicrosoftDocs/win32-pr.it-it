---
title: CB_SETDROPPEDWIDTH messaggio (Winuser.h)
description: Un'applicazione invia il messaggio CB SETDROPPEDWIDTH per impostare la larghezza minima consentita, in pixel, della casella di riepilogo di una casella combinata con lo stile CBS DROPDOWN o \_ \_ CBS \_ DROPDOWNLIST.
ms.assetid: 89f44733-aebe-44ea-b62d-8bd988f1bd6f
keywords:
- CB_SETDROPPEDWIDTH dei messaggi Windows controlli
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
ms.openlocfilehash: 05d59aee89c4be18ba8e5013fa1a1e685a56b727d293c833c7f99140b683efeb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089051"
---
# <a name="cb_setdroppedwidth-message"></a>Messaggio CB \_ SETDROPPEDWIDTH

Un'applicazione invia il messaggio **CB \_ SETDROPPEDWIDTH** per impostare la larghezza minima consentita, in pixel, della casella di riepilogo di una casella combinata con lo stile [**CBS \_ DROPDOWN**](combo-box-styles.md) o [**CBS \_ DROPDOWNLIST.**](combo-box-styles.md)

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

Se il messaggio ha esito negativo, il valore restituito è CB \_ ERR.

## <a name="remarks"></a>Commenti

Per impostazione predefinita, la larghezza minima consentita della casella di riepilogo a discesa è zero. La larghezza della casella di riepilogo è la larghezza minima consentita o la larghezza della casella combinata, a seconda di quale sia maggiore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CB \_ GETDROPPEDWIDTH**](cb-getdroppedwidth.md)
</dt> </dl>

 

 





