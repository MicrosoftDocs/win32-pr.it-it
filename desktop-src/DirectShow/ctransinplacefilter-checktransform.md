---
description: "Il metodo CheckTransform controlla se un tipo di supporto di input è compatibile con un tipo di supporto di output. Questo metodo esegue l'override del metodo CTransformFilter:: CheckTransform."
ms.assetid: d0953014-4a49-4738-a449-c247396a6794
title: Metodo CTransInPlaceFilter. CheckTransform (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.CheckTransform
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6a80132723be0b70f2c4afe93306d7f581b7734c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332980"
---
# <a name="ctransinplacefilterchecktransform-method"></a><span data-ttu-id="02aaa-104">CTransInPlaceFilter. CheckTransform, metodo</span><span class="sxs-lookup"><span data-stu-id="02aaa-104">CTransInPlaceFilter.CheckTransform method</span></span>

<span data-ttu-id="02aaa-105">Il `CheckTransform` metodo verifica se un tipo di supporto di input è compatibile con un tipo di supporto di output.</span><span class="sxs-lookup"><span data-stu-id="02aaa-105">The `CheckTransform` method checks whether an input media type is compatible with an output media type.</span></span> <span data-ttu-id="02aaa-106">Questo metodo esegue l'override del metodo [**CTransformFilter:: CheckTransform**](ctransformfilter-checktransform.md) .</span><span class="sxs-lookup"><span data-stu-id="02aaa-106">This method overrides the [**CTransformFilter::CheckTransform**](ctransformfilter-checktransform.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="02aaa-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="02aaa-107">Syntax</span></span>


```C++
HRESULT CheckTransform(
   const CMediaType *mtIn,
   const CMediaType *mtOut
);
```



## <a name="parameters"></a><span data-ttu-id="02aaa-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="02aaa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02aaa-109">*mtIn*</span><span class="sxs-lookup"><span data-stu-id="02aaa-109">*mtIn*</span></span> 
</dt> <dd>

<span data-ttu-id="02aaa-110">Puntatore a un oggetto [**CMediaType**](cmediatype.md) che specifica il tipo di input.</span><span class="sxs-lookup"><span data-stu-id="02aaa-110">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the input type.</span></span>

</dd> <dt>

<span data-ttu-id="02aaa-111">*mtOut*</span><span class="sxs-lookup"><span data-stu-id="02aaa-111">*mtOut*</span></span> 
</dt> <dd>

<span data-ttu-id="02aaa-112">Puntatore a un oggetto **CMediaType** che specifica il tipo di output.</span><span class="sxs-lookup"><span data-stu-id="02aaa-112">Pointer to a **CMediaType** object that specifies the output type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02aaa-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="02aaa-113">Return value</span></span>

<span data-ttu-id="02aaa-114">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="02aaa-114">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="02aaa-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="02aaa-115">Remarks</span></span>

<span data-ttu-id="02aaa-116">Il filtro **CTransInPlace** non chiama mai `CheckTransform` .</span><span class="sxs-lookup"><span data-stu-id="02aaa-116">The **CTransInPlace** filter never calls `CheckTransform`.</span></span> <span data-ttu-id="02aaa-117">Al contrario, tutte le connessioni pin utilizzano [**CTransformFilter:: CheckInputType**](ctransformfilter-checkinputtype.md) per verificare il tipo di supporto, supponendo che i tipi di input e di output corrispondano sempre.</span><span class="sxs-lookup"><span data-stu-id="02aaa-117">Instead, all pin connection use [**CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md) to check the media type, with the assumption that the input and output types always match.</span></span>

## <a name="requirements"></a><span data-ttu-id="02aaa-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="02aaa-118">Requirements</span></span>



| <span data-ttu-id="02aaa-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="02aaa-119">Requirement</span></span> | <span data-ttu-id="02aaa-120">Valore</span><span class="sxs-lookup"><span data-stu-id="02aaa-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02aaa-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="02aaa-121">Header</span></span><br/>  | <dl> <span data-ttu-id="02aaa-122"><dt>Transip. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="02aaa-122"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="02aaa-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="02aaa-123">Library</span></span><br/> | <dl> <span data-ttu-id="02aaa-124"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="02aaa-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02aaa-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="02aaa-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02aaa-126">**Classe CTransInPlaceFilter**</span><span class="sxs-lookup"><span data-stu-id="02aaa-126">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




