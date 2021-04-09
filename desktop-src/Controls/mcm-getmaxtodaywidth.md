---
title: Messaggio MCM_GETMAXTODAYWIDTH (COMmctrl. h)
description: Recupera la larghezza massima di \ 0034; Today \ 0034; stringa in un controllo di calendario mensile. Sono inclusi il testo dell'etichetta e il testo della data. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro MonthCal GetMaxTodayWidth.
ms.assetid: bb55c24e-ba04-4a57-97b0-ff04d77e1d43
keywords:
- Controlli di Windows Message MCM_GETMAXTODAYWIDTH
topic_type:
- apiref
api_name:
- MCM_GETMAXTODAYWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d2b4c188e994a1dcc5a8fbd80ae3f1b06894bfb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741818"
---
# <a name="mcm_getmaxtodaywidth-message"></a>\_Messaggio GETMAXTODAYWIDTH MCM

Recupera la larghezza massima della stringa "Today" in un controllo di calendario mensile. Sono inclusi il testo dell'etichetta e il testo della data. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MonthCal \_ GetMaxTodayWidth**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmaxtodaywidth) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce la larghezza, in pixel, della stringa "Today".

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





