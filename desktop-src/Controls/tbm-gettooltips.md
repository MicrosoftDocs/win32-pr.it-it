---
title: TBM_GETTOOLTIPS messaggio (Commctrl.h)
description: Recupera l'handle per il controllo della descrizione comando assegnato al trackbar, se presente.
ms.assetid: 30efef12-1aec-4635-94a7-1843db404c4f
keywords:
- TBM_GETTOOLTIPS dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- TBM_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c97c94ab3a696f5967f724e76d2d8702a01275bedc06ad7c13907d57710a078
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078065"
---
# <a name="tbm_gettooltips-message"></a>Messaggio TBM \_ GETTOOLTIPS

Recupera l'handle per il controllo della descrizione comando assegnato al trackbar, se presente.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'handle al controllo descrizione comando assegnato al trackbar oppure **NULL** se le descrizioni comando non sono in uso. Se il controllo trackbar non usa lo stile [**TBS \_ TOOLTIPS,**](trackbar-control-styles.md) il valore restituito è **NULL.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





