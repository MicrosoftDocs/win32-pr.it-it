---
title: TCM_DELETEITEM messaggio (Commctrl.h)
description: Rimuove un elemento da un controllo Struttura a schede. È possibile inviare questo messaggio in modo esplicito o tramite la macro TabCtrl \_ DeleteItem.
ms.assetid: 54bfa446-580a-4ea7-b5e9-9429f4ee1c2b
keywords:
- TCM_DELETEITEM dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- TCM_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cc9e90ab63e34545628019cd9dcde74c7b4e953fb6ee0b9eed138151129e7b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077875"
---
# <a name="tcm_deleteitem-message"></a>Messaggio TCM \_ DELETEITEM

Rimuove un elemento da un controllo Struttura a schede. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**TabCtrl \_ DeleteItem.**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_deleteitem)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice dell'elemento da eliminare.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo oppure FALSE **in** caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





