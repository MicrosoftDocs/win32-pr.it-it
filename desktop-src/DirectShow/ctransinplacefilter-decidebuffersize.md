---
description: Il metodo DecideBufferSize imposta i requisiti del buffer del PIN di output.
ms.assetid: f1ddc39e-dcd5-4a44-8a8e-e384692408e1
title: Metodo CTransInPlaceFilter. DecideBufferSize (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.DecideBufferSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 55227510eee3c1afdcd14ed390edf21eccfcf1de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326395"
---
# <a name="ctransinplacefilterdecidebuffersize-method"></a><span data-ttu-id="7a9de-103">CTransInPlaceFilter. DecideBufferSize, metodo</span><span class="sxs-lookup"><span data-stu-id="7a9de-103">CTransInPlaceFilter.DecideBufferSize method</span></span>

<span data-ttu-id="7a9de-104">Il `DecideBufferSize` metodo imposta i requisiti del buffer del PIN di output.</span><span class="sxs-lookup"><span data-stu-id="7a9de-104">The `DecideBufferSize` method sets the output pin's buffer requirements.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a9de-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7a9de-105">Syntax</span></span>


```C++
HRESULT DecideBufferSize(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *pProperties
);
```



## <a name="parameters"></a><span data-ttu-id="7a9de-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7a9de-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a9de-107">*pAlloc*</span><span class="sxs-lookup"><span data-stu-id="7a9de-107">*pAlloc*</span></span> 
</dt> <dd>

<span data-ttu-id="7a9de-108">Puntatore all'oggetto [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) usato dal pin di output.</span><span class="sxs-lookup"><span data-stu-id="7a9de-108">Pointer to the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) object used by the output pin.</span></span>

</dd> <dt>

<span data-ttu-id="7a9de-109">*pProperties*</span><span class="sxs-lookup"><span data-stu-id="7a9de-109">*pProperties*</span></span> 
</dt> <dd>

<span data-ttu-id="7a9de-110">Puntatore alle proprietà allocatore richieste per conteggio, dimensioni e allineamento, come specificato dalla struttura delle [**\_ proprietà dell'allocatore**](/windows/win32/api/strmif/ns-strmif-allocator_properties) .</span><span class="sxs-lookup"><span data-stu-id="7a9de-110">Pointer to the requested allocator properties for count, size, and alignment, as specified by the [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a9de-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7a9de-111">Return value</span></span>

<span data-ttu-id="7a9de-112">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7a9de-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="7a9de-113">I valori possibili includono quelli mostrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="7a9de-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="7a9de-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="7a9de-114">Return code</span></span>                                                                            | <span data-ttu-id="7a9de-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7a9de-115">Description</span></span>        |
|----------------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="7a9de-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7a9de-116"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="7a9de-117">Operazione riuscita</span><span class="sxs-lookup"><span data-stu-id="7a9de-117">Success</span></span><br/> |
| <dl> <span data-ttu-id="7a9de-118"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="7a9de-118"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="7a9de-119">Errore</span><span class="sxs-lookup"><span data-stu-id="7a9de-119">Failure</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7a9de-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="7a9de-120">Remarks</span></span>

<span data-ttu-id="7a9de-121">Questo metodo viene chiamato quando la classe **CTransInPlaceFilter** deve fornire una dimensione del buffer al filtro downstream.</span><span class="sxs-lookup"><span data-stu-id="7a9de-121">This method is called when the **CTransInPlaceFilter** class needs to provide a buffer size to the downstream filter.</span></span> <span data-ttu-id="7a9de-122">Se il filtro **CTransInPlaceFilter** è già connesso a upstream, USA le proprietà dell'allocatore nella connessione pin upstream.</span><span class="sxs-lookup"><span data-stu-id="7a9de-122">If the **CTransInPlaceFilter** filter is already connected upstream, it uses the allocator properties on the upstream pin connection.</span></span> <span data-ttu-id="7a9de-123">In caso contrario, le dimensioni del buffer vengono impostate su 1 byte come valore temporaneo del segnaposto.</span><span class="sxs-lookup"><span data-stu-id="7a9de-123">Otherwise, it sets the buffer size to 1 byte as a temporary place-holder value.</span></span> <span data-ttu-id="7a9de-124">Quando il filtro upstream si connette, la classe **CTransInPlaceFilter** rinegozia l'allocatore downstream.</span><span class="sxs-lookup"><span data-stu-id="7a9de-124">When the upstream filter connects, the **CTransInPlaceFilter** class renegotiates the downstream allocator.</span></span> <span data-ttu-id="7a9de-125">Per ulteriori informazioni sul processo di connessione del PIN in questa classe, vedere [**classe CTransInPlaceFilter**](ctransinplacefilter.md).</span><span class="sxs-lookup"><span data-stu-id="7a9de-125">For more information about the pin connection process in this class, see [**CTransInPlaceFilter Class**](ctransinplacefilter.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7a9de-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7a9de-126">Requirements</span></span>



| <span data-ttu-id="7a9de-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a9de-127">Requirement</span></span> | <span data-ttu-id="7a9de-128">Valore</span><span class="sxs-lookup"><span data-stu-id="7a9de-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a9de-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7a9de-129">Header</span></span><br/>  | <dl> <span data-ttu-id="7a9de-130"><dt>Transip. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7a9de-130"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7a9de-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="7a9de-131">Library</span></span><br/> | <dl> <span data-ttu-id="7a9de-132"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="7a9de-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a9de-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7a9de-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a9de-134">**Classe CTransInPlaceFilter**</span><span class="sxs-lookup"><span data-stu-id="7a9de-134">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




