---
description: Il metodo CheckTransform controlla se un tipo di supporto di input è compatibile con un tipo di supporto di output.
ms.assetid: 349145e5-c12d-41df-ae37-7846f8aaa423
title: Metodo CTransformFilter. CheckTransform (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.CheckTransform
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2b3302304e6a0f9df41005f7ed63d9316a3cd410
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329151"
---
# <a name="ctransformfilterchecktransform-method"></a><span data-ttu-id="33dc5-103">CTransformFilter. CheckTransform, metodo</span><span class="sxs-lookup"><span data-stu-id="33dc5-103">CTransformFilter.CheckTransform method</span></span>

<span data-ttu-id="33dc5-104">Il `CheckTransform` metodo verifica se un tipo di supporto di input è compatibile con un tipo di supporto di output.</span><span class="sxs-lookup"><span data-stu-id="33dc5-104">The `CheckTransform` method checks whether an input media type is compatible with an output media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="33dc5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="33dc5-105">Syntax</span></span>


```C++
virtual HRESULT CheckTransform(
   const CMediaType *mtIn,
   const CMediaType *mtOut
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="33dc5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="33dc5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33dc5-107">*mtIn*</span><span class="sxs-lookup"><span data-stu-id="33dc5-107">*mtIn*</span></span> 
</dt> <dd>

<span data-ttu-id="33dc5-108">Puntatore a un oggetto [**CMediaType**](cmediatype.md) che specifica il tipo di input.</span><span class="sxs-lookup"><span data-stu-id="33dc5-108">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the input type.</span></span>

</dd> <dt>

<span data-ttu-id="33dc5-109">*mtOut*</span><span class="sxs-lookup"><span data-stu-id="33dc5-109">*mtOut*</span></span> 
</dt> <dd>

<span data-ttu-id="33dc5-110">Puntatore a un oggetto [**CMediaType**](cmediatype.md) che specifica il tipo di output.</span><span class="sxs-lookup"><span data-stu-id="33dc5-110">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the output type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33dc5-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="33dc5-111">Return value</span></span>

<span data-ttu-id="33dc5-112">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="33dc5-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="33dc5-113">I valori possibili includono quelli mostrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="33dc5-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="33dc5-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="33dc5-114">Return code</span></span>                                                                                                | <span data-ttu-id="33dc5-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="33dc5-115">Description</span></span>                                    |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="33dc5-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="33dc5-116"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="33dc5-117">I tipi di supporto sono compatibili.</span><span class="sxs-lookup"><span data-stu-id="33dc5-117">The media types are compatible.</span></span><br/>     |
| <dl> <span data-ttu-id="33dc5-118"><dt>**\_tipo VFW \_ E \_ non \_ accettato**</dt></span><span class="sxs-lookup"><span data-stu-id="33dc5-118"><dt>**VFW\_E\_TYPE\_NOT\_ACCEPTED**</dt></span></span> </dl> | <span data-ttu-id="33dc5-119">I tipi di supporto non sono compatibili.</span><span class="sxs-lookup"><span data-stu-id="33dc5-119">The media types are not compatible.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="33dc5-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="33dc5-120">Remarks</span></span>

<span data-ttu-id="33dc5-121">La classe derivata deve implementare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="33dc5-121">The derived class must implement this method.</span></span> <span data-ttu-id="33dc5-122">Restituisce \_ OK se il filtro è in grado di accettare entrambi i tipi di supporto specificati o un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="33dc5-122">Return S\_OK if the filter can accept both of the specified media types, or an error code otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="33dc5-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="33dc5-123">Requirements</span></span>



| <span data-ttu-id="33dc5-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="33dc5-124">Requirement</span></span> | <span data-ttu-id="33dc5-125">Valore</span><span class="sxs-lookup"><span data-stu-id="33dc5-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33dc5-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="33dc5-126">Header</span></span><br/>  | <dl> <span data-ttu-id="33dc5-127"><dt>Transfrm. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="33dc5-127"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="33dc5-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="33dc5-128">Library</span></span><br/> | <dl> <span data-ttu-id="33dc5-129"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="33dc5-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




