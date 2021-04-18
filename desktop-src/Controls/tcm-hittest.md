---
title: Messaggio TCM_HITTEST (COMmctrl. h)
description: Determina la scheda, se presente, che si trova in una posizione dello schermo specificata. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro TabCtrl HitTest.
ms.assetid: 0334f616-8d39-4460-a7f8-692a9ffab012
keywords:
- Controlli di Windows Message TCM_HITTEST
topic_type:
- apiref
api_name:
- TCM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04787662e417513d8c9c93e45cecd0d8bddc6cfa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302361"
---
# <a name="tcm_hittest-message"></a>Messaggio di TCM \_ HITTEST

Determina la scheda, se presente, che si trova in una posizione dello schermo specificata. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**TabCtrl \_ HitTest**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_hittest) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**TCHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tchittestinfo) che specifica la posizione dello schermo da verificare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'indice della scheda oppure-1 se nessuna scheda si trova nella posizione specificata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





