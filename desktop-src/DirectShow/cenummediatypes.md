---
description: La classe CEnumMediaTypes implementa un enumeratore per i tipi di supporto preferiti.
ms.assetid: 50a90926-0bc7-4204-8000-81894bd154ac
title: Classe CEnumMediaTypes (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ad5e1de9eb2edbdb63eb6f476391ae8387c8d01e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329844"
---
# <a name="cenummediatypes-class"></a><span data-ttu-id="e8758-103">Classe CEnumMediaTypes</span><span class="sxs-lookup"><span data-stu-id="e8758-103">CEnumMediaTypes class</span></span>

![gerarchia di classi cenummediatypes](images/filter04.png)

<span data-ttu-id="e8758-105">La `CEnumMediaTypes` classe implementa un enumeratore per i tipi di supporto preferiti.</span><span class="sxs-lookup"><span data-stu-id="e8758-105">The `CEnumMediaTypes` class implements an enumerator for preferred media types.</span></span>

<span data-ttu-id="e8758-106">Questa classe implementa l'interfaccia [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) .</span><span class="sxs-lookup"><span data-stu-id="e8758-106">This class implements the [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) interface.</span></span> <span data-ttu-id="e8758-107">Chiama i metodi [**CBasePin**](cbasepin.md) seguenti:</span><span class="sxs-lookup"><span data-stu-id="e8758-107">It calls the following [**CBasePin**](cbasepin.md) methods:</span></span>

-   <span data-ttu-id="e8758-108">[**CBasePin:: GetMediaType**](cbasepin-getmediatype.md): Recupera un tipo di supporto, a cui fa riferimento un indice in base zero.</span><span class="sxs-lookup"><span data-stu-id="e8758-108">[**CBasePin::GetMediaType**](cbasepin-getmediatype.md):Retrieves a media type, referenced by a zero-based index.</span></span>
-   <span data-ttu-id="e8758-109">[**CBasePin:: GetMediaTypeVersion**](cbasepin-getmediatypeversion.md): determina se il set di tipi preferiti è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="e8758-109">[**CBasePin::GetMediaTypeVersion**](cbasepin-getmediatypeversion.md): Determines whether the set of preferred types has changed.</span></span>

<span data-ttu-id="e8758-110">Ogni volta che un pin modifica l'elenco dei tipi di supporto preferiti, il pin incrementa il numero di versione del tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="e8758-110">Whenever a pin alters its list of preferred media types, the pin increments the media-type version number.</span></span> <span data-ttu-id="e8758-111">Quando ciò si verifica, l'oggetto enumeratore non è più sincronizzato con il PIN e i metodi della classe restituiscono l'enumerazione VFW e non è \_ \_ \_ \_ \_ sincronizzata.</span><span class="sxs-lookup"><span data-stu-id="e8758-111">When this happens, the enumerator object is no longer synchronized with the pin, and the class methods return VFW\_E\_ENUM\_OUT\_OF\_SYNC.</span></span> <span data-ttu-id="e8758-112">Chiamare il metodo [**CEnumMediaTypes:: Reset**](cenummediatypes-reset.md) per risincronizzare l'enumeratore.</span><span class="sxs-lookup"><span data-stu-id="e8758-112">Call the [**CEnumMediaTypes::Reset**](cenummediatypes-reset.md) method to resynchronize the enumerator.</span></span>



| <span data-ttu-id="e8758-113">Metodi pubblici</span><span class="sxs-lookup"><span data-stu-id="e8758-113">Public Methods</span></span>                                               | <span data-ttu-id="e8758-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e8758-114">Description</span></span>                                                     |
|--------------------------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="e8758-115">**CEnumMediaTypes**</span><span class="sxs-lookup"><span data-stu-id="e8758-115">**CEnumMediaTypes**</span></span>](cenummediatypes-cenummediatypes.md)   | <span data-ttu-id="e8758-116">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="e8758-116">Constructor method.</span></span>                                             |
| [<span data-ttu-id="e8758-117">**~ CEnumMediaTypes**</span><span class="sxs-lookup"><span data-stu-id="e8758-117">**~CEnumMediaTypes**</span></span>](cenummediatypes--cenummediatypes.md) | <span data-ttu-id="e8758-118">Metodo del distruttore.</span><span class="sxs-lookup"><span data-stu-id="e8758-118">Destructor method.</span></span> <span data-ttu-id="e8758-119">Virtuale.</span><span class="sxs-lookup"><span data-stu-id="e8758-119">Virtual.</span></span>                                     |
| <span data-ttu-id="e8758-120">Metodi IEnumMediaTypes</span><span class="sxs-lookup"><span data-stu-id="e8758-120">IEnumMediaTypes Methods</span></span>                                      | <span data-ttu-id="e8758-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e8758-121">Description</span></span>                                                     |
| [<span data-ttu-id="e8758-122">**Clone**</span><span class="sxs-lookup"><span data-stu-id="e8758-122">**Clone**</span></span>](cenummediatypes-clone.md)                       | <span data-ttu-id="e8758-123">Crea una copia dell'enumeratore con lo stesso stato di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="e8758-123">Makes a copy of the enumerator with the same enumeration state.</span></span> |
| [<span data-ttu-id="e8758-124">**Avanti**</span><span class="sxs-lookup"><span data-stu-id="e8758-124">**Next**</span></span>](cenummediatypes-next.md)                         | <span data-ttu-id="e8758-125">Recupera un numero specificato di tipi di supporti.</span><span class="sxs-lookup"><span data-stu-id="e8758-125">Retrieves a specified number of media types.</span></span>                    |
| [<span data-ttu-id="e8758-126">**Reset**</span><span class="sxs-lookup"><span data-stu-id="e8758-126">**Reset**</span></span>](cenummediatypes-reset.md)                       | <span data-ttu-id="e8758-127">Riporta all'inizio la sequenza di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="e8758-127">Resets the enumeration sequence to the beginning.</span></span>               |
| [<span data-ttu-id="e8758-128">**Ignora**</span><span class="sxs-lookup"><span data-stu-id="e8758-128">**Skip**</span></span>](cenummediatypes-skip.md)                         | <span data-ttu-id="e8758-129">Ignora un numero specificato di tipi di supporti.</span><span class="sxs-lookup"><span data-stu-id="e8758-129">Skips over a specified number of media types.</span></span>                   |



 

## <a name="requirements"></a><span data-ttu-id="e8758-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e8758-130">Requirements</span></span>



| <span data-ttu-id="e8758-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8758-131">Requirement</span></span> | <span data-ttu-id="e8758-132">Valore</span><span class="sxs-lookup"><span data-stu-id="e8758-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8758-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e8758-133">Header</span></span><br/>  | <dl> <span data-ttu-id="e8758-134"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e8758-134"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e8758-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="e8758-135">Library</span></span><br/> | <dl> <span data-ttu-id="e8758-136"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e8758-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




