---
description: Il metodo Transform trasforma un campione sul posto.
ms.assetid: 2268041b-70d4-48a9-9bb8-4ab921cce649
title: Metodo CTransInPlaceFilter. Transform (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.Transform
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d5b84f326807f730745268a217b6066dacb9aaa7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333795"
---
# <a name="ctransinplacefiltertransform-method"></a><span data-ttu-id="08c2d-103">Metodo CTransInPlaceFilter. Transform</span><span class="sxs-lookup"><span data-stu-id="08c2d-103">CTransInPlaceFilter.Transform method</span></span>

<span data-ttu-id="08c2d-104">Il `Transform` metodo trasforma un campione sul posto.</span><span class="sxs-lookup"><span data-stu-id="08c2d-104">The `Transform` method transforms a sample in place.</span></span>

## <a name="syntax"></a><span data-ttu-id="08c2d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="08c2d-105">Syntax</span></span>


```C++
virtual HRESULT Transform(
   IMediaSample *pSample
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="08c2d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="08c2d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08c2d-107">*pSample*</span><span class="sxs-lookup"><span data-stu-id="08c2d-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="08c2d-108">Puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="08c2d-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08c2d-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="08c2d-109">Return value</span></span>

<span data-ttu-id="08c2d-110">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="08c2d-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="08c2d-111">I valori possibili includono quelli mostrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="08c2d-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="08c2d-112">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="08c2d-112">Return code</span></span>                                                                             | <span data-ttu-id="08c2d-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="08c2d-113">Description</span></span>                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <span data-ttu-id="08c2d-114"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="08c2d-114"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="08c2d-115">Non recapitare questo esempio.</span><span class="sxs-lookup"><span data-stu-id="08c2d-115">Do not deliver this sample.</span></span><br/> |
| <dl> <span data-ttu-id="08c2d-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="08c2d-116"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="08c2d-117">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="08c2d-117">Success.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="08c2d-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="08c2d-118">Remarks</span></span>

<span data-ttu-id="08c2d-119">La classe derivata deve implementare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="08c2d-119">The derived class must implement this method.</span></span> <span data-ttu-id="08c2d-120">Trasformare i dati di esempio sul posto.</span><span class="sxs-lookup"><span data-stu-id="08c2d-120">Transform the sample data in place.</span></span> <span data-ttu-id="08c2d-121">Se il filtro usa due allocatori, copia i dati dall'esempio di input in un nuovo esempio e passa la copia a questo metodo.</span><span class="sxs-lookup"><span data-stu-id="08c2d-121">If the filter is using two allocators, it copies the data from the input sample to a new sample, and passes the copy to this method.</span></span>

<span data-ttu-id="08c2d-122">Se il filtro non deve fornire questo esempio (ad esempio per supportare il controllo di qualità), il metodo deve restituire S \_ false.</span><span class="sxs-lookup"><span data-stu-id="08c2d-122">If the filter should not deliver this sample (for example, to support quality control), the method should return S\_FALSE.</span></span>

## <a name="requirements"></a><span data-ttu-id="08c2d-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="08c2d-123">Requirements</span></span>



| <span data-ttu-id="08c2d-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="08c2d-124">Requirement</span></span> | <span data-ttu-id="08c2d-125">Valore</span><span class="sxs-lookup"><span data-stu-id="08c2d-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08c2d-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="08c2d-126">Header</span></span><br/>  | <dl> <span data-ttu-id="08c2d-127"><dt>Transip. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="08c2d-127"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="08c2d-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="08c2d-128">Library</span></span><br/> | <dl> <span data-ttu-id="08c2d-129"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="08c2d-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08c2d-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="08c2d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08c2d-131">**Classe CTransInPlaceFilter**</span><span class="sxs-lookup"><span data-stu-id="08c2d-131">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




