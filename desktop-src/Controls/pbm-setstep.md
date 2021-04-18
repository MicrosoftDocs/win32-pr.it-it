---
title: Messaggio PBM_SETSTEP (COMmctrl. h)
description: Specifica l'incremento del passaggio per un indicatore di stato. L'incremento del passaggio è la quantità in base alla quale l'indicatore di stato aumenta la posizione corrente ogni volta che viene ricevuto un \_ messaggio STEPIT PBM. Per impostazione predefinita, l'incremento del passaggio è impostato su 10.
ms.assetid: 75c1085b-6c7a-4c44-9a12-f9bf21f7d945
keywords:
- Controlli di Windows Message PBM_SETSTEP
topic_type:
- apiref
api_name:
- PBM_SETSTEP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1240d09aeadcd7994187704d0b5a4630ab1b7afb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302054"
---
# <a name="pbm_setstep-message"></a>Messaggio in fase di esecuzione di PBM \_

Specifica l'incremento del passaggio per un indicatore di stato. L'incremento del passaggio è la quantità in base alla quale l'indicatore di stato aumenta la posizione corrente ogni volta che viene ricevuto un messaggio [**\_ STEPIT PBM**](pbm-stepit.md) . Per impostazione predefinita, l'incremento del passaggio è impostato su 10.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Incremento nuovo passaggio.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'incremento del passaggio precedente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





