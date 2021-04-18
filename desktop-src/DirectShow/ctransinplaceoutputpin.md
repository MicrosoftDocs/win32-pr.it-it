---
description: La classe CTransInPlaceOutputPin implementa un pin di output usato dalla classe CTransInPlaceFilter.
ms.assetid: 90d54807-85c1-43b9-8998-e1bcf7b54725
title: Classe CTransInPlaceOutputPin (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e41fbff07a9bdeb8990bbf3ddba6d9f7455d1bad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326168"
---
# <a name="ctransinplaceoutputpin-class"></a><span data-ttu-id="171d3-103">Classe CTransInPlaceOutputPin</span><span class="sxs-lookup"><span data-stu-id="171d3-103">CTransInPlaceOutputPin class</span></span>

![gerarchia di classi ctransinplaceoutputpin](images/tsip02.png)

<span data-ttu-id="171d3-105">La `CTransInPlaceOutputPin` classe implementa un pin di output usato dalla classe [**CTransInPlaceFilter**](ctransinplacefilter.md) .</span><span class="sxs-lookup"><span data-stu-id="171d3-105">The `CTransInPlaceOutputPin` class implements an output pin that is used by the [**CTransInPlaceFilter**](ctransinplacefilter.md) class.</span></span>

<span data-ttu-id="171d3-106">In genere, non è necessario derivare da questa classe.</span><span class="sxs-lookup"><span data-stu-id="171d3-106">Typically, you do not need to derive from this class.</span></span> <span data-ttu-id="171d3-107">In tal caso, è necessario eseguire l'override del metodo [**CTransInPlaceFilter:: GetPin**](ctransinplacefilter-getpin.md) del filtro per creare istanze della classe derivata.</span><span class="sxs-lookup"><span data-stu-id="171d3-107">If you do, you must override the filter's [**CTransInPlaceFilter::GetPin**](ctransinplacefilter-getpin.md) method to create instances of your derived class.</span></span>



| <span data-ttu-id="171d3-108">Variabili membro protette</span><span class="sxs-lookup"><span data-stu-id="171d3-108">Protected Member Variables</span></span>                                                      | <span data-ttu-id="171d3-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="171d3-109">Description</span></span>                                          |
|---------------------------------------------------------------------------------|------------------------------------------------------|
| [<span data-ttu-id="171d3-110">**\_pTIPFilter m**</span><span class="sxs-lookup"><span data-stu-id="171d3-110">**m\_pTIPFilter**</span></span>](ctransinplaceoutputpin-m-ptipfilter.md)                    | <span data-ttu-id="171d3-111">Puntatore al filtro che ha creato questo pin.</span><span class="sxs-lookup"><span data-stu-id="171d3-111">Pointer to the filter that created this pin.</span></span>         |
| <span data-ttu-id="171d3-112">Metodi pubblici</span><span class="sxs-lookup"><span data-stu-id="171d3-112">Public Methods</span></span>                                                                  | <span data-ttu-id="171d3-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="171d3-113">Description</span></span>                                          |
| [<span data-ttu-id="171d3-114">**CTransInPlaceOutputPin**</span><span class="sxs-lookup"><span data-stu-id="171d3-114">**CTransInPlaceOutputPin**</span></span>](ctransinplaceoutputpin-ctransinplaceoutputpin.md) | <span data-ttu-id="171d3-115">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="171d3-115">Constructor method.</span></span>                                  |
| [<span data-ttu-id="171d3-116">**CheckMediaType**</span><span class="sxs-lookup"><span data-stu-id="171d3-116">**CheckMediaType**</span></span>](ctransinplaceoutputpin-checkmediatype.md)                 | <span data-ttu-id="171d3-117">Determina se il pin accetta un tipo di supporto specifico.</span><span class="sxs-lookup"><span data-stu-id="171d3-117">Determines if the pin accepts a specific media type.</span></span> |
| [<span data-ttu-id="171d3-118">**Seallocator**</span><span class="sxs-lookup"><span data-stu-id="171d3-118">**SetAllocator**</span></span>](ctransinplaceoutputpin-setallocator.md)                     | <span data-ttu-id="171d3-119">Specifica un allocatore per la connessione.</span><span class="sxs-lookup"><span data-stu-id="171d3-119">Specifies an allocator for the connection.</span></span>           |
| [<span data-ttu-id="171d3-120">**ConnectedIMemInputPin**</span><span class="sxs-lookup"><span data-stu-id="171d3-120">**ConnectedIMemInputPin**</span></span>](ctransinplaceoutputpin-connectedimeminputpin.md)   | <span data-ttu-id="171d3-121">Recupera un puntatore al pin di input downstream.</span><span class="sxs-lookup"><span data-stu-id="171d3-121">Retrieves a pointer to the downstream input pin.</span></span>     |
| [<span data-ttu-id="171d3-122">**PeekAllocator**</span><span class="sxs-lookup"><span data-stu-id="171d3-122">**PeekAllocator**</span></span>](ctransinplaceoutputpin-peekallocator.md)                   | <span data-ttu-id="171d3-123">Recupera un puntatore all'allocatore del PIN.</span><span class="sxs-lookup"><span data-stu-id="171d3-123">Retrieves a pointer to the pin's allocator.</span></span>          |
| <span data-ttu-id="171d3-124">Metodi IPin</span><span class="sxs-lookup"><span data-stu-id="171d3-124">IPin Methods</span></span>                                                                    | <span data-ttu-id="171d3-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="171d3-125">Description</span></span>                                          |
| [<span data-ttu-id="171d3-126">**EnumMediaTypes**</span><span class="sxs-lookup"><span data-stu-id="171d3-126">**EnumMediaTypes**</span></span>](ctransinplaceoutputpin-enummediatypes.md)                 | <span data-ttu-id="171d3-127">Enumera i tipi di supporto preferiti del PIN.</span><span class="sxs-lookup"><span data-stu-id="171d3-127">Enumerates the pin's preferred media types.</span></span>          |



 

## <a name="requirements"></a><span data-ttu-id="171d3-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="171d3-128">Requirements</span></span>



| <span data-ttu-id="171d3-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="171d3-129">Requirement</span></span> | <span data-ttu-id="171d3-130">Valore</span><span class="sxs-lookup"><span data-stu-id="171d3-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="171d3-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="171d3-131">Header</span></span><br/>  | <dl> <span data-ttu-id="171d3-132"><dt>Transip. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="171d3-132"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="171d3-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="171d3-133">Library</span></span><br/> | <dl> <span data-ttu-id="171d3-134"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="171d3-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




