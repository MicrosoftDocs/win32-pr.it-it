---
description: Il metodo Receive viene chiamato quando l'oggetto riceve un campione multimediale dal pin di output. La classe derivata deve implementare questo metodo.
ms.assetid: ef45388b-b038-4838-b76b-dbbdc5388495
title: Metodo CPullPin. Receive (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3a651822378b6a3c0754ecbd5ace4a5e464f014f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331160"
---
# <a name="cpullpinreceive-method"></a><span data-ttu-id="8506b-104">Metodo CPullPin. Receive</span><span class="sxs-lookup"><span data-stu-id="8506b-104">CPullPin.Receive method</span></span>

<span data-ttu-id="8506b-105">Il `Receive` metodo viene chiamato quando l'oggetto riceve un campione multimediale dal pin di output.</span><span class="sxs-lookup"><span data-stu-id="8506b-105">The `Receive` method is called when the object receives a media sample from the output pin.</span></span> <span data-ttu-id="8506b-106">La classe derivata deve implementare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="8506b-106">The derived class must implement this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8506b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8506b-107">Syntax</span></span>


```C++
virtual HRESULT Receive(
   IMediaSample *pSample
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="8506b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="8506b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8506b-109">*pSample*</span><span class="sxs-lookup"><span data-stu-id="8506b-109">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="8506b-110">Puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'esempio multimediale.</span><span class="sxs-lookup"><span data-stu-id="8506b-110">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the media sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8506b-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8506b-111">Return value</span></span>

<span data-ttu-id="8506b-112">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8506b-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="8506b-113">Se si restituisce un valore diverso da S \_ OK, il thread di pull dei dati verrà interrotto.</span><span class="sxs-lookup"><span data-stu-id="8506b-113">Returning a value other than S\_OK will stop the data-pulling thread.</span></span>

## <a name="remarks"></a><span data-ttu-id="8506b-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="8506b-114">Remarks</span></span>

<span data-ttu-id="8506b-115">Questo metodo viene chiamato ogni volta che un nuovo campione arriva dal pin di output.</span><span class="sxs-lookup"><span data-stu-id="8506b-115">This method is called whenever a new sample arrives from the output pin.</span></span> <span data-ttu-id="8506b-116">Scrivere questo metodo in modo analogo al metodo [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) .</span><span class="sxs-lookup"><span data-stu-id="8506b-116">Write this method in the same manner as the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method.</span></span>

<span data-ttu-id="8506b-117">I timestamp dell'esempio specificano gli offset di byte rispetto alla posizione iniziale originale specificata nel metodo [**CPullPin:: Seek**](cpullpin-seek.md) .</span><span class="sxs-lookup"><span data-stu-id="8506b-117">The time stamps on the sample specify the byte offsets, relative to the original start position that was specified in [**CPullPin::Seek**](cpullpin-seek.md) method.</span></span>

<span data-ttu-id="8506b-118">La posizione iniziale viene arrotondata per difetto al limite di allineamento più vicino e la posizione di arresto viene arrotondata per eccesso al limite di allineamento più vicino.</span><span class="sxs-lookup"><span data-stu-id="8506b-118">The start position is rounded down to the nearest alignment boundary, and the stop position is rounded up to the nearest alignment boundary.</span></span> <span data-ttu-id="8506b-119">Inoltre, se la posizione di arresto supera la durata totale, viene invece utilizzata la durata.</span><span class="sxs-lookup"><span data-stu-id="8506b-119">Also, if the stop position exceeds the total duration, the duration is used instead.</span></span>

<span data-ttu-id="8506b-120">Tutti i timestamp vengono specificati come offset di byte moltiplicato per 10 milioni, definito come unità di costante.</span><span class="sxs-lookup"><span data-stu-id="8506b-120">All time stamps are given as a byte offset multiplied by 10,000,000, defined as the constant UNITS.</span></span> <span data-ttu-id="8506b-121">Di conseguenza, un secondo è un byte.</span><span class="sxs-lookup"><span data-stu-id="8506b-121">Thus, notionally one second is one byte.</span></span> <span data-ttu-id="8506b-122">Per trovare gli offset di byte effettivi, chiamare [**IMediaSample:: GetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-gettime) e dividere i risultati in base alle unità.</span><span class="sxs-lookup"><span data-stu-id="8506b-122">To find the actual byte offsets, call [**IMediaSample::GetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-gettime) and divide the results by UNITS.</span></span>

## <a name="requirements"></a><span data-ttu-id="8506b-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8506b-123">Requirements</span></span>



| <span data-ttu-id="8506b-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="8506b-124">Requirement</span></span> | <span data-ttu-id="8506b-125">Valore</span><span class="sxs-lookup"><span data-stu-id="8506b-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8506b-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8506b-126">Header</span></span><br/>  | <dl> <span data-ttu-id="8506b-127"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="8506b-127"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="8506b-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="8506b-128">Library</span></span><br/> | <dl> <span data-ttu-id="8506b-129"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="8506b-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8506b-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8506b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8506b-131">**Classe CPullPin**</span><span class="sxs-lookup"><span data-stu-id="8506b-131">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




