---
title: TDM_SET_PROGRESS_BAR_STATE messaggio (Commctrl.h)
description: Imposta lo stato dell'indicatore di stato in una finestra di dialogo attività.
ms.assetid: 8b0f2ee9-e6ca-4a5b-8687-6e2682eda7d0
keywords:
- TDM_SET_PROGRESS_BAR_STATE di controllo Windows messaggio
topic_type:
- apiref
api_name:
- TDM_SET_PROGRESS_BAR_STATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb3be7432ac3a93af4f27fe9b06dced50fc6c77c0176c3bff7419cf15f2c73ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104531"
---
# <a name="tdm_set_progress_bar_state-message"></a>TDM SET PROGRESS BAR STATE message (TDM \_ SET PROGRESS BAR STATE \_ \_ \_ MESSAGE)

Imposta lo stato dell'indicatore di stato in una finestra di dialogo attività.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ Pollici\]
</dt> <dd>

Valore **int** che specifica lo stato dell'indicatore di stato. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                   | Significato                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="PBST_NORMAL"></span><span id="pbst_normal"></span><dl> <dt>**PBST \_ NORMAL**</dt> </dl> | Imposta l'indicatore di stato sullo stato normale.<br/> |
| <span id="PBST_PAUSED"></span><span id="pbst_paused"></span><dl> <dt>**PBST \_ SOSPESO**</dt> </dl>    | Imposta l'indicatore di stato sullo stato sospeso.<br/> |
| <span id="PBST_ERROR"></span><span id="pbst_error"></span><dl> <dt>**ERRORE \_ PBST**</dt> </dl>    | Impostare l'indicatore di stato sullo stato di errore.<br/>   |



 

</dd> <dt>

*lParam* \[ Pollici\]
</dt> <dd>

Deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero. Per ottenere informazioni sull'errore estese, chiamare GetLastError.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





