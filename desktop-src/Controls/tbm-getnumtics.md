---
title: Messaggio TBM_GETNUMTICS (COMmctrl. h)
description: Recupera il numero di segni di graduazione in un TrackBar.
ms.assetid: 3c3f7ebb-a544-474c-ba14-68eae543ee38
keywords:
- Controlli di Windows Message TBM_GETNUMTICS
topic_type:
- apiref
api_name:
- TBM_GETNUMTICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 712e1a0190334ec279f28a68959f3e3d5d5ffd1d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963933"
---
# <a name="tbm_getnumtics-message"></a>\_Messaggio GETNUMTICS TBM

Recupera il numero di segni di graduazione in un TrackBar.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se non è impostato alcun [flag](trackbar-control-styles.md) di selezione, restituisce 2 per i cicli di inizio e fine. Se è impostato TBS nosegni, viene restituito zero. [**\_**](trackbar-control-styles.md) In caso contrario, prende la differenza tra il valore minimo e massimo dell'intervallo, divide in base alla frequenza di segno e aggiunge 2.

## <a name="remarks"></a>Commenti

Il messaggio **TBM \_ GETNUMTICS** conta tutti i segni di graduazione, inclusi il primo e l'ultimo segno di graduazione creato dal TrackBar.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





