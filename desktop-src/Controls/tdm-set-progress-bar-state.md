---
title: Messaggio TDM_SET_PROGRESS_BAR_STATE (COMmctrl. h)
description: Imposta lo stato dell'indicatore di stato in una finestra di dialogo attività.
ms.assetid: 8b0f2ee9-e6ca-4a5b-8687-6e2682eda7d0
keywords:
- Controlli di Windows Message TDM_SET_PROGRESS_BAR_STATE
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
ms.openlocfilehash: 00f0ae4ec104c8472d3640aa804650640d77cc63
ms.sourcegitcommit: e584514ced7396dde55e58501c8c8a872229acc4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/08/2021
ms.locfileid: "104352036"
---
# <a name="tdm_set_progress_bar_state-message"></a>\_Messaggio di \_ stato della barra di \_ \_ stato set TDM

Imposta lo stato dell'indicatore di stato in una finestra di dialogo attività.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

Valore **int** che specifica lo stato dell'indicatore di stato. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                   | Significato                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="PBST_NORMAL"></span><span id="pbst_normal"></span><dl> <dt>**PBST \_ normale**</dt> </dl> | Imposta lo stato normale per l'indicatore di stato.<br/> |
| <span id="PBST_PAUSED"></span><span id="pbst_paused"></span><dl> <dt>**PBST \_ sospeso**</dt> </dl>    | Imposta l'indicatore di stato sullo stato sospeso.<br/> |
| <span id="PBST_ERROR"></span><span id="pbst_error"></span><dl> <dt>**\_errore PBST**</dt> </dl>    | Impostare l'indicatore di stato sullo stato di errore.<br/>   |



 

</dd> <dt>

*lParam* \[ in\]
</dt> <dd>

Deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero. Per ottenere informazioni estese sull'errore, chiamare GetLastError.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





