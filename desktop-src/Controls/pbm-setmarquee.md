---
title: PBM_SETMARQUEE messaggio (Commctrl.h)
description: Imposta l'indicatore di stato sulla modalità di selezione. In questo modo l'indicatore di stato si sposta come un rettangolo di selezione.
ms.assetid: 6501bcb9-a711-470f-874f-f3484d3613b6
keywords:
- PBM_SETMARQUEE controlli di Windows messaggio
topic_type:
- apiref
api_name:
- PBM_SETMARQUEE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f724f87faa6e989fddb17e8d6fb3b115dd04859ea426addb7d4c0b893aff407a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986141"
---
# <a name="pbm_setmarquee-message"></a>PBM \_ SETMARQUEE message

Imposta l'indicatore di stato sulla modalità di selezione. In questo modo l'indicatore di stato si sposta come un rettangolo di selezione.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indica se attivare o disattivare la modalità di selezione.

</dd> <dt>

*lParam* 
</dt> <dd>Tempo, in millisecondi, tra gli aggiornamenti dell'animazione con sequenza temporale. Se questo parametro è zero, l'animazione del rettangolo di selezione viene aggiornata ogni 30 millisecondi.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce sempre **TRUE.**

## <a name="remarks"></a>Commenti

Usare questo messaggio quando non si conosce la quantità di avanzamento verso il completamento, ma si vuole indicare che lo stato di avanzamento è in corso.

Inviare il **messaggio \_ SETMARQUEE PBM** per avviare o arrestare l'animazione.

> [!Note]  
> È necessario impostare lo stile del controllo [**su PBS \_ MARQUEE**](progress-bar-control-styles.md) prima di tentare di avviare l'animazione.

 

> [!Note]  
> Questo messaggio richiede ComCtl32.dll versione 6.00 o successiva.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





