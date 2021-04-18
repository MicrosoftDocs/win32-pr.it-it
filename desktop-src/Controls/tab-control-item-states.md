---
title: Stati degli elementi di controllo Tab (CommCtrl. h)
description: Gli elementi di controllo struttura a schede supportano ora lo stato di un elemento per supportare il \_ messaggio TCM DESELECTALL. Inoltre, la struttura TCITEM supporta i valori dello stato dell'elemento.
ms.assetid: c4181fe6-0055-45c9-a3d0-8cda051383f2
topic_type:
- apiref
api_name:
- TCIS_BUTTONPRESSED
- TCIS_HIGHLIGHTED
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5214f1a2eee757bfdf5b2a81a8916292b9d7f98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327230"
---
# <a name="tab-control-item-states"></a>Stati degli elementi di controllo Tab

Gli elementi di controllo struttura a schede supportano ora lo stato di un elemento per supportare il messaggio [**TCM \_ DESELECTALL**](tcm-deselectall.md) . Inoltre, la struttura [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) supporta i valori dello stato dell'elemento.



| Costante                                                                                                                                                                     | Descrizione                                                                                                                                                                                                                                    |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TCIS_BUTTONPRESSED"></span><span id="tcis_buttonpressed"></span><dl> <dt>**\_ButtonPressed TCIS**</dt> </dl> | [Versione 4,70](common-control-versions.md). L'elemento di controllo Tab è selezionato. Questo stato è significativo solo se è stato impostato il flag di stile dei [**\_ pulsanti TCS**](tab-control-styles.md) .<br/>                                 |
| <span id="TCIS_HIGHLIGHTED"></span><span id="tcis_highlighted"></span><dl> <dt>**TCIS \_ evidenziato**</dt> </dl>       | [Versione 4,71](common-control-versions.md). L'elemento di controllo Tab è evidenziato e la scheda e il testo vengono disegnati utilizzando il colore di evidenziazione corrente. Quando si utilizza un colore elevato, si tratta di un'interpolazione vera, non di un colore con stato.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

 





