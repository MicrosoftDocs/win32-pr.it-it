---
title: PBM_SETBARCOLOR messaggio (Commctrl.h)
description: Imposta il colore dell'indicatore di stato nel controllo indicatore di stato.
ms.assetid: 4b512420-04ec-4884-ab13-4c58304b95f6
keywords:
- PBM_SETBARCOLOR del messaggio Windows controlli
topic_type:
- apiref
api_name:
- PBM_SETBARCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: babff5ad74d943d64f5ad61354447498e91e1325c99c82b32183fbc62eabafdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117830202"
---
# <a name="pbm_setbarcolor-message"></a>Messaggio \_ SETBARCOLOR PBM

Imposta il colore dell'indicatore di stato nel controllo indicatore di stato.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Valore **COLORREF** che specifica il nuovo colore dell'indicatore di stato. Se si specifica il valore CLR \_ DEFAULT, l'indicatore di stato utilizzerà il colore predefinito dell'indicatore di stato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il colore della barra dell'indicatore di stato precedente o CLR DEFAULT se il colore dell'indicatore \_ di stato è il colore predefinito.

## <a name="remarks"></a>Commenti

Quando gli stili di visualizzazione sono abilitati, questo messaggio non ha alcun effetto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





