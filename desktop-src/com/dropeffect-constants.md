---
title: Costanti DROPEFFECT (OleIdl. h)
description: Rappresenta le informazioni sugli effetti di un'operazione di trascinamento della selezione.
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
ms.openlocfilehash: f2b1888aa028d4e047a9a8ec1f54e2497fa28ce4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302590"
---
# <a name="dropeffect-constants"></a>Costanti DROPEFFECT

Rappresenta le informazioni sugli effetti di un'operazione di trascinamento della selezione. La funzione [**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) e molti dei metodi in [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) e [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget) utilizzano i valori di questa enumerazione.



| Costante/valore                                                                                                                                                                                                                            | Descrizione                                                                                                                         |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DROPEFFECT_NONE"></span><span id="dropeffect_none"></span><dl> <dt>**DropEffect \_ NESSUNO**</dt> <dt>0</dt> </dl>                | La destinazione di rilascio non può accettare i dati.<br/>                                                                                      |
| <span id="DROPEFFECT_COPY"></span><span id="dropeffect_copy"></span><dl> <dt>**DropEffect \_ COPIA**</dt> <dt>1</dt> </dl>                | Elimina i risultati in una copia. I dati originali non vengono toccati dall'origine di trascinamento.<br/>                                               |
| <span id="DROPEFFECT_MOVE"></span><span id="dropeffect_move"></span><dl> <dt>**DropEffect \_ Sposta**</dt> <dt>2</dt> </dl>                | Il trascinamento dell'origine deve rimuovere i dati. <br/>                                                                                     |
| <span id="DROPEFFECT_LINK"></span><span id="dropeffect_link"></span><dl> <dt>**DropEffect \_ COLLEGAMENTO**</dt> <dt>4</dt> </dl>                | Il trascinamento dell'origine deve creare un collegamento ai dati originali.<br/>                                                                   |
| <span id="DROPEFFECT_SCROLL"></span><span id="dropeffect_scroll"></span><dl> <dt>**DropEffect \_ Scorri**</dt> <dt>0x80000000</dt> </dl> | Lo scorrimento sta per iniziare o è in corso nella destinazione. Questo valore viene utilizzato oltre agli altri valori.<br/> |



## <a name="remarks"></a>Commenti

L'applicazione deve sempre mascherare i valori dell'enumerazione **DropEffect** per garantire la compatibilità con le implementazioni future. Attualmente, solo alcune delle posizioni in un valore di **DropEffect** hanno significato. In futuro verranno aggiunte altre interpretazioni per i bit. Le origini di trascinamento e le destinazioni di rilascio devono mascherare accuratamente questi valori prima del confronto. Non devono mai confrontare un **DropEffect** con, ad esempio, DropEffect \_ Copy eseguendo le operazioni seguenti:

``` syntax
if (dwDropEffect == DROPEFFECT_COPY)... 
```

Al contrario, l'applicazione deve sempre mascherare il valore o i valori cercati utilizzando una delle tecniche seguenti:

``` syntax
if (dwDropEffect & DROPEFFECT_COPY) == DROPEFFECT_COPY)...

if (dwDropEffect & DROPEFFECT_COPY)... 
```

Questo consente la definizione di nuovi effetti di rilascio, mantenendo la compatibilità con le versioni precedenti del codice esistente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>OleIdl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop)
</dt> <dt>

[**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource)
</dt> <dt>

[**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget)
</dt> </dl>

 

 





