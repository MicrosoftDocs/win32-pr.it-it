---
title: PBM_SETSTATE messaggio (Commctrl.h)
description: Imposta lo stato dell'indicatore di stato.
ms.assetid: 4626f334-db74-4618-8fc7-e6f21c88ca19
keywords:
- PBM_SETSTATE dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- PBM_SETSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 794006517eaa23789f3a25425b1213fede7f8dde9893587def02ebc9605b28f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986061"
---
# <a name="pbm_setstate-message"></a>Messaggio PBM \_ SETSTATE

Imposta lo stato dell'indicatore di stato.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Stato dell'indicatore di stato impostato. Uno dei valori seguenti.



| Valore                                                                                                                                                   | Significato                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="PBST_NORMAL"></span><span id="pbst_normal"></span><dl> <dt>**PBST \_ NORMAL**</dt> </dl> | Operazione in corso.<br/> |
| <span id="PBST_ERROR"></span><span id="pbst_error"></span><dl> <dt>**ERRORE \_ PBST**</dt> </dl>    | Errore.<br/>       |
| <span id="PBST_PAUSED"></span><span id="pbst_paused"></span><dl> <dt>**PBST \_ SOSPESO**</dt> </dl> | (sospeso)<br/>      |



 

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce lo stato precedente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





