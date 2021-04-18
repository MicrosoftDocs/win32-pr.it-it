---
description: Il metodo InitializeOutputSample recupera un nuovo esempio di output e lo inizializza.
ms.assetid: a4f8f514-cf1a-4f8f-ac17-17378705c2ea
title: Metodo CTransformFilter.InitializeOutputSample (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.InitializeOutputSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: efe7e62936c6feb1984a339a67783cdbc1e4f124
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331149"
---
# <a name="ctransformfilterinitializeoutputsample-method"></a><span data-ttu-id="26307-103">Metodo tializeOutputSample CTransformFilter.Ini</span><span class="sxs-lookup"><span data-stu-id="26307-103">CTransformFilter.InitializeOutputSample method</span></span>

<span data-ttu-id="26307-104">Il `InitializeOutputSample` metodo recupera un nuovo esempio di output e lo inizializza.</span><span class="sxs-lookup"><span data-stu-id="26307-104">The `InitializeOutputSample` method retrieves a new output sample and initializes it.</span></span>

## <a name="syntax"></a><span data-ttu-id="26307-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="26307-105">Syntax</span></span>


```C++
HRESULT InitializeOutputSample(
   IMediaSample *pSample,
   IMediaSample **ppOutSample
);
```



## <a name="parameters"></a><span data-ttu-id="26307-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="26307-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26307-107">*pSample*</span><span class="sxs-lookup"><span data-stu-id="26307-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="26307-108">Puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'esempio di input.</span><span class="sxs-lookup"><span data-stu-id="26307-108">Pointer to the input sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> <dt>

<span data-ttu-id="26307-109">*ppOutSample*</span><span class="sxs-lookup"><span data-stu-id="26307-109">*ppOutSample*</span></span> 
</dt> <dd>

<span data-ttu-id="26307-110">Riceve un puntatore all'interfaccia **IMediaSample** dell'esempio di output.</span><span class="sxs-lookup"><span data-stu-id="26307-110">Receives a pointer to the output sample's **IMediaSample** interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26307-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="26307-111">Return value</span></span>

<span data-ttu-id="26307-112">Restituisce S \_ OK o un altro valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="26307-112">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="26307-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="26307-113">Remarks</span></span>

<span data-ttu-id="26307-114">Questo metodo viene chiamato dal metodo [**CTransformFilter:: Receive**](ctransformfilter-receive.md) per preparare l'esempio di output.</span><span class="sxs-lookup"><span data-stu-id="26307-114">This method is called by the [**CTransformFilter::Receive**](ctransformfilter-receive.md) method to prepare the output sample.</span></span> <span data-ttu-id="26307-115">In genere non è necessario chiamare questo metodo nella classe derivata, a meno che non si esegua l'override del metodo **Receive** .</span><span class="sxs-lookup"><span data-stu-id="26307-115">Generally you do not have to call this method in your derived class, unless you override the **Receive** method.</span></span>

<span data-ttu-id="26307-116">Questo metodo recupera un nuovo campione dall'allocatore del PIN di output.</span><span class="sxs-lookup"><span data-stu-id="26307-116">This method retrieves a new sample from the output pin's allocator.</span></span> <span data-ttu-id="26307-117">Quindi copia le proprietà di esempio dall'esempio di input nell'esempio di output.</span><span class="sxs-lookup"><span data-stu-id="26307-117">Then it copies the sample properties from the input sample to the output sample.</span></span> <span data-ttu-id="26307-118">Le proprietà di esempio sono definite nella struttura delle [**\_ \_ Proprietà am SAMPLE2**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) .</span><span class="sxs-lookup"><span data-stu-id="26307-118">The sample properties are defined in the [**AM\_SAMPLE2\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="26307-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="26307-119">Requirements</span></span>



| <span data-ttu-id="26307-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="26307-120">Requirement</span></span> | <span data-ttu-id="26307-121">Valore</span><span class="sxs-lookup"><span data-stu-id="26307-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26307-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="26307-122">Header</span></span><br/>  | <dl> <span data-ttu-id="26307-123"><dt>Transfrm. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="26307-123"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="26307-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="26307-124">Library</span></span><br/> | <dl> <span data-ttu-id="26307-125"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="26307-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26307-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="26307-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26307-127">**Classe CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="26307-127">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




