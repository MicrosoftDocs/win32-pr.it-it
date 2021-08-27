---
title: Tree-View degli elementi di controllo (CommCtrl.h)
description: In questa sezione vengono elencati i flag di stato degli elementi utilizzati per indicare lo stato di un elemento in un controllo di visualizzazione albero.
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
ms.openlocfilehash: f5adb0371e3796c5d512ff3582a5c65850dc6cf8261f138934d46640aa57bf28
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045961"
---
# <a name="tree-view-control-item-states"></a>Tree-View degli elementi di controllo

In questa sezione vengono elencati i flag di stato degli elementi utilizzati per indicare lo stato di un elemento in un controllo di visualizzazione albero.



| Costante                                                                                                                                                                        | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TVIS_BOLD"></span><span id="tvis_bold"></span><dl> <dt>**TVIS \_ BOLD**</dt> </dl>                               | L'elemento è in grassetto.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="TVIS_CUT"></span><span id="tvis_cut"></span><dl> <dt>**TVIS \_ CUT**</dt> </dl>                                  | L'elemento viene selezionato come parte di un'operazione taglia e incolla. <br/>                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="TVIS_DROPHILITED"></span><span id="tvis_drophilited"></span><dl> <dt>**TVIS \_ DROPTED**</dt> </dl>          | L'elemento viene selezionato come destinazione di trascinamento della selezione.<br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="TVIS_EXPANDED"></span><span id="tvis_expanded"></span><dl> <dt>**TVIS \_ ESPANSO**</dt> </dl>                   | L'elenco degli elementi figlio dell'elemento è attualmente espanso. ciò significa che gli elementi figlio sono visibili. Questo valore si applica solo agli elementi padre.<br/>                                                                                                                                                                                                                                                                                                                  |
| <span id="TVIS_EXPANDEDONCE"></span><span id="tvis_expandedonce"></span><dl> <dt>**TVIS \_ EXPANDEDONCE**</dt> </dl>       | L'elenco degli elementi figlio dell'elemento è stato espanso almeno una volta. I codici di notifica [ \_ TVN ITEMEXPANDING](tvn-itemexpanding.md) e [ \_ TVN ITEMEXPANDED](tvn-itemexpanded.md) non vengono generati per gli elementi padre con questo stato impostato in risposta a un messaggio [**TVM \_ EXPAND.**](tvm-expand.md) L'uso di TVE \_ COLLAPSE e TVE \_ COLLAPSERESET con **TVM \_ EXPAND** causerà la reimpostazione di questo stato. Questo valore si applica solo agli elementi padre. <br/> |
| <span id="TVIS_EXPANDPARTIAL"></span><span id="tvis_expandpartial"></span><dl> <dt>**TVIS \_ EXPANDPARTIAL**</dt> </dl>    | **Versione 4.70.** Elemento di visualizzazione albero parzialmente espanso. In questo stato, alcuni, ma non tutti, degli elementi figlio sono visibili e viene visualizzato il simbolo più dell'elemento padre. <br/>                                                                                                                                                                                                                                                                              |
| <span id="TVIS_SELECTED"></span><span id="tvis_selected"></span><dl> <dt>**TVIS \_ SELEZIONATO**</dt> </dl>                   | L'elemento è selezionato. L'aspetto dipende dal fatto che abbia lo stato attivo. L'elemento verrà disegnato usando i colori di sistema per la selezione. <br/>                                                                                                                                                                                                                                                                                                              |
| <span id="TVIS_OVERLAYMASK"></span><span id="tvis_overlaymask"></span><dl> <dt>**MASCHERA DI \_ SOVRIMPRESSIONE TVIS**</dt> </dl>          | Maschera per i bit usati per specificare l'indice dell'immagine di sovrimpressione dell'elemento.<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="TVIS_STATEIMAGEMASK"></span><span id="tvis_stateimagemask"></span><dl> <dt>**TVIS \_ STATEIMAGEMASK**</dt> </dl> | Maschera per i bit utilizzati per specificare l'indice dell'immagine di stato dell'elemento.<br/>                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="TVIS_USERMASK"></span><span id="tvis_usermask"></span><dl> <dt>**TVIS \_ USERMASK**</dt> </dl>                   | Uguale a **TVIS \_ STATEIMAGEMASK.**<br/>                                                                                                                                                                                                                                                                                                                                                                                                                     |



## <a name="remarks"></a>Commenti

Quando si imposta o si recupera l'indice dell'immagine di sovrimpressione di un elemento o l'indice dell'immagine di stato, è necessario specificare le maschere seguenti nel membro **stateMask** della [**struttura TVITEM:**](/windows/win32/api/commctrl/ns-commctrl-tvitema)

-   **MASCHERA DI \_ SOVRIMPRESSIONE TVIS**
-   **TVIS \_ STATEIMAGEMASK**
-   **TVIS \_ USERMASK**

Questi valori possono essere usati anche per mascherare i bit di stato non di interesse.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



 

 





