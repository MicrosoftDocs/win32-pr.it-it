---
title: Messaggio TCM_SETIMAGELIST (COMmctrl. h)
description: Assegna un elenco di immagini a un controllo struttura a schede. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro TabCtrl.
ms.assetid: b457c73c-4c38-4bc5-af5d-12bbd24504a6
keywords:
- Controlli di Windows Message TCM_SETIMAGELIST
topic_type:
- apiref
api_name:
- TCM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59172c677998e816b295939c14effe45ff8aa961
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047842"
---
# <a name="tcm_setimagelist-message"></a>Messaggio dell'immagine di TCM \_

Assegna un elenco di immagini a un controllo struttura a schede. È possibile inviare questo messaggio in modo esplicito o utilizzando [**la \_ macro TabCtrl**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setimagelist) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Handle per l'elenco di immagini da assegnare al controllo struttura a schede.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'handle per l'elenco di immagini precedente oppure **null** se non è presente un elenco di immagini precedente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





