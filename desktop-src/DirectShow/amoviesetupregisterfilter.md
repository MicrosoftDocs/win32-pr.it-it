---
description: Obsoleta. In alternativa, usare AMovieSetupRegisterFilter2.
ms.assetid: 42278829-d09e-46c7-8f1a-fa4572f7cc00
title: Funzione AMovieSetupRegisterFilter (Dllsetup. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMovieSetupRegisterFilter
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 398d2d727e26feaca23d6bddbdcbc8a578d096eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329165"
---
# <a name="amoviesetupregisterfilter-function"></a><span data-ttu-id="ba630-104">AMovieSetupRegisterFilter (funzione)</span><span class="sxs-lookup"><span data-stu-id="ba630-104">AMovieSetupRegisterFilter function</span></span>

<span data-ttu-id="ba630-105">Obsoleta.</span><span class="sxs-lookup"><span data-stu-id="ba630-105">Obsolete.</span></span> <span data-ttu-id="ba630-106">In alternativa, usare [**AMovieSetupRegisterFilter2**](amoviesetupregisterfilter2.md) .</span><span class="sxs-lookup"><span data-stu-id="ba630-106">Use [**AMovieSetupRegisterFilter2**](amoviesetupregisterfilter2.md) instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba630-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ba630-107">Syntax</span></span>


```C++
HRESULT AMovieSetupRegisterFilter(
   const AMOVIESETUP_FILTER const * psetupdata,
         IFilterMapper              *pIFM,
         BOOL                       bRegister
);
```



## <a name="parameters"></a><span data-ttu-id="ba630-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ba630-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba630-109">*psetupdata*</span><span class="sxs-lookup"><span data-stu-id="ba630-109">*psetupdata*</span></span> 
</dt> <dd>

<span data-ttu-id="ba630-110">Riservato.</span><span class="sxs-lookup"><span data-stu-id="ba630-110">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="ba630-111">*pIFM*</span><span class="sxs-lookup"><span data-stu-id="ba630-111">*pIFM*</span></span> 
</dt> <dd>

<span data-ttu-id="ba630-112">Riservato.</span><span class="sxs-lookup"><span data-stu-id="ba630-112">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="ba630-113">*bRegister*</span><span class="sxs-lookup"><span data-stu-id="ba630-113">*bRegister*</span></span> 
</dt> <dd>

<span data-ttu-id="ba630-114">Riservato.</span><span class="sxs-lookup"><span data-stu-id="ba630-114">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba630-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ba630-115">Return value</span></span>

<span data-ttu-id="ba630-116">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ba630-116">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ba630-117">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ba630-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba630-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ba630-118">Requirements</span></span>



| <span data-ttu-id="ba630-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba630-119">Requirement</span></span> | <span data-ttu-id="ba630-120">Valore</span><span class="sxs-lookup"><span data-stu-id="ba630-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba630-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ba630-121">Header</span></span><br/>  | <dl> <span data-ttu-id="ba630-122"><dt>Dllsetup. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ba630-122"><dt>Dllsetup.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ba630-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="ba630-123">Library</span></span><br/> | <dl> <span data-ttu-id="ba630-124"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ba630-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba630-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ba630-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba630-126">**Funzioni di installazione DLL**</span><span class="sxs-lookup"><span data-stu-id="ba630-126">**DLL Setup Functions**</span></span>](dll-setup-functions.md)
</dt> </dl>

 

 




