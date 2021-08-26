---
title: Stati degli elementi del controllo Tab (CommCtrl.h)
description: Gli elementi del controllo Struttura a schede supportano ora lo stato di un elemento per supportare il messaggio \_ TCM DESELECTALL. Inoltre, la struttura TCITEM supporta i valori dello stato dell'elemento.
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
ms.openlocfilehash: 75f3bba0ecd29c7ab84c6b68010f8af52c8db2cfc9dc4080fb73e37b408ee1a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919281"
---
# <a name="tab-control-item-states"></a>Stati degli elementi del controllo Struttura a schede

Gli elementi del controllo Struttura a schede supportano ora lo stato di un elemento per supportare il [**messaggio \_ TCM DESELECTALL.**](tcm-deselectall.md) Inoltre, la struttura [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) supporta i valori dello stato dell'elemento.



| Costante                                                                                                                                                                     | Descrizione                                                                                                                                                                                                                                    |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TCIS_BUTTONPRESSED"></span><span id="tcis_buttonpressed"></span><dl> <dt>**PULSANTE \_ TCISPRESSO**</dt> </dl> | [Versione 4.70](common-control-versions.md). L'elemento del controllo Struttura a schede è selezionato. Questo stato è significativo solo se è stato impostato il flag di stile [**\_ TCS BUTTONS.**](tab-control-styles.md)<br/>                                 |
| <span id="TCIS_HIGHLIGHTED"></span><span id="tcis_highlighted"></span><dl> <dt>**TCIS \_ EVIDENZIATO**</dt> </dl>       | [Versione 4.71](common-control-versions.md). L'elemento del controllo Struttura a schede è evidenziato e la scheda e il testo vengono disegnati usando il colore di evidenziazione corrente. Quando si usa il colore alto, si tratta di una vera interpolazione, non di un colore dithering.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



 

 





