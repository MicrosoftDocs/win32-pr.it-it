---
description: Il metodo CheckMediaType determina se il filtro accetta un tipo di supporto specifico.
ms.assetid: 90d26cf6-443c-4a06-98c6-ffa14e27ee41
title: Metodo CBaseRenderer. CheckMediaType (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dc0d4fc70e9ed64f9481d827cb678eb3ff9721d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329401"
---
# <a name="cbaserenderercheckmediatype-method"></a><span data-ttu-id="805f1-103">CBaseRenderer. CheckMediaType, metodo</span><span class="sxs-lookup"><span data-stu-id="805f1-103">CBaseRenderer.CheckMediaType method</span></span>

<span data-ttu-id="805f1-104">Il `CheckMediaType` metodo determina se il filtro accetta un tipo di supporto specifico.</span><span class="sxs-lookup"><span data-stu-id="805f1-104">The `CheckMediaType` method determines if the filter accepts a specific media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="805f1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="805f1-105">Syntax</span></span>


```C++
virtual HRESULT CheckMediaType(
   const CMediaType *pmt
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="805f1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="805f1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="805f1-107">*PMT*</span><span class="sxs-lookup"><span data-stu-id="805f1-107">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="805f1-108">Puntatore a un oggetto [**CMediaType**](cmediatype.md) che contiene il tipo di supporto proposto.</span><span class="sxs-lookup"><span data-stu-id="805f1-108">Pointer to a [**CMediaType**](cmediatype.md) object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="805f1-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="805f1-109">Return value</span></span>

<span data-ttu-id="805f1-110">Restituisce \_ OK se il tipo di supporto proposto è accettabile.</span><span class="sxs-lookup"><span data-stu-id="805f1-110">Returns S\_OK if the proposed media type is acceptable.</span></span> <span data-ttu-id="805f1-111">In caso contrario, restituisce \_ false o un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="805f1-111">Otherwise, returns S\_FALSE or an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="805f1-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="805f1-112">Remarks</span></span>

<span data-ttu-id="805f1-113">Il pin di input chiama questo metodo dal proprio metodo [**CBasePin:: CheckMediaType**](cbasepin-checkmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="805f1-113">The input pin calls this method from its own [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method.</span></span> <span data-ttu-id="805f1-114">La classe derivata deve implementare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="805f1-114">The derived class must implement this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="805f1-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="805f1-115">Requirements</span></span>



| <span data-ttu-id="805f1-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="805f1-116">Requirement</span></span> | <span data-ttu-id="805f1-117">Valore</span><span class="sxs-lookup"><span data-stu-id="805f1-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="805f1-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="805f1-118">Header</span></span><br/>  | <dl> <span data-ttu-id="805f1-119"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="805f1-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="805f1-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="805f1-120">Library</span></span><br/> | <dl> <span data-ttu-id="805f1-121"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="805f1-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="805f1-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="805f1-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="805f1-123">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="805f1-123">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




