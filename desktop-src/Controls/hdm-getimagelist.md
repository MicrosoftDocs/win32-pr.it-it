---
title: HDM_GETIMAGELIST messaggio (Commctrl.h)
description: Ottiene l'handle per l'elenco di immagini impostato per un controllo intestazione esistente. È possibile inviare questo messaggio in modo esplicito o usare la macro Header \_ GetImageList o Header \_ GetStateImageList.
ms.assetid: 3e1a979c-60c5-4538-bd4d-16238829062e
keywords:
- HDM_GETIMAGELIST controlli Windows messaggio
topic_type:
- apiref
api_name:
- HDM_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8149dd4914ceb1835e9e04442492855e9c25340604ed4e4eeb2619c62b88e69f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540911"
---
# <a name="hdm_getimagelist-message"></a>Messaggio \_ HDM GETIMAGELIST

Ottiene l'handle per l'elenco di immagini impostato per un controllo intestazione esistente. È possibile inviare questo messaggio in modo esplicito o usare la macro [**Header \_ GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_getimagelist) [**o Header \_ GetStateImageList.**](/windows/desktop/api/Commctrl/nf-commctrl-header_getstateimagelist)

## <a name="parameters"></a>Parametri

<dl> <dt>*wParam*</dt> <dd>Uno dei valori seguenti:

| Valore                                                                                                                                                      | Significato                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="HDSIL_NORMAL"></span><span id="hdsil_normal"></span><dl> <dt>**HDSIL \_ NORMAL**</dt> </dl> | Indica che si tratta di un normale elenco di immagini.<br/> |
| <span id="HDSIL_STATE"></span><span id="hdsil_state"></span><dl> <dt>**STATO \_ HDSIL**</dt> </dl>    | Indica che si tratta di un elenco di immagini di stato.<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un handle al set di elenchi di immagini per il controllo intestazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





