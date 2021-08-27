---
title: PBM_GETSTATE messaggio (Commctrl.h)
description: Ottiene lo stato dell'indicatore di stato.
ms.assetid: ff240160-7db6-4711-8d4e-25a77dfba118
keywords:
- PBM_GETSTATE del messaggio Windows controlli
topic_type:
- apiref
api_name:
- PBM_GETSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cd157ccb6ab8a1fe4cd4a31bf1f8a033f0e591288338e21cc322a8ac10bfc41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047011"
---
# <a name="pbm_getstate-message"></a>Messaggio \_ GETSTATE PBM

Ottiene lo stato dell'indicatore di stato.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce lo stato corrente dell'indicatore di stato. Uno dei valori seguenti.



| Codice restituito                                                                                 | Descrizione             |
|---------------------------------------------------------------------------------------------|-------------------------|
| <dl> <dt>**PBST \_ NORMAL**</dt> </dl> | Operazione in corso.<br/> |
| <dl> <dt>**ERRORE \_ PBST**</dt> </dl>  | Errore.<br/>       |
| <dl> <dt>**PBST \_ IN PAUSA**</dt> </dl> | (sospeso)<br/>      |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





