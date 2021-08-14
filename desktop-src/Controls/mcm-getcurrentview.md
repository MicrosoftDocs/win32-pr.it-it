---
title: MCM_GETCURRENTVIEW messaggio (Commctrl.h)
description: Ottiene la visualizzazione corrente del calendario. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro MonthCal GetCurrentView.
ms.assetid: 9c42ebf6-611e-4e50-9dcc-cf7fd63b32eb
keywords:
- MCM_GETCURRENTVIEW dei messaggi Windows controllo
topic_type:
- apiref
api_name:
- MCM_GETCURRENTVIEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50f7fce3c1a22ec14ec34e849bd2e3fc4634118b11613913da4e6fae0b9b7b51
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119319681"
---
# <a name="mcm_getcurrentview-message"></a>Messaggio \_ MCM GETCURRENTVIEW

Ottiene la visualizzazione corrente del calendario. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ MonthCal GetCurrentView.**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcurrentview)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Visualizzazione corrente. Uno dei valori seguenti.



| Codice restituito                                                                                  | Descrizione              |
|----------------------------------------------------------------------------------------------|--------------------------|
| <dl> <dt>**MESE \_ MCMV**</dt> </dl>   | Visualizzazione mensile.<br/> |
| <dl> <dt>**MCMV \_ YEAR**</dt> </dl>    | Visualizzazione annuale.<br/>  |
| <dl> <dt>**MCMV \_ DECADE**</dt> </dl>  | Visualizzazione decennale.<br/>  |
| <dl> <dt>**MCMV \_ CENTURY**</dt> </dl> | Visualizzazione del secolo.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





