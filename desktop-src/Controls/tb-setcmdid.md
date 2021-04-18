---
title: Messaggio TB_SETCMDID (COMmctrl. h)
description: Imposta l'identificatore del comando di un pulsante della barra degli strumenti.
ms.assetid: 0674c905-2d9d-45d3-b565-2f3bcd7d6383
keywords:
- Controlli di Windows Message TB_SETCMDID
topic_type:
- apiref
api_name:
- TB_SETCMDID
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f91cc4fd4d70e912bed3163cdf783e8e17ab463
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301668"
---
# <a name="tb_setcmdid-message"></a>TB \_ SETCMDID messaggio

Imposta l'identificatore del comando di un pulsante della barra degli strumenti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero del pulsante di cui è necessario impostare l'identificatore di comando.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificatore del comando.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





