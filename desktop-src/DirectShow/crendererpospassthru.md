---
description: La classe CRendererPosPassThru gestisce i comandi Seek per i filtri renderer, passandoli upstream al filtro successivo.
ms.assetid: 7b532177-939c-4cb7-a6fa-c0133f65c768
title: Classe CRendererPosPassThru (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7154dde8adefdb3292107e9c33d7b6a2b54f6af0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327193"
---
# <a name="crendererpospassthru-class"></a><span data-ttu-id="6febe-103">Classe CRendererPosPassThru</span><span class="sxs-lookup"><span data-stu-id="6febe-103">CRendererPosPassThru class</span></span>

![gerarchia di classi crendererpospassthru](images/cutil14.png)

<span data-ttu-id="6febe-105">La `CRendererPosPassThru` classe gestisce i comandi Seek per i filtri renderer, passandoli upstream al filtro successivo.</span><span class="sxs-lookup"><span data-stu-id="6febe-105">The `CRendererPosPassThru` class handles seek commands for renderer filters, by passing them upstream to the next filter.</span></span>

<span data-ttu-id="6febe-106">Questa classe deriva dalla classe [**CPosPassThru**](cpospassthru.md) .</span><span class="sxs-lookup"><span data-stu-id="6febe-106">This class derives from the [**CPosPassThru**](cpospassthru.md) class.</span></span> <span data-ttu-id="6febe-107">Viene aggiunto il supporto per la memorizzazione nella cache dei timestamp degli esempi Man mano che arrivano.</span><span class="sxs-lookup"><span data-stu-id="6febe-107">It adds support for caching the time stamps from samples as they arrive.</span></span> <span data-ttu-id="6febe-108">Usare questa classe nello stesso modo della classe **CPosPassThru** .</span><span class="sxs-lookup"><span data-stu-id="6febe-108">Use this class in the same way as the **CPosPassThru** class.</span></span> <span data-ttu-id="6febe-109">Per informazioni dettagliate, vedere la documentazione di **CPosPassThru** .</span><span class="sxs-lookup"><span data-stu-id="6febe-109">Refer to the **CPosPassThru** documentation for details.</span></span>

<span data-ttu-id="6febe-110">Il filtro renderer deve aggiornare i `CRendererPosPassThru` timestamp memorizzati nella cache dell'oggetto, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="6febe-110">The renderer filter must update the `CRendererPosPassThru` object's cached time stamps, as follows:</span></span>

-   <span data-ttu-id="6febe-111">Per ogni esempio che il filtro riceve, chiamare il metodo [**CRendererPosPassThru:: RegisterMediaTime**](crendererpospassthru-registermediatime.md) .</span><span class="sxs-lookup"><span data-stu-id="6febe-111">For each sample the filter receives, call the [**CRendererPosPassThru::RegisterMediaTime**](crendererpospassthru-registermediatime.md) method.</span></span>
-   <span data-ttu-id="6febe-112">Quando il filtro viene arrestato o riceve una chiamata **EndFlush** , chiamare il metodo [**CRendererPosPassThru:: ResetMediaTime**](crendererpospassthru-resetmediatime.md) .</span><span class="sxs-lookup"><span data-stu-id="6febe-112">When the filter is stopped or receives an **EndFlush** call, call the [**CRendererPosPassThru::ResetMediaTime**](crendererpospassthru-resetmediatime.md) method.</span></span>
-   <span data-ttu-id="6febe-113">Quando il filtro riceve una notifica di fine flusso, chiamare il metodo [**CRendererPosPassThru:: EOS**](crendererpospassthru-eos.md) .</span><span class="sxs-lookup"><span data-stu-id="6febe-113">When the filter receives an end-of-stream notification, call the [**CRendererPosPassThru::EOS**](crendererpospassthru-eos.md) method.</span></span>

<span data-ttu-id="6febe-114">Per un esempio di come usare questa classe, vedere il codice sorgente di [**CBaseRenderer**](cbaserenderer.md) .</span><span class="sxs-lookup"><span data-stu-id="6febe-114">For an example of how to use this class, refer to the [**CBaseRenderer**](cbaserenderer.md) source code.</span></span>



| <span data-ttu-id="6febe-115">Metodi pubblici</span><span class="sxs-lookup"><span data-stu-id="6febe-115">Public Methods</span></span>                                                            | <span data-ttu-id="6febe-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6febe-116">Description</span></span>                                                         |
|---------------------------------------------------------------------------|---------------------------------------------------------------------|
| [<span data-ttu-id="6febe-117">**CRendererPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="6febe-117">**CRendererPosPassThru**</span></span>](crendererpospassthru-crendererpospassthru.md) | <span data-ttu-id="6febe-118">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="6febe-118">Constructor method.</span></span>                                                 |
| [<span data-ttu-id="6febe-119">**GetMediaTime**</span><span class="sxs-lookup"><span data-stu-id="6febe-119">**GetMediaTime**</span></span>](crendererpospassthru-getmediatime.md)                 | <span data-ttu-id="6febe-120">Recupera i timestamp sull'esempio corrente.</span><span class="sxs-lookup"><span data-stu-id="6febe-120">Retrieves the time stamps on the current sample.</span></span>                    |
| [<span data-ttu-id="6febe-121">**RegisterMediaTime**</span><span class="sxs-lookup"><span data-stu-id="6febe-121">**RegisterMediaTime**</span></span>](crendererpospassthru-registermediatime.md)       | <span data-ttu-id="6febe-122">Memorizza nella cache i timestamp dell'esempio corrente.</span><span class="sxs-lookup"><span data-stu-id="6febe-122">Caches the time stamps from the current sample.</span></span>                     |
| [<span data-ttu-id="6febe-123">**ResetMediaTime**</span><span class="sxs-lookup"><span data-stu-id="6febe-123">**ResetMediaTime**</span></span>](crendererpospassthru-resetmediatime.md)             | <span data-ttu-id="6febe-124">Reimposta i timestamp memorizzati nella cache su zero.</span><span class="sxs-lookup"><span data-stu-id="6febe-124">Resets the cached time stamps to zero.</span></span>                              |
| [<span data-ttu-id="6febe-125">**EOS**</span><span class="sxs-lookup"><span data-stu-id="6febe-125">**EOS**</span></span>](crendererpospassthru-eos.md)                                   | <span data-ttu-id="6febe-126">Aggiorna i timestamp memorizzati nella cache dopo una notifica di fine del flusso.</span><span class="sxs-lookup"><span data-stu-id="6febe-126">Updates the cached time stamps after an end-of-stream notification.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="6febe-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6febe-127">Requirements</span></span>



| <span data-ttu-id="6febe-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="6febe-128">Requirement</span></span> | <span data-ttu-id="6febe-129">Valore</span><span class="sxs-lookup"><span data-stu-id="6febe-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6febe-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6febe-130">Header</span></span><br/>  | <dl> <span data-ttu-id="6febe-131"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6febe-131"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6febe-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="6febe-132">Library</span></span><br/> | <dl> <span data-ttu-id="6febe-133"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="6febe-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




