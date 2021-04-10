---
title: Messaggio PBM_GETBARCOLOR (COMmctrl. h)
description: Ottiene il colore dell'indicatore di stato.
ms.assetid: d046f7e4-e21e-4dd9-a7be-2bf820c3c492
keywords:
- Controlli di Windows Message PBM_GETBARCOLOR
topic_type:
- apiref
api_name:
- PBM_GETBARCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35586d3483d1d487f740a1a3d991c884c814f452
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120518"
---
# <a name="pbm_getbarcolor-message"></a>\_Messaggio GETBARCOLOR PBM

Ottiene il colore dell'indicatore di stato.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il colore dell'indicatore di stato.

## <a name="remarks"></a>Commenti

Questo è il colore impostato dal messaggio [**\_ SETBARCOLOR di PBM**](pbm-setbarcolor.md) . Il valore predefinito è CLR \_ default, definito in commctrl. h.

Questa funzione ha effetto solo sulla modalità classica, non su qualsiasi stile di visualizzazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





