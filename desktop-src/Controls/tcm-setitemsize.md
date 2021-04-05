---
title: Messaggio TCM_SETITEMSIZE (COMmctrl. h)
description: Imposta la larghezza e l'altezza delle schede in un controllo struttura a larghezza fissa o disegnato dal proprietario. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro TabCtrl SetItemSize.
ms.assetid: 3935d686-f8bc-41fb-b025-04120cf03f02
keywords:
- Controlli di Windows Message TCM_SETITEMSIZE
topic_type:
- apiref
api_name:
- TCM_SETITEMSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e306af3f6462507a181de91104169c5ac7d6ce14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873277"
---
# <a name="tcm_setitemsize-message"></a>\_Messaggio TCM SETITEMSIZE

Imposta la larghezza e l'altezza delle schede in un controllo struttura a larghezza fissa o disegnato dal proprietario. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**TabCtrl \_ SetItemSize**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitemsize) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) è un valore **int** che specifica la nuova larghezza, in pixel. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) è un valore **int** che specifica la nuova altezza, in pixel.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce la larghezza e l'altezza precedenti. La larghezza si trova nell' [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) del valore restituito e l'altezza si trova in [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).

## <a name="remarks"></a>Commenti

Se la larghezza è impostata su un valore minore della larghezza dell'immagine impostata da [**ImageList \_ create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create), la larghezza della scheda viene impostata sul valore più basso maggiore della larghezza dell'immagine.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

