---
title: TB_HITTEST messaggio (Commctrl.h)
description: Determina la posizione di un punto in un controllo barra degli strumenti.
ms.assetid: d08f3805-2042-470e-8f5a-8a6a681d1189
keywords:
- TB_HITTEST di controllo Windows messaggio
topic_type:
- apiref
api_name:
- TB_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d89cecf1d1df5c370ab9a00ae1251df9df7ef919f9959b998407a9fb5881178
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696161"
---
# <a name="tb_hittest-message"></a>MESSAGGIO \_ HITTEST TB

Determina la posizione di un punto in un controllo barra degli strumenti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**POINT**](/previous-versions//dd162805(v=vs.85)) che contiene la coordinata x dell'hit test nel membro **x** e la coordinata y dell'hit test nel **membro** y. Le coordinate sono relative all'area client della barra degli strumenti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore intero. Se il valore restituito è zero o un valore positivo, è l'indice in base zero dell'elemento nonseparator in cui si trova il punto. Se il valore restituito è negativo, il punto non si trova all'interno di un pulsante. Il valore assoluto del valore restituito è l'indice di un elemento separator o dell'elemento nonseparator più vicino.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

