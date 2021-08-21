---
title: RB_SETUNICODEFORMAT messaggio (Commctrl.h)
description: 'RB_SETUNICODEFORMAT messaggio: imposta il flag di formato carattere Unicode per il controllo. Questo messaggio consente di modificare il set di caratteri utilizzato dal controllo in fase di esecuzione anziché dover creare nuovamente il controllo.'
ms.assetid: 769b74e0-c1f0-4068-80c4-075f1db2058a
keywords:
- RB_SETUNICODEFORMAT dei controlli Windows messaggio
topic_type:
- apiref
api_name:
- RB_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cdac1e9878c27ecd283d615fd9f3432c7c4b3b3baeec55ce818b9386d33c27e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078575"
---
# <a name="rb_setunicodeformat-message"></a>Messaggio RB \_ SETUNICODEFORMAT

Imposta il flag di formato carattere Unicode per il controllo . Questo messaggio consente di modificare il set di caratteri utilizzato dal controllo in fase di esecuzione anziché dover creare nuovamente il controllo.

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

Per una descrizione di questo messaggio, vedere le osservazioni relative a [**\_ CCM SETUNICODEFORMAT.**](ccm-setunicodeformat.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**RB \_ GETUNICODEFORMAT**](rb-getunicodeformat.md)
</dt> </dl>

 

 





