---
title: Messaggio TDM_SET_PROGRESS_BAR_RANGE (COMmctrl. h)
description: Imposta i valori minimo e massimo per l'indicatore di stato in una finestra di dialogo attività.
ms.assetid: ca8b48bc-cf56-4678-bb3d-7c730a96d98c
keywords:
- Controlli di Windows Message TDM_SET_PROGRESS_BAR_RANGE
topic_type:
- apiref
api_name:
- TDM_SET_PROGRESS_BAR_RANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d17ebb6caa2c33282dccbb117980fc970cd45477
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874593"
---
# <a name="tdm_set_progress_bar_range-message"></a>Messaggio di intervallo indicatore di \_ stato set TDM \_ \_ \_

Imposta i valori minimo e massimo per l'indicatore di stato in una finestra di dialogo attività.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* \[ in\]
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifica il valore minimo. Per impostazione predefinita, il valore minimo è zero. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica il valore massimo. Per impostazione predefinita, il valore massimo è 100.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce i valori minimo e massimo precedenti, se ha esito positivo, oppure zero in caso contrario. [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene il valore minimo e [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contiene il valore massimo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

