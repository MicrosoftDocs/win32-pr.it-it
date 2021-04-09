---
title: Messaggio MCM_GETMAXSELCOUNT (COMmctrl. h)
description: Recupera l'intervallo massimo di date che può essere selezionato in un controllo di calendario mensile. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro MonthCal GetMaxSelCount.
ms.assetid: 34204231-3a3c-4eba-913d-b0c27769c338
keywords:
- Controlli di Windows Message MCM_GETMAXSELCOUNT
topic_type:
- apiref
api_name:
- MCM_GETMAXSELCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5bddfdad17cc4a0fd6499514023cb499f55f40d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048518"
---
# <a name="mcm_getmaxselcount-message"></a>\_Messaggio GETMAXSELCOUNT MCM

Recupera l'intervallo massimo di date che può essere selezionato in un controllo di calendario mensile. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MonthCal \_ GetMaxSelCount**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmaxselcount) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore INT che rappresenta il numero totale di giorni che è possibile selezionare per il controllo.

## <a name="remarks"></a>Commenti

È possibile modificare l'intervallo massimo di date selezionabile usando il messaggio [**MCM \_ SETMAXSELCOUNT**](mcm-setmaxselcount.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





