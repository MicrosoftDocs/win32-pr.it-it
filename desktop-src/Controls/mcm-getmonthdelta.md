---
title: Messaggio MCM_GETMONTHDELTA (COMmctrl. h)
description: Recupera la velocità di scorrimento per un controllo di calendario mensile. La velocità di scorrimento indica il numero di mesi durante i quali il controllo sposta la visualizzazione quando l'utente fa clic su un pulsante di scorrimento. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro MonthCal GetMonthDelta.
ms.assetid: 6db02993-b22c-430f-8928-8bd5768b2151
keywords:
- Controlli di Windows Message MCM_GETMONTHDELTA
topic_type:
- apiref
api_name:
- MCM_GETMONTHDELTA
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01eaa40b930e6317cc2be6b674f0cea58115ae40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121758"
---
# <a name="mcm_getmonthdelta-message"></a>\_Messaggio GETMONTHDELTA MCM

Recupera la velocità di scorrimento per un controllo di calendario mensile. La velocità di scorrimento indica il numero di mesi durante i quali il controllo sposta la visualizzazione quando l'utente fa clic su un pulsante di scorrimento. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MonthCal \_ GetMonthDelta**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmonthdelta) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il Delta del mese è stato impostato in precedenza tramite il messaggio [**MCM \_ SETMONTHDELTA**](mcm-setmonthdelta.md) , restituisce un valore int che rappresenta la frequenza di scorrimento corrente del calendario mensile. Se il Delta del mese non è stato impostato in precedenza utilizzando il messaggio **MCM \_ SETMONTHDELTA** o il Delta del mese è stato reimpostato sull'impostazione predefinita, restituisce un valore int che rappresenta il numero corrente di mesi visibili.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





