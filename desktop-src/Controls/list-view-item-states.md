---
title: Stati degli elementi List-View (CommCtrl. h)
description: Il valore dello stato di un elemento è costituito dallo stato dell'elemento, da un indice della maschera di sovrapposizione facoltativo e da un indice facoltativo della maschera di immagine di stato.
ms.assetid: 21827f4a-f133-489b-bbd2-6979d1928b40
topic_type:
- apiref
api_name:
- LVIS_ACTIVATING
- LVIS_CUT
- LVIS_DROPHILITED
- LVIS_FOCUSED
- LVIS_OVERLAYMASK
- LVIS_SELECTED
- LVIS_STATEIMAGEMASK
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8432760dd4cc7efde30700f837864ddcf04aac31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327862"
---
# <a name="list-view-item-states"></a>Stati elemento List-View

Il valore dello stato di un elemento è costituito dallo stato dell'elemento, da un indice della maschera di sovrapposizione facoltativo e da un indice facoltativo della maschera di immagine di stato.

Lo stato di un elemento ne determina l'aspetto e le funzionalità. Lo stato può essere zero o uno o più dei valori seguenti:



| Costante                                                                                                                                                                        | Descrizione                                                                                                                                                          |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVIS_ACTIVATING"></span><span id="lvis_activating"></span><dl> <dt>**attivazione di LVIS \_**</dt> </dl>             | Non è attualmente supportato.<br/>                                                                                                                                  |
| <span id="LVIS_CUT"></span><span id="lvis_cut"></span><dl> <dt>**\_taglia lvis**</dt> </dl>                                  | L'elemento è contrassegnato per un'operazione di taglia e incolla.<br/>                                                                                                         |
| <span id="LVIS_DROPHILITED"></span><span id="lvis_drophilited"></span><dl> <dt>**\_DROPHILITED lvis**</dt> </dl>          | L'elemento è evidenziato come destinazione di trascinamento della selezione.<br/>                                                                                                        |
| <span id="LVIS_FOCUSED"></span><span id="lvis_focused"></span><dl> <dt>**LVIS con stato \_ attivo**</dt> </dl>                      | L'elemento ha lo stato attivo, quindi è racchiuso da un rettangolo di attivazione standard. Sebbene sia possibile selezionare più di un elemento, solo un elemento può avere lo stato attivo.<br/> |
| <span id="LVIS_OVERLAYMASK"></span><span id="lvis_overlaymask"></span><dl> <dt>**\_OVERLAYMASK lvis**</dt> </dl>          | L'indice dell'immagine sovrapposta dell'elemento viene recuperato da una maschera.<br/>                                                                                                    |
| <span id="LVIS_SELECTED"></span><span id="lvis_selected"></span><dl> <dt>**LVIS \_ selezionato**</dt> </dl>                   | L'elemento è selezionato. L'aspetto di un elemento selezionato dipende dal fatto che abbia lo stato attivo e anche sui colori di sistema usati per la selezione.<br/>             |
| <span id="LVIS_STATEIMAGEMASK"></span><span id="lvis_stateimagemask"></span><dl> <dt>**\_STATEIMAGEMASK lvis**</dt> </dl> | L'indice dell'immagine di stato dell'elemento viene recuperato da una maschera.<br/>                                                                                                      |



## <a name="remarks"></a>Commenti

È possibile usare **lvis \_ OVERLAYMASK** mask per isolare l'indice in base uno dell'immagine sovrapposta. È possibile usare **lvis \_ STATEIMAGEMASK** mask per isolare l'indice in base uno dell'immagine di stato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

 





