---
title: Messaggio CB_GETDROPPEDWIDTH (winuser. h)
description: Ottiene la larghezza minima consentita, in pixel, della casella di riepilogo di una casella combinata con l'elenco a \_ discesa CBS o \_ lo stile DropDownList CBS.
ms.assetid: d7f37a6c-a623-4b15-8ef7-4b64d85c15fa
keywords:
- Controlli di Windows Message CB_GETDROPPEDWIDTH
topic_type:
- apiref
api_name:
- CB_GETDROPPEDWIDTH
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 299b360348a6bf7378fdfc9bc9f0959b01366642
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048362"
---
# <a name="cb_getdroppedwidth-message"></a>\_Messaggio GETDROPPEDWIDTH CB

Ottiene la larghezza minima consentita, in pixel, della casella di riepilogo di una casella combinata con l'elenco a [**\_ discesa CBS**](combo-box-styles.md) o lo stile [**\_ DropDownList CBS**](combo-box-styles.md) .

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

Se il messaggio ha esito positivo, il valore restituito è la larghezza, in pixel.

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

[**CB \_ SETDROPPEDWIDTH**](cb-setdroppedwidth.md)
</dt> </dl>

 

 





