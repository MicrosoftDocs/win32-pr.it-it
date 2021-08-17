---
title: Costanti DROPEFFECT (OleIdl.h)
description: Rappresenta informazioni sugli effetti di un'operazione di trascinamento della selezione.
ms.assetid: d8e46899-3fbf-4012-8dd3-67fa627526d5
topic_type:
- apiref
api_name:
- DROPEFFECT_NONE
- DROPEFFECT_COPY
- DROPEFFECT_MOVE
- DROPEFFECT_LINK
- DROPEFFECT_SCROLL
api_location:
- OleIdl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05c9a4fa961b0da2e654d4672392104b95e718bbb176167c7bb715c39f25cfc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736953"
---
# <a name="dropeffect-constants"></a>Costanti DROPEFFECT

Rappresenta informazioni sugli effetti di un'operazione di trascinamento della selezione. La [**funzione DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) e molti dei metodi in [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) e [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget) usano i valori di questa enumerazione.



| Costante/valore                                                                                                                                                                                                                            | Descrizione                                                                                                                         |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DROPEFFECT_NONE"></span><span id="dropeffect_none"></span><dl> <dt>**DROPEFFECT \_ NONE**</dt> <dt>0</dt> </dl>                | La destinazione di rilascio non può accettare i dati.<br/>                                                                                      |
| <span id="DROPEFFECT_COPY"></span><span id="dropeffect_copy"></span><dl> <dt>**DROPEFFECT \_ COPIA**</dt> <dt>1</dt> </dl>                | Eliminare i risultati in una copia. I dati originali non vengono toccati dall'origine di trascinamento.<br/>                                               |
| <span id="DROPEFFECT_MOVE"></span><span id="dropeffect_move"></span><dl> <dt>**DROPEFFECT \_ MOVE**</dt> <dt>2</dt> </dl>                | Trascinare l'origine per rimuovere i dati. <br/>                                                                                     |
| <span id="DROPEFFECT_LINK"></span><span id="dropeffect_link"></span><dl> <dt>**DROPEFFECT \_ COLLEGAMENTO**</dt> <dt>4</dt> </dl>                | Trascinare l'origine per creare un collegamento ai dati originali.<br/>                                                                   |
| <span id="DROPEFFECT_SCROLL"></span><span id="dropeffect_scroll"></span><dl> <dt>**DROPEFFECT \_ SCORRIMENTO**</dt> <dt>0x80000000</dt> </dl> | Lo scorrimento sta per iniziare o è attualmente in corso nella destinazione. Questo valore viene usato in aggiunta agli altri valori.<br/> |



## <a name="remarks"></a>Commenti

L'applicazione deve sempre mascherare i valori **dell'enumerazione DROPEFFECT** per garantire la compatibilità con le implementazioni future. Attualmente, solo alcune delle posizioni in un **valore DROPEFFECT** hanno un significato. In futuro verranno aggiunte altre interpretazioni per i bit. Le origini di trascinamento e le destinazioni di rilascio devono mascherare attentamente questi valori in modo appropriato prima del confronto. Non devono mai confrontare **DROPEFFECT** con DROPEFFECT \_ COPY eseguendo le operazioni seguenti:

``` syntax
if (dwDropEffect == DROPEFFECT_COPY)... 
```

Al contrario, l'applicazione deve sempre mascherare il valore o i valori cercati usando una delle tecniche seguenti:

``` syntax
if (dwDropEffect & DROPEFFECT_COPY) == DROPEFFECT_COPY)...

if (dwDropEffect & DROPEFFECT_COPY)... 
```

Ciò consente la definizione di nuovi effetti di rilascio, mantenendo al tempo stesso la compatibilità con le versioni precedenti con il codice esistente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>OleIdl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Dodragdrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop)
</dt> <dt>

[**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource)
</dt> <dt>

[**Idroptarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget)
</dt> </dl>

 

 





