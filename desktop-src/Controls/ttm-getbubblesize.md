---
title: TTM_GETBUBBLESIZE messaggio (Commctrl.h)
description: Restituisce la larghezza e l'altezza di un controllo descrizione comando.
ms.assetid: 6afb971e-f05d-4b7a-b63d-3672bfcc32dc
keywords:
- TTM_GETBUBBLESIZE di controllo Windows messaggio
topic_type:
- apiref
api_name:
- TTM_GETBUBBLESIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8354a93521b6adac9306374f5bfbc99e84738ac87f0471a22f199b7b611f100b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769381"
---
# <a name="ttm_getbubblesize-message"></a>TTM \_ GETBUBBLESIZE message

Restituisce la larghezza e l'altezza di un controllo descrizione comando.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore alla struttura [**TOOLINFO della descrizione**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) comando.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce la larghezza della descrizione comando nella parola bassa e l'altezza nella parola superiore in caso di esito positivo. In caso contrario, restituisce **FALSE.**

## <a name="remarks"></a>Commenti

Se i flag TTF TRACK e TTF ABSOLUTE sono impostati nel membro \_ \_ **uFlags** della struttura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) della descrizione comando, questo messaggio può essere usato per posizionare in modo accurato la descrizione comando.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





