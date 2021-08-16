---
title: Valori di disegno personalizzati (CommCtrl.h)
description: Questa sezione elenca i valori usati per identificare le parti di un controllo Trackbar.
ms.assetid: 154321c7-99f8-4ed5-a5ff-fb96126b43c7
topic_type:
- apiref
api_name:
- TBCD_CHANNEL
- TBCD_THUMB
- TBCD_TICS
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb714df7c91819a7d459c4c9fbed1fbc1e0d4fd2455f52891030d95991fa6497
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831692"
---
# <a name="custom-draw-values"></a>Valori di disegno personalizzati

Questa sezione elenca i valori usati per identificare le parti di un controllo Trackbar.



| Costante                                                                                                                                                   | Descrizione                                                                                                     |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------|
| <span id="TBCD_CHANNEL"></span><span id="tbcd_channel"></span><dl> <dt>**CANALE \_ TBCD**</dt> </dl> | Identifica il canale lungo cui scorre l'indicatore di scorrimento del controllo trackbar.<br/>                        |
| <span id="TBCD_THUMB"></span><span id="tbcd_thumb"></span><dl> <dt>**TBCD \_ THUMB**</dt> </dl>       | Identifica il marcatore di scorrimento del controllo trackbar. Questa è la parte del controllo spostata dall'utente.<br/> |
| <span id="TBCD_TICS"></span><span id="tbcd_tics"></span><dl> <dt>**TBCD \_ TICS**</dt> </dl>          | Identifica i segni di graduazione visualizzati lungo il bordo del controllo trackbar.<br/>                      |



## <a name="remarks"></a>Commenti

I valori di Disegno personalizzato, ad esempio, vengono specificati nel **membro dwItemSpec** della [**struttura NMCUSTOMDRAW.**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



 

 





