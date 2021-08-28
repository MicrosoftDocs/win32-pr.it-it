---
title: PGM_FORWARDMOUSE messaggio (Commctrl.h)
description: Abilita o disabilita l'inoltro del mouse per il controllo pager. Quando l'inoltro del mouse è abilitato, il controllo pager inoltra i messaggi WM \_ MOUSEMOVE alla finestra contenuta. È possibile inviare questo messaggio in modo esplicito o usare la macro Pager \_ ForwardMouse.
ms.assetid: 269972fe-50b3-4c9f-b5ac-65e768b30684
keywords:
- PGM_FORWARDMOUSE dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- PGM_FORWARDMOUSE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 705b63ad39faea86e1f38a5b59dc73c6fc12f1e19fc17d0619c9a4b3dd5c6d26
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046971"
---
# <a name="pgm_forwardmouse-message"></a>Messaggio \_ FORWARDMOUSE PGM

Abilita o disabilita l'inoltro del mouse per il controllo pager. Quando l'inoltro del mouse è abilitato, il controllo pager inoltra [**i messaggi WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) alla finestra contenuta. È possibile inviare questo messaggio in modo esplicito o usare la macro [**Pager \_ ForwardMouse.**](/windows/desktop/api/Commctrl/nf-commctrl-pager_forwardmouse)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

**Valore BOOL** che determina se l'inoltro del mouse è abilitato o disabilitato. Se questo valore è diverso da zero, l'inoltro del mouse è abilitato. Se questo valore è zero, l'inoltro del mouse è disabilitato.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito non viene usato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

