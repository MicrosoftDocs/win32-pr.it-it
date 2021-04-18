---
description: La classe CBaseDispatch è una classe di base per l'implementazione dell'interfaccia IDispatch in un filtro DirectShow.
ms.assetid: 33a989be-d059-4ad7-99f8-715c55a128a2
title: Classe CBaseDispatch (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseDispatch
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d115412b2b668f640834d5a3fa3b134f7a8d9c01
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327965"
---
# <a name="cbasedispatch-class"></a><span data-ttu-id="36cf6-103">Classe CBaseDispatch</span><span class="sxs-lookup"><span data-stu-id="36cf6-103">CBaseDispatch class</span></span>

![gerarchia di classi cbasedispatch](images/cutil01.png)

<span data-ttu-id="36cf6-105">La classe **CBaseDispatch** è una classe di base per l'implementazione dell'interfaccia **IDispatch** in un filtro DirectShow.</span><span class="sxs-lookup"><span data-stu-id="36cf6-105">The **CBaseDispatch** class is a base class for implementing the **IDispatch** interface in a DirectShow filter.</span></span>

<span data-ttu-id="36cf6-106">Questa classe è limitata al supporto delle interfacce compatibili con l'automazione esportate dalla libreria dei tipi DirectShow, file QuartzTypeLib.</span><span class="sxs-lookup"><span data-stu-id="36cf6-106">This class is limited to supporting the Automation-compatible interfaces exported by the DirectShow type library, QuartzTypeLib.</span></span> <span data-ttu-id="36cf6-107">Ad esempio, le classi [**CMediaControl**](cmediacontrol.md) e [**CMediaPosition**](cmediaposition.md) usano **CBaseDispatch** per implementare rispettivamente [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) e [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition).</span><span class="sxs-lookup"><span data-stu-id="36cf6-107">For example, the [**CMediaControl**](cmediacontrol.md) and [**CMediaPosition**](cmediaposition.md) classes use **CBaseDispatch** to implement [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) and [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), respectively.</span></span> <span data-ttu-id="36cf6-108">A causa di questa limitazione, probabilmente non esiste alcun motivo per usare **CBaseDispatch** direttamente nei filtri personalizzati.</span><span class="sxs-lookup"><span data-stu-id="36cf6-108">Because of this limitation, there is probably no reason to use **CBaseDispatch** directly in your own filters.</span></span>

<span data-ttu-id="36cf6-109">Per usare questa classe, eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="36cf6-109">To use this class, do the following:</span></span>

-   <span data-ttu-id="36cf6-110">Dichiarare una nuova classe che supporta **IDispatch**.</span><span class="sxs-lookup"><span data-stu-id="36cf6-110">Declare a new class that supports **IDispatch**.</span></span>
-   <span data-ttu-id="36cf6-111">Assegnare alla nuova classe una variabile membro privata di tipo **CBaseDispatch**.</span><span class="sxs-lookup"><span data-stu-id="36cf6-111">Give your new class a private member variable of type **CBaseDispatch**.</span></span>
-   <span data-ttu-id="36cf6-112">Implementare i metodi **IDispatch** .</span><span class="sxs-lookup"><span data-stu-id="36cf6-112">Implement the **IDispatch** methods.</span></span>
-   <span data-ttu-id="36cf6-113">Nei metodi **IDispatch** chiamare i metodi **CBaseDispatch** .</span><span class="sxs-lookup"><span data-stu-id="36cf6-113">In your **IDispatch** methods, call the **CBaseDispatch** methods.</span></span>

<span data-ttu-id="36cf6-114">Per ulteriori informazioni, fare riferimento al codice sorgente per le classi di esempio dichiarate in Ctlutil. h.</span><span class="sxs-lookup"><span data-stu-id="36cf6-114">For more details, refer to the source code for any of the sample classes declared in Ctlutil.h.</span></span>



| <span data-ttu-id="36cf6-115">Metodi pubblici</span><span class="sxs-lookup"><span data-stu-id="36cf6-115">Public Methods</span></span>                                             | <span data-ttu-id="36cf6-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="36cf6-116">Description</span></span>                                                                                                         |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="36cf6-117">**CBaseDispatch**</span><span class="sxs-lookup"><span data-stu-id="36cf6-117">**CBaseDispatch**</span></span>](cbasedispatch-cbasedispatch.md)       | <span data-ttu-id="36cf6-118">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="36cf6-118">Constructor method.</span></span>                                                                                                 |
| [<span data-ttu-id="36cf6-119">**~ CBaseDispatch**</span><span class="sxs-lookup"><span data-stu-id="36cf6-119">**~CBaseDispatch**</span></span>](cbasedispatch--cbasedispatch.md)     | <span data-ttu-id="36cf6-120">Metodo del distruttore.</span><span class="sxs-lookup"><span data-stu-id="36cf6-120">Destructor method.</span></span>                                                                                                  |
| [<span data-ttu-id="36cf6-121">**GetIDsOfNames**</span><span class="sxs-lookup"><span data-stu-id="36cf6-121">**GetIDsOfNames**</span></span>](cbasedispatch-getidsofnames.md)       | <span data-ttu-id="36cf6-122">Esegue il mapping di un set di nomi a un set di DISPID corrispondente.</span><span class="sxs-lookup"><span data-stu-id="36cf6-122">Maps a set of names to a corresponding set of DISPIDs.</span></span>                                                              |
| [<span data-ttu-id="36cf6-123">**GetTypeInfo**</span><span class="sxs-lookup"><span data-stu-id="36cf6-123">**GetTypeInfo**</span></span>](cbasedispatch-gettypeinfo.md)           | <span data-ttu-id="36cf6-124">Recupera le informazioni sul tipo per l'oggetto, che può quindi essere utilizzato per ottenere le informazioni sul tipo per un'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="36cf6-124">Retrieves the type information for the object, which can then be used to get the type information for an interface.</span></span> |
| [<span data-ttu-id="36cf6-125">**GetTypeInfoCount**</span><span class="sxs-lookup"><span data-stu-id="36cf6-125">**GetTypeInfoCount**</span></span>](cbasedispatch-gettypeinfocount.md) | <span data-ttu-id="36cf6-126">Recupera il numero di interfacce di informazioni sul tipo fornite dall'oggetto.</span><span class="sxs-lookup"><span data-stu-id="36cf6-126">Retrieves the number of type information interfaces the object provides.</span></span>                                            |



 

## <a name="requirements"></a><span data-ttu-id="36cf6-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="36cf6-127">Requirements</span></span>



| <span data-ttu-id="36cf6-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="36cf6-128">Requirement</span></span> | <span data-ttu-id="36cf6-129">Valore</span><span class="sxs-lookup"><span data-stu-id="36cf6-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36cf6-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="36cf6-130">Header</span></span><br/>  | <dl> <span data-ttu-id="36cf6-131"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="36cf6-131"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="36cf6-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="36cf6-132">Library</span></span><br/> | <dl> <span data-ttu-id="36cf6-133"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="36cf6-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36cf6-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="36cf6-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36cf6-135">Classi base di DirectShow</span><span class="sxs-lookup"><span data-stu-id="36cf6-135">DirectShow Base Classes</span></span>](directshow-base-classes.md)
</dt> </dl>

 

 




