---
title: Messaggio DTM_GETDATETIMEPICKERINFO (COMmctrl. h)
description: Ottiene informazioni su un controllo di selezione data e ora (DTP).
ms.assetid: 04847b68-ac45-4b28-8f62-2cd68ffe48d4
keywords:
- Controlli di Windows Message DTM_GETDATETIMEPICKERINFO
topic_type:
- apiref
api_name:
- DTM_GETDATETIMEPICKERINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2398a2543caa6d7104339fb8debd83fcee3ac71f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475406"
---
# <a name="dtm_getdatetimepickerinfo-message"></a>\_Messaggio GETDATETIMEPICKERINFO DTM

Ottiene informazioni su un controllo di selezione data e ora (DTP).

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* \[ in\]
</dt> <dd> Puntatore a <a href="/windows/win32/api/commctrl/ns-commctrl-datetimepickerinfo">**DATETIMEPICKERINFO**</a> per ricevere le informazioni. Il chiamante è responsabile dell'allocazione della memoria per questa struttura. Impostare il membro **cbSize** della struttura su sizeof (DATETIMEPICKERINFO) prima di inviare questo messaggio.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito viene ignorato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





