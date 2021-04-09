---
title: Messaggio TDM_CLICK_VERIFICATION (COMmctrl. h)
description: Simula un clic della casella di controllo verifica di una finestra di dialogo attività, se esistente.
ms.assetid: 1c6c135e-4e39-4f1a-88f4-5e9f7181a2dd
keywords:
- Controlli di Windows Message TDM_CLICK_VERIFICATION
topic_type:
- apiref
api_name:
- TDM_CLICK_VERIFICATION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df61676104169e3084e7cde09439c218f2237e60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104118958"
---
# <a name="tdm_click_verification-message"></a>TDM- \_ Seleziona \_ messaggio di verifica

Simula un clic della casella di controllo verifica di una finestra di dialogo attività, se esistente.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

**True** per impostare lo stato della casella di controllo da controllare; **False** per impostarlo come deselezionato.

</dd> <dt>

*lParam* \[ in\]
</dt> <dd>

**True** per impostare lo stato attivo della tastiera sulla casella di controllo; In caso contrario, **false** .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito viene ignorato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





