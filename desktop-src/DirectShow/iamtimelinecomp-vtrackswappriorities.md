---
description: Il metodo VTrackSwapPriorities passa i livelli di priorità di due tracce.
ms.assetid: 87085060-5165-4c32-b5b0-895ae487e7ef
title: 'Metodo IAMTimelineComp:: VTrackSwapPriorities (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.VTrackSwapPriorities
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: df90fe3f4c481f454c6cc743f09de9538a2c892d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333706"
---
# <a name="iamtimelinecompvtrackswappriorities-method"></a><span data-ttu-id="f1298-103">Metodo IAMTimelineComp:: VTrackSwapPriorities</span><span class="sxs-lookup"><span data-stu-id="f1298-103">IAMTimelineComp::VTrackSwapPriorities method</span></span>

> [!Note]  
> <span data-ttu-id="f1298-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="f1298-104">\[Deprecated.</span></span> <span data-ttu-id="f1298-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f1298-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f1298-106">Il `VTrackSwapPriorities` metodo passa i livelli di priorità di due tracce.</span><span class="sxs-lookup"><span data-stu-id="f1298-106">The `VTrackSwapPriorities` method switches the priority levels of two tracks.</span></span>

<span data-ttu-id="f1298-107">Con due livelli di priorità, questo metodo cambia le tracce virtuali in base a tali priorità.</span><span class="sxs-lookup"><span data-stu-id="f1298-107">Given two priority levels, this method switches the virtual tracks at those priorities.</span></span> <span data-ttu-id="f1298-108">Quando il metodo restituisce, la traccia con il primo livello di priorità è ora al secondo livello di priorità e viceversa.</span><span class="sxs-lookup"><span data-stu-id="f1298-108">When the method returns, the track that was at the first priority level is now at the second priority level, and vice versa.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1298-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f1298-109">Syntax</span></span>


```C++
HRESULT VTrackSwapPriorities(
   long VirtualTrackA,
   long VirtualTrackB
);
```



## <a name="parameters"></a><span data-ttu-id="f1298-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="f1298-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1298-111">*VirtualTrackA*</span><span class="sxs-lookup"><span data-stu-id="f1298-111">*VirtualTrackA*</span></span> 
</dt> <dd>

<span data-ttu-id="f1298-112">Primo livello di priorità in cui scambiare le tracce virtuali.</span><span class="sxs-lookup"><span data-stu-id="f1298-112">First priority level at which to swap virtual tracks.</span></span>

</dd> <dt>

<span data-ttu-id="f1298-113">*VirtualTrackB*</span><span class="sxs-lookup"><span data-stu-id="f1298-113">*VirtualTrackB*</span></span> 
</dt> <dd>

<span data-ttu-id="f1298-114">Secondo livello di priorità in cui scambiare le tracce virtuali.</span><span class="sxs-lookup"><span data-stu-id="f1298-114">Second priority level at which to swap virtual tracks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1298-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f1298-115">Return value</span></span>

<span data-ttu-id="f1298-116">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f1298-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f1298-117">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f1298-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1298-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="f1298-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f1298-119">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="f1298-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f1298-120">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f1298-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f1298-121">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="f1298-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f1298-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f1298-122">Requirements</span></span>



| <span data-ttu-id="f1298-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1298-123">Requirement</span></span> | <span data-ttu-id="f1298-124">Valore</span><span class="sxs-lookup"><span data-stu-id="f1298-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f1298-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f1298-125">Header</span></span><br/>  | <dl> <span data-ttu-id="f1298-126"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1298-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f1298-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="f1298-127">Library</span></span><br/> | <dl> <span data-ttu-id="f1298-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f1298-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1298-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f1298-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1298-130">**Interfaccia IAMTimelineComp**</span><span class="sxs-lookup"><span data-stu-id="f1298-130">**IAMTimelineComp Interface**</span></span>](iamtimelinecomp.md)
</dt> <dt>

[<span data-ttu-id="f1298-131">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="f1298-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




