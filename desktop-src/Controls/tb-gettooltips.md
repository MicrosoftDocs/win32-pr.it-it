---
title: TB_GETTOOLTIPS messaggio (Commctrl.h)
description: Recupera l'handle per il controllo descrizione comando, se presente, associato alla barra degli strumenti.
ms.assetid: 1e0edfdc-d0cb-41f3-9178-1239d81d3034
keywords:
- TB_GETTOOLTIPS di controllo Windows messaggio
topic_type:
- apiref
api_name:
- TB_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41f326ffcc12e9fcf115b6f010e9fc8f7e327ce6381ce9a2fb3d397d8e322f92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118168227"
---
# <a name="tb_gettooltips-message"></a>TB \_ GETTOOLTIPS message

Recupera l'handle per il controllo descrizione comando, se presente, associato alla barra degli strumenti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'handle per il controllo descrizione comando oppure **NULL se** alla barra degli strumenti non è associata alcuna descrizione comando.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





