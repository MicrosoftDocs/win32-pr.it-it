---
title: TDM_SET_PROGRESS_BAR_RANGE messaggio (Commctrl.h)
description: Imposta i valori minimo e massimo per l'indicatore di stato in una finestra di dialogo attività.
ms.assetid: ca8b48bc-cf56-4678-bb3d-7c730a96d98c
keywords:
- TDM_SET_PROGRESS_BAR_RANGE controlli Windows messaggio
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
ms.openlocfilehash: 54d94da64bd01b17addeb8f65def177e7e7e5d7daccbafb1629d1158f8c6636d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875911"
---
# <a name="tdm_set_progress_bar_range-message"></a>Messaggio TDM \_ SET \_ PROGRESS BAR \_ \_ RANGE

Imposta i valori minimo e massimo per l'indicatore di stato in una finestra di dialogo attività.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ Pollici\]
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* \[ Pollici\]
</dt> <dd>

[**LoWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifica il valore minimo. Per impostazione predefinita, il valore minimo è zero. [**HiWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica il valore massimo. Per impostazione predefinita, il valore massimo è 100.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce i valori minimo e massimo precedenti, in caso di esito positivo, oppure zero in caso contrario. LOWORD [**contiene**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) il valore minimo e [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contiene il valore massimo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

