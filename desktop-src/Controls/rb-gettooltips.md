---
title: RB_GETTOOLTIPS messaggio (Commctrl.h)
description: Recupera l'handle per qualsiasi controllo descrizione comando associato al controllo Rebar.
ms.assetid: 87897b00-857f-4a8a-ae16-a48abf4c411d
keywords:
- RB_GETTOOLTIPS di controllo Windows messaggio
topic_type:
- apiref
api_name:
- RB_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 859934dcdec85d0b160f9076f2a77263a02a187ebf49f8ccbb4af20fc3e82d13
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540061"
---
# <a name="rb_gettooltips-message"></a>Messaggio RB \_ GETTOOLTIPS

Recupera l'handle per qualsiasi controllo descrizione comando associato al controllo Rebar.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HWND** che rappresenta l'handle per il controllo descrizione comando associato al controllo Rebar oppure zero se al controllo Rebar non è associato alcun controllo descrizione comando.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





