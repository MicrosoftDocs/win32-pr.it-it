---
description: La funzione AMovieSetupRegisterFilter2 registra il merito, i pin e i tipi di supporto del filtro nel registro di sistema tramite l'interfaccia IFilterMapper2.
ms.assetid: 8e0f3485-9e5d-4b22-853d-4ad9b1fb71d2
title: Funzione AMovieSetupRegisterFilter2 (Dllsetup. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMovieDllRegisterServer
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 272b781cf70f1dede9d4eea64b45d3d9d793a119
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331706"
---
# <a name="amoviesetupregisterfilter2-function"></a><span data-ttu-id="51272-103">AMovieSetupRegisterFilter2 (funzione)</span><span class="sxs-lookup"><span data-stu-id="51272-103">AMovieSetupRegisterFilter2 function</span></span>

<span data-ttu-id="51272-104">La funzione **AMovieSetupRegisterFilter2** registra il merito, i pin e i tipi di supporto del filtro nel registro di sistema tramite l'interfaccia [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) .</span><span class="sxs-lookup"><span data-stu-id="51272-104">The **AMovieSetupRegisterFilter2** function registers a filter's merit, pins, and media types in the registry using the [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="51272-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="51272-105">Syntax</span></span>


```C++
HRESULT AMovieDllRegisterServer(
   const AMOVIESETUP_FILTER const * psetupdata,
         IFilterMapper2             *pIFM2,
         BOOL                       bRegister
);
```



## <a name="parameters"></a><span data-ttu-id="51272-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="51272-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51272-107">*psetupdata*</span><span class="sxs-lookup"><span data-stu-id="51272-107">*psetupdata*</span></span> 
</dt> <dd>

<span data-ttu-id="51272-108">Puntatore ai dati [**del \_ filtro AMOVIESETUP**](amoviesetup-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="51272-108">Pointer to the [**AMOVIESETUP\_FILTER**](amoviesetup-filter.md) data.</span></span>

</dd> <dt>

<span data-ttu-id="51272-109">*pIFM2*</span><span class="sxs-lookup"><span data-stu-id="51272-109">*pIFM2*</span></span> 
</dt> <dd>

<span data-ttu-id="51272-110">Puntatore all'interfaccia [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) .</span><span class="sxs-lookup"><span data-stu-id="51272-110">Pointer to [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) interface.</span></span>

</dd> <dt>

<span data-ttu-id="51272-111">*bRegister*</span><span class="sxs-lookup"><span data-stu-id="51272-111">*bRegister*</span></span> 
</dt> <dd>

<span data-ttu-id="51272-112">Valore che indica se registrare il filtro. **True** indica che registra il filtro, **false** indica che è stata annullata la registrazione.</span><span class="sxs-lookup"><span data-stu-id="51272-112">Value indicating whether to register the filter; **TRUE** indicates register the filter, **FALSE** indicates unregister it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51272-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="51272-113">Return value</span></span>

<span data-ttu-id="51272-114">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="51272-114">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="51272-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="51272-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="51272-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="51272-116">Remarks</span></span>

<span data-ttu-id="51272-117">La funzione [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) chiama questa funzione helper per registrare un filtro dopo la registrazione del server com.</span><span class="sxs-lookup"><span data-stu-id="51272-117">The [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) function calls this helper function to register a filter after the COM server has been registered.</span></span>

<span data-ttu-id="51272-118">In genere, un filtro userà [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) e non chiamerà direttamente questa funzione.</span><span class="sxs-lookup"><span data-stu-id="51272-118">Typically, a filter will use [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) and will not call this function directly.</span></span>

## <a name="requirements"></a><span data-ttu-id="51272-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="51272-119">Requirements</span></span>



| <span data-ttu-id="51272-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="51272-120">Requirement</span></span> | <span data-ttu-id="51272-121">Valore</span><span class="sxs-lookup"><span data-stu-id="51272-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51272-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="51272-122">Header</span></span><br/>  | <dl> <span data-ttu-id="51272-123"><dt>Dllsetup. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="51272-123"><dt>Dllsetup.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="51272-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="51272-124">Library</span></span><br/> | <dl> <span data-ttu-id="51272-125"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="51272-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51272-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="51272-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51272-127">**Funzioni di installazione DLL**</span><span class="sxs-lookup"><span data-stu-id="51272-127">**DLL Setup Functions**</span></span>](dll-setup-functions.md)
</dt> </dl>

 

 




