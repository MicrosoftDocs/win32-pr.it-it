---
description: 'Non supportata. Chiamare invece il metodo IAMTimelineComp:: GetRecursiveLayerOfType.'
ms.assetid: 857f57e2-6123-43c3-bb74-62afd0fc0b52
title: 'Metodo IAMTimelineComp:: GetRecursiveLayerOfTypeI (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.GetRecursiveLayerOfTypeI
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8aded93aa0753ee8dddf173262c80678e28037a2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326628"
---
# <a name="iamtimelinecompgetrecursivelayeroftypei-method"></a><span data-ttu-id="d0985-104">Metodo IAMTimelineComp:: GetRecursiveLayerOfTypeI</span><span class="sxs-lookup"><span data-stu-id="d0985-104">IAMTimelineComp::GetRecursiveLayerOfTypeI method</span></span>

> [!Note]  
> <span data-ttu-id="d0985-105">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="d0985-105">\[Deprecated.</span></span> <span data-ttu-id="d0985-106">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d0985-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d0985-107">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="d0985-107">Not supported.</span></span> <span data-ttu-id="d0985-108">Chiamare invece il metodo [**IAMTimelineComp:: GetRecursiveLayerOfType**](iamtimelinecomp-getrecursivelayeroftype.md) .</span><span class="sxs-lookup"><span data-stu-id="d0985-108">Call the [**IAMTimelineComp::GetRecursiveLayerOfType**](iamtimelinecomp-getrecursivelayeroftype.md) method instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0985-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d0985-109">Syntax</span></span>


```C++
HRESULT GetRecursiveLayerOfTypeI(
   IAMTimelineObj      **ppVirtualTrack,
   long                **pWhichLayer,
   TIMELINE_MAJOR_TYPE Type
);
```



## <a name="parameters"></a><span data-ttu-id="d0985-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="d0985-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0985-111">*ppVirtualTrack*</span><span class="sxs-lookup"><span data-stu-id="d0985-111">*ppVirtualTrack*</span></span> 
</dt> <dd>

<span data-ttu-id="d0985-112">Riservato.</span><span class="sxs-lookup"><span data-stu-id="d0985-112">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="d0985-113">*pWhichLayer*</span><span class="sxs-lookup"><span data-stu-id="d0985-113">*pWhichLayer*</span></span> 
</dt> <dd>

<span data-ttu-id="d0985-114">Riservato.</span><span class="sxs-lookup"><span data-stu-id="d0985-114">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="d0985-115">*Tipo*</span><span class="sxs-lookup"><span data-stu-id="d0985-115">*Type*</span></span> 
</dt> <dd>

<span data-ttu-id="d0985-116">Riservato.</span><span class="sxs-lookup"><span data-stu-id="d0985-116">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0985-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d0985-117">Return value</span></span>

<span data-ttu-id="d0985-118">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d0985-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d0985-119">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d0985-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0985-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="d0985-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d0985-121">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="d0985-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d0985-122">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="d0985-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d0985-123">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="d0985-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d0985-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d0985-124">Requirements</span></span>



| <span data-ttu-id="d0985-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0985-125">Requirement</span></span> | <span data-ttu-id="d0985-126">Valore</span><span class="sxs-lookup"><span data-stu-id="d0985-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d0985-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d0985-127">Header</span></span><br/>  | <dl> <span data-ttu-id="d0985-128"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0985-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="d0985-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="d0985-129">Library</span></span><br/> | <dl> <span data-ttu-id="d0985-130"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d0985-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0985-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d0985-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0985-132">**Interfaccia IAMTimelineComp**</span><span class="sxs-lookup"><span data-stu-id="d0985-132">**IAMTimelineComp Interface**</span></span>](iamtimelinecomp.md)
</dt> </dl>

 

 




