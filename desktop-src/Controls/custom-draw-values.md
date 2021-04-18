---
title: Valori di estrazione personalizzati (CommCtrl. h)
description: In questa sezione vengono elencati i valori utilizzati per identificare le parti di un controllo TrackBar.
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
ms.openlocfilehash: ccf05ab951fdc83ec5be414688be56d710ba0d98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327247"
---
# <a name="custom-draw-values"></a>Valori di estrazione personalizzati

In questa sezione vengono elencati i valori utilizzati per identificare le parti di un controllo TrackBar.



| Costante                                                                                                                                                   | Descrizione                                                                                                     |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------|
| <span id="TBCD_CHANNEL"></span><span id="tbcd_channel"></span><dl> <dt>**\_canale TBCD**</dt> </dl> | Identifica il canale con cui scorre il marcatore Thumb del controllo TrackBar.<br/>                        |
| <span id="TBCD_THUMB"></span><span id="tbcd_thumb"></span><dl> <dt>**TBCD \_ Thumb**</dt> </dl>       | Identifica il marcatore Thumb del controllo TrackBar. Questa è la parte del controllo che l'utente sposta.<br/> |
| <span id="TBCD_TICS"></span><span id="tbcd_tics"></span><dl> <dt>**\_TIC TBCD**</dt> </dl>          | Identifica i segni di graduazione visualizzati lungo il bordo del controllo TrackBar.<br/>                      |



## <a name="remarks"></a>Commenti

I valori di estrazione personalizzati, ad esempio, vengono specificati nel membro **dwItemSpec** della struttura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

 





