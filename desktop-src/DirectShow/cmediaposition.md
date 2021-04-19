---
description: La classe CMediaPosition gestisce i metodi IDispatch dell'interfaccia duale IMediaPosition.
ms.assetid: 5e84a2b6-39d4-47a4-93b4-690df12e2d19
title: Classe CMediaPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 60d06a08badf3302ef4ddb352d840842a2605600
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326409"
---
# <a name="cmediaposition-class"></a><span data-ttu-id="82d39-103">Classe CMediaPosition</span><span class="sxs-lookup"><span data-stu-id="82d39-103">CMediaPosition class</span></span>

![gerarchia di classi cmediaposition](images/cutil14.png)

<span data-ttu-id="82d39-105">La classe **CMediaPosition** gestisce i metodi **IDispatch** dell'interfaccia duale [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) .</span><span class="sxs-lookup"><span data-stu-id="82d39-105">The **CMediaPosition** class handles the **IDispatch** methods of the [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) dual interface.</span></span>

<span data-ttu-id="82d39-106">Questa classe eredita l'interfaccia [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) , ma non la implementa.</span><span class="sxs-lookup"><span data-stu-id="82d39-106">This class inherits the [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) interface but does not implement it.</span></span> <span data-ttu-id="82d39-107">Implementa **IDispatch** tramite la classe [**CBaseDispatch**](cbasedispatch.md) e la libreria dei tipi DirectShow.</span><span class="sxs-lookup"><span data-stu-id="82d39-107">It implements **IDispatch** through the [**CBaseDispatch**](cbasedispatch.md) class and the DirectShow type library.</span></span> <span data-ttu-id="82d39-108">Non usare direttamente questa classe.</span><span class="sxs-lookup"><span data-stu-id="82d39-108">Do not use this class directly.</span></span> <span data-ttu-id="82d39-109">Usare invece una delle classi seguenti:</span><span class="sxs-lookup"><span data-stu-id="82d39-109">Instead, use one of the following classes:</span></span>

-   <span data-ttu-id="82d39-110">Filtri di origine: usare la classe di base [**CSourceSeeking**](csourceseeking.md) per implementare la ricerca.</span><span class="sxs-lookup"><span data-stu-id="82d39-110">Source filters: Use the [**CSourceSeeking**](csourceseeking.md) base class to implement seeking.</span></span>
-   <span data-ttu-id="82d39-111">Filtri di trasformazione: usare la classe [**CPosPassThru**](cpospassthru.md) per passare i comandi di ricerca upstream.</span><span class="sxs-lookup"><span data-stu-id="82d39-111">Transform filters: Use the [**CPosPassThru**](cpospassthru.md) class to pass seeking commands upstream.</span></span>
-   <span data-ttu-id="82d39-112">Renderer: usare la classe [**CRendererPosPassThru**](crendererpospassthru.md) per passare i comandi di ricerca upstream.</span><span class="sxs-lookup"><span data-stu-id="82d39-112">Renderers: Use the [**CRendererPosPassThru**](crendererpospassthru.md) class to pass seeking commands upstream.</span></span>



| <span data-ttu-id="82d39-113">Metodi pubblici</span><span class="sxs-lookup"><span data-stu-id="82d39-113">Public Methods</span></span>                                              | <span data-ttu-id="82d39-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="82d39-114">Description</span></span>                                                                                                         |
|-------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="82d39-115">**CMediaPosition**</span><span class="sxs-lookup"><span data-stu-id="82d39-115">**CMediaPosition**</span></span>](cmediaposition-cmediaposition.md)     | <span data-ttu-id="82d39-116">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="82d39-116">Constructor method.</span></span>                                                                                                 |
| <span data-ttu-id="82d39-117">IDispatch (metodi)</span><span class="sxs-lookup"><span data-stu-id="82d39-117">IDispatch Methods</span></span>                                           | <span data-ttu-id="82d39-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="82d39-118">Description</span></span>                                                                                                         |
| [<span data-ttu-id="82d39-119">**GetIDsOfNames**</span><span class="sxs-lookup"><span data-stu-id="82d39-119">**GetIDsOfNames**</span></span>](cmediaposition-getidsofnames.md)       | <span data-ttu-id="82d39-120">Esegue il mapping di un set di nomi a un set di DISPID corrispondente.</span><span class="sxs-lookup"><span data-stu-id="82d39-120">Maps a set of names to a corresponding set of DISPIDs.</span></span>                                                              |
| [<span data-ttu-id="82d39-121">**GetTypeInfo**</span><span class="sxs-lookup"><span data-stu-id="82d39-121">**GetTypeInfo**</span></span>](cmediaposition-gettypeinfo.md)           | <span data-ttu-id="82d39-122">Recupera le informazioni sul tipo per l'oggetto, che può quindi essere utilizzato per ottenere le informazioni sul tipo per un'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="82d39-122">Retrieves the type information for the object, which can then be used to get the type information for an interface.</span></span> |
| [<span data-ttu-id="82d39-123">**GetTypeInfoCount**</span><span class="sxs-lookup"><span data-stu-id="82d39-123">**GetTypeInfoCount**</span></span>](cmediaposition-gettypeinfocount.md) | <span data-ttu-id="82d39-124">Recupera il numero di interfacce di informazioni sul tipo fornite dall'oggetto.</span><span class="sxs-lookup"><span data-stu-id="82d39-124">Retrieves the number of type information interfaces the object provides.</span></span>                                            |
| [<span data-ttu-id="82d39-125">**Richiamare**</span><span class="sxs-lookup"><span data-stu-id="82d39-125">**Invoke**</span></span>](cmediaposition-invoke.md)                     | <span data-ttu-id="82d39-126">Fornisce l'accesso alle proprietà e ai metodi esposti dall'oggetto.</span><span class="sxs-lookup"><span data-stu-id="82d39-126">Provides access to properties and methods exposed by the object.</span></span>                                                    |



 

## <a name="requirements"></a><span data-ttu-id="82d39-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="82d39-127">Requirements</span></span>



| <span data-ttu-id="82d39-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="82d39-128">Requirement</span></span> | <span data-ttu-id="82d39-129">Valore</span><span class="sxs-lookup"><span data-stu-id="82d39-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82d39-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="82d39-130">Header</span></span><br/>  | <dl> <span data-ttu-id="82d39-131"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="82d39-131"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="82d39-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="82d39-132">Library</span></span><br/> | <dl> <span data-ttu-id="82d39-133"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="82d39-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82d39-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="82d39-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82d39-135">Classi base di DirectShow</span><span class="sxs-lookup"><span data-stu-id="82d39-135">DirectShow Base Classes</span></span>](directshow-base-classes.md)
</dt> </dl>

 

 




