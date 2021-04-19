---
description: Il metodo Transform trasforma un esempio di input per produrre un esempio di output.
ms.assetid: 30ef8c0c-e834-481a-93ff-d06e6fa1ddeb
title: Metodo CTransformFilter. Transform (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.Transform
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8498a9a6ce266e0646dbbdcb4f322c093d6e0cc3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326664"
---
# <a name="ctransformfiltertransform-method"></a><span data-ttu-id="f3f09-103">Metodo CTransformFilter. Transform</span><span class="sxs-lookup"><span data-stu-id="f3f09-103">CTransformFilter.Transform method</span></span>

<span data-ttu-id="f3f09-104">Il `Transform` metodo trasforma un esempio di input per produrre un esempio di output.</span><span class="sxs-lookup"><span data-stu-id="f3f09-104">The `Transform` method transforms an input sample to produce an output sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3f09-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f3f09-105">Syntax</span></span>


```C++
virtual HRESULT Transform(
   IMediaSample *pIn,
   IMediaSample *pOut
);
```



## <a name="parameters"></a><span data-ttu-id="f3f09-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f3f09-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3f09-107">*pIn*</span><span class="sxs-lookup"><span data-stu-id="f3f09-107">*pIn*</span></span> 
</dt> <dd>

<span data-ttu-id="f3f09-108">Puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'esempio di input.</span><span class="sxs-lookup"><span data-stu-id="f3f09-108">Pointer to the input sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> <dt>

<span data-ttu-id="f3f09-109">*Broncio*</span><span class="sxs-lookup"><span data-stu-id="f3f09-109">*pOut*</span></span> 
</dt> <dd>

<span data-ttu-id="f3f09-110">Puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'esempio di output.</span><span class="sxs-lookup"><span data-stu-id="f3f09-110">Pointer to the output sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3f09-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f3f09-111">Return value</span></span>

<span data-ttu-id="f3f09-112">La classe base restituisce E \_ imprevisto.</span><span class="sxs-lookup"><span data-stu-id="f3f09-112">The base class returns E\_UNEXPECTED.</span></span>

<span data-ttu-id="f3f09-113">La classe derivata deve restituire un valore **HRESULT** che indica l'esito positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="f3f09-113">The derived class should return an **HRESULT** value, indicating success or failure.</span></span> <span data-ttu-id="f3f09-114">I valori possibili includono quelli mostrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="f3f09-114">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="f3f09-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="f3f09-115">Return code</span></span>                                                                             | <span data-ttu-id="f3f09-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f3f09-116">Description</span></span>                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <span data-ttu-id="f3f09-117"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="f3f09-117"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="f3f09-118">Non recapitare questo esempio.</span><span class="sxs-lookup"><span data-stu-id="f3f09-118">Do not deliver this sample.</span></span><br/> |
| <dl> <span data-ttu-id="f3f09-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f3f09-119"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="f3f09-120">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="f3f09-120">Success.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="f3f09-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="f3f09-121">Remarks</span></span>

<span data-ttu-id="f3f09-122">Eseguire l'override di questo metodo per produrre dati di output.</span><span class="sxs-lookup"><span data-stu-id="f3f09-122">Override this method to produce output data.</span></span> <span data-ttu-id="f3f09-123">Leggere i dati di input dall'esempio specificato dal parametro *pin* e scrivere i nuovi dati nell'esempio specificato dal parametro *broncio* .</span><span class="sxs-lookup"><span data-stu-id="f3f09-123">Read the input data from the sample specified by the *pIn* parameter, and write the new data into the sample specified by the *pOut* parameter.</span></span>

<span data-ttu-id="f3f09-124">Prima che il filtro chiami questo metodo, copia le proprietà dall'esempio di input nell'esempio di output.</span><span class="sxs-lookup"><span data-stu-id="f3f09-124">Before the filter calls this method, it copies the properties from the input sample to the output sample.</span></span> <span data-ttu-id="f3f09-125">Il `Transform` metodo deve impostare qualsiasi proprietà che differisca tra i due esempi, usando i metodi **IMediaSample** o l'interfaccia [**IMediaSample2**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) (se disponibile).</span><span class="sxs-lookup"><span data-stu-id="f3f09-125">The `Transform` method should set any properties that differ between the two samples, using **IMediaSample** methods or the [**IMediaSample2**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) interface (if available).</span></span>

<span data-ttu-id="f3f09-126">Se il filtro non deve fornire questo esempio (ad esempio per supportare il controllo di qualità), il metodo deve restituire S \_ false.</span><span class="sxs-lookup"><span data-stu-id="f3f09-126">If the filter should not deliver this sample (for example, to support quality control), the method should return S\_FALSE.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3f09-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f3f09-127">Requirements</span></span>



| <span data-ttu-id="f3f09-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3f09-128">Requirement</span></span> | <span data-ttu-id="f3f09-129">Valore</span><span class="sxs-lookup"><span data-stu-id="f3f09-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3f09-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f3f09-130">Header</span></span><br/>  | <dl> <span data-ttu-id="f3f09-131"><dt>Transfrm. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f3f09-131"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f3f09-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="f3f09-132">Library</span></span><br/> | <dl> <span data-ttu-id="f3f09-133"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f3f09-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3f09-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f3f09-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3f09-135">**Classe CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="f3f09-135">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




