---
title: Stati degli elementi di controllo Tree-View (CommCtrl. h)
description: In questa sezione sono elencati i flag di stato dell'elemento utilizzati per indicare lo stato di un elemento in un controllo di visualizzazione albero.
ms.assetid: 5b11d575-6dfd-47a8-b959-b19aaeeca70e
topic_type:
- apiref
api_name:
- TVIS_BOLD
- TVIS_CUT
- TVIS_DROPHILITED
- TVIS_EXPANDED
- TVIS_EXPANDEDONCE
- TVIS_EXPANDPARTIAL
- TVIS_SELECTED
- TVIS_OVERLAYMASK
- TVIS_STATEIMAGEMASK
- TVIS_USERMASK
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef4a19306855b7f38d03aa00323b26407f108bfe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326839"
---
# <a name="tree-view-control-item-states"></a>Stati degli elementi di controllo Tree-View

In questa sezione sono elencati i flag di stato dell'elemento utilizzati per indicare lo stato di un elemento in un controllo di visualizzazione albero.



| Costante                                                                                                                                                                        | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TVIS_BOLD"></span><span id="tvis_bold"></span><dl> <dt>**TVIS \_ grassetto**</dt> </dl>                               | L'elemento è in grassetto.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="TVIS_CUT"></span><span id="tvis_cut"></span><dl> <dt>**\_taglia TVIS**</dt> </dl>                                  | L'elemento viene selezionato come parte di un'operazione di taglia e incolla. <br/>                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="TVIS_DROPHILITED"></span><span id="tvis_drophilited"></span><dl> <dt>**\_DROPHILITED TVIS**</dt> </dl>          | L'elemento è selezionato come destinazione di trascinamento della selezione.<br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="TVIS_EXPANDED"></span><span id="tvis_expanded"></span><dl> <dt>**TVIS \_ espansa**</dt> </dl>                   | L'elenco di elementi figlio dell'elemento è attualmente espanso; ovvero gli elementi figlio sono visibili. Questo valore si applica solo agli elementi padre.<br/>                                                                                                                                                                                                                                                                                                                  |
| <span id="TVIS_EXPANDEDONCE"></span><span id="tvis_expandedonce"></span><dl> <dt>**\_EXPANDEDONCE TVIS**</dt> </dl>       | L'elenco di elementi figlio dell'elemento è stato espanso almeno una volta. I codici di notifica di [TVN \_ ITEMEXPANDING](tvn-itemexpanding.md) e [TVN \_ ITEMEXPANDED](tvn-itemexpanded.md) non vengono generati per gli elementi padre con questo stato impostato in risposta a un messaggio di [**\_ espansione TVM**](tvm-expand.md) . L'uso \_ di TVE Collapse e TVE \_ COLLAPSERESET con **TVM \_ expand** provocherà la reimpostazione di questo stato. Questo valore si applica solo agli elementi padre. <br/> |
| <span id="TVIS_EXPANDPARTIAL"></span><span id="tvis_expandpartial"></span><dl> <dt>**\_EXPANDPARTIAL TVIS**</dt> </dl>    | **Versione 4,70**. Elemento visualizzazione albero parzialmente espanso. In questo stato, alcuni, ma non tutti, gli elementi figlio sono visibili e viene visualizzato il simbolo più dell'elemento padre. <br/>                                                                                                                                                                                                                                                                              |
| <span id="TVIS_SELECTED"></span><span id="tvis_selected"></span><dl> <dt>**TVIS \_ selezionato**</dt> </dl>                   | L'elemento è selezionato. Il relativo aspetto dipende dal fatto che abbia lo stato attivo. L'elemento verrà disegnato usando i colori di sistema per la selezione. <br/>                                                                                                                                                                                                                                                                                                              |
| <span id="TVIS_OVERLAYMASK"></span><span id="tvis_overlaymask"></span><dl> <dt>**\_OVERLAYMASK TVIS**</dt> </dl>          | Maschera per i bit utilizzati per specificare l'indice dell'immagine sovrapposta dell'elemento.<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="TVIS_STATEIMAGEMASK"></span><span id="tvis_stateimagemask"></span><dl> <dt>**\_STATEIMAGEMASK TVIS**</dt> </dl> | Maschera per i bit utilizzati per specificare l'indice dell'immagine di stato dell'elemento.<br/>                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="TVIS_USERMASK"></span><span id="tvis_usermask"></span><dl> <dt>**\_usermask TVIS**</dt> </dl>                   | Uguale a **TVIS \_ STATEIMAGEMASK**.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                     |



## <a name="remarks"></a>Commenti

Quando si imposta o recupera l'indice dell'immagine sovrapposta o dell'immagine di stato di un elemento, è necessario specificare le maschere seguenti nel membro **stateMask** della struttura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) :

-   **\_OVERLAYMASK TVIS**
-   **\_STATEIMAGEMASK TVIS**
-   **\_usermask TVIS**

Questi valori possono essere usati anche per mascherare i bit di stato che non sono di interesse.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

 





