---
title: Messaggio PBM_GETBKCOLOR (COMmctrl. h)
description: Ottiene il colore di sfondo dell'indicatore di stato.
ms.assetid: 9526ed78-08d9-468f-831b-72bb7c8c92d1
keywords:
- Controlli di Windows Message PBM_GETBKCOLOR
topic_type:
- apiref
api_name:
- PBM_GETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2240025629bbcc242ea7ed47be2e3db42ae73b15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874161"
---
# <a name="pbm_getbkcolor-message"></a>\_Messaggio GETBKCOLOR PBM

Ottiene il colore di sfondo dell'indicatore di stato.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il colore di sfondo dell'indicatore di stato.

## <a name="remarks"></a>Commenti

Questo è il colore impostato dal messaggio [**\_ SETBKCOLOR di PBM**](pbm-setbkcolor.md) . Il valore predefinito è CLR \_ default, definito in commctrl. h.

Questa funzione ha effetto solo sulla modalità classica, non su qualsiasi stile di visualizzazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





