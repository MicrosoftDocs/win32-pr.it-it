---
title: List-View stati degli elementi (CommCtrl.h)
description: Il valore dello stato di un elemento è costituito dallo stato dell'elemento, da un indice di maschera di sovrimpressione facoltativo e da un indice di maschera immagine di stato facoltativo.
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
ms.openlocfilehash: 9040272afc16f500806a3d7a90a0b062018d2f4dec8510e4abe57b24cbc75e88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958390"
---
# <a name="list-view-item-states"></a>List-View stati degli elementi

Il valore dello stato di un elemento è costituito dallo stato dell'elemento, da un indice di maschera di sovrimpressione facoltativo e da un indice di maschera immagine di stato facoltativo.

Lo stato di un elemento ne determina l'aspetto e la funzionalità. Lo stato può essere zero o uno o più dei valori seguenti:



| Costante                                                                                                                                                                        | Descrizione                                                                                                                                                          |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVIS_ACTIVATING"></span><span id="lvis_activating"></span><dl> <dt>**ATTIVAZIONE DI \_ LVIS**</dt> </dl>             | Non è attualmente supportato.<br/>                                                                                                                                  |
| <span id="LVIS_CUT"></span><span id="lvis_cut"></span><dl> <dt>**LVIS \_ CUT**</dt> </dl>                                  | L'elemento è contrassegnato per un'operazione taglia e incolla.<br/>                                                                                                         |
| <span id="LVIS_DROPHILITED"></span><span id="lvis_drophilited"></span><dl> <dt>**LVIS \_ DROPTED**</dt> </dl>          | L'elemento viene evidenziato come destinazione di trascinamento della selezione.<br/>                                                                                                        |
| <span id="LVIS_FOCUSED"></span><span id="lvis_focused"></span><dl> <dt>**LVIS \_ INCENTRATO**</dt> </dl>                      | L'elemento ha lo stato attivo, quindi è racchiuso da un rettangolo di attivazione standard. Anche se è possibile selezionare più di un elemento, solo un elemento può avere lo stato attivo.<br/> |
| <span id="LVIS_OVERLAYMASK"></span><span id="lvis_overlaymask"></span><dl> <dt>**LVIS \_ OVERLAYMASK**</dt> </dl>          | L'indice dell'immagine di sovrimpressione dell'elemento viene recuperato da una maschera.<br/>                                                                                                    |
| <span id="LVIS_SELECTED"></span><span id="lvis_selected"></span><dl> <dt>**LVIS \_ SELEZIONATO**</dt> </dl>                   | L'elemento è selezionato. L'aspetto di un elemento selezionato dipende dal fatto che abbia lo stato attivo e anche dai colori di sistema usati per la selezione.<br/>             |
| <span id="LVIS_STATEIMAGEMASK"></span><span id="lvis_stateimagemask"></span><dl> <dt>**LVIS \_ STATEIMAGEMASK**</dt> </dl> | L'indice dell'immagine di stato dell'elemento viene recuperato da una maschera.<br/>                                                                                                      |



## <a name="remarks"></a>Commenti

È possibile usare la maschera **LVIS \_ OVERLAYMASK** per isolare l'indice in base uno dell'immagine di sovrimpressione. È possibile usare la maschera **LVIS \_ STATEIMAGEMASK** per isolare l'indice in base uno dell'immagine di stato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



 

 





