---
title: PBM_GETBARCOLOR messaggio (Commctrl.h)
description: Ottiene il colore dell'indicatore di stato.
ms.assetid: d046f7e4-e21e-4dd9-a7be-2bf820c3c492
keywords:
- PBM_GETBARCOLOR di controllo Windows messaggio
topic_type:
- apiref
api_name:
- PBM_GETBARCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cb42d878840ad05f0854ec7ca9cb50dc1b3be2a55b3b65ddf652d961b6d818b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119312441"
---
# <a name="pbm_getbarcolor-message"></a>Messaggio PBM \_ GETBARCOLOR

Ottiene il colore dell'indicatore di stato.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il colore dell'indicatore di stato.

## <a name="remarks"></a>Commenti

Si tratta del colore impostato dal messaggio [**PBM \_ SETBARCOLOR.**](pbm-setbarcolor.md) Il valore predefinito è CLR DEFAULT, definito \_ in commctrl.h.

Questa funzione influisce solo sulla modalità classica, non su qualsiasi stile di visualizzazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





