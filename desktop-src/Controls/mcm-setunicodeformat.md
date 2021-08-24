---
title: MCM_SETUNICODEFORMAT messaggio (Commctrl.h)
description: 'MCM_SETUNICODEFORMAT messaggio: imposta il flag di formato carattere Unicode per il controllo.'
ms.assetid: 250789b5-694b-4502-9cc0-3bc260ea06e7
keywords:
- MCM_SETUNICODEFORMAT di controllo Windows messaggio
topic_type:
- apiref
api_name:
- MCM_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d5671384a43b4308ae08317137c00e213a5a7dbb37c5f0310d2d32e4716f176
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119435162"
---
# <a name="mcm_setunicodeformat-message"></a>Messaggio \_ MCM SETUNICODEFORMAT

Imposta il flag di formato carattere Unicode per il controllo. Questo messaggio consente di modificare il set di caratteri utilizzato dal controllo in fase di esecuzione anziché dover creare nuovamente il controllo. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ MonthCal SetUnicodeFormat.**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setunicodeformat)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Determina il set di caratteri utilizzato dal controllo . Se questo valore è diverso da zero, il controllo userà caratteri Unicode. Se questo valore è zero, il controllo userà caratteri ANSI.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il flag di formato Unicode precedente per il controllo.

## <a name="remarks"></a>Commenti

Per una descrizione di questo messaggio, vedere le osservazioni per [**CCM \_ SETUNICODEFORMAT.**](ccm-setunicodeformat.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCM \_ GETUNICODEFORMAT**](mcm-getunicodeformat.md)
</dt> </dl>

 

 





