---
title: Messaggio MCM_GETUNICODEFORMAT (COMmctrl. h)
description: Recupera il flag del formato carattere Unicode per il controllo. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro GetUnicodeFormat di MonthCal.
ms.assetid: 28261e11-0fd0-407e-9f62-446536d62460
keywords:
- Controlli di Windows Message MCM_GETUNICODEFORMAT
topic_type:
- apiref
api_name:
- MCM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4be573923f154958e1defd0be2adb02068076950
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743575"
---
# <a name="mcm_getunicodeformat-message"></a>\_Messaggio GETUNICODEFORMAT MCM

Recupera il flag del formato carattere Unicode per il controllo. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ GetUnicodeFormat di MonthCal**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getunicodeformat) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il flag di formato Unicode per il controllo. Se questo valore è diverso da zero, il controllo utilizza caratteri Unicode. Se questo valore è zero, il controllo utilizza caratteri ANSI.

## <a name="remarks"></a>Commenti

Per una descrizione di questo messaggio, vedere la sezione Osservazioni per [**CCM \_ GETUNICODEFORMAT**](ccm-getunicodeformat.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_SETUNICODEFORMAT MCM**](mcm-setunicodeformat.md)
</dt> </dl>

 

 





