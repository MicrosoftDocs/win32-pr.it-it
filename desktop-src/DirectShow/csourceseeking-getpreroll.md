---
description: "Il metodo GetPreroll recupera l'ora di preroll. Questo metodo implementa il metodo IMediaSeeking:: GetPreroll."
ms.assetid: 2395d5b2-8c1f-40cd-8d4a-48620debe7a7
title: Metodo CSourceSeeking. GetPreroll (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetPreroll
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 097af089a7221f005cf7f3aac74953166af3cb2a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329504"
---
# <a name="csourceseekinggetpreroll-method"></a><span data-ttu-id="8daab-104">CSourceSeeking. GetPreroll, metodo</span><span class="sxs-lookup"><span data-stu-id="8daab-104">CSourceSeeking.GetPreroll method</span></span>

<span data-ttu-id="8daab-105">Il `GetPreroll` metodo recupera l'ora di preregistrazione.</span><span class="sxs-lookup"><span data-stu-id="8daab-105">The `GetPreroll` method retrieves the preroll time.</span></span> <span data-ttu-id="8daab-106">Questo metodo implementa il metodo [**IMediaSeeking:: GetPreroll**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpreroll) .</span><span class="sxs-lookup"><span data-stu-id="8daab-106">This method implements the [**IMediaSeeking::GetPreroll**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpreroll) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8daab-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8daab-107">Syntax</span></span>


```C++
HRESULT GetPreroll(
   LONGLONG *pPreroll
);
```



## <a name="parameters"></a><span data-ttu-id="8daab-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="8daab-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8daab-109">*pPreroll*</span><span class="sxs-lookup"><span data-stu-id="8daab-109">*pPreroll*</span></span> 
</dt> <dd>

<span data-ttu-id="8daab-110">Puntatore a una variabile che riceve l'ora di preregistrazione.</span><span class="sxs-lookup"><span data-stu-id="8daab-110">Pointer to a variable that receives the preroll time.</span></span> <span data-ttu-id="8daab-111">Il valore è impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="8daab-111">The value is set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8daab-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8daab-112">Return value</span></span>

<span data-ttu-id="8daab-113">Restituisce uno dei valori **HRESULT** elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="8daab-113">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="8daab-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="8daab-114">Return code</span></span>                                                                               | <span data-ttu-id="8daab-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8daab-115">Description</span></span>                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="8daab-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8daab-116"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="8daab-117">Operazione riuscita</span><span class="sxs-lookup"><span data-stu-id="8daab-117">Success</span></span><br/>                |
| <dl> <span data-ttu-id="8daab-118"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="8daab-118"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="8daab-119">Valore del puntatore **null**</span><span class="sxs-lookup"><span data-stu-id="8daab-119">**NULL** pointer value</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8daab-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8daab-120">Requirements</span></span>



| <span data-ttu-id="8daab-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="8daab-121">Requirement</span></span> | <span data-ttu-id="8daab-122">Valore</span><span class="sxs-lookup"><span data-stu-id="8daab-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8daab-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8daab-123">Header</span></span><br/>  | <dl> <span data-ttu-id="8daab-124"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8daab-124"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8daab-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="8daab-125">Library</span></span><br/> | <dl> <span data-ttu-id="8daab-126"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="8daab-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8daab-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8daab-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8daab-128">**Classe CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="8daab-128">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




