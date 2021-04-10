---
title: Messaggio PBM_GETSTEP (COMmctrl. h)
description: Recupera l'incremento di passaggio da un indicatore di stato. L'incremento del passaggio è la quantità in base alla quale l'indicatore di stato aumenta la posizione corrente ogni volta che viene ricevuto un \_ messaggio STEPIT PBM. Per impostazione predefinita, l'incremento del passaggio è impostato su 10.
ms.assetid: 0cf3052a-cf86-4c0e-ad59-ddab7c6e3602
keywords:
- Controlli di Windows Message PBM_GETSTEP
topic_type:
- apiref
api_name:
- PBM_GETSTEP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0dcc4adb18d2b60d2936c2cdc7ab79d00389b3ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964564"
---
# <a name="pbm_getstep-message"></a>\_Messaggio dell'istruzione GETstep di PBM

Recupera l'incremento di passaggio da un indicatore di stato. L'incremento del passaggio è la quantità in base alla quale l'indicatore di stato aumenta la posizione corrente ogni volta che viene ricevuto un messaggio [**\_ STEPIT PBM**](pbm-stepit.md) . Per impostazione predefinita, l'incremento del passaggio è impostato su 10.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'incremento del passaggio corrente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





