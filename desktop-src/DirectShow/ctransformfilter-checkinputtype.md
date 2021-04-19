---
description: Il metodo CheckInputType controlla se un tipo di supporto specificato è accettabile per l'input.
ms.assetid: 11f156f7-add2-45be-a0d3-05d21f596b89
title: Metodo CTransformFilter. CheckInputType (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.CheckInputType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 63c48a0502ee074b0940f85386dca0619a3ad12d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325731"
---
# <a name="ctransformfiltercheckinputtype-method"></a><span data-ttu-id="d2a06-103">CTransformFilter. CheckInputType, metodo</span><span class="sxs-lookup"><span data-stu-id="d2a06-103">CTransformFilter.CheckInputType method</span></span>

<span data-ttu-id="d2a06-104">Il `CheckInputType` metodo controlla se un tipo di supporto specificato è accettabile per l'input.</span><span class="sxs-lookup"><span data-stu-id="d2a06-104">The `CheckInputType` method checks whether a specified media type is acceptable for input.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2a06-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d2a06-105">Syntax</span></span>


```C++
virtual HRESULT CheckInputType(
   const CMediaType *mtIn
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="d2a06-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d2a06-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2a06-107">*mtIn*</span><span class="sxs-lookup"><span data-stu-id="d2a06-107">*mtIn*</span></span> 
</dt> <dd>

<span data-ttu-id="d2a06-108">Puntatore a un oggetto [**CMediaType**](cmediatype.md) che specifica il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="d2a06-108">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2a06-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d2a06-109">Return value</span></span>

<span data-ttu-id="d2a06-110">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d2a06-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="d2a06-111">I valori possibili includono quelli mostrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="d2a06-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="d2a06-112">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="d2a06-112">Return code</span></span>                                                                                                | <span data-ttu-id="d2a06-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d2a06-113">Description</span></span>                              |
|------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <span data-ttu-id="d2a06-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d2a06-114"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="d2a06-115">Il tipo di supporto è accettabile.</span><span class="sxs-lookup"><span data-stu-id="d2a06-115">Media type is acceptable.</span></span><br/>     |
| <dl> <span data-ttu-id="d2a06-116"><dt>**\_tipo VFW \_ E \_ non \_ accettato**</dt></span><span class="sxs-lookup"><span data-stu-id="d2a06-116"><dt>**VFW\_E\_TYPE\_NOT\_ACCEPTED**</dt></span></span> </dl> | <span data-ttu-id="d2a06-117">Il tipo di supporto non è accettabile.</span><span class="sxs-lookup"><span data-stu-id="d2a06-117">Media type is not acceptable.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d2a06-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="d2a06-118">Remarks</span></span>

<span data-ttu-id="d2a06-119">La classe derivata deve implementare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="d2a06-119">The derived class must implement this method.</span></span> <span data-ttu-id="d2a06-120">Restituisce \_ OK se il formato di input proposto è accettabile o in caso contrario un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="d2a06-120">Return S\_OK if the proposed input format is acceptable, or an error code otherwise.</span></span>

<span data-ttu-id="d2a06-121">Questo metodo non deve verificare che il formato di input sia compatibile con il formato di output (se presente).</span><span class="sxs-lookup"><span data-stu-id="d2a06-121">This method does not need to verify that the input format is compatible with the output format (if any).</span></span> <span data-ttu-id="d2a06-122">Il pin di input verifica che chiamando il metodo [**CheckTransform**](ctransformfilter-checktransform.md) .</span><span class="sxs-lookup"><span data-stu-id="d2a06-122">The input pin verifies that by calling the [**CheckTransform**](ctransformfilter-checktransform.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2a06-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d2a06-123">Requirements</span></span>



| <span data-ttu-id="d2a06-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2a06-124">Requirement</span></span> | <span data-ttu-id="d2a06-125">Valore</span><span class="sxs-lookup"><span data-stu-id="d2a06-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2a06-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d2a06-126">Header</span></span><br/>  | <dl> <span data-ttu-id="d2a06-127"><dt>Transfrm. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d2a06-127"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d2a06-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="d2a06-128">Library</span></span><br/> | <dl> <span data-ttu-id="d2a06-129"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d2a06-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2a06-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d2a06-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2a06-131">**Classe CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="d2a06-131">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




