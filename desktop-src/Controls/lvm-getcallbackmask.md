---
title: LVM_GETCALLBACKMASK messaggio (Commctrl.h)
description: Ottiene la maschera di callback per un controllo di visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro ListView GetCallbackMask.
ms.assetid: fb05593d-14b9-4e53-acb3-d5ac61e517ec
keywords:
- LVM_GETCALLBACKMASK di controllo Windows messaggio
topic_type:
- apiref
api_name:
- LVM_GETCALLBACKMASK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58cbfec76df9418c2bc94e0083928f28e462188383a203237dd03f3f175c74b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119920231"
---
# <a name="lvm_getcallbackmask-message"></a>Messaggio LVM \_ GETCALLBACKMASK

Ottiene la maschera di callback per un controllo di visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ ListView GetCallbackMask.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcallbackmask)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce la maschera di callback.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





