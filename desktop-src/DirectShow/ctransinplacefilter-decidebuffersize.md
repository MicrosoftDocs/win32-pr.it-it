---
description: 'Metodo CTransInPlaceFilter.DecideBufferSize: il metodo DecideBufferSize imposta i requisiti del buffer del pin di output.'
ms.assetid: f1ddc39e-dcd5-4a44-8a8e-e384692408e1
title: Metodo CTransInPlaceFilter.DecideBufferSize (Transip.h)
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
ms.openlocfilehash: b3ffb3ec7b1ef59c6e7f3d49e39fbe69e8cc1c08
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094829"
---
# <a name="ctransinplacefilterdecidebuffersize-method"></a><span data-ttu-id="668e6-103">Metodo CTransInPlaceFilter.DecideBufferSize</span><span class="sxs-lookup"><span data-stu-id="668e6-103">CTransInPlaceFilter.DecideBufferSize method</span></span>

<span data-ttu-id="668e6-104">Il `DecideBufferSize` metodo imposta i requisiti del buffer del pin di output.</span><span class="sxs-lookup"><span data-stu-id="668e6-104">The `DecideBufferSize` method sets the output pin's buffer requirements.</span></span>

## <a name="syntax"></a><span data-ttu-id="668e6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="668e6-105">Syntax</span></span>


```C++
HRESULT DecideBufferSize(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *pProperties
);
```



## <a name="parameters"></a><span data-ttu-id="668e6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="668e6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="668e6-107">*pAlloc*</span><span class="sxs-lookup"><span data-stu-id="668e6-107">*pAlloc*</span></span> 
</dt> <dd>

<span data-ttu-id="668e6-108">Puntatore [**all'oggetto IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) usato dal pin di output.</span><span class="sxs-lookup"><span data-stu-id="668e6-108">Pointer to the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) object used by the output pin.</span></span>

</dd> <dt>

<span data-ttu-id="668e6-109">*pProperties*</span><span class="sxs-lookup"><span data-stu-id="668e6-109">*pProperties*</span></span> 
</dt> <dd>

<span data-ttu-id="668e6-110">Puntatore alle proprietà dell'allocatore richieste per conteggio, dimensioni e allineamento, come specificato dalla [**struttura ALLOCATOR \_**](/windows/win32/api/strmif/ns-strmif-allocator_properties) PROPERTIES.</span><span class="sxs-lookup"><span data-stu-id="668e6-110">Pointer to the requested allocator properties for count, size, and alignment, as specified by the [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="668e6-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="668e6-111">Return value</span></span>

<span data-ttu-id="668e6-112">Restituisce un **valore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="668e6-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="668e6-113">I valori possibili includono quelli illustrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="668e6-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="668e6-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="668e6-114">Return code</span></span>                                                                            | <span data-ttu-id="668e6-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="668e6-115">Description</span></span>        |
|----------------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="668e6-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="668e6-116"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="668e6-117">Operazione riuscita</span><span class="sxs-lookup"><span data-stu-id="668e6-117">Success</span></span><br/> |
| <dl> <span data-ttu-id="668e6-118"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="668e6-118"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="668e6-119">Operazioni non riuscite</span><span class="sxs-lookup"><span data-stu-id="668e6-119">Failure</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="668e6-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="668e6-120">Remarks</span></span>

<span data-ttu-id="668e6-121">Questo metodo viene chiamato quando la **classe CTransInPlaceFilter** deve fornire una dimensione del buffer al filtro downstream.</span><span class="sxs-lookup"><span data-stu-id="668e6-121">This method is called when the **CTransInPlaceFilter** class needs to provide a buffer size to the downstream filter.</span></span> <span data-ttu-id="668e6-122">Se il **filtro CTransInPlaceFilter** è già connesso upstream, usa le proprietà dell'allocatore nella connessione pin upstream.</span><span class="sxs-lookup"><span data-stu-id="668e6-122">If the **CTransInPlaceFilter** filter is already connected upstream, it uses the allocator properties on the upstream pin connection.</span></span> <span data-ttu-id="668e6-123">In caso contrario, imposta le dimensioni del buffer su 1 byte come valore segnaposto temporaneo.</span><span class="sxs-lookup"><span data-stu-id="668e6-123">Otherwise, it sets the buffer size to 1 byte as a temporary place-holder value.</span></span> <span data-ttu-id="668e6-124">Quando il filtro upstream si connette, la **classe CTransInPlaceFilter** rinegozia l'allocatore downstream.</span><span class="sxs-lookup"><span data-stu-id="668e6-124">When the upstream filter connects, the **CTransInPlaceFilter** class renegotiates the downstream allocator.</span></span> <span data-ttu-id="668e6-125">Per altre informazioni sul processo di connessione pin in questa classe, vedere [**Classe CTransInPlaceFilter.**](ctransinplacefilter.md)</span><span class="sxs-lookup"><span data-stu-id="668e6-125">For more information about the pin connection process in this class, see [**CTransInPlaceFilter Class**](ctransinplacefilter.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="668e6-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="668e6-126">Requirements</span></span>



| <span data-ttu-id="668e6-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="668e6-127">Requirement</span></span> | <span data-ttu-id="668e6-128">Valore</span><span class="sxs-lookup"><span data-stu-id="668e6-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="668e6-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="668e6-129">Header</span></span><br/>  | <dl> <span data-ttu-id="668e6-130"><dt>Transip.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="668e6-130"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="668e6-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="668e6-131">Library</span></span><br/> | <dl> <span data-ttu-id="668e6-132"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="668e6-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="668e6-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="668e6-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="668e6-134">**Classe CTransInPlaceFilter**</span><span class="sxs-lookup"><span data-stu-id="668e6-134">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




