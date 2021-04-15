---
title: Messaggio TBM_CLEARTICS (COMmctrl. h)
description: Rimuove i segni di graduazione correnti da un TrackBar. Questo messaggio non rimuove il primo e l'ultimo segno di graduazione, che vengono creati automaticamente dal TrackBar.
ms.assetid: 2830497c-2cf0-4068-810c-c05d4e0abb8b
keywords:
- Controlli di Windows Message TBM_CLEARTICS
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
ms.openlocfilehash: 7a1ecb4f9f931c976b2542a1f263fc069f1eca10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475922"
---
# <a name="tbm_cleartics-message"></a>\_Messaggio CLEARTICS TBM

Rimuove i segni di graduazione correnti da un TrackBar. Questo messaggio non rimuove il primo e l'ultimo segno di graduazione, che vengono creati automaticamente dal TrackBar.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Ridisegni flag. Se questo parametro è **true**, il TrackBar viene ridisegnato dopo la cancellazione dei segni di graduazione. Se questo parametro è **false**, il messaggio Cancella i segni di graduazione senza ricreare il TrackBar.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





