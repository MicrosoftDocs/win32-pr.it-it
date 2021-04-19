---
description: 'Il metodo StartAt comunica al pin quando iniziare a consegnare i dati. Questo metodo implementa il metodo IAMStreamControl:: StartAt.'
ms.assetid: fd2943e8-8d35-4122-a99e-96d12459b335
title: Metodo CBaseStreamControl. StartAt (Strmctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.StartAt
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a7adcf7cbd435992333bb8ae59d5ab1674056223
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324028"
---
# <a name="cbasestreamcontrolstartat-method"></a><span data-ttu-id="e1aaf-104">CBaseStreamControl. StartAt, metodo</span><span class="sxs-lookup"><span data-stu-id="e1aaf-104">CBaseStreamControl.StartAt method</span></span>

<span data-ttu-id="e1aaf-105">Il `StartAt` metodo informa il PIN quando iniziare a consegnare i dati.</span><span class="sxs-lookup"><span data-stu-id="e1aaf-105">The `StartAt` method informs the pin when to start delivering data.</span></span> <span data-ttu-id="e1aaf-106">Questo metodo implementa il metodo [**IAMStreamControl:: startat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) .</span><span class="sxs-lookup"><span data-stu-id="e1aaf-106">This method implements the [**IAMStreamControl::StartAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1aaf-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e1aaf-107">Syntax</span></span>


```C++
HRESULT StartAt(
   const REFERENCE_TIME *ptStart = NULL,
         DWORD          dwCookie = 0
);
```



## <a name="parameters"></a><span data-ttu-id="e1aaf-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e1aaf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1aaf-109">*ptStart*</span><span class="sxs-lookup"><span data-stu-id="e1aaf-109">*ptStart*</span></span> 
</dt> <dd>

<span data-ttu-id="e1aaf-110">Puntatore a un valore di [**\_ ora di riferimento**](reference-time.md) che specifica quando il PIN deve iniziare a consegnare i dati.</span><span class="sxs-lookup"><span data-stu-id="e1aaf-110">Pointer to a [**REFERENCE\_TIME**](reference-time.md) value that specifies when the pin should start delivering data.</span></span>

</dd> <dt>

<span data-ttu-id="e1aaf-111">*dwCookie*</span><span class="sxs-lookup"><span data-stu-id="e1aaf-111">*dwCookie*</span></span> 
</dt> <dd>

<span data-ttu-id="e1aaf-112">Specifica un valore da inviare insieme alla notifica di avvio.</span><span class="sxs-lookup"><span data-stu-id="e1aaf-112">Specifies a value to send along with the start notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1aaf-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e1aaf-113">Return value</span></span>

<span data-ttu-id="e1aaf-114">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e1aaf-114">Returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1aaf-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e1aaf-115">Requirements</span></span>



| <span data-ttu-id="e1aaf-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1aaf-116">Requirement</span></span> | <span data-ttu-id="e1aaf-117">Valore</span><span class="sxs-lookup"><span data-stu-id="e1aaf-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1aaf-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e1aaf-118">Header</span></span><br/>  | <dl> <span data-ttu-id="e1aaf-119"><dt>Strmctl. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e1aaf-119"><dt>Strmctl.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e1aaf-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="e1aaf-120">Library</span></span><br/> | <dl> <span data-ttu-id="e1aaf-121"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e1aaf-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1aaf-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e1aaf-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1aaf-123">**Classe CBaseStreamControl**</span><span class="sxs-lookup"><span data-stu-id="e1aaf-123">**CBaseStreamControl Class**</span></span>](cbasestreamcontrol.md)
</dt> </dl>

 

 




