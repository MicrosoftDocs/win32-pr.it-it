---
title: DTM_GETIDEALSIZE messaggio (Commctrl.h)
description: Ottiene le dimensioni necessarie per visualizzare il controllo senza ritaglio. Inviare questo messaggio in modo esplicito o usando la \_ macro DateTime GetIdealSize.
ms.assetid: 15ec26a1-645b-4a96-af66-1031e1a46c6c
keywords:
- DTM_GETIDEALSIZE dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- DTM_GETIDEALSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 639fbbb25fbf61695f83b54f106f45ff3dd421f528807120be52edd7031e4f66
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119878231"
---
# <a name="dtm_getidealsize-message"></a>Messaggio DTM \_ GETIDEALSIZE

Ottiene le dimensioni necessarie per visualizzare il controllo senza ritaglio. Inviare questo messaggio in modo esplicito o usando la macro [**\_ DateTime GetIdealSize.**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getidealsize)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non usato. Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura SIZE**](/previous-versions//dd145106(v=vs.85)) per ricevere le dimensioni ideali. L'applicazione chiamante è responsabile dell'allocazione di questa struttura.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

