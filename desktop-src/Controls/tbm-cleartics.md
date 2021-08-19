---
title: TBM_CLEARTICS messaggio (Commctrl.h)
description: Rimuove i segni di graduazione correnti da un trackbar. Questo messaggio non rimuove il primo e l'ultimo segno di graduazione, che vengono creati automaticamente dal trackbar.
ms.assetid: 2830497c-2cf0-4068-810c-c05d4e0abb8b
keywords:
- TBM_CLEARTICS dei messaggi Windows controllo
topic_type:
- apiref
api_name:
- TBM_CLEARTICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9390fc45c5b96a7b85d3b1b366e34d24c3b4bf0bc60ec066ead28357bcec1439
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046771"
---
# <a name="tbm_cleartics-message"></a>Messaggio \_ TBM CLEARTICS

Rimuove i segni di graduazione correnti da un trackbar. Questo messaggio non rimuove il primo e l'ultimo segno di graduazione, che vengono creati automaticamente dal trackbar.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Flag di ridisegno. Se questo parametro è **TRUE,** il trackbar viene ridisegnato dopo che i segni di graduazione sono stati cancellati. Se questo parametro è **FALSE,** il messaggio cancella i segni di graduazione ma non ridisegna il trackbar.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





