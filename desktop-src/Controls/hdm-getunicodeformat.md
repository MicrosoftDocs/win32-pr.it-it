---
title: Messaggio HDM_GETUNICODEFORMAT (COMmctrl. h)
description: Ottiene il flag del formato carattere Unicode per il controllo. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro GetUnicodeFormat dell'intestazione.
ms.assetid: 2b36265a-023c-4083-a755-769461f3804b
keywords:
- Controlli di Windows Message HDM_GETUNICODEFORMAT
topic_type:
- apiref
api_name:
- HDM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce625cc9d4c0ede0c4ce9b54dc852025b22d4870
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119830"
---
# <a name="hdm_getunicodeformat-message"></a>\_Messaggio HDM GETUNICODEFORMAT

Ottiene il flag del formato carattere Unicode per il controllo. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ GetUnicodeFormat dell'intestazione**](/windows/desktop/api/Commctrl/nf-commctrl-header_getunicodeformat) .

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

[**\_SETUNICODEFORMAT HDM**](hdm-setunicodeformat.md)
</dt> </dl>

 

 





