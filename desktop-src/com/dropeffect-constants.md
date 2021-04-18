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
# <a name="dropeffect-constants"></a><span data-ttu-id="51074-103">Costanti DROPEFFECT</span><span class="sxs-lookup"><span data-stu-id="51074-103">DROPEFFECT Constants</span></span>

<span data-ttu-id="51074-104">Rappresenta le informazioni sugli effetti di un'operazione di trascinamento della selezione.</span><span class="sxs-lookup"><span data-stu-id="51074-104">Represents information about the effects of a drag-and-drop operation.</span></span> <span data-ttu-id="51074-105">La funzione [**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) e molti dei metodi in [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) e [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget) utilizzano i valori di questa enumerazione.</span><span class="sxs-lookup"><span data-stu-id="51074-105">The [**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) function and many of the methods in the [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) and [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget) use the values of this enumeration.</span></span>



| <span data-ttu-id="51074-106">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="51074-106">Constant/value</span></span>                                                                                                                                                                                                                            | <span data-ttu-id="51074-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="51074-107">Description</span></span>                                                                                                                         |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DROPEFFECT_NONE"></span><span id="dropeffect_none"></span><dl> <span data-ttu-id="51074-108"><dt>**DropEffect \_ NESSUNO**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="51074-108"><dt>**DROPEFFECT\_NONE**</dt> <dt>0</dt></span></span> </dl>                | <span data-ttu-id="51074-109">La destinazione di rilascio non può accettare i dati.</span><span class="sxs-lookup"><span data-stu-id="51074-109">Drop target cannot accept the data.</span></span><br/>                                                                                      |
| <span id="DROPEFFECT_COPY"></span><span id="dropeffect_copy"></span><dl> <span data-ttu-id="51074-110"><dt>**DropEffect \_ COPIA**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="51074-110"><dt>**DROPEFFECT\_COPY**</dt> <dt>1</dt></span></span> </dl>                | <span data-ttu-id="51074-111">Elimina i risultati in una copia.</span><span class="sxs-lookup"><span data-stu-id="51074-111">Drop results in a copy.</span></span> <span data-ttu-id="51074-112">I dati originali non vengono toccati dall'origine di trascinamento.</span><span class="sxs-lookup"><span data-stu-id="51074-112">The original data is untouched by the drag source.</span></span><br/>                                               |
| <span id="DROPEFFECT_MOVE"></span><span id="dropeffect_move"></span><dl> <span data-ttu-id="51074-113"><dt>**DropEffect \_ Sposta**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="51074-113"><dt>**DROPEFFECT\_MOVE**</dt> <dt>2</dt></span></span> </dl>                | <span data-ttu-id="51074-114">Il trascinamento dell'origine deve rimuovere i dati.</span><span class="sxs-lookup"><span data-stu-id="51074-114">Drag source should remove the data.</span></span> <br/>                                                                                     |
| <span id="DROPEFFECT_LINK"></span><span id="dropeffect_link"></span><dl> <span data-ttu-id="51074-115"><dt>**DropEffect \_ COLLEGAMENTO**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="51074-115"><dt>**DROPEFFECT\_LINK**</dt> <dt>4</dt></span></span> </dl>                | <span data-ttu-id="51074-116">Il trascinamento dell'origine deve creare un collegamento ai dati originali.</span><span class="sxs-lookup"><span data-stu-id="51074-116">Drag source should create a link to the original data.</span></span><br/>                                                                   |
| <span id="DROPEFFECT_SCROLL"></span><span id="dropeffect_scroll"></span><dl> <span data-ttu-id="51074-117"><dt>**DropEffect \_ Scorri**</dt> <dt>0x80000000</dt></span><span class="sxs-lookup"><span data-stu-id="51074-117"><dt>**DROPEFFECT\_SCROLL**</dt> <dt>0x80000000</dt></span></span> </dl> | <span data-ttu-id="51074-118">Lo scorrimento sta per iniziare o è in corso nella destinazione.</span><span class="sxs-lookup"><span data-stu-id="51074-118">Scrolling is about to start or is currently occurring in the target.</span></span> <span data-ttu-id="51074-119">Questo valore viene utilizzato oltre agli altri valori.</span><span class="sxs-lookup"><span data-stu-id="51074-119">This value is used in addition to the other values.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="51074-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="51074-120">Remarks</span></span>

<span data-ttu-id="51074-121">L'applicazione deve sempre mascherare i valori dell'enumerazione **DropEffect** per garantire la compatibilità con le implementazioni future.</span><span class="sxs-lookup"><span data-stu-id="51074-121">Your application should always mask values from the **DROPEFFECT** enumeration to ensure compatibility with future implementations.</span></span> <span data-ttu-id="51074-122">Attualmente, solo alcune delle posizioni in un valore di **DropEffect** hanno significato.</span><span class="sxs-lookup"><span data-stu-id="51074-122">Presently, only some of the positions in a **DROPEFFECT** value have meaning.</span></span> <span data-ttu-id="51074-123">In futuro verranno aggiunte altre interpretazioni per i bit.</span><span class="sxs-lookup"><span data-stu-id="51074-123">In the future, more interpretations for the bits will be added.</span></span> <span data-ttu-id="51074-124">Le origini di trascinamento e le destinazioni di rilascio devono mascherare accuratamente questi valori prima del confronto.</span><span class="sxs-lookup"><span data-stu-id="51074-124">Drag sources and drop targets should carefully mask these values appropriately before comparing.</span></span> <span data-ttu-id="51074-125">Non devono mai confrontare un **DropEffect** con, ad esempio, DropEffect \_ Copy eseguendo le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="51074-125">They should never compare a **DROPEFFECT** against, say, DROPEFFECT\_COPY by doing the following:</span></span>

``` syntax
if (dwDropEffect == DROPEFFECT_COPY)... 
```

<span data-ttu-id="51074-126">Al contrario, l'applicazione deve sempre mascherare il valore o i valori cercati utilizzando una delle tecniche seguenti:</span><span class="sxs-lookup"><span data-stu-id="51074-126">Instead, the application should always mask for the value or values being sought as using one of the following techniques:</span></span>

``` syntax
if (dwDropEffect & DROPEFFECT_COPY) == DROPEFFECT_COPY)...

if (dwDropEffect & DROPEFFECT_COPY)... 
```

<span data-ttu-id="51074-127">Questo consente la definizione di nuovi effetti di rilascio, mantenendo la compatibilità con le versioni precedenti del codice esistente.</span><span class="sxs-lookup"><span data-stu-id="51074-127">This allows for the definition of new drop effects, while preserving backward compatibility with existing code.</span></span>

## <a name="requirements"></a><span data-ttu-id="51074-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="51074-128">Requirements</span></span>



| <span data-ttu-id="51074-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="51074-129">Requirement</span></span> | <span data-ttu-id="51074-130">Valore</span><span class="sxs-lookup"><span data-stu-id="51074-130">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="51074-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="51074-131">Minimum supported client</span></span><br/> | <span data-ttu-id="51074-132">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="51074-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="51074-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="51074-133">Minimum supported server</span></span><br/> | <span data-ttu-id="51074-134">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="51074-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="51074-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="51074-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="51074-136"><dt>OleIdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="51074-136"><dt>OleIdl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51074-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="51074-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51074-138">**DoDragDrop**</span><span class="sxs-lookup"><span data-stu-id="51074-138">**DoDragDrop**</span></span>](/windows/desktop/api/Ole2/nf-ole2-dodragdrop)
</dt> <dt>

[<span data-ttu-id="51074-139">**IDropSource**</span><span class="sxs-lookup"><span data-stu-id="51074-139">**IDropSource**</span></span>](/windows/desktop/api/OleIdl/nn-oleidl-idropsource)
</dt> <dt>

[<span data-ttu-id="51074-140">**IDropTarget**</span><span class="sxs-lookup"><span data-stu-id="51074-140">**IDropTarget**</span></span>](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget)
</dt> </dl>

 

 





